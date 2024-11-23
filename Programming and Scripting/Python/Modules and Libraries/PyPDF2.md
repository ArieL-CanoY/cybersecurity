
Merge multiple PDF file into single file
```python
import PyPDF2

folderPath = r'C:\Users\User\Desktop\pdf merger test files\\'

def merge_pdfs(pdf_list, output):
    pdf_writer = PyPDF2.PdfWriter()

    for pdf in pdf_list:
        pdf_reader = PyPDF2.PdfReader(pdf)
        for page in range(len(pdf_reader.pages)):
            pdf_writer.add_page(pdf_reader.pages[page])

    with open(output, 'wb') as out:
        pdf_writer.write(out)

pdf_files = [f'{folderPath}file1.pdf',
             f'{folderPath}file2.pdf']

merge_pdfs(pdf_files, f'{folderPath}merged_output.pdf')
```


