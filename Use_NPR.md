# How to use NPR in your Mods
## Requirements
I will not cover elements common with the basic part of modding  
As a result, you will need to know and understand, before proceeding;
- How to reference a .mate inside a .menu
- How to edit a .mate
- What Hair/Trans/OutlineTex/CutoutAtC default shaders are
- What a .tex is
- For more advanced shader options you'll need to know what RGB and Alpha channels are

This is an archive with all NPR's .mate templates translated for better understanding
## The Basic of NPR
■ Adding any NPR .mate on a COM model isn't much different than using .mate in a classic situation.  
- Prepare your .model with material neatly sorted  
- Reference the corresponding .mate in your .menu  

The main difference is the way the .mate will be named.  
Indeed, the plugin side of NPR uses the .mate (rather long) suffixes to know which one of the shaders NPR proposes you're trying to load.  

Let's take this .mate name:```MyAwesomeMaterial_NPRMAT_NPRToonV2_.mate```  
The suffix in this case is:```_NPRMAT_NPRToonV2_```  
If you downloaded the .mate template archive, you'll see that the freely editable part is between **{ }**  
**Each NPR shader has its own suffix and it MUST be respected**  

- ```MyAwesomeMaterial_NPRMAT_NPRToonV2_UnlitReflection_OutlineTex_.mate``` is a valid file.  
- ```MyAwesomeMaterial_NPRMAT_NPRToonV2_UnlitReflection_OutlineTex_2.mate``` is NOT valid.  
- ```_NPRMAT_NPRToonV2_UnlitReflection_OutlineTex_MyAwesomeMaterial.mate``` is NOT valid either.

**Failure to abide by this simple rule will make this .mate ignored by the plugin and NPR effects not applied.**
  
  
■ Infos inside NPR .mate are edited in exactly the same way and with the same tools as classic .mate  
■ NPR has an UI that works almost in the same way as AccEx, simply click the NPR icon in your gear menu, and preview your changes before copying them in your .mate
■ I advise you to know in advance what shader you'll need

## NPR Shader Types
You'll notice soone enough that suffixes are logical and will be able to know which one you want on a glimpse

#### NPR version of classic shaders
I almost feel I don't need to explain those, they are your classic COM shaders but with added NPR settings (see bellow).  
Probably the ones you'll use most often.
```_NPRMAT_NPRToonV2_```  
```_NPRMAT_NPRToonV2_OutlineTex_```  
```_NPRMAT_NPRToonV2_Hair_```  
```_NPRMAT_NPRToonV2_Hair_OutlineTex_```  
```_NPRMAT_NPRToonV2_Trans_```  
```_NPRMAT_NPRToonV2_CutoutAtC_```  

#### Advanced shaders
```_NPRMAT_NPRToonV2_Emissiv_```  
This one and its variations are used when you want to animate the emission map, it's not required if you want a simple emission.  
```_NPRMAT_NPRToonV2_Fabric_```  
This one and its variations is supposed to give a better fabric feeling to the texture.  
```_NPRMAT_NPRToonV2_Reflection_```  
This one and its variation is to have a real time reflection  
```_NPRMAT_NPRToonV2_UnlitReflection_```  
Same as above, but unaffected by global lighting

#### Stencil shaders (AKA: gave up sanity)
This will need its own section, but you'll probably never use them, and if you do you'll be way above the understanding level this guide is meant for.
One common use is the hair transparency effect (which is a misnomer since it's not transparency at all)  
```_NPRMAT_NPRToon_StencilWrite_```  
```_NPRMAT_NPRToon_StencilRead_```  

#### Depreciated shaders
```_NPRMAT_NPRToon_/OutlineTex_/Hair_/Hair_OutlineTex_/Trans_/CutoutAtC_```  
First shaders NPR came with, they are still compatible but you don't want to use them, better use the NPRToonV2 above

## Global NPR settings
**Those settings are common to every NPR shader**