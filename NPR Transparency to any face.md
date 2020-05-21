# How to apply NPR Hair transparency to any face.
![Example](https://imgur.com/lxKb8DL.png)

Contrary to what you might think this effect isn't only due to a change in the hair.
Instead, NPR stencil shader relies on a combination between face and hair materials.

There are two ways to go about this:

1. Simple but can only be used with already made faces gracefully provided by NPR author(s)

2. Need more work but can be done with any faces in the game!

## Simple Method
### Needed:
- COM3D2 (doesn’t work with CM)
- NPR shader 0.6.0 or above
https://ux.getuploader.com/sixima/download/18
- Sixima’s stencil shader compatible faces
https://ux.getuploader.com/sixima/download/15
- COM3D2.AutoEraseOutline.Plugin disabled (both plugins are incompatible)

### How to Proceed:
-	Install NPR shader plugin
You only need what’s in the Sybaris folder, other folders are just examples made for modder’s sake.
Install like any plugins.
-	Install Sixima’s stencil shader compatible faces
This is a mod, so in the mod folder it goes like any other mods.
-	In game, be sure to select one of these faces:

![NPRFace](https://imgur.com/zubXpA4.png)
 -	In your hair color setting, select one of those two icons (the only real difference between them is the transparency amount)
 
![NPRIcon](https://imgur.com/6fkEJj5.png)
-	That’s it. Done!

### Notes:
-	Some hair mods don’t include all available color preset, you’ll have to edit their .menu.
-	Like any NPR shaders, stencil is applied once and will not be removed unless you select another color preset and change the hair model.


## Advanced method:
### Needed:
-	Same things as the method above
-	Blender 2.79b with CM3D2 converter (and a basic understanding of how to use it)
-	[CM3D2]menu←→txt Converter.exe or [CM3D2]menuEdit.exe
-	A face to edit… obviously
-	Some patience, it can be a little bit daunting at first but can be made quickly once understood.

#### How to proceed:
-	Make a backup or duplicate your face.
-	Import the face .model into blender and duplicate its SkinAlpha material.

 ![Step1.1](https://imgur.com/zkQFAeb.png)
 ![Step1.2](https://imgur.com/8oQOEBo.png)
 ![Step1.3](https://imgur.com/MUDb7w3.png)
-	New material’s name doesn’t really matter but rename it properly anyway.
- Be REALLY Careful with material order, it’s VERY important later on. Basically, keep it like it was and put your new material at the bottom.
-	In Edit mode, select everything assigned to the original SkinAlpha material EXCEPT the eyelashes, and assign to the new material.

 ![Step2.1](https://imgur.com/i0hTDi1.png)
-	Eyeleshes are now assigned to SkinAlpha, tears, drool, shade and blush are assigned to SkinAlpha_Ex

 ![Step2.2](https://imgur.com/AfVeAdW.png)
-	Export your model
-	Open the face’s .menu either with [CM3D2]menu←→txt Converter.exe or [CM3D2]menuEdit.exe
I recommend the former as it’s easier to add and edit lines, just be careful with your structure.
-	We want to add NPR specific shaders to each material of the face that need one. Note that GP01 compatible faces need more changes.
-	Although you can go with the .mate included in sixima’s example I recommend you to copy them and rename them for yourself:

sixima_eyel_Stencil5 **_NPRMAT_NPRToon_StencilWrite.mate** . 
**Bold** part of the name is mandatory, the rest can be named as you wish.
-	Two examples:
1. Standard faces

![Step3.1](https://imgur.com/dvi5OTN.png)

2. GP-01 Faces

![Step3.2](https://imgur.com/gW9mWSy.png) 
-	Remember this material order I told you to be careful about?
That’s the number you see above each .mate, so be very careful to match each .mate number with the proper material

![Step3.3](https://imgur.com/rZdpo7s.png) 
-	Do not forget to change any relevant info like model name/icon/description and save.
-	You can edit any of those .mate to your liking. Just do not touch the StencilID part.
-	Try your new face in game, be sure to check blush or shade as they are the most likely to be broken if you messed up along the way.
-	Use NPR sample hair color preset or make a haircolor.menu with your own settings.

### Notes:
-	It is possible to change the transparency amount of the hair with the color alpha value of _NPRMAT_NPRToon_Hair_OutlineTex_StencilRead2_.mate
-	AccEx can’t read NPR specific .mate, so you won’t be able to change any values in game.
-	Some hair mods don’t include all available color preset, you’ll have to edit their .menu.
-	Like any NPR shaders, stencil is applied once and will not be removed unless you select another color preset and change the hair model.
- If you change the shader name inside .mate you'll probably have to make your own .pmat 
- Feel free to ask for help on Discord.
