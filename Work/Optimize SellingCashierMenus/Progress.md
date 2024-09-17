

```
HomeController.cs
Main.UI.js
SellingCashierMenu.html


item master
	# item master
		search items
			pop item search master
		search av items
			pop search available items

	# item per location
		item code, name, and total quantity not input-capable
        dropdown before show items button only show 2
		show items
			request to GetItemPerLocation * 2 but no data return
		reload icon on datagrid - no no dg on staging
			request to GetItemPerLocation * 1 but no data return
		dropdown has 2 option
        
	# open po
		item code and name not input-capable
		show items
			request to GetItemOpenPo * 2 but no data return
		reload icon on datagrid - no datagrid on staging
			request to GetItemOpenPo * 1 but no data return

    # inventory items
        select location is dropdown (has many items)
        select (has 3 items only)
        show items  
            request to GetInventoryItems but invicible data
        reload icon on dg
            request to GetInventoryItems but invicible data
        print 
            print all the items on datagrid while the datagrid has invicible data but scrollable

    # inv. reports per location
        load locations btn 
            request to getAllLocations and will get data
        dropdown after load locations btn 
            has 3 options only
        search text input-capable
            does not work, there is no payload on request
        save to btn
            need to select one of the data
                open new tab: path is /Reports/InventoryReportPerLocRepo
                    report has no data
        reload icon
            does not work

    # repossess inv. with serial
        search
            working
        location
            working
        item status
            working
        reload
            working - request to GetRepossessItem
        
    # available items
        working
            search item, location, sn status, date from, date to
		reload icon
			working
	            request to GetAVSerializedItems and return data
        reload
            working
            request to GetAVSerializedItems and return data
		remarks plus icon
			working
				select any item, click remarks with + icon > click edit > input remarks > save
		generate 
			working
				open new tab and generate a report with items from datagrid
		remarks save icon
			working
				open new tab and open /Reports/SerialNoWithRemarks
```


