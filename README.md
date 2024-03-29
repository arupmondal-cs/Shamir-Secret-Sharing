## Shamir's Secret Sharing Scheme

Shamir's Secret Sharing is an algorithm in cryptography created by Adi Shamir. It is a form of secret sharing, where a secret is divided into parts, giving each participant its own unique part.

To reconstruct the original secret, a minimum number of parts is required. In the threshold scheme this number is less than the total number of parts. Otherwise all participants are needed to reconstruct the original secret.

## High-level Explanation

Shamir's Secret Sharing is used to secure a secret in a distributed way, most often to secure other encryption keys. The secret is split into multiple parts, called **shares**. These shares are used to reconstruct the original secret.

To unlock the secret via Shamir's secret sharing, you need a minimum number of shares. This is called the **threshold**, and is used to denote the minimum number of shares needed to unlock the secret. Let us walk through an example:

  * **Problem:** Company XYZ needs to secure their vault's passcode. They could use something standard, such as AES, but what                   if the holder of the key is unavailable or dies? What if the key is compromised via a malicious hacker or the                   holder of the key turns rogue, and uses their power over the vault to their benefit?

This is where SSS comes in. It can be used to encrypt the vault's passcode and generate a certain number of shares, where a certain number of shares can be allocated to each executive within Company XYZ. Now, only if they pool their shares can they unlock the vault. The threshold can be appropriately set for the number of executives, so the vault is always able to be accessed by the authorized individuals. Should a share or two fall into the wrong hands, they couldn't open the passcode unless the other executives cooperated.

## Execution

  ```
  $ python Shamir_Secret_Sharing.py
  ```
  
  ## References
  
   * https://en.wikipedia.org/wiki/Shamir%27s_Secret_Sharing
