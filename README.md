# hackintosh_setup
# Windows way to create bootable MacOS usb installer<br>
# chỉ dùng cho dell eXX50 lattitude
-----
## laptop status<br>
##### dell e7250 lattitude<br>
##### i5 5300U Broadwell ~ smbios: MacBookPro 11,2 x<br>
##### intel graphics HD 5500 <br>
##### Wifi : intel wireless-AC 7265 : both bluetooth and wifi working<br>
##### (kext provided in Intex Wifi and BT fix ..)<br>
##### Simcard : dell wireless-5808e: haven't tested yet<br>
-----
## Pre-install Additional tools:<br>
##### Rufus: for format usb drive with this option<br>
##### [xxx]<br>
##### BalenarEtcher (Flash dmg file - recommend portable version)<br>
##### Minitool Partition wizard (to access EFI partition after flash) <br>
##### Explorer++<br>
-----
## Post-install tools<br>
##### OCC - for mount EFI from usb to hard disk and update kext for later (when current kext not work)<br>
##### GenSMBIOS -  tự tìm hiểu đi<br>
-----
## MacOs version for this kext setup<br>
##### BigSur 11.0 or above (mine is 11.2.3)<br>
-----
## Installation step-by-step<br>
##### Lười chụp bỏ mẹ:<br>
##### 1: format = rufush<br>
##### 2: flash dmg file macOS vào usbDrive = BalenarEtcher ( usb dung lượng >= 16gb)<br>
##### 3: Dùng minitool partition -> select vào ổ efi của usb -> change letter -> Apply change<br>
##### 4: Dùng Explorer++ -> chuyển cả thư mục efi (trong git này) vào EFI <br>
##### 5: Tháo usb ra, cắm vào máy cần cài, bước đầu chọn boot từ usb giống cài win<br>
##### 6: Format ổ cứng của máy cần cài theo [APFS|GUID]<br>
##### 7: Ấn install như bt, tuyệt đối không được rút usb ra <br>
##### 8: Đợi<br>
##### 9: Sau khi cài xong thành công, màn hình setup language các kiểu rồi vào được macOS, vẫn chưa được tháo usb ra<br>
##### 10: Dùng Mount-usb update.zip (có ở trong git này) (yêu cầu usb thứ 2) mount usb, guide thì có trên mạng search theo keyword: mount efi usb to disk github rồi coi video yt<br>
##### 11: Sau khi mount xong, copy EFI từ usb vào trong máy, lúc này có thể rút usb<br>
##### 11: Card wifi không hoat động, dùng **Intex Wifi and BT fix**<br>
##### 12: Setup smBios: https://dortania.github.io/OpenCore-Install-Guide/extras/smbios-support.html : Dựa theo thông số máy để chọn. Full hướng dẫn có trên mạng.
