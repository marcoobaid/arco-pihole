### Network-wide AD Blocking via Pi-Hole on ArcoLinux

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
  - 
```
git clone --depth 1 https://github.com/pi-hole/pi-hole.git Pi-hole
cd "Pi-hole/automated install/"
sudo bash basic-install.sh
```
