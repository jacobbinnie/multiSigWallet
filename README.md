// Hey! Thanks for checking out my Multi Sig Wallet. Follow me on github for more at github.com/jacobbinnie

//      NOTE:
//      For the example below, I used 3x owner accounts with a minimum of 2 confirmations required to execute the transaction.

//      1)
//      Simply enter a few remix 0x addresses into the deploy function and specify the number of confirmations required in order for the transaction to execute. For my example, I added 3X addresses and 2 as the minimum confirmations. Deploy the contract.
//      Fund the contract with an owner address for 2 Ether using the deposit function.

//      2)
//      Choose another address from remix that is NOT associated as an owner.
//      Enter this address into the submitTransaction field with a uint256 value of wei (must be 18 digits) to send. For the transaction bytes, send 0x. Ensure you are doing this using one of the owner accounts.

//      3)
//      If successful, a new transaction will have been added to the _txIndex. Find the getTransaction call function and submit an index value of 0.
//      This will return that transaction's data. You'll also notice the current number of confirmations is 0.

//      4)
//      As your first owner account, find the confirmTransaction function. Enter an index value of 0 and confirm the transaction.
//      Now we only need one more confirmation in order for this transaction to execute. You'll even notice that the numConfirmations in the getTransaction function updates if called at index 0 again.
//      You can try the executeTransaction function using an index of 0 to test the Multisig. It should fail.
//      As your second owner account, find the confirmTransaction function. Enter an index value of 0 and confirm the transaction. Now 2x confirmations have occurred.

//      5)
//      Now you can execute the transaction by entering an index of 0 into the executeTransaction function.
//      Now, browse back to the original remix wallet address that we wanted to send funds to. You'll notice that it has now received funds.
