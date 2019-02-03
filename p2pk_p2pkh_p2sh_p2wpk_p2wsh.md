# P2PK, P2PKH, P2SH, P2WPK, P2WSH... what the f** is happening

Bitcoin, as a public ledger, maintains a set of Unspent Transaction Outputs (UTXOs). Each UTXO has a certain amount of bitcoins locked in.

## Main concepts

When someone wants to send bitcoins (from UTXOs) has to fill a field inside the transaction. This field is a *lock* and will be only opened if its conditions are satisfied by the redeemer (who wants to spend bitcoins). This field is named **Pubkey Script or ScriptPubKey**.

By the other hand, the redeemer has to provide the necessary input data to Pubkey script to evaluate correctly. Otherwise, he won't be able to spend bitcoin. This input data is named **Signature script or ScriptSig**.

That's it, only 2 terms are used to lock/unlock bitcoins:

1. Pubkey or ScriptPubKey
2. Signature script or ScriptSig

A tip to remember these concepts:

1. Pubkey or ScriptPubKey: 
    * PubKey (Public Key) --> Lock bitcoins
2. Signature script or ScriptSig: 
    * Sig (Signature) --> Unlock bitcoins

These two variables are script, ie are programs, written in a language similar to Forth:

```Bitcoin uses a scripting system for transactions. Forth-like, Script is simple, stack-based, and processed from left to right. It is intentionally not Turing-complete, with no loops. ```https://en.bitcoin.it/wiki/Script


to choose from the following **standard** destinations (As of Bitcoin Core 0.9)[[1]]:

* Pubkey
* Pay To Public Key Hash (P2PKH)
* Pay To Script Hash (P2SH)
* Multisig
* Null Data

### Pubkey

This form is not commonly used anymore.

## References

[1]: https://bitcoin.org/en/developer-guide#standard-transactions[https://bitcoin.org/en/developer-guide#standard-transactions]

1. https://bitcoin.org/en/developer-guide#standard-transactions
