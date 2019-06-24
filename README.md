## Network-wide AD Blocking via Pi-Hole on ArcoLinux

<p align="left">

<a href="http://www.arcolinux.com" alt="ArcoLinux">
<img src=".scrots/arcolinux_website.png" width="150" height="150" alt="Pi-hole">
</a>
<img src=".scrots/plus.png">
<a href="https://pi-hole.net">
<img src="https://pi-hole.github.io/graphics/Vortex/Vortex_with_text.png" width="100" height="205" alt="Pi-hole"> 
</a> 
<img src=".scrots/equal.png"> 
<img src=".scrots/adblocking.jpg" width="150" height="150" alt="No Ads">

<br/>

</p>

The Pi-hole[®](https://pi-hole.net/trademark-rules-and-brand-guidelines/) is a [DNS sinkhole](https://en.wikipedia.org/wiki/DNS_Sinkhole) that protects your devices from unwanted content, without installing any client-side software.

-----

## Automated Install For ArcoLinux (or ArchLinux)
Pi-hole automated installer does not support ArchLinux. Running Pi-hole on Arch-based systems entails installing Pi-hole via AUR respository, in addition to some related depedencies. Instructions are detailed in <a href="https://wiki.archlinux.org/index.php/Pi-hole">ArchWiki Pi-hole page</a>.

The script provided in this page is intended to automate Pi-hole installation on ArcoLinux/ArchLinux systems. 

- Peform a fresh install of ArcoLinuxD (for a dedicated Ad-Blocker system), or ArchLinux.
- Clone this repository to your system 
```
git clone https://github.com/marcoobaid/arch-pihole Pi-hole
cd "Pi-hole"
./install-pi-hole-server-v1.sh
```
_The script will ask you to enter a password to access The Web Interface Dashboard._

## Post-install: Configure your network to point to Pi-hole

Once the installer has been run, you will need to [configure your router to have **DHCP clients use Pi-hole as their DNS server**](https://discourse.pi-hole.net/t/how-do-i-configure-my-devices-to-use-pi-hole-as-their-dns-server/245) which ensures that all devices connecting to your network will have content blocked without any further intervention.

If your router does not support setting the DNS server, you can [use Pi-hole's built-in DHCP server](https://discourse.pi-hole.net/t/how-do-i-use-pi-holes-built-in-dhcp-server-and-why-would-i-want-to/3026); just be sure to disable DHCP on your router first (if it has that feature available).

As a last resort, you can always manually set each device to use Pi-hole as their DNS server.

-----

## The Web Interface Dashboard
This [optional dashboard](https://github.com/pi-hole/AdminLTE) allows you to view stats, change settings, and configure your Pi-hole. It's the power of the Command Line Interface, with none of the learning curve!

<img src="https://pi-hole.github.io/graphics/Screenshots/pihole-dashboard.png"  alt="Pi-hole Dashboard"/></a>

Some notable features include:
* Mobile friendly interface
* Password protection
* Detailed graphs and doughnut charts
* Top lists of domains and clients
* A filterable and sortable query log
* Long Term Statistics to view data over user-defined time ranges
* The ability to easily manage and configure Pi-hole features
* ... and all the main features of the Command Line Interface!

There are several ways to [access the dashboard](https://discourse.pi-hole.net/t/how-do-i-access-pi-holes-dashboard-admin-interface/3168):

1. `http://<IP_ADDPRESS_OF_YOUR_PI_HOLE>/admin/`
2. `http://pi.hole/admin/` (when using Pi-hole as your DNS server)
3. `http://pi.hole/` (when using Pi-hole as your DNS server)

-----

## Resources
- [Pi-hole](https://pi-hole.net)
- [Pi-hole ArchWiki](https://wiki.archlinux.org/index.php/Pi-hole)
- [The Big Blocklist Collection](https://wally3k.github.io)
- [Pie in the Sky-Hole](https://dlaa.me/blog/post/skyhole)
- [Copernicus: Windows Tray Application](https://github.com/goldbattle/copernicus)
- [Magic Mirror with DNS Filtering](https://zonksec.com/blog/magic-mirror-dns-filtering/#dnssoftware)
- [Windows DNS Swapper](https://github.com/roots84/DNS-Swapper)
