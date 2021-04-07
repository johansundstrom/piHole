# piHole

Hur jag installerade PiHole på 15 minuter

Förutsättningar
* Pi3 Model B
* 8GB SD
* DietPi OS (64-bit)

## Installera DietPi (5 min)

* Hämta <a href="https://dietpi.com/">64-bit img-fil</a> och packa upp  
* Med <a href="https://www.raspberrypi.org/software/">Raspberry Pi Imager</a> (så har du testat den också) flasha SD
* Starta upp SD-kortet på din Pi
* Standard inloggning är ```root``` och ```dietpi```
* Byt förslagsvis lösenordet

## Konfigurera DietPi-Config (5 min)

* Etablera fast IP i lokala nätverket samt korrekt IP till Default Gateway
* Ange t.ex Google's DNS (8.8.8.8 och 8.8.4.4) som ny DNS 
* Avsluta DietPi-Config
* ```reboot```
* Efter reboot uppdateras DietPi automatiskt
* Invänta uppdateringen

## Installera PiHole (4 min)

* ```curl -sSL https://install.pi-hole.net | bash```
* Installationen avslutas med IP och password - Notera detta
* Byt till eget lösenord för PiHile med ```pihole -a -p``` i SSH-konsolen

## Konfigurera klienter (1 min)

### Manuellt

* Uppdatera klienternas DNS till den nya IP adressen

### Automatiskt med DHCP

* Ange ny den nya IP adressen som DNS

## Bonus

* Registrera pihole.<din-domän>
* Registrera pihole.<din-domän> och port forward 80 till t.ex. 8888 i din router genom ```sudo sed -ie "s/= 80/= 8888/g" /etc/lighttpd/lighttpd.conf```
