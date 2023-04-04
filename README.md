# Distributed Ledger Mutual Fund Accounting 
This code attempts to replicate Transfer Agent functions (trading, transfers, dividends,etc) for Level3 & Omnibus mutual funds on a distributed ledger. The native Ethereum EVM was chosen mainly due to security and thru-put needs, as the volume of Transfer Agent (TA) processing would not come close to the needs of a Layer2 or other scaling solution.  This is a work in process, and even if functional would still require signaficant changes to Investment Company Act of 1940, SEC 15c3-3, FINRA 11870, as well many others, primarily related to $ clearing and ACATS.
  
# Why mutual funds?
Mutual fund processing operates via rules governed by the NSCC and DTCC, known as Fund/SERV®. This is the U.S. industry standard for settling mutual fund, bank collective fund and other pooled investment products between fund companies and distributors (brokers/intermediaries). The current standards are limited by the speed of the dollar (overnight transactions), and  functions as read-only private blockchain that updates once a day. Brokers/intermediaries submit their transactions out to the NSCC, check the next day for any (un)expected changes, and then reconcile/account for differences. It is specifically the nature of Fund/SERV® and Transfer Agent processing that allows for simple registration, accounting, and transactions via distributed ledger.
  
# Why distributed ledgers?
As noted above, the current mutual fund industry infrastructure updates once a day. Of the 500+ mutual fund companies with publicly registered securities, the majority entrust their Transfer Agent processing to one or two companies. These companies can be considered centralized record-keepers for ownership of shares. Prior to digital registrations, these were recorded with physical certificates for particular mutual fund directly in the client's name, but are now usually registered under the broker/intermedaries' name where a client may choose hold the shares. In most cases, mutual funds behave like the UTXO accounting model behind Bitcoin (more on this later).
   
To first understand why this concept makes sense, you must first understand muutal fund processing, at least from an extremely high level. 




---------------
<!--
This mutual record-keeping arrangement of brokers and transfer agents means that there are always a minimum of 3 parties to every transaction. These may include the client, the broker, and the Transfer Agent. Others may include the mutual fund company itself, or another broker/intermediary. 
  
For example,  
  
 > A client with cash at a broker may choose to buy a mutual fund. This requires an update to the broker, the fund 
 cash and share reconcilation 
  
> A client with an existing mutual fund position may choose to sell. The request to sell must be communicated to the broker (either at an individual or omnibus/aggregated level), and the sell must also be communicated to transfer agent. The fund company must be notified to reduce its total holdings in the mutual fund by the net change in buys/sells of the underlying securities in the fund. The client must see their balance in the fund decrease, and expect cash in return. 
  
> A client with an existing mutual fund position no longer wants to receive dividends in the payment of cash, but wants future dividends reinvested. The request to change dividend elections must be updated for the client, it may be updated for the broker or its intermediary(ies), and it may be updated at the Transfer Agent.   
  
In all cases, any tranasction with mutual fund requires multiple updates submitted to a centralized record-keeper. This submit-and-verify arrangement may allow for decentralized registration and processing of mutual funds with brokers and funds acting on a private permissioned chain. Distributed Ledger Mutual Fund Accounting can operate according to existing standards (NAV struck at 4pm EST), or allow for near real-time settlements with private or public payment rails, including USDC and FedNow. 
 ------------------
-->
