# CSS hacks for fugitech discord reactives

![image](https://github.com/user-attachments/assets/9371e9d2-5f55-4e45-901f-6fe30cc4ac2b)

A collection of CSS tweaks to make fugitech reactives look nicer on your stream.
Add the fugitech reactive group source as an OBS browser source, go to properties, Custom CSS and paste in the tweaks you want

## Basic tweaks:
### FixedIconSizeAndRepositionText.css
This will resolve spacing issues if you have guests with non-square reactive images. 
- Tall images will be padded to a matching width, and wide images will be cropped.
- Images will have a drop shadow applied and this even works properly if your guest is using transparent images
- Text labels will be moved above the image and limited to one line.
- Long names will be truncated with an ellipsis ...
- You can provide a custom font, colour, text-shadow etc.

Unfortunately fugitech reactives crop the bottom few pixels off guest images and this cannot be fixed, so I recommend placing your reactives at the bottom of your stream layout, or inside a box element of some sort.
If you are using the default values, your browser source should be 160 pixels high. For other sizes I recommend editing the sizes in the CSS and the height of your browser source rather than applying OBS scaling.

### HideDiscordNotLoadedError.css
If you have not loaded discord and you leave the browser source for reactives enabled, you get an annoying grey bar with an animated cog logo. Usually right at the start of your stream when your previous stream was a multiplayer game. Add this CSS to disable it!

### RecolourTextOnSpeech.css
This will change the colour of your guest's text label when they speak. This is mainly useful if you have disabled image dimming and your guests have not got a visually distinctive speaking image uploaded

## Tweaks for use with Twitch Stream Together (formerly Guest Star)
These were originally built for VTuber FFXIV raid streams, where not every guest can have their model on stream as Twitch is limited to six guests but you need 8 people to raid.
For these you will need to get the Discord ID of the users in question. To do this go to Settings -> Advanced and enable Developer Mode, you can then right click your guest and choose 'Copy ID'

### HideSpecificUsers.css
This will allow you to completely remove a user from the Reactives so they aren't appearing twice if you have them on Stream Together. I recommend creating an entry in advance for every user who is likely to be on Stream Together and then commenting them out

### TextOnlyReactiveLabels.css
This will allow you to create a SEPARATE browser source for one user that shows their text label without their profile pic. For a Stream Together guest you could place this over their Stream Together feed so they still have a light up speaking label.

Warning: If you need to create a speaking label for yourself. You will need to enable "Include Own Image in Group View" in the Fugitech settings, you will probably also want to include yourself in HideSpecificUsers.css

If you find these useful, consider giving me a follow or a raid over at:
### https://twitch.tv/LumKitty
