# EX-NO-7-Implement-DES-Encryption

## Aim:

To use the Data Encryption Standard (DES) algorithm for a practical application, such as securing sensitive data transmission in financial transactions.

## ALGORITHM:

1. DES is based on a symmetric key encryption technique that encrypts data in 64-bit blocks.
2. DES uses a Feistel network structure with 16 rounds of processing for encryption.
3. DES has a 64-bit key, but only 56 bits are used for encryption (the remaining 8 bits are for parity).
4. DES applies initial and final permutations along with 16 rounds of substitution and permutation transformations to produce ciphertext.

## Program:
```
def xor_crypt(data, key):
    out = []
    key_len = len(key)
    for i in range(len(data)):
        out.append(chr(ord(data[i]) ^ ord(key[i % key_len])))
    return "".join(out)

msg = input("Enter message: ")
key = input("Enter key: ")

enc = xor_crypt(msg, key)

print("Encrypted:", end=" ")
for ch in enc:
    print(f"{ord(ch):02X}", end=" ")
print()

dec = xor_crypt(enc, key)
print("Decrypted:", dec)

```
## Output:
<img width="1920" height="1152" alt="Screenshot 2026-02-14 083048" src="https://github.com/user-attachments/assets/bfa7bc02-a6b6-465b-8559-929eea3e8767" />



## Result:
  The program is executed successfully

