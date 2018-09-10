
### Posting example of javascript 


```javascript

function mailcheck()  // = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = =
{
	var ierrcnt = 0 ; 
	var sErrDesc = "" ;

	//	alert("Your survey BRI has " + ierrcnt + " error\n" + serrdesc );	
//  doc is "email_bri"
//	alert("Testing...");

	var iVerchkno1 = -1 ; 
	var iVerchkno2 = -1 ; 
 	for (i=0;i<=1; i++ ) 
	{
		if (document.email_bri.bver1[i].checked) 
		   iVerchkno1 = i+1 ;
	} // for (i=0,i<=3, i++ )
	if (iVerchkno1 <= 0)
	{
		ierrcnt++ ; 
		sErrDesc += "> Person 1 missing version selection\n" ; 
	}
	
	if (document.email_bri.nfirst1.value <= " " && document.email_bri.nlast1.value <= " ")
	{
		ierrcnt++ ; 
		sErrDesc += "> Person 1 needs a first and/or last name\n" ; 	
	}
	
	if ( document.email_bri.email1.value <= " " )
	{
		ierrcnt++ ; 
		sErrDesc += "> Person 1 e-mail address is blank\n" ; 	
	}	


	// Check second person, if applicable = = = = = = = = = = = = = = = = = = = = =
	if (document.email_bri.ignore2.checked) 
		sErrDesc += ""  // "> ignore checked \n" ; 	
	else
	{
		// We need to check person 2 - - - - - - - -
	 	for (i=0;i<=1; i++ ) 
		{
			if (document.email_bri.bver2[i].checked) 
			{
			   iVerchkno2 = i+1 ;
			}
		} // for (i=0,i<=3, i++ )
		if (iVerchkno2 <= 0)
		{
			ierrcnt++ ; 
			sErrDesc += "> Person 2 missing version selection\n" ; 
		}
		
		if (document.email_bri.nfirst2.value <= " " && document.email_bri.nlast2.value <= " ")
		{
			ierrcnt++ ; 
			sErrDesc += "> Person 2 needs a first and/or last name\n" ; 	
		}
	
		if ( document.email_bri.email2.value <= " " )
		{
			ierrcnt++ ; 
			sErrDesc += "> Person 2 e-mail address is blank\n" ; 	
		}			
		
		if (document.email_bri.part2.checked) 
		{
			//sErrDesc += "> Partner checked\n" ; 		
			if (iVerchkno1 != 1 || iVerchkno2 != 1 )
			{
				ierrcnt++ ; 
				sErrDesc += "> For partner selection, both persons need to be Social version\n" ; 		
			}
		}
		
	} // if (document.email_bri.ignore2.checked) else  
	
	// See if we need to return True or False - - - - - -
	if (ierrcnt > 0 )
	{
		alert(sErrDesc);
		return false ; 
	}
	else
	{
//		alert("iVerchkno:" + iVerchkno);
		return true ; 
	}

} // function mailcheck()
 	
	
function handkey(element) 		// = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = =
{
//	var elmtname = element.name;
	document.email_bri.ignore2.checked = false ; 
	
} // function handkey(element) 	

```

```PHP
<?PHP

	$var = 1 + 1 ; 

?>

```

