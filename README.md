# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:

```
#include <stdio.h>
#include <string.h>
#include <ctype.h>
int main() {
 char text[100];
 int key;
 printf("Enter plaintext: ");
 scanf(" %[^\n]", text);
 printf("Enter key: ");
 scanf(" %d", &key);

 char encrypted[100];
 strcpy(encrypted, text);
 for (int i = 0; i < strlen(encrypted); i++) {
 if (isalpha(encrypted[i])) {
 char base = isupper(encrypted[i]) ? 'A' : 'a';
 encrypted[i] = (encrypted[i] - base + key) % 26 + base;
 }
 }
 printf("Encrypted text: %s\n", encrypted);

 char decrypted[100];
 strcpy(decrypted, encrypted);
 for (int i = 0; i < strlen(decrypted); i++) {
 if (isalpha(decrypted[i])) {
 char base = isupper(decrypted[i]) ? 'A' : 'a';
 decrypted[i] = (decrypted[i] - base - key + 26) % 26 + base;
 }
 }
 printf("Decrypted text: %s\n", decrypted);
 return 0;
}
```
## OUTPUT:
<img width="902" height="447" alt="image" src="https://github.com/user-attachments/assets/dc069e2d-ee5b-4f1e-8f84-3640f5fa02ea" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
