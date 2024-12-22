# *Brocade FastIron LS648*
![ues648ls_gfphdr_login](https://github.com/user-attachments/assets/c9ff20b6-4446-4cb6-b87f-02ca291cba9c)
</br>
I am not affiliated with Brocade and this is just an unofficial guide on configuring it.</br>
I am writing this having in mind that you searched for this as the FLS648 is not a popular switch. Therefore I may not explain everything very clearly but I will try to. However since you searched for this I guess you must have bought it. If you bought that switch, you probably are familiar with things such as Telnet, PuTTY, Serial connection. You will also need some electrical equipment such as female to female pin connectors.
## Description

  The Brocade FLS648 is a L2 switch featuring:
  
  On the front:
  
- 48x 1 Gigabit ports
- 4x 1 Gigabit SFP ports
- RS-232 Console port
  
On the back:
  
- 2x slot for FLS-1XGC Stacking module
- Power port

## Communication with the switch
The first configuration of the switch needs to be done with the console port. </br> 
This is where it starts being tricky. I guess Brocade just didn`t want to go with the standards and the console port on this switch has a custom pinout. This makes it impossible to communicate with it in a typical way.</br>
 ### Here is how you communicate with it using serial connection with PuTTY.

 First you need to buy a USB to serial converter. You can get one of those relatively cheap. Look for those with a male connector. </br>
 After you get it you need to get a couple of cables. The best ones are those that have a female connector on both sides because we are gonna be connecting two male DB9 connectors.</br></br>
 Here you can see the way you should connect the two Serial ports. As you can see here, the TX and RX pins are connected completly different than the way the serial connection should work. You need to connect the RX pin to the RX pin and TX to TX. 
 ![FL](https://github.com/user-attachments/assets/ac0f176c-5bc9-4e80-95c8-9042486e4161)
</br> Before you proceed with connecting to the switch, you need to test your adapter to know does it even work. Simply open a Serial connection with 
You will also need the following settings for your serial connection.
 - Baud rate: 9600
 - Data bits: 8
 - Stop bits: 1
 - Parity: None
 - Flow control: None
</br>
Make sure to download the latest drivers for your USB to Serial adapter.
