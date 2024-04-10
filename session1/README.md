# Session 1

## Befehle

- `ansible all --key-file ~/.ssh/devopsbasics -i inventory -u superuser -m ping`: Verwendet Ansible, um eine SSH-Verbindung zu allen Hosts in der Inventardatei unter Verwendung der angegebenen SSH-Schlüsseldatei, des Benutzernamens und des Moduls herzustellen. Es handelt sich dabei nicht um einen herkömmlichen Ping, sondern um einen Versuch, eine SSH-Verbindung zum Server herzustellen.

- `ansible all --list-hosts`: Listet alle in der Ansible-Inventardatei definierten Hosts auf.

- `ansible all -m gather_facts`: Sammelt Fakten (Systeminformationen) von allen in der Inventardatei angegebenen Hosts.

- `ansible all -m gather_facts --limit 10.37.129.2`: Sammelt Fakten von einem bestimmten Host mit der IP-Adresse 10.37.129.2.

- `ansible all -m gather_facts apt --help`: Zeigt Hilfsinformationen für das Modul "gather_facts" speziell für den "apt"-Systempaketmanager an.

- `ansible all -m apt -a name=tmux`: Verwendet das Modul "apt", um das Paket "tmux" auf allen Hosts zu installieren.

- `ansible all -m apt -a name=tmux --become --ask-become-pass`: Installiert das Paket "tmux" auf allen Hosts und fordert erhöhte Rechte (become) unter Verwendung des angegebenen Passworts an.

- `tail -f /var/log/apt/history.log`: Zeigt den letzten Teil der angegebenen Protokolldatei an, aktualisiert kontinuierlich und zeigt neue Einträge im Zusammenhang mit der Paketverwaltung an. (Muss am Server ausgeführt werden)

- `sudo apt update`: Aktualisiert den lokalen Paketindex, um die neuesten Änderungen in den Repositories widerzuspiegeln. (Muss am Server ausgeführt werden)

- `sudo apt dist-upgrade`: Aktualisiert die installierten Pakete, behandelt Abhängigkeiten intelligent und kann je nach Bedarf zusätzliche Pakete entfernen oder installieren. (Muss am Server ausgeführt werden)
