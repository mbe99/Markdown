# Virtualisierung

## VirtualBox Version 5.6
Alle benötigten Software Komponenten können problemlos als VM innerhalb der VirtualBox installiert werden. Das hat den Vorteil, dass die bestehende Installtion nicht beeinträchtigt wird.

### Netzwerk
Damit vom Host System auf die Applikationen innerhalb der VM zugegriffen werden kann (wir verwenden Privat Networks, resp. NAT), müssen entsprechende Portweiterleitungen Konfiguriert werden. Für eine einheitliche Installtion und damit auch für einen besseren Support, verwenden wir folgende Portweiterleitungen:

##### Windows
*(Gast Port --> Host Port)*
* 80 --> 8088
* 3306 --> 3366

#### Linux
*(Gast Port --> Host Port)*
* 80 --> 8080
* 3306 --> 3377

Ensprechendn müssen danach die Clients, welche vom Hostsystem auf die Applikationen (Bsp. HeidiSQL) in der VM zugreiffen wollen angepasst werden.

### Gasterweiterungen
In der VM sollten die VirtualBox Gasterweiterungen installiert werden, damit mit dem Hostsystem **gemeinsame Ordner** und **Drag und Drop** verwendet werden können. Beide Optionen sind per Default deaktiviert und müssen zuerest konfiguriert und aktiviert werden. Dabei jeweils die Option **bidirektional** verwenden.

shared Folder:
> Host: c:\tmp Gast: /tmp
