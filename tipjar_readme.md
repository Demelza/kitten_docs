# Kitten Tip Jar
The tip jar acts as a server and safety system for all the other scripts: opening the most important menus of the AFK Controls object will need to be allowed by the tip jar. For example, if someone tries to open the Undresser menu, the Undresser script will ask the tip jar: 1: if the avatar trying to open the menu is the same as the wearer, and 2: if not, if the avatar trying to open the menu has tipped your tip jar and has an active paid session. If any of those checks succeeds, your Undresser menu will be displayed and the avatar who opened it (you or your client) will be able to use the options in that menu (change your outfit, undress parts (or all) of it, etc.
It will also communicate with the Furniture script that you have added inside furniture: if your furniture doesn't contain the furniture script, it will not be displayed in the Mover, meaning other avatars cannot move you to it. If someone tries to sit on furniture that contains the Furniture script, they will either 1: be ejected and forced to stand if they have not tipped you, or 2: be allowed to sit if they tipped you and their session is still active.

Effectively, nobody can move you, sit on furniture, or use your Undresser unless they tip you first and their time hasn't expired.

It contains 3 items: its script (kitten.tipjar) and its configuration notecard (TipJarConfig), and a copy of the AFK Controls that AFK avatars can grab with the "Get Controls" button in the tip jar menu and equip.

It is configurable via its notecard, with the following options:

## TIP_AMOUNT=(number)
The minimum amount of L$ that needs to be paid to the tip jar. If a lower amount than this is paid, it will be automatically refunded to the payer (this function is the reason why, when the tip jar is first rezzed, it will ask you for L$ withdraw permissions: if it can't withdraw money from you, it cannot refund an avatar that tips an incorrect amount. This permission is ONLY used for that function.)  
Valid values: any number. For example: TIP_AMOUNT=100

## SESSION_MINUTES=(number)
The time (in minutes) you want a session to last. Once the session ends, the client is automatically forced to stand from the furniture, and you are returned to your home furniture. This setting is "tied" to TIP_AMOUNT above: a tip equal to TIP_AMOUNT will give your client a session that lasts SESSION_MINUTES.  
Valid values: any number. For example: SESSION_MINUTES=30

## TIP_NOTIFICATIONS=
If set to TRUE, you will be notified whenever someone tips one of your tip jars. Please note that it notifies the owner of the tip jar, not the avatar who is logged in to the tip jar (they already receive a notification when someone tips them), in case those are not the same avatar. If for example you are an AFK sim owner and leave this setting to TRUE, you will be notified every time one of the AFK avatars at your sim gets tipped. If this is too spammy or you don't want to receive notifications, set it to FALSE.  
Valid values: TRUE or FALSE

## MULTIPLE_LOGIN=
If set to TRUE, it will allow you to login to multiple tip jars at the same time (which can be useful for home escorting, for example). I recommend not leaving this enabled if you are an AFK sim owner, as one avatar would be able to login to multiple or all the tip jars on your sim.  
Valid values: TRUE or FALSE

## AUTO_LOGOUT_ON_LEAVE=
If set to TRUE, it will log out any avatar logged in to the tip jar if they leave the sim or disconnect. Grace period during which they can come back or relog can be configured in the next setting.  
Valid values: TRUE or FALSE

## LEAVE_GRACE_SECONDS=(number)
The amount of time (in seconds) that an avatar is allowed to be away from the tip jar for before the tip jar logs them out, if the auto logout setting is enabled. If the auto logout is not enabled, this doesn't do anything.  
Valid values: any number. For example: LEAVE_GRACE_SECONDS=60

## RESERVED_AVATAR=
If you want your tip jar to be reserved for a single avatar, you need to enter the avatar's UUID here. Avatar UUID can be found in an avatar's profile next to their name. If left blank or not present, the tip jar will let anyone log in.  
Valid values: any avatar UUID. For example: RESERVED_AVATAR=00000000-0000-0000-0000-000000000000

## TEXT_COLOR=(RGB colors)
This setting changes the color of the floating text above the tip jar and the AFK Controls worn object.  
Valid values: RGB colors. For example: TEXT_COLOR=255,255,255

## MOVER_TEXT=(text)
Text you want to display above the AFK Controls worn object. You can use it to display info about yourself, give short instructions on how to use your objects, etc. It supports multiple lines with \n.  
Valid values: any text. For example (one line): MOVER_TEXT=Hello! | For example (two lines): MOVER_TEXT=Hello!\nI'm AFK!

## GIVE_TIPS_PERCENT=(number)
The percentage of tips that should go to the avatar logged in to the tip jar. For example, if this setting is set to 90, it'll give 90% of the tips to the avatar logged in to the tip jar and 10% to the owner of the tip jar. If set to 0 or lower, all tips will be paid to the owner of the tip jar. If set to 100 or higher, all tips will be paid to the avatar logged in to the tip jar.  
Valid values: any number. For example: GIVE_TIPS_PERCENT=80

## PICTURE=(UUID)
The UUID of the default picture of the tip jar when nobody is logged in. The tip jar already comes with a default picture but you can set your own if you prefer.  
Valid values: image UUID. For example: PICTURE=00000000-0000-0000-0000-000000000000

## FURNITURE=(object UUID)
The UUIDs of all the furniture you want the Mover to recognize, one per line. To get your furniture UUID, rez them and right click them, then click Edit. In the first tab of this menu, there's a "Copy Keys" button. Click it and paste it as a value for this setting. Repeat for every piece of furniture you want to use with the mover. Please note that every piece of furniture also needs to have the Furniture script inside, otherwise the tip jar and mover will not recognize them or allow moving to them.  
Valid values: any furniture UUID. For example: FURNITURE=00000000-0000-0000-0000-000000000000
