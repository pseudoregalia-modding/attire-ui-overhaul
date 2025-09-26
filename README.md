<h1 align="center" id="title">Attire UI Overhaul</h1>

This Mod reworks the default Attire UI to contain a live view of Sybil and the outfits you've unlocked for her. Added features include the ability to change the Dream Breaker model and change the colour of the dash.
  
<h2>Attire UI Overhaul Features</h2>

*   Reworks the Attire Menu
*   Allows for modded outfits
*   Allows for modded weapon skins
*   Allows for dash color to be customized

<h2>WeaponMesh DataTable & TestActor Plugin</h2>

The Plugin, which can be found [Here](https://www.nexusmods.com/pseudoregalia/mods/8) under `WeaponMesh DataTable and TestActor` in Misc, lets weapon modelers visualize the changes made to the weapons transform for custom weapons that don't conform to the Dream Breaker's tonfa design.

<h3>Installing the plugin</h3>

This plugin contains 'ST_WeaponData' (which is a Data Structure that I've created.) and 'TestActor' (Which is a blueprint actor that helps visualise your custom weapon and light transform data.)

To install the WeaponData Struct and TestActor into your project, I have packed it as if it were a plugin.

<h4>Install Process:</h4>

1. Copy the `WeaponMeshData` folder contained in the zip into the unreal engine plugins folder. By default, this is located here: `C:\Program Files\Epic Games\UE_5.1\Engine\Plugins`
2. In your project you'll need to search for the plugin in the plugins page, enable it and then click restart when it says to.<br>
![image](https://github.com/pseudoregalia-modding/attire-ui-overhaul/assets/102454745/78c8c780-70b4-4e8c-9634-d13a7272b209)
3. To make the struct and blueprint actor visible, on the file content browser in the right hand side, you can see a settings option. In that settings menu, select `Show Engine Content` and `Show Plugin Content`<br>
![image](https://github.com/pseudoregalia-modding/attire-ui-overhaul/assets/102454745/27779ca4-c205-4837-b026-7398134fa3ab)

<h4>DataTable Instructions:</h4>

1. Search for `ST_WeaponData` in the content browser. This will be found in `Plugins/WeaponMeshData/Content/Data/Structs`. Copy that file into the following folder in your project: `Content/Data/Structs`. If this folder doesn't exist, you'll need to create it.
2. Create A DataTable in the following directory: `Content/Data/DataTables`. (DataTables can be found in the miscellaneous tab, make sure it is a DataTable and NOT a Composite Table) If the required folder doesn't exist, you'll need to create it. You will need to name the DataTable with the naming convention DT_WeaponData_My_Custom_Weapon (please rename the "My_Custom_Weapon" to a unique name, preferably the name of your mod/weapon so that other mods don't clash)
3. Inside the Table, Add a new row and give that row a custom name, then add a name, link to your weapon mesh, and the two transform values are the important values. These will let you rotate and transform the weaponMesh and lightMesh in the UI and when thrown. For scaling, the default values for weaponMesh is 1,1,1 and the default for Light mesh is 0.25,0.25,0.4. To test these values without having to pak and run the game, you can use the TestActor to test out different transform values.

<h4>TestActor Instructions:</h4>

1. Search for `TestActor` in the content browser. This will be found in `Plugins/WeaponMeshData/Testing`. You should not make a copy of this and instead open the actor by double clicking.
![image](https://github.com/pseudoregalia-modding/attire-ui-overhaul/assets/102454745/6b878b84-5e19-43f2-9641-7abaad500e2b)
2. When you first open the TestActor, you'll see the `EventGraph`, we want to be in the `Viewport` tab. You can see these tabs at the top of the window.
![image](https://github.com/pseudoregalia-modding/attire-ui-overhaul/assets/102454745/6cc0e341-840f-42fe-a6a2-ba6153dcc524)
3. Once you have opened the `Viewport` tab, you'll see two scenes, the Dreambreaker as it's seen in the UI, and Sybil holding the Dreambreaker with a light effect equivalent. These will be used to test your weapon and custom transforms.
4. On the left you'll see a drop down labelled `VARIABLES`. In the variables tab you'll see four values, these are the only things you'll need to change. Everything else can be thought of as read only.
5. When highlighting a variable, you'll see options to modify it on the right hand side of the window. The only thing you will need to touch is the `Default Value` drop down, here you can see the transform/mesh/boolean to change. Changes to these values will directly effect the center display.
![image](https://github.com/pseudoregalia-modding/attire-ui-overhaul/assets/102454745/845aacae-6774-4c63-87a6-610d8e6b682b)

<h4>Variables:</h4>
<pre>
WeaponMesh            - Assign your custom weaponMesh to see how it will display both in the UI and the player's hand.
CustomWeaponTransform - UI Representation of the weapon, making transforms to the placement of the weapon.
CustomLightTransform  - Light mesh on the held weapon, making transforms to the placement of the weapon's light.
UIView?               - UI has the weapon rotated and slightly slanted by default,
                        switching this value to false will set a straight vertical representation of the mesh.
</pre>
