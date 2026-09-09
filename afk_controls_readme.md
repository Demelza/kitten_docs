# Kitten AFK Controls
The AFK controls are the part that lets your clients interact with you. Currently, it offers the following options in the main menu:

* Undress  
  This button will let your clients open the Kitten Undresser menu. However, the Undresser script communicates with your tip jar and will refuse to open if they have not tipped you first. There is a standalone replacement script provided in case you want to leave this functionality available even for non-tippers.  
  If you wish to entirely remove this functionality, you may remove the Undresser script (kitten.undresser) from the AFK controls object. This button will also entirely disappear from the main menu.

* Move  
  This button will let your clients move you to any furniture you have configured in the notecard inside the tip jar. Since it communicates with the tip jar, it will also only open if the avatar has tipped you first.  
  While it is possible to remove the mover script (kitten.mover) from the AFK controls object without breaking the menu, please note that it is not advised, as your clients will not be able to move you and won't be able to sit in furniture unless they have tipped you first. If you still wish to remove it, please make a backup first.

* Face Controls  
  This button will open the face controls menu, which lets your clients change your face expressions. It had options for blush, eyes, mouth, expression presets, and, if configured in the notecard (SettingsM4), your own custom expressions presets. It is currently only compatible with Utilizator M4 heads, and I am looking into making it compatible with more heads.  
  If you wish to entirely remove this functionality, you may remove the Face Controls script (kitten.facecontrols) and its notecard (SettingsM4) from the AFK controls object. This button will also entirely disappear from the main menu.

* Cum  
  Clicking this button will communicate with your cum system and open its menu. While I wish I could do this, I cannot make it so that it works only if you have been tipped first: people would be able to cum on you regardless, as that's what those systems are designed for.  
  If you don't want others to be able to play with your cum menu, there are a couple solutions: either make your cum system an accessory in your Undresser folders (that way other avatars will only be able to make you wear it if they tip you to access the undresser first; please see the Undresser section below), or detach it entirely. It is currently only compatible with the Spunked cum system.  
  If you don't want this button to be visible in the menu, you will have to detach your cum system from yourself. If it can't communicate with a cum system, this button will hide itself.

## Undresser
The Undresser (accessible via the Undress button in the main menu of your AFK controls) will let others change your outfits, undress or redress you, and change your avatar.  
In order to make it work, you'll have to do the following steps:  
* Open your inventory, and create a folder named #RLV, if it's not already there
* Inside the #RLV folder, create a folder named ~kitten
* Inside the ~kitten folders, create a folder named Avatars
* Inside the Avatars folder, you may create any number of folders you want, one per avatar. Remember their names, as we will use them soon
* Inside this Avatar name folder, you can add any mesh item, BOM layers, alpha layers, tattoos, skins, etc, that will ALWAYS be worn by this avatar. They will never be detached unless someone changes you into another avatar
* Back in the ~kitten folder, create a folder with the following pattern: [avatar name]_Outfits. For example: Human_Outfits. Note that this folder is avatar-specific, so you will need to make one for each avatar in the Avatars folder
* Inside this Outfits folder, you can now create one folder per outfits you want to make. For example, you can make a Casual folder, a FormalDress folder, a Pajamas folder, and so on.
* Inside each specific folder, create another folder named Base_X.XXX, where X.XXX is a number that represents the hover height that will suit this outfit. This hover height will be applied automatically when you change into this outfit. This is useful in cases where your outfit has very high platform shoes, for example, so that they don't sink into the floor because you're not hovering high enough. Hover height will reset itself back to 0 when you're sitting and will go back to this configured value if you stand up. This Base folder will not be visible in the Undress menu, and cannot be detached by others. You can put some parts that are essential to the outfit and should never be detached while it is worn (for example, a cum attachment for this outfit's specific foot height, or a piercing, etc).
* Still inside the specitif outfits folder, you will now need to create 2 folders per piece of clothing. For example, Panties_1 and Panties_2 for underwear, Shoes_1 and Shoes_2 for your shoes, etc.
* The folder that ends in _1 is what will be equipped when the associated piece of clothing is worn.
* The folder that ends in _2 is what will be equipped when the associated piece of clothing is not worn.
* You can, for example, have your pair of panties in the Panties_1 folder, and your mesh genitals in the Panties_2 folder. When you or someone else removes your panties, it'll automatically attach your genitals.

The complete structure will look like this:  
![Undresser Folder Structure](/images/undresser_folder_structure.png)

As you can see here:  
* The ~kitten/Avatars/Neko contains all pieces of my avatar that are never detached: body, ears, tail, skin, hair, shape...
* The ~kitten/Neko_Outfits folder contains a Bikini folder, which is the base folder for this outfit
* The ~kitten/Neko_Outfits/Bikini folder contains a folder named Base_0.010. The items in it will never be detached while the outfit is worn, and since it ends with 0.001, when the outfit is worn, it will set my hover height to 0.010
* It also contains, among others, the folders BikiniBottom_1 and BikiniBottom_2. The first folder contains the actual bikini bottoms, while the second one contains my mesh genitals that will automatically be attached when someone strips my bikini bottoms.

You can also see a Neko_Accessories folder in ~kitten. This folder itself contains 4 more folders: Hair, HUDs, Jewelry and Misc. And inside each of those folders, you can make another folder and put the accessory you want to wear in that folder. There is however no need for a _1 and _2 folder in there. Your accessory will either be worn or not, like this:  
![Accessory Folder Structure](/images/accessory_folder_structure.png)  
It is worth noting that accessories are not detached when you switch outfits, but will be detached when switching avatars, as the accessory folders are avatar-specific, like the outfits folders.

Once all that is done, the system is ready to be used. Attach your AFK controls object and click it. You should see a main menu with an Undress button. When you click it, you will be presented with this menu:
![Undresser Menu](/images/undresser_menu.png)  
* The "Avatars" button lets you or your client change the avatar you're wearing
* The "Outfits" button lets you or your client change your outfit
* The "Undress" button lets you or your client remove your clothes one by one: they can choose to remove your top and your skirt without removing your socks and shoes, for example
* The "Undress All" button will remove all your clothes
* The "Redress All" button will re-attach all your clothes
* The "Access" button is only visible by you: and it lets you configure the visibility of the Avatars, Outfits and Undress menus to your clients. For example, if you don't want them to be able to change your avatar, you can disable it there, and only you will be able to see it
* The "Accessories" button will let your client attach or remove accessories from you. You can use it to let them change your hair, or equip different attachments like piercings, etc

## Mover
If you click the "Move" button in the main AFK Controls menu, you will be presented with a list of buttons with furniture names (and, if there are too many, also menus to navigate between pages). Clicking one of those buttons will move you to the associated furniture.  
Please note that in order for the furniture to be listed in here, it must fill BOTH of those conditions:
* The furniture has been added to the tip jar's configuration notecard
* The furniture contains the furniture script bundled with the Kitten AFK system

## Face Controls
The Face Controls lets other people control your face expressions while they're playing with you, giving them a better, more real experience. The current version of the face controls only supports the Utilizator M4 heads, but there are plans to extend it to more types of heads. It has the following options:
* Blush: lets you set the blush level. Some heads support 2 levels while others support 3. Setting your hear properly in the SettingsFace notecard will allow the menu to adjust to this setting properly
* Eyes: supports 4 levels of eye openness for every head: Open, Half Closed, Almost Closed, and Closed
* Mouth: supports 3 levels for every head: Closed, Open, Tongue Out. The Closed option can be configured in the SettingsFace notecard
* Expressions: comes with a few pre-made expressions presets, adjusted for every head it supports
* Custom Expressions: the settings notecard allows you to configure up to 8 custom presets. This menu will not be shown unless the notecard is configured to show the menu

## Cum
If you are wearing a compatible cum system (currently, only the Spunked cum system is supported), the Cum button will appear in the main menu of your Kitten AFK controls. Clicking it will simply bring up the cum menu of your cum attachment. It communicates with your cum system API to determine if you're wearing it or not

## Removing functionality
Some of the functionality can be removed if you don't need it. Here is everything that can be removed from the AFK controls object:
* kitten.undresser script: will remove the Undress button from the main menu and the Undresser won't be available to use anymore
* kitten.mover script: will remove the Move button from the main menu and the Mover won't be available to use anymore. I REALLY do NOT recommend removing this
* kitten.facecontrols script and SettingsM4 notecard: will remove the Face Controls button and functionality from the main menu entirely. I recommend removing those if you are not using a supported head
* kitten.accessories script: will remove the Accessories functionality from the Undresser entirely
* kitten.avatars script: will remove the Avatars functionality from the Undresser entirely
* kitten.outfits script: will remove the Outfits and Undress functionality from the Undresser entirely
* The cum functionality can only "removed" by not wearing a compatible cum system. The Cum button in the main menu will only show up if you are wearing one and simply calls for your cum addon menu to be displayed via its API
