# Solitaire Cipher
#### by Grace Cantarella and Anna Zhang

## Description
This is our repo containing our Python implementation of the Solitaire cipher. This cipher is traditionally carried out through non-electronic means—the message is encrypted and decrypted using a deck of 54 cards (13 cards in each suit and 2 jokers).

Our cipher has two modes: encrypt and decrypt.

Each mode has three separate key options: the first option is f (file), where the program will encrypt or decrypt based on a key provided in a file. The file must contain numbers from 1 to 54 separated by new lines. An example of a suitable file has been provided in the repo (key.txt).

The next option is o (order), where an ordering is provided via a string of numbers 1-54 separated by whitespace. See encryption examples for an example of how to format this input.

The third option is w (word), where the initial ordering is decided using a plaintext word. See encryption examples for an example of how to format this input.

Each mode also comes with the option to use verbose mode (v) in order to see the process of producing the keystream. See examples on how to pass this flag as an argument.

## Launch

### Encryption:

to encrypt using a key from a file:
```
make encrypt ARGS='[text] f [filename]'
#example: make encrypt ARGS='hello f yes.txt'
```

to encrypt using a predetermined order:
```
make encrypt ARGS='[text] o [order]'
#example: make encrypt ARGS='hello o "54 1 53 2 52 3 51 4 50 5 49 6 48 7 47 8 46 9 45 10 44 11 43 12 42 13 41 14 40 15 39 16 38 17 37 18 36 19 35 20 34 21 33 22 32 23 31 24 30 25 29 26 28 27"'
```

to encrypt using a plaintext keyword:
```
make encrypt ARGS='[text] w [keyword]'
#example: make encrypt ARGS='hello w yes'
```

### Decryption:

to decrypt using a key from a file:
```
make decrypt ARGS='[text] f [filename]'
#example: make decrypt ARGS='goodbye f no.txt'
```

to decrypt using a predetermined order:
```
make decrypt ARGS='[text] o [order]'
#example: make decrypt ARGS='goodbye o "1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54"'
```

to decrypt using a plaintext keyword:
```
make decrypt ARGS='[text] w [keyword]'
#example: make decrypt ARGS='goodbye w no'
```
### Verbose Mode:

to make encryption verbose:
```
make encrypt ARGS='[text] [mode f, o, or w] [keyword or filename] v'
#example: make encrypt ARGS='hello w yes v'
```

to make decryption verbose:
```
make decrypt ARGS='[text] [mode f, o, or w] [keyword or filename] v'
#example: make decrypt ARGS='goodbye f no.txt v'
```

 ## Citations
 https://www.schneier.com/academic/solitaire/  
 https://en.wikipedia.org/wiki/Solitaire_(cipher)
