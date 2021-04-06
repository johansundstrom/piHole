# piHole

Hur jag installerade PiHole

Förutsättningar
* Pi3 Model B
* 8GB RAM
* DietPi OS (64-bit)

## Install DietPi

* Hämta 64-bit img-fil och packa upp https://dietpi.com/ 
* Med Raspberry Pi Imager skriv DietPi
* Standard inloggning är root och dietpi
* Byt lösenordet  

## Konfigurera DietPi-Config

* Etablera fast IP i lokala nätverket samt korrekt IP till Default Gateway
* 
* Avsluta DietPi-Config
* ```reboot```
* Efter reboot uppdateras DietPi automatiskt

## Installera PiHole

* ```curl -sSL https://install.pi-hole.net | bash```
* Installationen avslutas med IP och password - Notera detta
