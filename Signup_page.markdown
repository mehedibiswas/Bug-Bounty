### Testing injections:
            a)html
            b)sql
            c)xxe
            d)Nosql
            e)xss

### Parameter guessing:
      Use burpsuite extention param miner to guess any paremeter.Something like "isAdmin:True", "id:0","isDevelper:true" etc.This vulnerability is known as mass 
      assignment.

### Testing Duplicate username:
      Check if same username or email can be used to create two different accounts.

### Password Validations:
      Check if password is validating only client side.The requirments such as 1 capital,number and special char, password length etc.

### Without email verification:
      Try to signup without verifications of email.
