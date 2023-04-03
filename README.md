# Distributed Ledger Mutual Fund Accounting 
This code attempts to replicate Transfer Agent functions (trading, transfers, dividends,etc) in the Solidity programming language for Level3 & Omnibus mutual fund relationships. The native Ethereum EVM would be prefered to Layer 2 substrates, mainly due to thru-put needs and security. This is a work in process, and even if functional would still require signaficant changes to Investment Company Act of 1940, SEC 15c3-3, FINRA 11870, as well many others, primarily related to $ clearing and ACATS.
  
# Why mutual funds?
Mutual fund processing operates via rules governed by the NSCC and DTCC, known as Fund/SERV®. This is the U.S. industry standard for settling mutual fund, bank collective fund and other pooled investment products between fund companies and distributors (brokers/intermediaries). The current standards are limited by the speed of overnight dollar transactions/settlements, and effectively functions as multiple a read-only private blockchain that updates once a day. Brokers/intermediaries submit their transactions out to the NSCC, check the next day for any, and then reconcile/account for differences.
  
# Why distributed ledgers?
As noted above, the current mutual fund industry infrastructure updates once a day. Of the 500+ mutual fund companies with publicly registered securities, the majority entrust their Transfer Agent processing to one or two companies. These companies can be considered centralized record-keepers for ownership of shares. Prior to digital registrations, these were recorded with physical certificates for particular mutual fund directly in the client's name, but are now usually registered under the broker/intermedaries' name where a client may choose hold the shares.  
  
This mutual record-keeping arrangement of brokers and transfer agents means that there are always a minimum of 3 parties to every transaction: the client, the broker, and the Transfer Agent. Others may include the mutual fund company itself, or another broker/intermediary. 
  
For example,  
  
 > A client with cash at a broker may choose to buy a mutual fund. The desired fund must have a selling agreement to be traded through the broker, and a purchase requires changes to client, the broker, and the Transfer Agent that recording the transaction. The client must see shares eventually settled in their account, the broker must update its own records to account for the client position (and any newly created assets/liabilities), and the Transfer Agent must record shares as an individual client position (Level3), or an aggregated balance at the broker (Omnibus). Cash must be deducted from the client account and provided to the mutual fund company via the broker. The mutual fund company must also either increase its total holdings in the mutual fund by the net change in buys/sells of the underlying securities in the fund. 
  
> A client with an existing mutual fund position may choose to sell. The request to sell must be communicated to the broker (either at an individual or omnibus/aggregated level), and the sell must also be communicated to transfer agent. The fund company must be notified to reduce its total holdings in the mutual fund by the net change in buys/sells of the underlying securities in the fund. The client must see their balance in the fund decrease, and expect cash in return. 
  
> A client with an existing mutual fund position no longer wants to receive dividends in the payment of cash, but wants future dividends reinvested. The request to change dividend elections must be updated for the client, it may be updated for the broker or its intermediary(ies), and it may be updated at the Transfer Agent.   
  
In all cases, any tranasction with mutual fund requires multiple updates submitted to a centralized record-keeper. This submit-and-verify arrangement may allow for decentralized registration and processing of mutual funds with brokers and funds acting on a private permissioned chain. Distributed Ledger Mutual Fund Accounting can operate according to existing standards (NAV struck at 4pm EST), or allow for near real-time settlements with private or public payment rails, including USDC and FedNow. 
  
This  is a work in progress.
