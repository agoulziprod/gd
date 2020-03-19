# Code example and ..

GitDocs was built by the good folks over here at [Timber](https://timber.io). You should check us out.

# This is another title

and here is the code as u see:

```javascript
C_TEXT($1;$attribut)
C_TEXT($0;$value)

ARRAY OBJECT($_adresses;0)
C_OBJECT($address)
C_OBJECT($detail)

$attribut:=$1

OB GET ARRAY([Member]address;"address";$_adresses)
If (Size of array($_adresses)>0)
	
	$address:=$_adresses{1}
	$detail:=OB Get($address;"detail";Is object)
	$value:=OB Get($detail;$attribut;Is text)
Else 
	$value:=""
End if 

$0:=$value
```