# piHole

Hur jag installerade PiHole på 15 minuter

Förutsättningar
* Pi3 Model B
* 8GB RAM
* DietPi OS (64-bit)

## Install DietPi (5 min)

* Hämta 64-bit img-fil och packa upp https://dietpi.com/ 
* Med Raspberry Pi Imager flasha DietPi
* Starta upp SD-kortet
* Standard inloggning är root och dietpi
* Byt lösenordet  

## Konfigurera DietPi-Config (5 min)

* Etablera fast IP i lokala nätverket samt korrekt IP till Default Gateway
* Ange t.ex Google's DNS (8.8.8.8 och 8.8.4.4) som ny DNS 
* Avsluta DietPi-Config
* ```reboot```
* Efter reboot uppdateras DietPi automatiskt

## Installera PiHole (4 min)

* ```curl -sSL https://install.pi-hole.net | bash```
* Installationen avslutas med IP och password - Notera detta

## Konfigurera klienter (1 min)

### Manuellt

* Uppdatera klienternas DNS till den nya IP adressen

### Automatiskt med DHCP

* Ange ny den nya IP adressen som DNS
