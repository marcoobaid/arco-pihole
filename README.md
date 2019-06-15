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

## Automated Install For ArcoLinux (ArchLinux)
Pi-hole automated installer does not support ArchLinux. Running Pi-hole on Arch-based systems entails installing Pi-hole via AUR respository, in addition to some related depedencies. Instructions are detailed in <a href="https://wiki.archlinux.org/index.php/Pi-hole">ArchWiki Pi-hole page</a>.

The script provided in this page is intended to automate Pi-hole installation on ArcoLinux/ArchLinux systems. 

- Peform a fresh install of ArcoLinuxD (for a dedicated Ad-Blocker system), or ArchLinux.
- Clone this repository to your system 
```
git clone https://github.com/marcoobaid/arch-pihole Pi-hole
cd "Pi-hole"
./install-pi-hole-server-v1.sh
```
# Post-install: Configure your network to point to Pi-hole

Once the installer has been run, you will need to [configure your router to have **DHCP clients use Pi-hole as their DNS server**](https://discourse.pi-hole.net/t/how-do-i-configure-my-devices-to-use-pi-hole-as-their-dns-server/245) which ensures that all devices connecting to your network will have content blocked without any further intervention.

If your router does not support setting the DNS server, you can [use Pi-hole's built-in DHCP server](https://discourse.pi-hole.net/t/how-do-i-use-pi-holes-built-in-dhcp-server-and-why-would-i-want-to/3026); just be sure to disable DHCP on your router first (if it has that feature available).

As a last resort, you can always manually set each device to use Pi-hole as their DNS server.

