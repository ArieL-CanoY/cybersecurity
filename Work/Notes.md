4) Item Master
        a) Item Master
            - Missing Popup for Supplier > In iBAS, when clicking New, there's a popup to set the default supplier for the item
            - Sys. Ass. Barcode is unchecked whereas iBAS is checked.
            - Edit, Save, Update, Search Items, Search A.V. Items > Not Working
            - Cancel > Doesn't clear all the fields
            - Bundle Item button > Not displaying items for bundle
        b) Item Per Location
            - Item Code and Name is not showing in the screen
            - Total quantity is not being calculated
        c) Open P.O.
            - Not working since ITEM CODE is not specified
        d) Inv. Reports Per Location
            - When source has been selected, no data being displayed
    5) Items On Sale
        - Table header doesn't occupy the whole row
        - Clicked Add button > Popup > Enter SN or button to look for items (item master)
            - DOesn't show the item name, item price (local and foreign)
        - Search for Items on Sale
            - Table header doesn't occupy the whole row
            - Doesn't display any data
    6) STF Remarks
        - Add > Generates the code > Working
        - Edit > Working but if the 'Update' button is still clicked without changes, EntityError (Mofidied, Unchaged)
        - Search > Working
    7) Supplier Master
        - In iBAS, Allow Changes in Payee and Vatable 10.00% is pre-checked
        - Term Code/Default Term Code is not being selected even if it's already set/Options are not the same with iBAS
        - TAG is not also being displayed
        - Edit > Working
        - Update > Working
            - Change 'Tittle' label to Title
            - 'Tin' to TIN
            - 'fax No' to Fax No.

















database_work

CREATE VIEW vw_customerPOMonitoring AS
(
SELECT t1.*, t2.acctName
FROM     dbo.customerPOTranHdr t1
INNER JOIN dbo.arAccountMaster t2 ON t1.acctNo = t2.acctNo and t1.divisionCode = t2.divisionCode 
)






