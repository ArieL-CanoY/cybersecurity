# easyui-datebox

```javascript
- here I will explain how to properly set its value to empty

> when using easyui like datebox, to set its value to empty or null, use its function "datebox" ex. "mydate.datebox('setValue', '')", because if we use "mydate.val('')", it will not let it put its value again, unless you use the "datebox" function.




```


# timeout
```javascript
setTimeout(function () {
alert('timeout');
}, 5000);
```


# datatable
```javascript
function initializeDatagrid() {
    var table = $('#mytable').DataTable({
        ajax: {
            url: '/Movies/GetMoviesData',
            type: 'GET'
        },
        columns: [
            { title: 'Name', data: 'title' },
            {
                title: 'Release Date',
                data: 'releaseDate',
                type: 'string',
                render: function (data) {
                    var dateOnly = data.split("T")[0];
                    var splitDate = dateOnly.split("-");
                    var month = splitDate[1];
                    var day = splitDate[2];
                    var year = splitDate[0];
                    return `${month}-${day}-${year}`;

                }
            },
            { title: 'Genre', data: 'genre', orderable: false},
            { title: 'Price', data: 'price', type: 'string' },
            {
                title: 'Action',
                render: function (data, type, row) {
                    return `<button class='btn btn-primary' onclick='editMovie(${row.id})'>Edit</button>  ` +
                        `<button class='btn btn-danger' onclick='deleteMovie(${row.id})'>Delete</button>`;
                },
                orderable: false
            }
        ],
        columnDefs: [{
            targets: '_all',
            className: 'dt-center'
        }],
        "drawCallback": function (settings) {
            var api = this.api();
            var currentPage = api.page.info().page;
            var currentLength = api.page.len();
            $.ajax({
                url: '/Movies/GetMoviesData',
                type: 'GET',
                data: {
                    page: currentPage,
                    length: currentLength
                }
            });
        }
    });

    table.on('change', function () {
        alert('datatable changed');
    });
}
```



# Event for changing page or rows
```js
    $('#dg-DeliveryMonitoringInvoices').datagrid('getPager').pagination({
        onSelectPage: function (page, rows) {
            alert(`pageNumber: ${page}, pageSize: ${rows}`);
        }
    });
```



# POST
```javascript 
var name = $('#nameInput').val();

$.post('/controller_name/function_name',
	{
		parameterNameFromServer: name
	},
	function (response) {
		if (response.success) {
			$('#mydatagrid').datagrid('reload');
			$.messager.alert('Success', 'Successfully Added New Response', 'info');
		}
		if (response.errorMessage.trim().length > 0) {
			$.messager.alert('Error', response.errorMessage, 'error');
		}
	}
).fail(function (xhr, status, error) {  // handle the request if it returns other 
	tranUnLockScreen();
	$.messager.alert('Error', 'There was an error processing your request. Pleast reload the page.', 'error');
});

```






















