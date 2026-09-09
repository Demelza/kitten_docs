# Kitten Documentation
Kitten is a fully configurable Pay-to-Play system for AFK workers, AFK sim owners and home escorts in Second Life. It is comprised of different parts that all interact with each other for a seamless experience, for both you and your clients.

## Tip Jar
The main item of the Kitten system is the tip jar. It acts as the server for all the other components and will receive your tips distribute them if applicable, and make sure that only paying avatars can play with you. Inside the tip jar is a single script controling it, and a notecard that you will need to modify in order to configure the tip jar.

For more information on how to use and configure your Kitten Tip Jar, please consult the [tip jar documentation](tipjar_readme).

## AFK Controls
The AFK control object is made to be worn by the avatar logged into the tip jar. It will present your clients (or yourself) with a menu when clicked, letting you pick between several options, like "Undress" and "Move". It has multiple scripts inside, and almost all scripts are removable from the object if you don't need the functionality associated with it. Some of its functions are locked behind paying the tip jars, while some are not.

For more information on how to use and configure your Kitten AFK Controls, please consult the [AFK controls documentation](afk_controls_readme).

## Furniture Script
In order for the tip jar and mover to be able to recognize your furniture, you will need to insert this script inside your furniture. Please note that this means your furniture needs to have Modify permissions, otherwise you won't be able to put the script inside.

There is nothing to configure for this script to work, simply rez your furniture, put the script inside, and wait a few minutes while your furniture scripts reset.

## AFK Pad
The AFK pad is an object that can be rezzed on the ground and will act as your "home furniture". You will need to set it as your first FURNITURE line in the configuration notecard of your tip jar.

It is also possible to use your own AFK pad instead of the provided one. In this case, some of the scripts present inside the provided AFK pad may be transferred to a different object.

For more information on how to use and configure your Kitten AFK Pad, please consult the [AFK pad documentation](afk_pad_readme).
