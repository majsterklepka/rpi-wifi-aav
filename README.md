#rpi-wifi-aav
Malinkowy AP

Witam!

No tak, na ten temat jest pełno materiału w Internecie, ale pokrótce:

## Co potrzeba?

- RaspberryPi 4 szt. 1
- modem USB LTE szt. 1
- drobiazgi takie jak: obudowa do RaspberryPI, zasilacz do RaspberryPi, karta pamięci z wgranym systemem Raspbian Buster ...

Nie będę tu opisywać co należy zrobić aby nasza Malinka ruszyła, na ten temat jest całe mnóstwo materiałów w Sieci, tu tylko podam, co należy zrobić aby ruszył AP!!!

## A więc ...

po instalacji hostapd należy zrobić kopię bezpieczeństwa jego plików konfiguracyjnych, w folderze /etc/hostapd należy umieścić plik hostapd.conf modyfikując go do własnych potrzeb. 

Jeśli dnsmasq jest niezainstalowane, to należy go zainstalować i zrobić to co poprzednio, czyli w folderze /etc umieścić plik konfiguracyjny dnsmasq.conf modyfikując go odpowiednio do własnych potrzeb

Następnie aby mieć dostęp do portu Ethernet należy go połączyć mostkiem z interfejsem wlan0, najpierw należy utworzyć mostek poleceniem:

```
brctl addbr br0
brctl addif br0 eth0 wlan0
```

Następnie należy w folderze /etc/network zmodyfikować plik interfaces(można go skopiować z repozytorium, uprzednio robiąc kopię oryginału)

- - - 

ciąg dalszy nastąpi ...

- - - 

do zrobienia:

- iptables
- uruchamianie
- ip4-forwarding



