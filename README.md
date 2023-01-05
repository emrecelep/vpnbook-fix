# VPNBOOK FİX

Vpnbook adresinden indirilen openvpn çalıştırılmak istediğinde hep aynı hata ile karşılaşılıyor.

`OpenSSL: error0A00018E:SSL routines::ca md too weak`
`Cannot load inline certificate file`
`Exiting due to fatal error`

-----

Günümüzde vpnbook sertifikalarını güvensiz bulduğu için sertifikaları kullanmayı reddediyor bu imzalama için kullanılan hashing algoritmasından kaynaklanabilir.

![](https://i.ibb.co/sVcvdMD/1.png)

Öncelikle **https://www.vpnbook.com** adresine girerek size uygun olan openvpn dosyasını indiriyorsunuz.

![](https://i.ibb.co/6JDXcR1/2.png)

Sonrasında indirilen zip uzantılı dosyayı '**Extract Here**' diyerek bulunduğu dizine çıkartıyorsunuz.

![](https://i.ibb.co/S5kN38h/3.png)

İndirdiğiniz vpnbook dizini içine girerek istediğiniz bir dosyayı seçiyorsunuz ve sağ tılayıp mousepad editor ile açıyorsunuz.

![](https://i.ibb.co/Ch59VJK/5.png)

ovpn uzantılı dosyanın içerisinde kırmızı ok ile belirtilen satırı ekliyorsunuz ve dosyayı kaydedip çıkıyorsunuz.
`tls-cipher "DEFAULT:@SECLEVEL=0"`

![](https://i.ibb.co/09Mk3Ph/6.png)

Ben örnek olarak '**vpnbook-us1-udp25000.ovpn**' seçtim terminalden 
**`openvpn vpnbook-us1-udp25000.ovpn`** komutunu çalıştıyorsunuz ve çıkan ekranda kullanıcı adı ve şifrenizi yazıyorsunuz.

![](https://i.ibb.co/6P1tsyr/7.png)

Son olarak vpn bağlantımızın gelmesini bekiyoruz. 'Initialization Sequence Completed' geldiği zaman işlemlerimiz tamamdır.

![](https://i.ibb.co/5x1CBTQ/8.png)

En son olarak gerçekten çalışıyor mu bunu test etmek için herhangi bir tarayıcıyı kullanarak search yerine 'what is my ip' yazarak hem internete erişebildiğinizi hemde public ip adresinizin değişip değişmediğini kontrol edebilirsiniz.

![](https://i.ibb.co/zxNZw2N/9.png)






