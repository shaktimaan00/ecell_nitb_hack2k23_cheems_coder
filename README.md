
# Graphical Authentication System for Online Banking

A graphical authentication system for online banking is a type of authentication method used to secure online banking transactions. This system is based on graphical passwords that are easier for users to remember than traditional text-based passwords. Instead of requiring users to remember and enter a string of text, a graphical authentication system presents users with a series of graphical images and asks them to select a specific image or sequence of images. The image selection process serves as the user's password and is used to confirm the user's identity before allowing access to their online banking account.


## Features

- Light/dark mode toggle.
- Friendly User Experience.

## Project flow

- First the pages are divided into two sections Signup and Login page.
  - Signup Page
    - You can choose to enter your email address and password, then click the "next" button.
    - Then it will have a grid of five by five emojis to choose four of the available twenty-five, and this transforms into encrypted data that is saved in a real-time firebase database.
    - The encryption technique sha-256 is used to encrypt data which uses cryptographic hash function that produces a 256-bit hash value.
  - Login Page
    - You can choose to enter your email address and password, then click the "next" button.
    - Then to authenticate the randomized grid of five by five to choose your serialized password and you have only 3 chances to choose the correct one, if it exceeds the account will be terminated for 48 hours.

## Implementation Techniques

- Grid generation :- A grid of five by five is generated randomly, then user needs to select the 4 out of 25 grids, that selected grids is the sequential pattern which user needs to remember and use it everytime they login.
- Encryption Technique :- The grids which user selects as password is then encypted using a hash algorithm like SHA-256 which is computationally infeasible to recreate the original password from the hash.
- Database :- The email, password and encrypted image is stored into the firbase database.

