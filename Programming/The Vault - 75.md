Problem
===
Welp, looks like the source code to our bank got leaked. Ah well, that's not a big deal... right? 

http://pastebin.com/xRFWgnHR

Write-Up
===
Looking at the bottom of the code on pastebin:
```
int main(void)
{
	printf("Welcome to the most secure bank in NEO.");
  printf("%s\n", vault-1);
  return 0;
}
```

This line looked extremely suspicious, so we alter it give us what we need:
```
  printf("%s\n", vault-1);
```
```
  printf("%s\n", vault);
```

After compiling the code using gcc, we get the following:
```
Welcome to the most secure bank in NEO.
||====================================================================||
||//$\\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\//$\\||
||(100)==================| RESERVE BANK OF NEO  |================(100)||
||\\$//        ~         '------========--------'                \\$//||
||<< /        /$\              // ____ \\                         \ >>||
||>>|        //L\\            // ///..) \\              XXXX       |<<||
||<<|        \\ //           || <||  >\  ||                        |>>||
||>>|         \$/            ||  $$ --/  ||          XXXXXXXXX     |<<||
||<<|     Free to Use        *\\  |\_/  //*                        |>>||
||>>|                         *\\/___\_//*                         |<<||
||<<\      Rating: E     _____/ F LAG{HI_\________    XX XXXXX     />>||
||//$\                 ~|    REPUBLIC_OF_NEO}A_  |~               /$\\||
||(100)===================   ONE HUNDRED RUPEES =================(100)||
||\\$//\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\/\\$//||
||====================================================================||
```

There in the image is our flag.

Flag: FLAG{HI_REPUBLIC_OF_NEO}

*write-up by evanyeyeye*
