This one contract regulates the incentive structure of Swarm.

# Methods

## Sign up as a node

Pay a deposit in Ether and register public key. Comes with an accessor for checking that a node is signed up.

## Demand compensation for loss of chunk

Present a signed receipt by a signed up node and a deposit covering the upload of a chunk. After a given deadline, the corresponding compensation is paid and the deposit refunded, unless the chunk is presented. Comes with an accessor for checking that a given chunk has been lost (compensation has been paid), so that other claimants can also demand their compensation.

## Present PoC to avoid paying compensation

No compensation is paid for lost chunks, if chunk is presented within the deadline. The cost of uploading the chunk is compensated exactly from the demand's deposit, with the remainder refunded. Comes with an accessor for checking that a given node is liable for compensation, so the node is notified to present the chunk in a timely fashion.