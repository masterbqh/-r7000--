To flash the custom CFE route, please follow this steps:

1. the router has to be accessible via SSH/telnet

2. make a backup of your stock CFE:
dd if=/dev/mtd0 of=stock-cfe.bin

3. modify the custom CFE by CFEEdit to reflect your router's MAC addresses and WPS pin:

ETH MAC Address = LAN_MAC_Address (from the bottom of the case)
WL1 MAC Address = ETH MAC Address (Press "=" button)
WL2 MAC Address = ETH MAC Address + 4 (Press "=" button, Then press "+" button four times)

secret_code=12345670 (type in your WPS pin here)

4. Using WinSCP, move the "custom CFE" to "/tmp/home/root".

5. the router has to be accessible via SSH/telnet ；

using the command "dd if=new-cfe.bin of=/dev/mtd0" without quotes

6. reboot and clear NVRAM to factory defaults.
