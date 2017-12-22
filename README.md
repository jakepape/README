# Encryption and Decryption with predefined key
plaintext = open("lab4file.txt") #open file
alphabet = 'abcdefghijklmnopqrstuvwxyz'
space = ' '
a=0
key = input("ESET415PROJECT") #key
cipher = ' '

while (len(key) < len(plaintext)):
    key += key
    
if (choice == 'e'):
    
    for c in plaintext:
        if c in alphabet:
            #position = (alphabet.index(c)+alphabet.index(key[a]))%len(alphabet)
            #print(position)
            #cipher += alphabet[position]
            cipher += alphabet[(alphabet.index(c)+alphabet.index(key[a]))%len(alphabet)]
        elif c in space:
            cipher += ' '   
        else:
            cipher += c
        a += 1
        
    


if (choice == 'd'):

    for c in plaintext:
        if c in alphabet:
            cipher += alphabet[(alphabet.index(c)-alphabet.index(key[a])%(len(alphabet)))] 
        elif c in space:
            cipher += ' '
        else:
            cipher += c
        a += 1

print('Encrypted Message is: ', cipher)
