In this challange we are provided with a png file

Using String gives us a kind of poem without any hint towards our flag


![[Pasted image 20250828151944.png]]

since this is a png file we cant use exif but exiftool can be handy here...lets try that 
![[Pasted image 20250828152231.png]]

this gives us an overview of the metadata but no clue to getting our flag here
Next thing that comes in mind is to dig further and apply some stegnography  skills a tool such as zsteg comes in mind and using zsteg we get 

![[Pasted image 20250828152523.png]]

we can see the meta poem again but by now we are sure its just a decoy as it has no connection to getting the flag.

Looking closely we see a hidden base64 string for b1,rgba,msb,xy 

- **`b1`** → “bit plane 1” (the **least significant bit**).
    
- **`rgba`** → It looked at all 4 channels (Red, Green, Blue, Alpha).
    
- **`lsb`** → extraction from the **least significant bits**.
    
- **`xy`** → standard pixel ordering (row by row).

with we can decode this string on cyberchef to get the flag to be picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}




