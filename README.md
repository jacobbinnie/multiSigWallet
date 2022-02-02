<h1>The Multi Sig Wallet</h1>

<h3>This Multi Sig Wallet allows an owner to assign other owners authority to approve transactions on this contract. A minimum number of confirmations may also be set by the contract deployer.</h3>

<p><img alt="" src="https://uploads-ssl.webflow.com/61e4bede52417c68fe202935/61f9ff84fabcc90c22bf1587_61e4bedf52417c2ca3202a5b_sciops-hero-1.jpg" style="height:420px; width:600px" /></p>

<h3><br />
<strong>TRY FOR YOURSELF</strong></h3>

<ul>
	<li>Create a new remix project at https://remix.ethereum.org/</li>
	<li>Create a file called multiSigWallet.sol</li>
	<li>Paste the contract code from contracts/multiSigWallet.sol</li>
</ul>

<h3>Instructions:</h3>

<p>Choose a few remix 0x addresses into the deploy function and specify the number of confirmations required in order for the transaction to execute. You&#39;ll need to format the addresses as shown below. For my example, I added 3x addresses and 2 as the minimum confirmations.</p>

<p><br />
<br />
[&quot;0x1234&quot;,&quot;0x5678&quot;,&quot;0x0987&quot;]<br />
2</p>

<p><strong>Deploy the contract.</strong></p>

<p>&nbsp;</p>

<p>Fund the contract with an owner address for 2 Ether using the deposit function.</p>

<p>Choose another address from remix that is NOT associated as an owner.</p>

<p>Enter this address into the <strong>submitTransaction</strong> field with a uint256 value of wei (must be 18 digits) to send. For the transaction bytes, send 0x. Ensure you are doing this using one of the owner accounts.</p>

<p>&nbsp;</p>

<p>If successful, a new transaction will have been added to the <strong>_txIndex</strong>. Find the <strong>getTransaction</strong> call function and submit an index value of 0.</p>

<p>This will return that transaction&#39;s data. You&#39;ll also notice the current number of confirmations is 0.</p>

<p>&nbsp;</p>

<p>As your first owner account, find the <strong>confirmTransaction</strong> function. Enter an index value of 0 and confirm the transaction.</p>

<p>Now we only need one more confirmation in order for this transaction to execute. You&#39;ll even notice that the <strong>numConfirmations</strong> in the <strong>getTransaction</strong> function updates if called at index 0 again.</p>

<p><u>Bonus</u>: You can try the <strong>executeTransaction</strong> function using an index of 0 to test the Multisig. It should fail.</p>

<p>As your second owner account, find the <strong>confirmTransaction</strong> function. Enter an index value of 0 and confirm the transaction. Now 2x confirmations have occurred.</p>

<p>&nbsp;</p>

<p>Now you can execute the transaction by entering an index of 0 into the <strong>executeTransaction</strong> function.</p>

<p>Now, browse back to the original remix wallet address that we wanted to send funds to. You&#39;ll notice that it has now received funds.</p>

<p>&nbsp;</p>

<p>Thanks! Let me know if you have any questions.&nbsp;</p>

<p>Jacob</p>
