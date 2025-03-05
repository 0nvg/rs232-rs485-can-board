# Giriş
  Raspberry Pi'nin endüstriyel ortamda kullanılamayacağından hâlâ endişeli misiniz? Bu eklenti kartı Raspberry Pi'niz için çeşit çeşit endüstriyel iletişim arayüzleri sunuyor: 2x RS485, 1x RS232, 1x CAN FD ve 1x CAN, ve elektrik izolasyon korumasıyla beraber geliyor. Ayrıca kıvılcım ve anti-elektrostatik korumalı, stabil bir iletişim sunuyor. Ek olarak, özelleştirilebilir endüstriyel ray-montajı sayesinde diğer endüstriyel kontrol uygulamalarıyla beraber kullanılmasını kolaylaştırıyor. Raspberry Pi 5 için, daha fazla eklentilere olanak sağlayan PCIe arayüzü bulunduruyor ve kullanıcılarımızın içine yeni özellikler eklemesini sağlayacak kadar boş alan bırakıyor. Bu eklenti kartı sizin Raspberry Pi'nizin sadece endüstriyal kontrol uygulamalarına daha iyi entegre edilmesini sağlamakla kalmaz, ayrıca daha fazla geliştirmeniz için imkânlar da verir.




# Özellikler
**Uyumluluk:** Raspberry Pi 4B, ve standart 40-pinli GPIO başlıklı Raspberry Pi 5 ile uyumludur.

**Çoklu Endüstriyel İletişim Arayüzleri:** 2x RS485, 1x RS232, 1x CAN FD ve 1x CAN iletişim arayüzleri sunar.

**Elektrik İzolasyon Koruması:** İletişim güvenliği için her arayüz elektrik izolasyonludur.

**Esnek İmkanlar:** SC16IS752 ve SP485 ikili çipleri bulunur, SPI arayüzü kullanılarak 2 adet RS485 eklenebilir. MCP2515 ve SN65HVD230 ikili çipleri bulunur, SPI arayüzü kullanılarak 1 adet CAB arayüzü eklenebilir. MCP2518FD ve MCP2562FD ikili çipleri bulunur, 1 adet CAN FD arayüzü eklenebilir. Raspberry UART ve SP3232EEN ikili çipleri bulunur, UART arayüzü kullanılarak 1 adet RS232 eklenebilir.

**Koruma:** Dahilî TVS (Transient Voltage Suppressor) ve kıvılcımgeçirmez ve ESD korumaları, kurtarma sigortası ve koruma diyotları, anti-dalgalanma, aşırı-voltaj korumaları ve anti-şok özelliği.

**Güç İzolasyonu:** Dahilî tek gövde güç izolasyonu vardır, herhangi bir ek güç kaynağı bulunmaz. Böylece RS232, RS485, CAN, ve CAN FD için kararlı akım ve voltaj çıkışı anti-parazit kabiliyetiyle sağlanır.

**Sinyal İzolasyonu:** Dahilî dijital izolasyon çipi; sinyal izolasyonunun anti-parazit gücünü, dayanıklılığını ve güvenilirliğini iyice geliştirir.

**Esnek Güç Kaynağı:** 7V ila 36V giriş desteği vardır ve Raspberry Pi ile HAT'inizi çalıştırmak için Pi5 Connector Adapter (B) kullanarak çalışabilir.

**Ayarlanabilir Terminal Direnç:** 120Ω terminal direnç, jumper cap (geçici bağlantı teli) ile aktive edilebilir.

**Rezerv Bölme Direnci:** Rezerv kesme direnci pedi, esnek kesme pimi anahtarlamasını destekler, böylece özel pimleri işgal etmekten kaçınır.

**Genişletme ve Kurulum:** Daha fazla özellik eklenebilmesi için Raspberry Pi 5 reserv PCIe bağlantısı bulunur, ve özelleştirilebilir ray-montaj kasası sayesinde bolca boş alan vardır.

**Ek Kaynaklar:** Online geliştirme kaynakları ve manuelleri sunar (Raspberry Python, C demoları, vb.)



# Parametreler
**Kullanılabilir Kartlar:**	Raspberry Pi 4B, Raspberry Pi 5 <br>

**İletişim Arayüzü:**	SPI + UART <br>

**Endüstriyel Arayüz:**	<br>
  1x İzole CAN FD <br> 
			- Çip Şeması	: MCP2518FD + MCP2562FD <br>
			- Baud Hızı	: 5 KB/s - 8 MB/s <br>

  1x İzole CAN <br>
			- Çip Şeması: MCP2515 + SN65HVD230 <br>
			- Baud Hızı: 5 KB/s - 1 MB/s <br>

  2x İzole RS485 <br>
			- Çip Şeması: SC16IS752 + SP485 <br>
			- Baud Hızı: 300 B/s - 921600 B/s <br>

  1x İzole RS232 <br>
			- Çip Şeması: SP3232EEN <br>
			- Baud Hızı: 300 B/s - 921600 B/s <br>

**Genişletebilirlik:**	<br>
	Pi5 <br>
			- NVMe, ETH, USB ve 4G/5G arayüzlerini PCIe bağlantısı ile desteklemektedir <br>

  Pi 4B/5 <br>
			- Boyutlar aynı olduğu sürece bazı 40pin GPIO başlıkları üst üste eklenebilir <br>

**Güç Kaynağı (Opsiyonel):**	5V Type-C port + External DC 7V ila 36V girişi <br>

**Ebat:**	154.6 × 83.7 × 59 mm <br>

**Kasa:**	Çevre dostu plastik kasa, ray ve duvar montajı desteği <br>



# Dahilî Arayüz
![RS232-RS485-CAN-Board-details-11.jpg](https://www.waveshare.com/w/upload/3/32/RS232-RS485-CAN-Board-details-11.jpg)



# Pin Girişleri ve Anlamları
![RS232-RS485-CAN-Board-details-inter.jpg](https://www.waveshare.com/w/upload/5/5c/RS232-RS485-CAN-Board-details-inter.jpg)

## CAN Veriyolu
![RS485_CAN_HAT_MCP2515.png](https://www.waveshare.com/w/upload/6/61/RS485_CAN_HAT_MCP2515.png) <br>
CAN modülünün işlevi bir CAN veriyolundaki tüm veri alışverişini yönetmektir. Bir mesaj gönderildiğinde, mesaj ilk önce doğru mesaj tamponuna ve kontrol kayıtlarına yüklenir. Bir iletim işlemi, SPI arayüzü aracılığıyla kontrol kaydındaki ilgili biti ayarlayarak veya iletim etkinleştirme pimini kullanarak başlatılabilir. İletişim durumu ve hatalar, ilgili kayıtları okuyarak kontrol edilebilir. CAN veri yolunda algılanan herhangi bir mesaj hatalara karşı kontrol edilir ve ardından mesajın iki alım tamponundan birine taşınıp taşınmayacağını belirlemek için kullanıcı tarafından tanımlanan bir filtreyle eşleştirilir.

⚠️ Raspberry Pi'nin kendisi CAN veri yolunu desteklemediğinden, CAN fonksiyonunu tamamlamak için SPI arayüzlü CAN kontrolcüsü bir trans-alıcı ile birlikte kullanılır.

Mikroçipte bulunan MCP2515, CAN V2.0B spesifikasyonunu tamamen destekleyen bir CAN protokol denetleyicisidir. Cihaz, standart ve genişletilmiş veri çerçevelerinin yanı sıra uzak çerçeveleri gönderebilir ve alabilir. MCP2515, istenmeyen mesajları filtrelemek için iki kabul maskesi kaydı ve altı kabul filtresi kaydıyla birlikte gelir, böylece SPI arabirimi aracılığıyla cihaza bağlanan ana mikrodenetleyicinin (MCU) kaynaklarından tasarruf edilir: yani Raspberry Pi, SPI arabirimi aracılığıyla çipe bağlanır ve Raspberry Pi'nin sürücüyü derlemesi gerekmez, yalnızca kullanmak için cihaz ağacında çekirdek sürücüsünü açması gerekir. MCP2518FD ile tek bir kanal üzerinden kullanımı destekler, yalnızca çip seçici pimi farklıdır!	



## RS-485 Veriyolu

### Kontrol Cihazı
Bu ürün RS-485 veriyoluna karşı kontrol cihazı olarak SC16IS752 kullanır. SC16IS752, çift kanal (SPI and I2C) desteğine sahip yüksek performanslı bir UART eklenti kartıdır.  Bu modül SPI arayüzünü benimser. Dahili güç izolasyonu, ADI manyetik izolasyon, dahili TVS (geçici voltaj bastırma tüpü), kurtarma sigortaları, koruma diyotları ve otomatik alıcı-verici dönüşüm devresi bulunur. Devredeki dalgalanma voltajını ve geçici sivri voltajı etkili bir şekilde bastırma, yıldırım ve statik elektriği önleme, aşırı akım ve aşırı voltajı önleme, şok direncini artırma, sinyal izolasyonu, yüksek güvenilirlik, güçlü anti-parazit, ve düşük güç tüketimi özelliklerine sahiptir.

### İletişim Protokolü
![2-CH-RS485_-HAT-2.png](https://www.waveshare.com/w/upload/thumb/0/02/2-CH-RS485_-HAT-2.png/600px-2-CH-RS485_-HAT-2.png)

- CS: Slave (köle) çip seçimi, CS düşük olduğunda, slave çip etkinleştirilir.
- SCLK: SPI iletişim saati.
- MOSI/SI: SPI İletişim ana bilgisayarı verileri gönderir ve slave verileri alır.
- MOSI/SI: SPI İletişim ana bilgisayarı verileri alır ve slave verileri gönderir.



## RS232 Veriyolu
Bu ürün alıcı olarak SP3232'yi kullanır. SP3232E serisi, dizüstü veya avuç içi bilgisayarlar gibi taşınabilir veya elde taşınabilir uygulamalar için tasarlanmış RS232 alıcı-verici çözümleridir. SP3232E serisi 3.3 V çalışmada *yalnızca 0,1 µF* kapasitör gerektiren yüksek verimli bir şarj pompası güç kaynağına sahiptir. Bu şarj pompası, SP3232E serisinin 3,0 V ila 5,5 V aralığındaki tek bir güç kaynağından gerçek RS232 performansı sunmasını sağlar. SP3232E cihazları 2-driver/2-receiver şeklindedir. Kapatma sırasında, besleme akımı 1 µA'nın altına düşer. Daha fazla ayrıntı için sayfasına başvurabilirsiniz.



# Ebat
![RS232-RS485-CAN-Board-details-size.jpg](https://www.waveshare.com/w/upload/7/7b/RS232-RS485-CAN-Board-details-size.jpg)


# Parçaların Montajı
![RS232-RS485-CAN-Board-details-13.jpg](https://www.waveshare.com/w/upload/6/6e/RS232-RS485-CAN-Board-details-13.jpg)

# Gerekli Özellik Librarylerini İndirme

* BCM2835'i indirin (Raspberry Pi terminalini açıp aşağıdaki komutları çalıştırın):
```bash
wget http://www.airspayce.com/mikem/bcm2835/bcm2835-1.60.tar.gz
tar zxvf bcm2835-1.60.tar.gz 
cd bcm2835-1.60/
sudo ./configure
sudo make
sudo make check
sudo make install
```
Bu konuda daha fazla detay almak için http://www.airspayce.com/mikem/bcm2835 bakabilirsiniz.

## wiringPi
### 32-bit Raspberry Pi Sistem
* Raspberry Pi terminalini açıp aşağıdaki komutları çalıştırın:
```bash
cd
sudo apt-get install wiringpi
#Mayis 2019 sonrasi Raspberry Pi sistemleri icin guncelleme gerekebilir:
wget https://project-downloads.drogon.net/wiringpi-latest.deb
sudo dpkg -i wiringpi-latest.deb
gpio -v
#Eger gpio -v yazdiginizda versiyon 2.52 gostermiyorsa kurulumda bir hata var demektir.

#Bullseye Branch sistemi icin asagidaki komutlari calistirin: 
git clone https://github.com/WiringPi/WiringPi
cd WiringPi
./build
sudo gpio -v
#Eger gpio -v yazdiginizda versiyon 2.70 gostermiyorsa kurulumda bir hata var demektir.
```

### 64-bit Raspberry Pi Sistem
1.	Kaynak paketlerini Raspberry Pi'nize klonlamak için aşağıdaki komutu çalıştırın:
```bash
wget https://files.waveshare.com/upload/8/8c/WiringPi-master.zip
```

2.	Zipten çıkarmak için gerekli environmenti indirin:
```bash
sudo apt-get install unzip
```

3.	Dosya PATH'ini (konumunu) girin ve şu komutu çalıştırın:
```bash
unzip WiringPi-master.zip
```

4.	WiringPi-master dosya dizinine girin
```bash
cd WiringPi-master/
```

5.	Şu komutu çalıştırın:
```bash
sudo ./build
```

* Eğer olmuyorsa şu komutu çalıştırıp 4. adımı tekrar deneyin:
```bash
chmod +x ./build
```

Referans görseller:
![64-bit_wiringPi1.png](https://www.waveshare.com/w/upload/b/bb/64-bit_wiringPi1.png)
![64-bit_wiringPi2.png](https://www.waveshare.com/w/upload/c/c0/64-bit_wiringPi2.png)

6. Python özellikler librarysini indirin:
```bash
#python2 icin 
sudo apt-get update
sudo apt-get install python-pip
sudo apt-get install python-pil
sudo apt-get install python-numpy
sudo pip install RPi.GPIO
sudo pip install spidev
sudo pip install python-can

#python3 icin
sudo apt-get update
sudo apt-get install python3-pip
sudo apt-get install python3-pil
sudo apt-get install python3-numpy
sudo pip3 install RPi.GPIO
sudo pip3 install spidev 
sudo pip3 install python-can
```

7. İlgili ürünü resmî web sitesinde bulun, ürün bilgilerindeki indirme yolunu açın ve wiki'deki örnek demoyu indirin.

8. Ziplenmiş dosyayı alın, unzipleyin ve demoyu Raspberry Pi'ye klonlayın.

## Hazırlık
### Arayüzünü Aktive Etme
Raspberry Pi terminalini açın ve konfigürasyona başlamak için aşağıdaki komutu çalıştırın:
```bash
sudo raspi-config
```
<br>
Giriş shellini kapatıp seri bağlantı noktasını açın:

*Interfacing Options -> Serial -> No -> Yes*

![L76X_GPS_Module_rpi_serial.png](https://www.waveshare.com/w/upload/thumb/3/31/L76X_GPS_Module_rpi_serial.png/800px-L76X_GPS_Module_rpi_serial.png)

`/boot/config.txt` dosyasını açın ve şu argümanı aratın (CTRL + F):
```
enable_uart=1
```
Eğer yoksa, dosyanın en son satırına yapıştırın.
<br>

Sonra:

*Interfacing Options -> SPI -> Yes*

![RPI_open_spi.png](https://www.waveshare.com/w/upload/1/1e/RPI_open_spi.png)

Ve sonunda Raspberry Pi'nize restart atın:
```bash
sudo reboot
```

Lütfen SPI'in başka cihazlar tarafından meşgul edilmediğinden emin olun (buna `/boot/config.txt` dosyasından bakabilirsiniz).

### config.txt Dosyasını Modifiye Etme

Modülü Raspberry Pi'ye takın, ve config.txt dosyasını modifiye etmeye başlayın:
```bash
sudo nano /boot/config.txt  
```

⚠️ Eğer Pi 5 kullanıyorsanız dosya konumunu `/boot/firmwave/config.txt` olarak değiştirin.
⚠️ Eğer Ubuntu üzerinden yapıyorsanız dosya konumunu `/boot/firmware/config.txt` olarak değiştirin.

Şu argümanları dosyada son satırdan itibaren sırayla ekleyin:
```
dtparam=spi=on
dtoverlay=i2c0 
dtoverlay=spi1-3cs
dtoverlay=sc16is752-spi1,int_pin=25
dtoverlay=mcp2515,spi0-0,oscillator=16000000,interrupt=23
dtoverlay=mcp251xfd,spi0-1,interrupt=24
```

Tüm ayarları uygulamak için Raspberry Pi'nize tekrar restart atın:
```bash
sudo reboot
```

Raspberry Pi açıldıktan sonra, SPI bilgilerini görüntülemek için şunu yazın:
```bash
dmesg | grep spi1
```

Şöyle gözükmesi gerekir:
![Rs232_rs485_can_board_01.png](https://www.waveshare.com/w/upload/6/6a/Rs232_rs485_can_board_01.png)

CAN'i açın:
```bash
sudo ip link set can0 up type can bitrate 1000000
sudo ip link set can1 up type can bitrate 1000000
sudo ifconfig can0 txqueuelen 65536
sudo ifconfig can1 txqueuelen 65536
```

Daha fazla CAN kernel komutları için şu linki ziyaret edebilirsiniz: https://www.kernel.org/doc/Documentation/networking/can.txt

ifconfig'i görüntüleyin:
```bash
ifconfig
```
![ifconfig.jpg](https://www.waveshare.com/w/upload/thumb/2/2a/2-CH-CAN-HAT-ifconfig.jpg/700px-2-CH-CAN-HAT-ifconfig.jpg)

CAN cihazını kapatmak için:
```bash
sudo ifconfig can0 down
sudo ifconfig can1 down
```

# Demolar
## CAN Veriyolu Demo
- Dizinde gezinin.
- Alıcı `receive.py`'i çalıştırır:
```bash
sudo python receive.py
```

- Verici `send.py`'i çalıştırır:
```bash
sudo python send.py
```

Vericinin CAN1 ve alıcının CAN0 kullandığını unutmayın. Daha fazla bilgi için aşağıdaki demoya bakınız:

## Demo Açıklamaları
### Python Demo
Bu demo Python platformuna dayalıdır, o yüzden `python-can` library'sinin yüklü olduğundan emin olun.
Sadece MCP2515 kerneli çalıştığından dolayı lütfen vericiyi kullanmadan önce CAN device oluşturmayı unutmayın:
```py
os.system('sudo ip link set can0 type can bitrate 100000')
os.system('sudo ifconfig can0 up')
```

Yukarıdaki komut CAN0'ı yapılandırıp verici/alıcı arayüzü olarak belirterek başlatır. CAN1'e geçmek için yazmanız gereken kod şu şekildedir:
```py
os.system('sudo ip link set can1 type can bitrate 100000')
os.system('sudo ifconfig can1 up')
```

**Adım 1:** CAN Veriyoluna Bağlanma
```py
can0 = can.interface.Bus(channel = 'can0', bustyp = 'socketcan_ctypes')
```
- ⚠️ `python-can` versiyonu 4.0.0'a güncellendiğinden mevzubahis kod şuna modifiye edilmelidir, yoksa hata verebilir:
```py
can1 = can.interface.Bus(channel = 'can0', bustype = 'socketcan')
```

CAN1 olarak değiştirmek için:
```py
can0 = can.interface.Bus(channel = 'can1', bustype = 'socketcan')
```

**Adım 2:** Mesaj Oluşturma
```py
msg = can.Message(arbitration_id=0x123, data=[0, 1, 2, 3, 4, 5, 6, 7], extended_id=False)
```
- ⚠️ `python-can` versiyonu 4.0.0'a güncellendiğinden mevzubahis kod şuna modifiye edilmelidir, yoksa hata verebilir:
```py
msg = can.Message(is_extended_id=False, arbitration_id=0x123, data=[0, 1, 2, 3, 4, 5, 6, 7])
```

**Adım 3:** Mesajı Gönderme
```py
can0.send(msg)
```

CAN1 olarak değiştirmek için:
```py
can1.send(msg)
```

Son olarak, CAN cihazı kapatılır:
```py
os.system('sudo ifconfig can0 down')
```

CAN1 olarak değiştirmek için:
```py
os.system('sudo ifconfig can1 down')
```

Veriyi alır:
```py
msg = can0.recv(10.0)
```
- Burdaki `recv()` zamanaşımı veri alım süresini tanımlar.

Daha fazla bilgi için python-can dokümanına göz atabilirsiniz: https://python-can.readthedocs.io/en/stable/interfaces/socketcan.html

### WringPi Demo
Veri alımını engellemek için Raspberry Pi bir terminal açar ve şunları çalıştırır:
```bash
cd 2-CH_CAN_HAT_Code/wiringPi/receive/
make clean
sudo make
sudo ./can_receive
```

Sonra da şunları çalıştırır:
```bash
cd 2-CH_CAN_HAT_Code/ wiringPi/receive/
make clean
sudo make
sudo ./can_send
```

## RS-485 Veriyolu Demo

Test demoyu indirip çalıştırın:
```bash
sudo apt-get install p7zip-full
wget https://files.waveshare.com/upload/4/44/2-CH_RS485_HAT_code.7z
7z x 2-CH_RS485_HAT_code.7z
sudo chmod 777 -R  2-CH_RS485_HAT
cd 2-CH_RS485_HAT/
```

Projeyi Github'dan da klonlayabilirsiniz:
```bash
sudo git clone https://github.com/waveshare/2-CH-RS485-HAT
cd 2-CH-RS485-HAT/
```

**C demo:**
```bash
cd c
make clean
make
sudo ./main
```

**Python demo:**
```py
cd python 
cd examples
sudo python3 main.py
#veya
sudo python3 test.py
```

## RS-232 Bus 
RS-232'i kullanmak daha kolay: Raspberry Pi UART özelliğini açmanız yeterli, ve `/dev/ttyAMA0`'dan hemen sonra seri bağlantı noktası iletişimi olarak kullanılabilir.









