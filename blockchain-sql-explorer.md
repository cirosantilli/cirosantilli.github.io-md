# Blockchain SQL explorer

↑ **Parent:** [Blockchain explorer](blockchain-explorer.md)

- [https://bitcoin.stackexchange.com/questions/11687/reliable-efficient-way-to-parse-the-blockchain-into-a-sql-database](https://bitcoin.stackexchange.com/questions/11687/reliable-efficient-way-to-parse-the-blockchain-into-a-sql-database)
- [https://bitcoin.stackexchange.com/questions/93080/what-is-the-currently-most-efficient-and-reliable-method-to-store-the-bitcoin-bl?noredirect=1&lq=1](https://bitcoin.stackexchange.com/questions/93080/what-is-the-currently-most-efficient-and-reliable-method-to-store-the-bitcoin-bl?noredirect=1&lq=1)
- [https://www.reddit.com/r/Bitcoin/comments/6wcbbs/recent_blockchain_sql_dumps/](https://www.reddit.com/r/Bitcoin/comments/6wcbbs/recent_blockchain_sql_dumps/)
- [https://bitcointalk.org/index.php?topic=5464721.0](https://bitcointalk.org/index.php?topic=5464721.0)

Cloud options:
- [Google BigQuery](google-bigquery.md): [https://cloud.google.com/blog/topics/public-datasets/bitcoin-in-bigquery-blockchain-analytics-on-public-data](https://cloud.google.com/blog/topics/public-datasets/bitcoin-in-bigquery-blockchain-analytics-on-public-data) Sample query to get all addresses ever:
  ```
  SELECT block_number, transaction_hash, index, type, addresses, value
  FROM `bigquery-public-data.crypto_bitcoin.outputs`
  ORDER BY block_number ASC, transaction_hash ASC, index ASC, index ASC
  LIMIT 100
  ```

  First output lines:
  ```
  block_number,transaction_hash,index,type,addresses,value
  0,4a5e1e4baab89f3a32518a88c31bc87f618f76673e2cc77ab2127b7afdeda33b,0,pubkey,[1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa],5000000000
  1,0e3e2357e806b6cdb1f70b54c3a3a17b6714ee1f0e68bebb44a74b1efd512098,0,pubkey,[12c6DSiU4Rq3P4ZxziKxzrL5LmMBrzjrJX],5000000000
  2,9b0fc92260312ce44e74ef369f5c66bbb85848f2eddd5a7a1cde251e54ccfdd5,0,pubkey,[1HLoD9E4SDFFPDiYfNYnkBLQ85Y51J3Zb1],5000000000
  ```
- [Amazon Athena](amazon-athena.md): [https://aws.amazon.com/blogs/web3/access-bitcoin-and-ethereum-open-datasets-for-cross-chain-analytics/](https://aws.amazon.com/blogs/web3/access-bitcoin-and-ethereum-open-datasets-for-cross-chain-analytics/)

## ↑ Ancestors (11)

1. [Blockchain explorer](blockchain-explorer.md)
2. [How to extract data from the Bitcoin blockchain](how-to-extract-data-from-the-bitcoin-blockchain.md)
3. [Bitcoin](bitcoin.md)
4. [List of cryptocurrencies](list-of-cryptocurrencies.md)
5. [Cryptocurrency](cryptocurrency-split.md)
6. [Blockchain](blockchain.md)
7. [Money](money.md)
8. [Social technology](social-technology-split.md)
9. [Area of technology](area-of-technology.md)
10. [Technology](technology-split.md)
11. [Ciro Santilli's Homepage](split.md)
