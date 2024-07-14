# New
```



---------------- training


dictionary:
	A.R. - Accounts Receivable
	C.R. - Cash Receipt
	I.R. - Internal Receipt 
	M.R - Mobile Receipt
	P.R. - Provision Receipt
	M.I. - Monthly Installment
	E.I. - Easy Installment
	S.T.F. - Stock Transfer

definitions:
	General Ledger - backbone of any accounting system which holds financial data for an organization.
	 
	 Procurement - involves every activity involved in obtaining the goods and services a company needs to support its daily operations including sourcing, negotiating terms, purchasing items, receiving and inspecting goods as necessary and keeping records of all the steps in the processc

	Credit Memo - CM (Credit Memo) with dynamic credit entry: CM issued by a seller to a buyer used to correct errors in invoices or to provide refund for returned or damaged goods. some has only privilege to avoid malicious intent(tanggal ng utang)




MACSBE
	account:
		register in user master then cashier should register the same from the user master


2 station of cashier:
	selling
	deffered


--- selling cashier
selling


modules:
	inventory
	

--- STF
	stock transfer
	
	used if someone request item from another branch
	def no: from warehouse
	intended location, kung saan babato yung item na nirequest
	delivery personnel: magdedeliver

	2 - stf slip from guard and destination
	STF slip should be attached to credit memo

	if there is no item in item master, the store manager should purchase directly to suppliers

	IC - inventory controller






--- por direct deliver(purchase order receipt)

	merchandize create PO (Purchase Order) 

	if the item is serialized

	scan if not serialized

	wearhouse should approve the PO Receipt




----- deffered cashier
	utang



sales charge and billing not from tarlac


sales invoice - series(workstation) of invoice
sales invoice should be equal to invoice number from printer


sales internal - for employee 




cashier station:
	selling
	easy installment


1530 - 
1321 - easy installment


sales invoice - have series with invoice
sales internal - no series in invoice but progressive transaction


types/modes of payment:
	cash
	credit
	check or cheque - 
	pdc - post dated check - date tomorrow and onwards


--- cash receipt
	unang utang, unang babayaran

	points = % payment

	select customer to see their balance
	remarks is required

	collector - name of cashier
	receipt type: internal control

	sales slip if no sales invoice
		sales slip - record of transaction but limited information

	









--- credit card
	swipe credit card

	different months, different % 


	cash in bank
	receipt type : internal


	click add privilege - insert the card


	credit card does not end after swipe - settlement - process(cashier)

	(cashier) every transaction - settle it immediately

	what if customer refund the item: cannot void only refund


	credit card settlement
	if not settle the card, the bank will not pay you

	credit card payment then credit card settlement



--- ar others 
	see the accounts receivable


--- check receipt
dated check - check that is date backwards
(pdc) post dated check - check that is date onwards 


--- PDC (Post Dated Check/Cheque) receipt
	future(tomorrow and onwards) date on the cheque/check

	if the customer is clear, go to ---check clearing CRON






	


checking date:
	descending


stale cheque
	check that is remains undeposited or uncashed between the valid date to be issued or 6 months
	validity from 6 months to 1 year


--- remittance cash
	type:
		cash
		cheque

	make deposit slip and copy it

	total collection within the day

	remitted by: (cashier)
	bank account no

	at the end of the day, they have remittance report


	cash deposit copy to this remittance cash



--- remittance check




--- demit memo (cashier selling)
	debit to AR
	
	utang: delivery charge, gift wrap 
	additional payment: delivery charge (not in sales invoice)
	approved by: manager(example)



--- apply open credit
	advanced payment
	sales return



--- sales return
	refund the item for higher or equal amount
	last is to apply open credit



SO and invoice



day to day:
	sales order
	sales invoice/internal
	collect of payment - depends in mode of payment (cash, check/cheque, pdc, credit)
	remit





--- item master
	check the item

serialized - usually for big item, item tracking







merchandizing:
	PO (Purchase Order) > send to supplier > deliver the supply
	serialize item only
	non-serialize: received then send to central
	create and update of item

central use IBAS system:
	purchase order receipt



STF (Stock Transfer) received



inventory items: 1 location
inventory reports per location: multiple location (common used)



--- customer master
	if customer not exist > add new > 
	---Sales order automatic add new customer if not exist

--- sales order
	need approval if the transaction is super high
	xx days - need approval
	sales personel: nag assist or nag benta
	remarks: type - if none
	particulars: type - if none

	check OD (Online Discount), click request online discount, request and wait for approval
	if save click: pop up sales internal, sales invoice

	sales internal: employee of megasaver
	sales invoice: if not employee of megasaver

	
--- sales invoice
	reference type: salesorder


--- manager is for approval of discount,
--- district manager will approve if manager is not exist
--- cashier only have the ability to discount if sunday and holiday




merchanziding









report of system should be the same as the report of bank system



--------------- iBAS

maintenance:
	sales person master - input sales person 

transactions:
	------- treasury

	if remittance is not correct
	accounting will cancel
	cashier will input again



	credit card collection:
		select terminal code for search
		then retrieve all the desposit money

	general ledger: sales order automatically put data on the online pass

	collector code: cashier who collected the payment

	bounce check:
		search for bank code then input cheque no.

	CRON check clearing:
		dropdown - search for specific branch then it will list to be check


	O.R. (Official Receipt) - proof of payment 
	O.R. Cancellation: used to reverse or correct previous sales transaction
		cash
		credit

	skip workstation receipt:
		select workstation to skip, useful when customer does not require a receipt




	------- billing and collection

	CM (Credit Memo) with dynamic credit entry: CM issued by a seller to a buyer used to correct errors in invoices or to provide refund for returned or damaged goods. some has only privilege to avoid malicious intent(tanggal ng utang)
		cm batch request
		cm batch approval

	DM (Debit Memo) same as CM

	Edit sales term:
		if terms (6 months, 12 months, etc), then cashier will call accounting



---------- end of iBAS





Application:
	Home credit - third party, no items, borrowed items from store and they will have debt from the store
		to customer - SO,SI,unang bayad, then customer have balance, then the balance is from home credit
	EI (Easy Installment) - own store


home credit:
	customer master > SO: terms: digital payment, sales categ:home credit
	give exact amount then customer will give downpayment, and go to cash receipt
	debt will put to the credit using bank terminal: home credit
	credit card settlement
	

	


# normal transactions

--- deffered
	EI clerk will give customer manual form
	EI Form:
	
	Pre credit line form:
		to know fast what would be their limit
		application type:
			new - automatically add new customer info to master
				- reassesment auto yes
		score will be based on the credit limit


		CI/FS - field specialist - verified the person who has debt

	EI monitoring:
		in list of customer:
			attach btn:
				attach the info or valid ids

		monitor the pre credit and credir form for pending, verification, or approval.


	--- if customer is approved
		
		customer master is different from customer selling and deferred

		customer contract:
			downpayment and 12 months
			1st months pay to 12 months


	specific appliance have their own months to pay
	gadgets minimum of 6 months to pay

	Least Common Price - LCP
		base price for specific item

		date will not fill if wiritng contract

	if customer contract approved, release item

	do not create contract if current is CI



--- collection
	search customer > 


	
	sales invoice series selling
	cash receipt series to deffered

	internal receipt

	cashier - collection if customer online4

	division = same as branch
	
	reference no. used to apply the payment from a branch to another branch



	Principal - remaining balance of the load after each payment

	penalty after 5 days not bayad after due date
	total balance * (5% * total balance) if penalty (compounding - nag aadd ang penalty sa total balance if di nabayaran)


--- field collector confirmation
	--- collection confirmation
		confirm the collector transaction that customer paid to the collector from the system


if item pull out or deposit, give customer 30 days to bought back the item


--- item for deposit
	if contract not bayad in 2 months or 60 days, FS/Collector will go to customer that did not pay, item will deposit



	sometimes customer dala ang item to the store
	cashier> item for deposit 

--- item pullout
	search for name to pullout


if item deposit or pullout, the item will store at the store


---release of depo item before ---collection


--- release of depo item:
	search for customer


-- skip docs series
	magbabayad from other branches to the main branches kung saan bumili ang customer
	then sales internal yung type


----- deferred repo transaction - modules from deferred
	---ar others
		account type: repo customer
		then S.O.

	---sales order
		add serial number
		no discount


		serial number - have RE... tag on the number to identify the item as repo
	

	--- repo sales - next

	--- cash receipt or check, etc. - next

	MCAir - another company - fix aircon


	









report july 12
	am
		PO
		POR

	pm
		AP accounts payable
		

ERP: https://www.youtube.com/watch?v=kGQ1fNQVbj8

```



Sample documentation of a system:
https://systemsia.com/help-center/index.php/category/getting-started/