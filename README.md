# Distributed Ledger Mutual Fund Accounting 
This code attempts to replicate Transfer Agent functions (trading, transfers, dividends,etc) for Level3 & Omnibus mutual funds on a distributed ledger. The native Ethereum EVM was chosen mainly due to security and thru-put needs, as the volume of Transfer Agent (TA) processing would not come close to the needs of a Layer2 or other scaling solution.  This is a work in process, and even if functional would still require signaficant changes to Investment Company Act of 1940, SEC 15c3-3, FINRA 11870, as well many others, primarily related to $ clearing and ACATS.
  
# Why mutual funds?
Mutual fund processing, and Transfer Agency services in general, does not rely on real-time price information. The price of a mutual fund (NAV) is determined only once per day 4pm EST M-F (not including US Equity market holidays), and any transactions submitted to the mutual fund are based on this once-a-day price. The regulated platform behind mutual fund trading and settlements is known Fund/SERV®, a product of the NSCC/DTCC. This is the U.S. industry standard for settling mutual fund, bank collective fund and other pooled investment products between fund companies and distributors (brokers/intermediaries). 
  
# Why distributed ledgers?
As noted above, the current mutual fund industry infrastructure updates once a day. Of the 500+ mutual fund companies with publicly registered securities, the majority entrust their Transfer Agent processing to one or two companies. These companies can be considered centralized record-keepers for ownership of shares. In most cases, mutual funds behave like the UTXO accounting model behind Bitcoin (more on this later).

# Minimum Requirements
1. Basic functionality: The smart contract would need to include the basic functionality of a mutual fund processing platform, including the ability to process trades, transfers, and dividends, as well as calculate daily NAV for each fund.

2. Level 3 and Omnibus accounting: The smart contract would need to include support for Level 3 and Omnibus mutual fund accounting, as these are common methods used by publicly registered broker-dealers to manage their clients' investments.

3. User permissions and administration protections: The smart contract would need to include a multi-signature authorization system that allows a designated group of administrators to control key aspects of the platform, such as the vendor supplying NAV data, original registration information, and overwrite privileges.

4. Integration with third-party data sources: The smart contract would need to be able to integrate with third-party data sources to obtain daily NAV information, as well as other data related to mutual fund performance.

5. Registration and compliance: The smart contract would need to include functionality to track the registration and compliance status of all parties involved in mutual fund processing, including broker-dealers, Transfer Agents, and Fund Companies.

6. Security and privacy: The smart contract would need to be designed with security and privacy in mind, and should include measures such as data encryption, access controls, and auditing functionality to ensure that all transactions are recorded accurately and securely.
---------------

