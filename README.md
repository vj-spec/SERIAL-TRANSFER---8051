# SERIAL-TRANSFER-OF-SINGLE-BYTE-CHARACTER-USING-8051-KEIL.-EMBEDDED-C-PROGRAM-

**AIM:** 

To write and execute Embedded C Program for Serial Transfer of Single Byte / Character using 8051 KEIL

**APPARATUS REQUIRED:**

Personal computer with Keil software

**PROGRAM:**

**(i)	Serial port transfer a character A**
```
#include<reg51.h> void main(void)

{

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

while(1)

{ SBUF='A';

while(TI==0); TI=0;

}

}
```

**OUTPUT:**
<img width="1919" height="1140" alt="Screenshot 2025-11-11 083441" src="https://github.com/user-attachments/assets/f6c59017-77a1-402a-9757-401b10a8e36f" />


**(ii)	Serial port to Transfer a Message**
```
#include<reg51.h> void main(void)

{

unsigned char msg[]="Programming 8051"; unsigned char i;

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

for (i=0; i<17;i++)

{

SBUF= msg[i]; while(TI==0); TI=0;

}

while(1);

}
```
 
**OUTPUT:**
<img width="1919" height="1143" alt="Screenshot 2025-11-11 082953" src="https://github.com/user-attachments/assets/d4ddd80a-597b-4e23-a774-7be460475cfb" />

**Result:**

Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
