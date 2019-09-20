 # Encryption Decryption 
 ````
 sample input
 a
 sample output
 e
 
 ````

		var x=document.getElementById("enc_button");
		var y=document.getElementById("dec_button");


		var dict_enc={'a':'e','b':'f','c':'g','d':'$','e':'i','f':'j','g':'k','h':'l','i':'m','j':'%','k':'o','l':'p',
		'm':'q','n':'*','o':'s','p':'t','q':'u','r':'v','s':'w','t':'?','u':'@','v':'z','w':'a','x':'b','y':'#','z':'d',' ':' '};
		var dict_dec={' ':' ','d':'z','#':'y','b':'x','a':'w','z':'v','@':'u','?':'t','w':'s','v':'r','u':'q','t':'p','s':'o','*':'n','q':'m'		
,'p':'l','o':'k','%':'j','m':'i','l':'h','k':'g','j':'f','i':'e','$':'d','g':'c','f':'b','!':'e'};

x.addEventListener("click", function()
	{
		document.getElementById("dec").value=encrypt(document.getElementById("enc").value);
	});
y.addEventListener("click", function()
	{
		document.getElementById("enc").value=decrypt(document.getElementById("dec").value);
	});

function encrypt(str){
	new_str=""
	for (var i = 0; i < str.length; i++) {
		if (str.charAt(i)=="\n")
		{
			new_str+="\n";
			continue;
		}
    new_str+=dict_enc[str.charAt(i)];
}
return new_str;
	}

function decrypt(str){
	new_str=""
	for (var i = 0; i < str.length; i++) {
   new_str+=dict_dec[str.charAt(i)];
}
return new_str;
	}
