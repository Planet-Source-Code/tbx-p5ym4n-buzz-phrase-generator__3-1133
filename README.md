<div align="center">

## Buzz Phrase Generator


</div>

### Description

This is a reasonably simple piece of code to generate a random hitec phrase. Its something I made just for the practice, but has a nice demonstration of switches and random number generation. Also now generates a logfile and reports on the size of that logfile.

(I plan to infect Bill Gates PC with this a sa virus and make it pop up random phrases every 7.65 minutes. MWA HA HA HA HA!!!!)
 
### More Info
 
has some odd bugs in the number generation and the final phrase is a little 'sticky' (random# gen gone wrong somewhere)


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[\[tBx\]P5yM4n](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/tbx-p5ym4n.md)
**Level**          |Beginner
**User Rating**    |4.8 (19 globes from 4 users)
**Compatibility**  |C\+\+ \(general\), Microsoft Visual C\+\+
**Category**       |[Games](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/games__3-13.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/tbx-p5ym4n-buzz-phrase-generator__3-1133/archive/master.zip)

### API Declarations

```
#include <time.h>
#include <iostream.h>
#include <stdlib.h>
#include <stdio.h>
#include <math.h>
```


### Source Code

```
/********************************************************************
*                                  *
* This is a nice simple piece of code to generate random hi-tech  *
* sounding phrases. Someone might find a use for this, I dont know.*
* its the first program I have ever written that works.      *
* you may do what you like with this code, copy it, sell it or   *
* modify it. I dont care.                     *
*                                  *
********************************************************************/
#include <time.h>
#include <iostream.h>
#include <stdlib.h>
#include <stdio.h>
#include <math.h>
#include <fstream.h>
#include <string.h>
int word1,word2,word3,power, output,power2, mark,x;
char quitcon='y',one[30],two[20],three[20],four[30];
long a=0;
float logsize,maxlog=30000,l,m;
void main(void)
{
//intro:
cout << "*********************************************************************" << endl;
cout << "* BUZZ - PHRASE GENERATOR        (C)2001 [tBx}P5yM4n     *" << endl;
cout << "*********************************************************************" << endl;
cout << endl;
cout << "enter ran# seed for final phrase (30-300, 1=off)";
cin >> x;
//open log file
ofstream file;
file.open ("buzzlog.txt", ios::app|ios::in|ios::binary);
//////////////////////BUG////////////////////////////////////
//reports logfile size                   //
//l = file.tellg();                    //
//file.seekg (0, ios::end);                //
//m = file.tellg();                    //
//cout << "logfile is " << (m/maxlog)*100 << "% full";   //
/////////////////////////////////////////////////////////////
//seed ran# generator:
srand((unsigned)time(NULL));
//loop to make multiple phrases
do{
//generate ran#:
power=rand()%10;
power2=rand()%9;
word1=rand()%34;
word2=rand()%28;
word3=rand()%31;
mark=rand()%x;
//display output level in MW:
output=powf(10,power)*(power2+1);
cout << output << "MW ";
file << output << "MW ";
//display phrase 1 (particle type)
	switch (word1)
	{
	case 1:
		strcpy(one, "Proton"); break;
	case 2:
		strcpy(one, "Electron"); break;
	case 3:
		strcpy(one,"Neutron"); break;
	case 4:
		strcpy(one, "Positron"); break;
	case 5:
		strcpy(one, "Magnetic"); break;
	case 6:
		strcpy(one,"Chronitron"); break;
	case 7:
		strcpy(one,"Photon"); break;
	case 8:
		strcpy(one, "Muon"); break;
	case 9:
		strcpy(one,"Boson"); break;
	case 10:
		strcpy(one,"Graviton"); break;
	case 11:
		strcpy(one,"Quantum"); break;
	case 12:
		strcpy(one,"Matter"); break;
	case 13:
		strcpy(one,"Anti-Matter"); break;
	case 14:
		strcpy(one, "Phaser"); break;
	case 15:
		strcpy(one,"Laser"); break;
	case 16:
		strcpy(one,"Bio-Hazzard"); break;
	case 17:
		strcpy(one,"Ultrasound"); break;
	case 18:
		strcpy(one,"Bionic"); break;
	case 19:
		strcpy(one,"Cyborg"); break;
	case 20:
		strcpy(one,"Tiberium"); break;
	case 21:
		strcpy(one,"Pryonic"); break;
	case 22:
		strcpy(one,"Grim"); break;
	case 23:
		strcpy(one,"Psymon"); break;
	case 24:
		strcpy(one,"type 3"); break;
	case 25:
		strcpy(one,"type 7"); break;
	case 26:
		strcpy(one,"High-Warp"); break;
	case 27:
		strcpy(one,"Subspace"); break;
	case 28:
		strcpy(one,"Pneumonoultramicroscopicsiliocovolcanoconiosis"); break; //the longest word in the English language if you must know.
	case 29:
		strcpy(one,"deoxy-ribonucleic acid"); break;
	case 30:
		strcpy(one,"restricted endo-nuclear"); break;
	case 31:
		strcpy(one,"temporal"); break;
	case 32:
		strcpy(one,"hologramatic"); break;
	case 33:
		strcpy(one,"cellular"); break;
	default:
		strcpy(one,"Error"); break;
	}
	cout << one << " ";
	file << one << " ";
//display phrase 2 (action)
	switch (word2)
	{
	case 1:
		strcpy(two,"field"); break;
	case 2:
		strcpy(two,"emitter"); break;
	case 3:
		strcpy(two, "deployment"); break;
	case 4:
		strcpy(two,"sensing"); break;
	case 5:
		strcpy(two,"deflector"); break;
	case 6:
		strcpy(two,"inverter"); break;
	case 7:
		strcpy(two,"phasing"); break;
	case 8:
		strcpy(two,"generator"); break;
	case 9:
		strcpy(two,"shielding"); break;
	case 10:
		strcpy(two,"synthesiser"); break;
	case 11:
		strcpy(two,"processing"); break;
	case 12:
		strcpy(two,"filter"); break;
	case 13:
		strcpy(two,"pulse"); break;
	case 14:
		strcpy(two,"alternator"); break;
	case 15:
		strcpy(two,"worm-hole"); break;
	case 16:
		strcpy(two,"controller"); break;
	case 17:
		strcpy(two,"lateraly inverting"); break;
	case 18:
		strcpy(two,"storage"); break;
	case 19:
		strcpy(two,"emergency release"); break;
	case 20:
		strcpy(two,"imobiliser"); break;
	case 21:
		strcpy(two,"phase-invertor"); break;
	case 22:
		strcpy(two,"field-invertor"); break;
	case 23:
		strcpy(two,"anhialation"); break;
	case 24:
		strcpy(two,"reconstructiong"); break;
	case 25:
		strcpy(two,"re-constituting"); break;
	case 26:
		strcpy(two,"calculating"); break;
	case 27:
		strcpy(two,"ring-tone"); break;
	default:
		strcpy(two,"error") ;break;
	}
	cout << " ";
//display phrase 3 (object)
	switch (word3)
	{
	case 1:
		strcpy(three,"array"); break;
	case 2:
		strcpy(three,"generator"); break;
	case 3:
		strcpy(three,"tube"); break;
	case 4:
		strcpy(three,"coil"); break;
	case 5:
		strcpy(three,"display"); break;
	case 6:
		strcpy(three,"gauge"); break;
	case 7:
		strcpy(three,"tool"); break;
	case 8:
		strcpy(three,"device"); break;
	case 9:
		strcpy(three,"field");break;
	case 10:
		strcpy(three,"drive"); break;
	case 11:
		strcpy(three,"grid"); break;
	case 12:
		strcpy(three,"conduit"); break;
	case 13:
		strcpy(three,"storage device"); break;
	case 14:
		strcpy(three,"reaction vessel"); break;
	case 15:
		strcpy(three,"transportation system"); break;
	case 16:
		strcpy(three,"system"); break;
	case 17:
		strcpy(three,"bio-bed"); break;
	case 18:
		strcpy(three,"hard-light hologram"); break;
	case 19:
		strcpy(three,"I/O stream"); break;
	case 20:
		strcpy(three,"realy system"); break;
	case 21:
		strcpy(three,"nullifier"); break;
	case 22:
		strcpy(three,"multiplier"); break;
	case 23:
		strcpy(three,"inversion field"); break;
	case 24:
		strcpy(three,"engine"); break;
	case 25:
		strcpy(three,"32-bit driver file"); break;
	case 26:
		strcpy(three,"nova bomb"); break;
	case 27:
		strcpy(three,"homo sapien"); break;
	case 28:
		strcpy(three,"for felix purposes"); break;
	case 29:
		strcpy(three,"growth curve"); break;
	case 30:
		strcpy(three,"culture"); break;
	default:
		strcpy(three,"error"); break;
	}
	cout << three << " ";
	file << three << " ";
	switch(mark)
	{
	case 1:
		strcpy(four, "Mk I"); break;
	case 2:
		strcpy(four,"Mk II"); break;
	case 3:
		strcpy(four,"Mk III"); break;
	case 4:
		strcpy(four,"Mk IV"); break;
	case 5:
		strcpy(four,"Mk V"); break;
	case 6:
		strcpy(four,"Mk Ia"); break;
	case 7:
		strcpy(four,"Mk IIa"); break;
	case 8:
		strcpy(four,"Mk IIIa"); break;
	case 9:
		strcpy(four,"Mk IVa"); break;
	case 10:
		strcpy(four,"Mk Va"); break;
	case 11:
		strcpy(four,"named BoB"); break;
	case 12:
		strcpy(four,"economy version"); break;
	case 13:
		strcpy(four,"budget edition"); break;
	case 14:
		strcpy(four,"M1cr0$5h1t3 edition"); break;
	case 15:
		strcpy(four,"**batteries not included**"); break;
	case 16:
		strcpy(four,"Limited edition"); break;
	case 17:
		strcpy(four,"with Linux support"); break;
	default:
		break;
	}
cout << four << endl;
file << four << endl;
//close log file
void close();
//reports size of file as it grows
int out;
//reopen file
 ifstream file ("buzzlog.txt", ios::in|ios::binary);
 //i dont realy understand this yet.
 l = file.tellg();
 file.seekg (0, ios::end);
 m = file.tellg();
 //close the file again
 file.close();
logsize=(m/maxlog)*100;
//stores filesize as an int to improve clarity
out=logsize;
//variable 'a' stops the program from repeating itself too often
//just put that in cos i was bored :)
if(out%5==0 && a>=0){
	cout << "logfile is " << out << "% full" << endl;
	a=-6;
}
a++;
quitcon='n';
cout << endl << endl;
cout << "make another? [y/N]";
cin >> quitcon;
}while (quitcon=='y');
}
// If you want to add more possibilities, just make sure that the
// number after rand()% is 1 more than the highest case statement
// those who know their maths can figure out why.
// (C)2001 [tBx]P5ym4n
// last update: 21/01/01
// number of outputs: 28.6k phrases * 81 power levels
//= 258k total outputs (not including final phrase)
```

