# GNU Privacy Guard

↑ **Parent:** [Cryptography](cryptography-split.md)  
🏷️ **Tags:** [GNU package](gnu-package.md)  
ⓦ [Wiki](https://en.wikipedia.org/wiki/GNU_Privacy_Guard)

Generate public private key, test encrypt and test decrypt:
```
# Create your pubkey.
gpg --gen-key
gpg --armor --output pubkey.gpg --export <myemail>

# Encrypt using someone's pubkey.
gpg --import pubkey2.gpg
echo 'hello world' > hello.txt
gpg --output hello.txt.gpg --encrypt --recipient <other-email> hello.txt

# Double check it is not plaintext in the encrypted message.
grep hello hello.txt.gpg

# Decrypt.
gpg --output hello.decrypt.txt --decrypt --recipient <myemail> hello.txt.gpg
diff -u hello.decrypt.txt hello.txt
```

## ↑ Ancestors (7)

1. [Cryptography](cryptography-split.md)
2. [Computer science](computer-science-split.md)
3. [Computer](computer-split.md)
4. [Information technology](information-technology.md)
5. [Area of technology](area-of-technology.md)
6. [Technology](technology-split.md)
7. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [How to contact Ciro Santilli](contact.md)
