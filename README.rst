when trying to transfer Monero using monero-wallet-cli
==========================================================
The following error happend when trying to open a wallet using ombre-wallet-cli

"Error: refresh failed: no connection to daemon. Please make sure daemon is running.. Blocks received: 0"


Try this
--------------
* Exit ombred by typing exit.
* Delete p2pstate.bin (located in ~/.ombred Linux and Mac OS X) or C:\ProgramData\ombre (Windows)).
* Pop 10000 blocks using ombre-blockchain-import. :code:`./ombre-blockchain-import --pop-blocks 10000`
* Restart ombred and let it resync the last 10000 blocks.

Important note
---------------------
if the blockchain got corrupted somehow, this might not work.

Therefore, the blockchain must be sync from the beginning.
 
References
---------------
https://www.reddit.com/r/Monero/comments/8hd5qh/error_no_connection_to_daemon_please_make_sure/dyjf9lu/

https://monerodocs.org/interacting/monero-blockchain-import-reference/

https://monero.stackexchange.com/questions/1854/what-is-the-best-way-to-pop-the-top-block-from-the-monero-blockchain-and-fix-a-b
