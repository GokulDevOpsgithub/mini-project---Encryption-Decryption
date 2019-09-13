 #Encryption
 ````
 sample input
 a
 sample output
 e
 
 ```
 alphabet='abcdefghijklmnopqrstuvwxyz'
key = 4

newmsg = ''
message = raw_input("Enter the message")  

for character in message:
         
    position = alphabet.find(character) 
    newposition = (position+key)%26  
    newchar = alphabet[newposition]
    print 'Encrypted new character is',newchar
    newmsg+=newchar
print 'The encrypted final message is', newmsg

 
