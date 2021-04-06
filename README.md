# piHole

Hur jag installerade PiHole på 15 minuter

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
* Ange t.ex Google's DNS (8.8.8.8 och 8.8.4.4) som ny DNS 
* Avsluta DietPi-Config
* ```reboot```
* Efter reboot uppdateras DietPi automatiskt

## Installera PiHole

* ```curl -sSL https://install.pi-hole.net | bash```
* Installationen avslutas med IP och password - Notera detta

## Konfigurera klienter

### Manuellt

* Uppdatera klienternas DNS till den nya IP adressen

### Automatiskt med DHCP

* Ange ny den nya IP adressen som DNS
