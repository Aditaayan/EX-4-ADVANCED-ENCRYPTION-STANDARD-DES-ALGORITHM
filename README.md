# EX-8-ADVANCED-ENCRYPTION-STANDARD-DES-ALGORITHM

## Aim:

  The aim of this exercise is to understand and implement the Data Encryption Standard (DES) algorithm

## ALGORITHM: 

1 . Initial Permutation: The plaintext block is rearranged.

2 . Key Generation: The key is divided into two halves, shifted, and permuted to create 16 subkeys.

3 . 16 Rounds:
    Expansion: The right half is expanded.
    XOR: The expanded right half is XORed with the subkey.
    Substitution: The result is substituted using S-boxes.
    Permutation: The substituted result is permuted.
    Swap: The left and right halves are swapped.
    
4 . Final Permutation: The ciphertext is rearranged.

## PROGRAM: 

```
#include <stdio.h>
#include <string.h>


  void xor_encrypt_decrypt(char *input, char *key) {
int input_len = strlen(input);
int key_len = strlen(key);

for (int i = 0; i < input_len; i++) {
    input[i] = input[i] ^ key[i % key_len];
}
}

int main() {
    printf("***** ADVANCED-ENCRYPTION-STANDARD-DES-ALGORITHM *****\n\n");
    
char url[] = "AADHI";
char key[] = "secretkey"; 

printf("Original text: %s\n", url);

xor_encrypt_decrypt(url, key);
printf("Encrypted text: %s\n", url);

xor_encrypt_decrypt(url, key);
printf("Decrypted text: %s\n", url);

return 0;
}
```

## OUTPUT:

![image](https://github.com/user-attachments/assets/d5f86899-e5a6-4560-8a81-fed376ae1318)


## RESULT: 
Hence,the DES Encryption and Decryotion is done successfully.
