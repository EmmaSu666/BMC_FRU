# BMC_FRU
A tool that follows the FRU format spec, and can transfer the FRU binary value according to the settings from initial file.





# CMD for Testing FRU 

1. 在螢幕上顯示FRU資料
>>>  ipmitool -I ms fru

2. 將機器裡的FRU資料存成FRU.bin (0x00 means FRU ID is 0)
>>> ipmitool -I ms fru read 0x00 FRU.bin

3. 將output.bin寫進機器裡 (output.bin是新的FRU資訊)
>>> ipmitool -I ms fru write 0x00 FRU.bin
