# CIPHER SHIFTED BY PREDEFINED SHIFT
plaintext = input('Enter Message: ')
alphabet = 'abcdefghijklmnopqrstuvwxyz'
space = ' '
k = 4
ciphertext = ' '
for c in plaintext:
    if c == i alphabet:
        ciphertext += alphabet[(alphabet.index(c)+k)%(len(alphabet))]
    elif c i space;
        ciphertext += ' '
    else:
        ciphertext += c


print('Encrypted Message is', ciphertext)

