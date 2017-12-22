# Encryption and decryption with input key
choice = input("Choose e for encrytpion or d for decryption:")
plaintext = input('Enter Message:')
alphabet = 'abcdefghijklmnopqrstuvwxyz'
space = ' '
k = 4
key = input("Enter key:")
ciphertext = ' '
while(len(key) < len(plaintext)):
    key += key
if (choice == 'e'):
        
    for c in plaintext:
        if c in alphabet:
            ciphertext += alphabet[(alphabet.index(c)+k)%(len(alphabet))]
        elif c in space:
            ciphertext += ' '
    else:
        ciphertext += c
        k += 1

if (choice == 'd'):
    for c in plaintext:
        if c in alphabet:
                ciphertext += alphabet[((alphabet.index(c)-alphabet.index(key[k]))%(len(alphabet)))] 
        elif c in space:
            ciphertext += ' '
        else:
            ciphertext += c
        k += 1



print('Encrypted Message is', ciphertext)

