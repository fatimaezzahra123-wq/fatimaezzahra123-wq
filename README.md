#casear cipher algorithm  for encryption and decryption
text=input("enter your text")
key=int(input("enter the key value"))
encrypted_text=""
for i in text :
    if i.isalpha():
       shift_base= 65 if i.isupper() else 97
       encrypted_text += chr((ord(i)-shift_base + key) % 26 +shift_base)
    else:
       encrypted_text+=i
 #print the encrypted text
print(f"Encrypted message:{encrypted_text}")

decrypted_text=""
for i in encrypted_text :
    if i.isalpha():
       shift_base= 65 if i.isupper() else 97
       decrypted_text+= chr((ord(i)-shift_base - key) % 26 +shift_base)
    else:
       decrypted_text+=i
#print the decrypted text
print(f"decrypted text:{decrypted_text}")
