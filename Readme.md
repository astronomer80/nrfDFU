#CocoaApplication to Scan BLE devices with DFU Service and to perform the DFU via BLE using iOSDFULibrary.framework
Usage: nrf_bledfu_mac [help] or [scan] or [update -f <bin_file> -d <dat_file> -a <device_address>] or [update -z <zip_file> -a <device_address>]<br/>
<br/>
OTA DFU update application for nrf5x MCUs. Visit https://github.com/astronomer80/nrf52_bledfu_mac for more information<br/>
Here a list of commands available:<br/>
help: Show this help<br/>
scan: Scan BLE devices already paired with Windows Settings<br/>
update -f < bin_file > -d < dat_file > -a <device_address>. bin_file is the file generated from the Arduino IDE. dat_file is the init packet generated by nrfutil application. device_address: is the address of the device returned using 'scan' command.<br/>
update -z < zip_file > -a <device_address>. zip_file is the archive generated by nrfutil application. device_address: is the address of the device returned using 'scan' command.<br/>
update -h < hex_file/bin_file > -a <device_address>. hex_file or the bin_file is generated by the Arduino IDE. nrfutil application generates the zip archive. device_address: is the address of the device returned using 'scan' command.<br/>
<br/>
<i>Optional parameter</i>
-v: Verbose mode. Adding this parameter as last shows more information during the update procedure.
<br/>
Example:<br/>
nrf_bledfu_mac help<br/>
nrf_bledfu_mac scan<br/>
nrf_bledfu_mac update -z application.zip -a xxxxxxx<br/>
nrf_bledfu_mac update -f application.bin -d application.dat -a xxxxxxx<br/>
nrf_bledfu_mac update -h application.bin -a xxxxxxx -v<br/>
where xxxxxxx is the device address returned by scan command
<br/>


**TODO**
 - Control the progress of the DFU and automatically close the app after DFU
 - Add nrfutil integration (to create the dat file from hex file)
 - Check softdevice and bootloader update<br/>
 - BLE Dfu with key<br/>

