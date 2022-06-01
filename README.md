# ftpiiu-everywhere-tiramisu
Forked from https://github.com/FIX94/ftpiiu to create working Tiramisu FTP

Download [TIRAMISU---ftpiiu_everywhere.zip](https://github.com/xMunji/ftpiiu-everywhere-tiramisu/blob/Tiramisu-FTPiiU_Everywhere/TIRAMISU---ftpiiu_everywhere.zip)  which contains ``ftpiiu_everywhere.elf``, ``icon.png`` and ``meta.xml`` to a folder in ``sd:wii u/apps``


found code here: https://nesretro-com.translate.goog/x/t/wii-u-n-softmodaaminen-feat-region-free-tiramisu-ftpiiu-everywhere.1279/?_x_tr_sl=fi&_x_tr_tl=en&_x_tr_hl=en&_x_tr_pto=sc


The main reason I was looking for this in 2022 is to change the name of games installed on USB or Nand. If you're looking for the same thing, here's the solution:

Download Notepad++
Download WinSCP
Choose install with one window
Download ftpiiu_everywhere.zip from above


The steps I followed are [from an old forum post](htps://gbatemp.net/threads/how-to-rename-game-title.463283/). Still holds up. I'll copy here incase it ever gets deleted or something. 

"Whether sourced from disc or eShop, the name comes from /usr/title/000500e/restoftitleID/meta/meta.xml 
(if the title has an update installed) or /usr/title/0005000/restoftitleID/meta/meta.xml if there is no update."



1. Find your game's TitleID using that Title Database](https://wiiubrew.org/wiki/Title_database)
2. Run ftpiiu_everwhere on your WiiU, and connect to it using the ip it gives when opening as the "Host Name" and the number after the colon as the port number Username/password doesn't matter.

   *Example: ``FTPiiU is listening on 123.456.7.910:21`` means you type in ``123.456.7.910`` for ``"Hostname"`` and ``21`` for the ``"Port number:"``*

3. Navigate to ``/usr/title/0005000/``restoftitleID``/meta/meta.xml`` and right click to edit, choosing Notepad++ as your editor.

   *Note: you may have to find the usr folder inside of its corresponding storage medium. Because I installed to usb, my usr folder was in storage_usb/usr*
4. Look for the title's longname and change at least the entry for your language.
5. Ctr+S to save.
6. Restart the WiiU or switch users (you can change several titles before doing so, if you want).
You're done!

"Thoughts:
Be careful. I suspect that the icon will just show ??? if you mess up the XML, but I'm not going to try it just to find out.
If you use out-of-region games you could add (EUR) (US) or (JP) to the end
Maybe add a * at the end of a name to denote that you need signature patches for those titles that do.
Make sure you use &lt; &amp; &gt; &quot; and &apos; for < & > " ' , e.g. Pirate&apos;s Curse"
