So ownership logic works as contract uses constructor and inside the `constructor()`, we run the line `owner = msg.sender`.
This runs once when the contract is deployed, permanently saving the address of the deployer as the owner.
To restrict the access the `withdraw()` function includes a security check:
`require(msg.sender == owner);` 
where if the accesser is not the owner then the accesser can't use the personal saving banks for his own beneficiary purposes.
