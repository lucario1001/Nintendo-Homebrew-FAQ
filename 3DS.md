***Excessively Asked Questions***



**Q: Is it safe to update to x firmware? (The day that this becomes false, it will be removed, yes it is up to date, yes I am always watching, and yes I am a human who typed this)**
A: As long as you have Luma and A9LH or B9S, it is safe to update to the latest firmware. 
If you do not know if you have Luma and A9LH OR B9S, hold select on boot. If it shows luma configuration, you have Luma and A9LH or B9S. 
If you are still not completely sure that you want to be on the latest firmware, you can make a NAND backup, and restore it at a later date with minimal consequences.

While you are updating your system firmware, you should also consider updating to the latest luma (8.1.1 as of this last edit), and to b9s 1.2 if you are still using a9lh or using b9s 1.0. 
<https://3ds.guide/updating-b9s>
<https://3ds.guide/a9lh-to-b9s>
<https://github.com/AuroraWright/Luma3DS/releases/>

If you are on a firmware on or above 11.4, and do not have cfw or any form of homebrew, there is no point in staying on lower firmware (stated as of 11.6 being the latest firmware)
If you are on a firmware on or above 11.4, and do not have cfw but do have some form of homebrew, please ask about how to update homebrew to work on the latest firmware before updating. Note that notehax was patched in 11.6, and thus cannot be used after 11.5.
If you are on a firmware below 11.4, you should consider getting cfw by following <http://3ds.guide/> and asking in #3ds-assistance-1 or #3ds-assistance-2 if you are unsure of anything.


**Q: I am on 11.4+, what can I do with my system?**
A: You have 3 possible options for installing CFW:
- NTRBoot, which needs a compatible DS flashcart and maybe an additional hacked 3DS or DS(i) console depending on the flashcart.
- DSiWare, which requires a hacked 3DS.
- Hardmod which requires soldering Not for beginners!
 Downgrading is impossible on 11.4+!
Please see <http://3ds.guide/> for more information on each of these and which you should do.


**Q: I don't know which version of Luma I have, how do I check?**
A: Hold select on boot, and it will be the numbers and/or characters between "Luma3DS" and "configuration".


**Q: What is the difference between CFW and Homebrew? Which one should I get/use?**
A: CFW stands for custom firmware, which allows one to run apps and other tools which are not signed by nintendo. This basically means that we can do just about whatever we want as long as someone puts the time and effort into it. Note that you can still use homebrew applications with CFW through Rosalinas homebrew loading (as described in the guide).
Homebrew allows for some unsigned code to be run, however it is buggy, often loses support, and is generally pointless with newer advancements in installing CFW. The extent of this is essentially a few emulators, which may be slow, and save managers. In addition, it is also often more expensive now than to just do ntrboot.
Please refer to other entries for information on installing CFW.


**Q: What is a NAND? What is an emuNAND, do I have it, and do I need or want it?**
A: NAND is essentially storage on your devices motherboard which keeps system data and dsiware titles (when they can be played). 
EmuNAND is a method of having the system redirect reads and writes from the systems physical nand chip to a partition on the SD card. This was used before we had the ability to protect firms on nand as updating would result in a loss of cfw.
You probably do not have an emunand unless your system was hacked over about 2 years ago, but you can check by booting into godmode9. From here, it will list emunand partitions like sysnand. 
Unless you know what you are doing, you do not need an emunand. Note that the safest method of region swapping should be done by using an emunand and not touching your sysnand (to retain as much functionality as possible).


**Q: What is homebrew, CFW, and/or what can I do?**
A: Please refer to this page of the guide: <https://3ds.guide/>. it covers most of this quite well (note: you may need to scroll down some)



***General Errors***



**Q: I updated luma and now the blue light just turns on and off.**
A: Either boot.firm (B9S) or arm9loaderhax.bin (A9LH) is missing from your SD card and/or nand, or the below.
Luma 8.0+ requires the use of B9S 1.2 or above in order to function, thus if you are below B9S 1.2, your system will not correctly boot.
If you know that you have B9S and updated luma prior to this: download this version of luma: <https://github.com/AuroraWright/Luma3DS/releases/tag/v7.1>, put boot.firm on the root of your sd card, and follow this part of the guide: <https://3ds.guide/updating-b9s>
If you know that you are still on A9LH: download this version of luma: <https://github.com/AuroraWright/Luma3DS/releases/tag/v7.0.5>, put arm9loaderhax.bin on the root of your sd card, and follow this part of the guide: <https://3ds.guide/a9lh-to-b9s>
If neither of these work, please state your issue in one of the assistance channels and state that neither of these worked.


**Q: After booting, I get a black screen that says "An excpetion occurred," and the current process is menu.**
A: Do the below steps for the region of your console. Booting now should lead to the home menu regenerating home menu data.
1. Navigate to the following folder on your SD card: ``/Nintendo 3DS/(32 Character ID)/(32 Character ID)/extdata/00000000/``
2. Delete the corresponding folder for your region:
   ``USA: 0000008f``  
   ``EUR: 00000098``  
   ``JPN: 00000082``  
   ``KOR: 000000A9``  
   
   
**Q: I installed CFW using the DSiWare/system transfer method, and now both of the consoles have the same friendcode.**
A: This occurs if you restore a NAND backup to the source console. To fix this, either:  
      1) Wait 1 week, and perform a system transfer from target back to source  
      2) Format one of the consoles. Formatting does not affect CFW.  
      3) Delete the Friend List module save data. (This resets friendcode and friendlist)  
        -For this purpose we have a gm9 script(https://goo.gl/W13vo1). Place in /gm9/scripts in your 3ds SD then run it from godmode9  scripts menu.
**Warning:**  Going online with both consoles simultaneously will lead to unintended consequences, including but not limited to temporary disruption of connectivity.



***GodMode9 and Other B9S Payload Questions***



**Q: How do I use GodMode9?**
A: Please look at this page (<https://3ds.guide/godmode9-usage>) for general GodMode9 usage. If what you wish to do is not mentioned here, ask in the assistance channels.


**Q: How do I boot into GodMode9 or Luma's configuration?**
A: Hold start when turning your system on to boot into GodMode9. If you see a list of tools, just select the one you wish to use.
Hold select when turning your system on to enter Luma's configuration window.



***CFW Installation and flashcarts***



**Q: Which flashcarts work with ntrboot?**
A: Refer to this image: https://i.imgur.com/FKF1rHG.jpg

Take note!
If your flashcart is not on the green pane it is likely not supported.

Regarding the DSTT
Not all DSTT flashcarts will work with ntrboot. If the flasher application won't recognize it, it is not supported.


**Q: What is a flashcart, and what do they normally do?**
A: A DS flashcart is a special type of NDS game cartridge with a microSD card slot in it. It can be used for playing NDS ROMs or NDS homebrew. Some also have the ability to have rewritable firmware, which allows us to install boot9strap and CFW with them.


**Q: Where do I place the magnet for ntrboot?**
A: The below image is approximately where you should place the magnet for ntrboot https://i.imgur.com/AaO4RNB.png (credit goes to @jason0597)


**Q: What magnet should I use for ntrboot, and which side should I use?**
A: Any magnet will work, and polarity (north/south) does not matter. To check if the magnet is strong enough, place the magnet on the console while powered on and see if it triggers sleep mode.


**Q: Which flashcart should I buy then? Clearly the R4i SDHC Gold Pro 2017 seems like a better choice!**
A: The R4i SDHC Gold Pro 2017 has the unwanted effect of a timebomb. This means, that once a certain year has been reached (2019-2020 in this case), the flashcart will stop functioning. You can however circumvent this by just setting the clock on your 3DS/DS back to 2017 (alternatively, see below for another method). The R4i SDHC 3DS RTS does not have this behaviour. Both flashcarts can perform NTRBoot just fine, so if you only care about that, then clearly the R4i SDHC Gold Pro 2017 is a better choice due to the price.

Note: they're usually easy to get around, by installing a different menu or "kernel" such as YSmenu.
There's more information available about this on the internet; support for this is for #legacy-systems, however, as the "time bomb" doesn't impact 3DS/NTRboot functions.
The NTRboot functions will continue to work, on the cheaper "time-bombed" cards, regardless of the system date or time.



***Banwave Questions***



**Q: How do I avoid being banned from network services, or getting caught in a banwave, while using homebrew?**
A: Here are some tips for avoiding a banwave for using homebrew: https://i.imgur.com/50p4TNv.png
1. TURN OFF WIFI
2. Go to Friend List, click Settings in the corner of the screen, go to settings, and DISABLE Share Currently Playing Game. and blank your Favorite Game.
3. Go to System Settings -> Internet Settings -> SpotPass -> Sending of System Information; turn it OFF.

After these steps, you may turn wifi back on.


**Q: What is the banwave? Do you know more about the bans and preventing them?**
A: Wide-sweeping bans for homebrew users are not currently happening at the time of writing this, though they have in the past, and they may happen in the future.
The bans are permanent. This means that Nintendo will not reverse them under any circumstance.
We will not help you with any unban methods, and we will not discuss them in this server.
Furthermore, the steps above will NOT GUARANTEE THAT YOU WILL NOT BE BANNED IN THE FUTURE. IT IS A SAFETY NET.


**As for our research and development into ban prevention:**
We have been looking at some data, and title data is sent to ``pls.c.shop.nintendowifi.net`` from your 3DS, when spotpass sending is on (the default).
You may block this server from your router, through DNS. We will not guide you through this, it is for advanced users.
If you followed the Avoiding Bans section above, you don't need to worry about this unless you're super paranoid.
It's not necessary if you've disabled sending of system information by SpotPass.

**WARNING:** Finally, you WILL be PERMANENTLY banned from network services for playing leaked or early-access copies of games online before the release date at midnight local time. This is completely unavoidable - don't play leaked games, and don't pirate!



***Homebrew and Homebrew Title Questions***



**Q: Where do I download CIAs?**
A: Open FBI, and select TitleDB. From there, you can download a number of free homebrew applications made by the community. 
Note: We do not support piracy here (as stated in rule 11 in #welcome-and-rules).


**Q: When trying to apply themes in Anemone3DS, I get an error saying that extdata does not exist.**
A: Go to the home menu, click the button at the top left, select "Change Theme" and set it to a different default theme. After this is applied, restart Anemone.


**Q: What is NTR CFW?**
NTR is something loaded on top of your existing CFW (for most of you, this is Luma3DS). It allows for game plugins, cheats, streaming of game footage (N3DS/N2DS only) and RAM viewing/editing through the debugger.


**Q: How do I install/launch NTR CFW?**
BootNTR selector is recommended for launching NTR. It can be downloaded from https://github.com/Nanquitas/BootNTR/releases. You will want to install one (or more) of the provided CIA files. Please do not download the 3dsx.

__*N3DS*__
Choose one of the non-mode3 variants. The choice of banner is purely a matter of preference.

__*O3DS*__
Choose the non-mode3 variant. If you intend to use NTR with an extended memory game (eg. Smash, generation VII Pokemon), then you will need the mode3 variant (CIA only) for those games instead. The choice of banner is purely a matter of preference.

Take note!
NTR CFW is not a CFW in itself, and requires Luma3DS to work. Streaming works only from N3DS/N2DS.
NTR CFW is not related to ntrboot.


**Q: How do I use sploit installers on cartridges with Rosalina?**
A: Due to restrictions in Rosalina's homebrew, you currently must have Rosalina temporarily use the title which you wish to install an entrypoint to.
To do this, you must launch the game, open Rosalinas menu (default is L + Select + Down), go to "Miscellaneous options..." > "Switch the hb. title to the current app.", close Rosalina and the game, and relaunch. From there, run the relevant installer, and do the necessary steps for that entrypoint.
