# GNU Taler

↑ **Parent:** [Electronic money](electronic-money.md)  
🏷️ **Tags:** [GNU package](gnu-package.md)

Centralized system that still attempts some level of privacy.

In it, a central bank issue tokens that are stored offline in your cell phone, a bit like cash bank notes.

When you take those tokens, a corresponding amount gets removed from your bank account, a bit like cash bank notes.

When a transaction is made, tokens are put into a spent token list via central API, and cannot be double spent thereafter. The corresponding ammount is then added to the bank account of the receiver. This also means that offline transactions are not possible.

When emitting, the bank signs the token with their private key. When spending, the bank checks that signature.

How do we prevent the bank from logging which token goes to which user besides trusting that they are running the software we whink they are running? Notably, couldn't timing be used to identify that?

## ↑ Ancestors (9)

1. [Electronic money](electronic-money.md)
2. [Digital currency](digital-currency.md)
3. [Fiat currency](fiat-currency.md)
4. [Currency](currency.md)
5. [Money](money.md)
6. [Social technology](social-technology-split.md)
7. [Area of technology](area-of-technology.md)
8. [Technology](technology-split.md)
9. [Ciro Santilli's Homepage](split.md)
