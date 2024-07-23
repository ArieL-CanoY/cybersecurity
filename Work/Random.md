# New
```
VAT


---------------- training






dictionary:
	A.R. - Account Receivable
	C.R. - Cash Receipt
	I.R. - Internal Receipt 
	M.R - Mobile Receipt
	P.R. - Provision Receipt
	P.O. - Purchase Order
	M.I. - monthly installment
	E.W.T - Expanding withholding tax
	I.C. - inventory controller 
	TMEI - tarlac mac enterprise inc.
	DAEI - double alpha enterprise inc.
	S.T.F - Stock Transfer
	D.R. - Directly Receipt
	


	SO invoice purpose - magkano ang at ano ano ang mga binebenta - no changes - out sa inventory
		finalize the sales


	




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
	
	request item from another branch
	def no: from warehouse
	intended location, kung saan babato yung item na nirequest
	delivery personnel: magdedeliver

	2 - stf slip from guard and destination
	STF slip should be attached to credit memo

	if there is no item in item master, the store manager should purchase directly to suppliers





--- por direct deliver(purchase order receipt)

	merchandizer create PO (Purchase Order) 


	if the item is serialized

	scan if not serialized

	wearhouse should approve the POR




--- deffered cashier
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
	check or cheque
	pdc receipt - post date check


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
	see the account receivable


--- check receipt
dated check - check that is date backwards
(pdc) post dated check - check that is date onwards 


--- PDC (Post Dated Cheque) receipt
	or PD collection
	future date on the cheque/check

	if the customer is clear, go to check clearing CRON


	


checking date:
	descending


stale cheque
	check that is remains undeposited or uncashed between the valid date to be issued



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





--- demit memo
	debit to AR
	
	utang: delivery charge, gift wrap 
	additional payment: delivery charge (not in sales invoice)
	approved by: manager(example)



--- apply open credit
	advanced payment
	sales return - float as advancement ng customer > then apply open credit




--- sales return
	refund the item for higher or equal amount

	last is to apply open credit



SO and invoice




day to day:
	sales order
	sales invoice/internal
	collect of payment - depends in mode of payment
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
	if customer not exist > add new > Sales order

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



	after remittance > check online if deposit to the bank > confirm in macsbe/ibas


	--- cash deposit entry

	--- check deposit entry





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

	DM (Debit Memo) same as CM:
		utang ng customer (selling)

	Edit sales term:
		if terms (6 months, 12 months, etc), then cashier will call accounting



---------- end of iBAS





Application:
	Home credit - third party, no items, borrowed items from store and debt from the store
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

	penalty after 5 days not bayad in due date
	total balance * 5 % if penalty (compounding)


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


if item deposit and pullout, the item will store at the store


---release of depo item before ---collection


--- release of depo item:
	search for customer


-- skip docs series
	magbabayad from other branches to the main branches kung saan bumili ang customer


----- deferred repo transaction - modules from deferred
	---ar others
		account type: repo customer
		then S.O.

	---sales order
		add serial number
		no discount


		serial number - have RE on the number to identify the item as repo
	

	--- repo sales - next

	--- cash receipt or check, etc. - next

	MCAir - another company - fix aircon





------iBAS
--- item master
	macsbe and ibas is the same function, diff using

	--- suppliers info
	user: merchandizer


	search for string code > list item
	if no item barcode (or info) > new

	new:
		trade outright - lahat ng dumating na item, babayaran
		trade consignment - kung ano lang
		non-trade - gas, electric, walang kapalit na item
		branch - branches
		refund - madalang


		inputs:
			zip code  along with type of supplier: local, foreign

		default term code: ilang araw bago bayaran
		
		tag TMEI/DAEI
	


	if supplier is new > merchandizing will create new suppliers info

	if supplier is created > add item barcode

	item name structure: brand name model

	brand: new add the new brand name



	disable item categ because the sub categ will also fall to item categ(auto select categ)


	stock type:
		fixed assets
		inventory
		other

	barcode size:
		small
		large


	merchandizing can select if serialize or not

	product line:
		depending on item categ


		size: no if not TV
		costing type:
			costed
			bundle
			free

		purchase type: depend on the input before



	-- cost
	peso (puhunan): 500
	foreign: auto generated

	sales margin: 0% if no sales


	unit measure and qty per unit - no input because it is:
		for MCAir

	
	then save





	Transaction > P.O. ---purchase order (local) 

	--- purchase order (local)
		if not item to current branch and other branch, will call merchandizer
		inputs:
			location: central warehouse
			department: SDH Tarlac - Savers Digital H? Tarlac


			auto vat depends on previous input on item master



		delivery date:
			30 days period

		choose pick up item cost


		item code:
			item code: 8 digits only

		
		save > return pdf P.O. purchase order


		then --- P.O. monitoring
			approved if authorized or have permission
		
		P.O. then pending > will verified > will approved


		serialized - select the item and ref no: DR#, P.O.R. direct deliver

		non-serialized - scan the item and email the D.R. Delivery Receipt, quantity only for validation, manager will be accountable

		if wearhouse have to received

		inventory control > transaction > PO Receipt (local currency)

		merchandizer PO > deliver item to branch > item serialized
		IC > POR direct deliver > input serial > have slip > slip attach to DR of supplier for 

		wearhouse > IC

		central warehouse > not manual key in > load 


	if POR direct, choose delivery man
	if not POR direct, choose the manager

	warehouse > POR > STF

	T.F. Transfer Form

	after PO di pa dumarating

	PO sa branch and POR sa branch




	merchandizing purchase items that branch request
	PO if stock in warehouse
	if there are stock only stock transfer

	warehouse > load items if serialize > scan

	model/sku/item if serialize then pop up screen > screen will barcode > 
	POR direct deliver - bagsak deliver direct to the branch, enter serialized item

	if POR direct delivery

	if item direct to the branch
	
	POR direct delivery



	merchandizing PO > save > have slip and have PO number
	branch POR direct deliver > search for PO > enter serial > save
	PO > brand delivery items to store > scan serial > have DR > to warehouse > PO Receipt (local) warehouse

	no serial because 

	common all PO to warehouse
	warehouse not using POR direct 


	PO direct warehouse > no scanning > PO
	PO direct deliver > 




	if not branch received > warehouse > 

	if item damaged, sent back to supplier:
		Purchase order return:
			enter item code then SN() for what item because every item has serial number
			item master will less

	AC > item put 10 > return 1 >




Account payable: dealing with anything that we have to have
or we have to claim as advances to 3rd party (supplier or dealer)


if may utang sa supplier at advances > AC


frontline see DR

Invoice from supplier will invoice to our system to receive

if invoice reference POR
--- invoice PO receipt
	supplier issue invoice to financing for payable







----- account payable
---- maintenance
--- supplier's info

	debit memo - advance to supplier

	how to pay debt to supplier:
		cheque - common payment
		cash
		debit memo - advancement: PO return, inventory cost advancement (per serial, per quantity) (rebate, discount), discount, manual, cheque advances(no invoice - issue to supplier)
			open debit - float advancement, pwedeng iapply sa invoice(utang sa supplier)

	


	--- PO  
		inputs:
			supplier with item
	

	PO > delivery warehouse (meaning no PO Direct Deliver) > PO Receipt (local currency) (final) (received) 

	open PO - no received or partial received

	if supplier D.R. or Invoice > Invoice PO Receipt

	PO > item deliver > supplier > invoice to us > 

	nagreturn tayo ng item, pero di pa nag appear ang minus > open debit

	---open debit ledger
		history

	---subsidiary ledger
		



GL modules
	open debit memo

payment pay > AP > transactions > AP payment


AP clerk cannot create cheque > need approvable > approve > ---approve to pay > search corporation >print the paper > sign by manager





---AP payment:
	for issuing cheque




--- bank credit card confirmation
	check if the bank pay us



more topics:
	fix asset
	general leadge


(customer) aging detailed
(customer) aging summary

(other ar) aging detailed
(other ar) aging summary - banks, suppliers, 





invoice PO Receipt to reflect items on the payments > approve to pay(manager) > print cheque > enter payments


PO rece > invoice por > approve to pay > payment



----- AP














javascript > jquery > typescript



-- PO
	choose supplier > choose term > input location> input department > purchase order


	PO submit to samsung > 

--- PO receipt (local)
	input PO no > input serial number of items na nadeliver > PO receipt > items input to item master(not payable)



	---ap
		--- transaction
			---- invoice po receipt:
				input supplier > choose or with the same PO number > check it then save > have payables


PO > invoice POR > AP(---approve to pay) > 
	--- approve to pay
		choose supplier > choose invoice no. > check full amount > save

	--- enter payment (ap payment)
		input supplier > input bank > check apply full amount checkbox > input amount > input ref no.(samsa..) > output 


approve to pay output approve to pay slip 
voucher > check/cheque
		

--- open debit - can apply without approve > save > output apply open debit slip 




---subsidiary ledge 
	summary of all payments



--- AP
	after enter payment (ap payment  - check/cheque ) > bawas utang (open debit) 

--- apply open debit


--- check releasing
	kapag irerelease ang cheche
	after makagawa ng check/cheque  > go to this
		pinapapirma sa supplier

--- check nogotiated
	bank accept the cheque and cleared

cost adjustment - discount




--- enter payable
--- void check
	check/cheque

--- void payable






--- skip check
	cheque payment - reserve


--- drawings entry
	lipat per

--- funds transfer (local to local)
	bank to bank






	



















	
	









	
















		

		


	
		
		

		


		



















	



	
	












	












	
	

	

	



	











		






















	






















































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