### where to test

  Header
  Query string parameters
  Parameters in POST/PUT requests
  
### How to test

  When reviewing API documentation, if the API is expecting a certain type of input (number, string, boolean value) send:

    A very large number
    A very large string
    A negative number
    A string (instead of a number or boolean value)
    Random characters
    Boolean values
    Meta characters

[If a certain type of input causes a verbose error or causes a delayed response then you could be on the trail of an injection vulnerability.]

sql meta character:

'

''

;%00

--

-- -

""

;

' OR '1

' OR 1 -- -

" OR "" = "

" OR 1 = 1 -- -

' OR '' = '

OR 1=1


Nosql meta character:

$gt 

{"$gt":""}

{"$gt":-1}

$ne

{"$ne":""}

{"$ne":-1}

 $nin

{"$nin":1}

{"$nin":[1]}

{"$where":  "sleep(1000)"}


Command injection meta character:

|

||

&

&&

'

"

;

'"



