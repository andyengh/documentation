========================
Main accounting concepts
========================

Double-entry bookkeeping
========================

Odoo automatically creates all the underlying journal entries for each of your accounting
transactions:

- Customer invoices;
- Vendor bills;
- Point-of-sale orders;
- Expenses;
- Inventory valuations;
- and more ..

Odoo follows the double-entry bookkeeping system, whereby the total amount debited always equals the
total amount credited.

.. seealso::
   - :doc:`Accounting Cheat Sheet <cheat_sheet>`

Accrual and cash basis methods
==============================

Odoo supports both accrual and cash basis reporting. This allows to report income/expense when
transactions occur (i.e., accrual basis), or when payment is made or received (i.e., cash
basis).

.. seealso::
   - :doc:`Cash basis <../taxation/taxes/cash_basis_taxes>`

Multi-company
=============

Odoo allows the management of several companies within the same database. Each company has its
:doc:`Chart of Accounts <initial_configuration/chart_of_accounts>` and gets consolidation reports
following its rules. Users can access several companies but can only work in one company at a time.

Multi-currency environment
==========================

Odoo offers a :doc:`multi-currency <../others/multi_currency>` environment with an automated
exchange rate to ease your international transactions. Every transaction is recorded in the
company's default currency; for transactions occurring in another currency, Odoo stores both the
value in the company's currency and the transactions' currency value. Odoo generates currency gains
and losses after reconciling the journal items.

.. seealso::
   - :doc:`Manage a bank in a foreign currency <../bank/setup/foreign_currency>`

International Standards
=======================

Odoo Accounting supports more than 70 countries. It provides the central standards and mechanisms
common to all nations, and thanks to country-specific modules, local requirements are fulfilled.
Fiscal positions exist to address regional specificities like the chart of accounts, taxes, and any
requirement.

.. seealso::
   - :doc:`Fiscal localization packages <../../fiscal_localizations>`

Accounts receivable and payable
===============================

By default, Odoo uses a single account for all account receivable entries and one all accounts
payable entries. Transactions are related to your contacts, which allow you to perform analysis per
customer, vendor or supplier.

The **Partner Ledger** report displays the balance of your customers and suppliers. It is available
by going to :menuselection:`Accounting --> Reporting --> Partner Ledger`.

Reporting
=========

The following financial :doc:`reports <../reporting/overview/main_reports>` are available and
updated in real-time:

- Statement reports: balance sheet, profit and loss, cash flow statement, tax report, ES sales list.
- Audit reports: general ledger, trial balance, journal report, intrastat report, check register.
- Partner reports: partner ledger, aged receivable, aged payable.
- Management: invoice analysis, unrealized gains/losses, depreciation schedule, disallowed expenses,
  budget analysis, product margins, 1099 report.
- Country specific reports based on your company's location and the fiscal localization packages
  installed on your database.

.. tip::
   Odoo's report engine allows you to customize your own report based on your own
   :doc:`formulas <../reporting/overview/customize>`.

Tax report
----------

Odoo computes all accounting transactions for the specific tax period and uses these totals to
calculate the tax obligation.

.. important::
  Once the tax report has been generated, Odoo does not allow to make journal entries involving VAT
  involving VAT in the closed period. If the period is locked, any correction to customer or vendor
  bills have to be recorded in the next period.

.. note::
   Depending on the country's localization, an .XML file can be generated to upload the tax report
   directly on the VAT platform of the legal administration.

Bank synchronization
====================

Odoo bank synchronization system directly connects with your bank institution to automatically
import all bank transactions into your database. This means a daily view about cashflow
will be available without having to log into the online banking system or wait for paper bank
statements.

.. seealso::
   :doc:`Bank Synchronization <../bank/bank_synchronization>`

Inventory Valuation
===================

Odoo support both periodic (manual) and perpetual (automated) inventory valuations. The available
methods are standard price, average price, LIFO and FIFO.

.. seealso::
   - :doc:`View impact of the valuation method on your transactions
     </applications/inventory_and_mrp/inventory/management/reporting/inventory_valuation_config>`

Easy retained earnings
======================

Retained earnings are the portion of income retained by your business. Odoo automatically calculates
your current year earnings in real-time, so no year-end journal or rollover is required. This is
calculated by automatically reporting the profit and loss balance to your balance sheet report.

.. seealso::
   - :doc:`Accounting Cheat Sheet <cheat_sheet>`

Fiduciaries
===========

The :guilabel:`Accounting Firms` mode can be activated from the Accounting Settings. When enabled:

- The document's sequence becomes editable on all documents;
- A new field :guilabel:`Total (tax incl.)` appears in order to speed up and control the encoding by
   automating line creation with the right account and tax;
- Default customer invoices and vendor bills dates are suggested.
