/*
 Arduino Nano ---> Remarks      
     D2             RX
     D3             TX
ADJUST TO HC-05 CONNECTION

  Step:
  1.BEFORE YOU CONNECT THE ARDUINO TO THE USB remove the VCC (power)
    red wire from the HC-05 so it's not getting any power from the Arduino.
    All other wires are still connected.
  2.Now connect the Arduino Uno to the USB cable extended from your PC.
  3.Make sure the HC-05 module is NOT PAIRED with any other Bluetooth device.
  4.Re-connect the Arduino Uno 5V wire to the HC-05's VCC (5V power) pin.
  5.The HC-05 LED will blink on and off at about 2 second intervals.
    Now the HC-05 is in AT command mode ready to accept commands to change configuration and settings.
  6.To test if everything is wired correctly,  open the Serial Monitor from the Arduino IDE
    and type "AT" and click SEND. You should see an "OK"
  7.If you don't see an "OK" check your wiring.

 SLAVE (CHARGING STATION)
  Reset to Default setting ---> AT+ORGL
  Change device name       ---> AT+NAME:xxxxx
  Change baudrate          ---> AT+UART:115200,1,0
  Set Role Slave           ---> AT+ROLE:0
  Check Bluetooth Address  ---> AT+ADDR? ----> you will get hc-05 mac address, input at Master AT+BIND

 MASTER (ROBOT)
  Reset to Default setting ---> AT+ORGL
  Change device name       ---> AT+NAME:xxxxx
  Change baudrate          ---> AT+UART:115200,1,0
  Set Role Master          ---> AT+ROLE:1
  Set Binding              ---> AT+BIND:xxxx,xx,xxxxxx (Bluetooth Address Target binding/Slave mac address)

*/
