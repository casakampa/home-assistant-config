# Home Assistant configuratie

## Het doel
Het doel van deze automatiseringen is een waardevolle toevoeging te zijn op het dagelijkse leven, waardoor er niet nagedacht hoeft te worden over eenvoudige handelingen.

## Begin
In 2018 ben ik begonnen met Home Assistant op een Raspberry Pi 3B. In de loop der jaren is dit gegroeid naar onderstaande situatie: 

# Smart Home
Mijn Smart Home bestaat uit de volgende software en hardware:

 - ### Home Assistant
	 - [Home Assistant OS](https://www.home-assistant.io/installation/alternative) in [VMware ESXi 8](https://customerconnect.vmware.com/en/evalcenter?p=vsphere-eval-8) (*Guest OS: Other 5.x Linux (64-bit)*)
		 - vCPU: 2
		 - RAM: 4GB
		 - Disk: 32GB NVME
		 - Netwerk: IPv4 & IPv6
		 - Zigbee: [Electrolama ZZH!](https://electrolama.com/projects/zig-a-zig-ah/) (CC2652R), toegevoegd als USB device aan de virtuele machine
			 - Reserve: [Slae.sh](https://slae.sh/projects/cc2652/) (CC2652RB)
- ### Philips Hue
	- [Hue White E27 - 800lm](https://www.philips-hue.com/nl-nl/p/hue-white-a60---e27-slimme-lamp---800/8719514329843) (Zigbee)
	- [Hue White E27 - 1100lm](https://www.philips-hue.com/nl-nl/p/hue-white-a60---e27-slimme-lamp---1100/8719514288232) (Zigbee & Bluetooth)
	 - [Hue White Ambiance E27 - 800lm](https://www.philips-hue.com/nl-nl/p/hue-white-ambiance-a60---e27-slimme-lamp---800/8719514328167) (Zigbee & Bluetooth)
	 - [Hue White Ambiance GU10 - 450lm](https://www.philips-hue.com/nl-nl/p/hue-white-ambiance-gu10---slimme-spot/8719514339903) (Zigbee & Bluetooth)
	 - Hue White and Color ambiance LightStrip Plus (Zigbee)
	 - [Hue White Welcome schijnwerper - 2300lm](https://www.philips-hue.com/nl-nl/p/hue-white-welcome-verstraler-voor-buiten/8719514382763) (Zigbee)
	 - [Hue White Lucca - 800lm](https://www.philips-hue.com/nl-nl/p/hue-white-lucca-buitenwandlamp/1740193P0) (Zigbee)
	 - [Hue Motion Buitensensor](https://www.philips-hue.com/nl-nl/p/hue-buitensensor/8719514342262) (Zigbee)
	 - [Hue Motion Sensor](https://www.philips-hue.com/nl-nl/p/hue-bewegingssensor/8719514342125) (Zigbee)
	 - [Hue Smart Stekker](https://www.philips-hue.com/nl-nl/p/hue-smart-stekker/8719514342309) (Zigbee) en (Zigbee & Bluetooth)
	 - Hue Dimmer Switch V1 (Zigbee)
- ### Aquara
	 - [Door & Windows sensor](https://www.aqara.com/en/door_and_window_sensor.html) (Zigbee)
 - ### Blitzwolf
	 - [Blitzwolf BW-SHP13](https://www.blitzwolfeurope.com/BlitzWolf-BW-SHP13-ZigBee-WIFI-Smart-Socket) (Zigbee) - oude generatie met werkende energiemeting
 - ### Chromecast
	 - Google Chromecast (2018)
 - ### Raspberry Pi 3B
	 - [Raspberry Pi OS Bullseye 64-bit](https://www.raspberrypi.com/software/operating-systems/)
	   - [DSMR-reader](https://github.com/dsmrreader/dsmr-reader) - voor het registreren van mijn energie- en gasverbruik door het uitlezen van mijn 'slimme' DSMR5 energiemeter.
	   - [Doorbell](https://github.com/casakampa/doorbell) - mijn Python script dat de functionaliteit van een deurbel verzorgd om mijn domme deurbel 'slim' te maken.


## Integraties
De volgende integraties worden gebruikt:

- [Accuweather](https://www.home-assistant.io/integrations/accuweather/)
- [DSMR Reader](https://www.home-assistant.io/integrations/dsmr_reader/)
- [Enphase Envoy](https://www.home-assistant.io/integrations/enphase_envoy/)
- [Forecast.solar](https://www.home-assistant.io/integrations/forecast_solar/)
- [Google Cast](https://www.home-assistant.io/integrations/cast/)
- [HERE Travel Time](https://www.home-assistant.io/integrations/here_travel_time/)
- [LG webOS Smart TV](https://www.home-assistant.io/integrations/webostv/)
- [Local IP Address](https://www.home-assistant.io/integrations/local_ip/)
- [Met.no](https://www.home-assistant.io/integrations/met/)
- [Home Assistant iOS](https://www.home-assistant.io/integrations/ios/)
- [Mosquitto broker](https://www.home-assistant.io/integrations/mqtt/)
- [OpenTherm Gateway](https://www.home-assistant.io/integrations/opentherm_gw/)
- [Scrape](https://www.home-assistant.io/integrations/scrape/)
- [Zigbee Home Automation (ZHA)](https://www.home-assistant.io/integrations/zha/)
- [Sun](https://www.home-assistant.io/integrations/sun/)

## Add-ons
De volgende add-ons worden gebruikt:

- [MariaDB](https://github.com/home-assistant/addons/blob/master/mariadb/DOCS.md)
- [Mosquitto broker](https://github.com/home-assistant/addons/blob/master/mosquitto/DOCS.md)
- [Studio Code Server](https://github.com/hassio-addons/addon-vscode)
- [Terminal & SSH](https://github.com/home-assistant/addons/blob/master/ssh/DOCS.md)

## Javascript
Als uitbreiding op de Home Assistant front-end worden de volgende scripts gebruikt:

- [Mini Graph Card](https://github.com/kalkih/mini-graph-card)
- [Hass Hue Icons](https://github.com/arallsopp/hass-hue-icons)

## Custom Components
Het volgende custom component wordt gebruikt:

- [Home Assistant Afvalwijzer](https://github.com/xirixiz/homeassistant-afvalwijzer)

# Automatiseringen
De automatiseringen nemen onder andere de volgende taken uit handen:

- [In- en uitschakelen van verlichting of apparatuur op basis van tijd, beweging, locatie of bediening](https://github.com/mvandek/home-assistant-config/tree/master/automations/hue)
- [Wekker (met wake-up functionaliteit)](https://github.com/mvandek/home-assistant-config/blob/master/automations/wekker.yaml)
- [Deurbel (met pauzeren van streaming en inschakelen verlichting)](https://github.com/mvandek/home-assistant-config/blob/master/automations/deurbel.yaml)

## Notificaties

- [Notificaties van bewegingsdetectie bij afwezigheid](https://github.com/mvandek/home-assistant-config/blob/master/automations/meldingen/melding_bewegingsdetectie.yaml)
- [Notificaties betreffende de wasmachine (inclusief startuitstel)](https://github.com/mvandek/home-assistant-config/blob/master/automations/wasmachine.yaml)
- [Notificaties over afval aan de weg](https://github.com/mvandek/home-assistant-config/blob/master/automations/meldingen/melding_kliko.yaml)
- [Notificaties over software updates](https://github.com/mvandek/home-assistant-config/blob/master/automations/meldingen/melding_software_updates.yaml)
- [Notificaties over lege batterijen](https://github.com/mvandek/home-assistant-config/blob/master/automations/meldingen/melding_batterijniveau.yaml)
- [Notificaties over beschikbaarheid lampen](https://github.com/mvandek/home-assistant-config/blob/master/automations/meldingen/melding_beschikbaarheid_lampen.yaml)
- [Notificaties over energieverbruik](https://github.com/mvandek/home-assistant-config/blob/master/automations/meldingen/melding_energieverbruik.yaml)
- [Notificaties over UV-sterkte](https://github.com/mvandek/home-assistant-config/blob/master/automations/meldingen/melding_uv_index.yaml)
