# TrueNas-setup
How to setup TrueNas properly

After making a bootable USB stick with Ventoy and your TrueNas Iso,
  - Boot on it with your NAS, once TrueNas is installed shutdown the NAS and remove the USB stick.
  - You will have to set up your IPv4 so that each of your devices have the same subnet mask, in my case, I had to check my Bouygues router DHCP Window (192.168.1.0 to 192.168.1.200
  - Get your NAS Mac adress and set up its Static IP through your router, here I chose 192.168.1.93
  - On the TrueNas Machine, in the menu, select 1
        - Change the IPV4DHCP Automatic attribution to 'No'
        - Change the Allias to the same that you set on your router, here it's 192.168.1.93. Save all of the changes
  - Go back to the menu and select 2
        - Change the default IPv4 and DNS to the one of your Router, for me it was 192.168.1.254 for both
  - Reboot your NAS

Afterward, if you have routers, or repeaters in your household, they may have a different automatic DHCP from your main router
  - So make sure to change it, for me it was 192.168.3.1 => I changed it to 192.168.1.3
      - Now, even the switchs/routers that amplify the signals of my main router have the same subnet mask as my main router.
      - If you have issues, reset your IPconfig on your devices for instance on windows : ip config /release | ipconfig /renew
      - Or set a fix IPv4 with the same subnet mask, here I chose 192.168.1.37
