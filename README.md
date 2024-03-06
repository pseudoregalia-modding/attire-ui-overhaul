<h1 align="center" id="title">Attire UI Overhaul</h1>

<p id="description">This Mod reworks the default Attire UI to contain a live view of Sybil and the outfits you've unlocked for her. Added features include the ability to change the Dream Breaker model and change the colour of the dash.</p>

  
<h2>Attire UI Overhaul Features</h2>

*   Reworks the Attire Menu
*   Allows for modded outfits
*   Allows for modded weapon skins
*   Allows for dash color to be customized

<h2>WeaponMesh DataTable & TestActor Plugin</h2>
<p>The Plugin, which can be found <a href="https://www.nexusmods.com/pseudoregalia/mods/8?tab=files&file_id=151">Here</a>, lets weapon modelers visualize the changes made to the weapons transform for custom weapons that don't conform to the Dream Breaker's tonfa design.</p>

<h3>Installing the plugin</h3>
<p>
  Installing the plugin will require manually moving the unzipped "weaponMeshData" Folder. <br>
  This can be achieved by following these steps:
</p>

1. Find your project folder (e.g. "C:\Users\USER\Documents\Unreal Projects\pseudoregalia\Plugins") and paste the unzipped folder there.
2. Open the Unreal project and click the Settings dropdown in the top right hand corner, then select "Plugins"
![image](https://github.com/Foe-Hammer/Attire-UI-Overhaul/assets/102454745/0fe651bb-d52f-4ed5-b4f8-ccec93a82556)
3. In the Plugins menu, search for "WeaponMesh" and enable the plugin. The editor will prompt for a restart.
4. After restarting, navigate to the Content browser and select the settings icon on the top right hand side of the window.
5. Enable the following setting labelled "Show Plugin Content"<br>
![image](https://github.com/Foe-Hammer/Attire-UI-Overhaul/assets/102454745/7a5b20f3-de07-4c9a-acc2-8107c9470e3d)

<h3>Using the plugin</h3>
<p>To use the plugin, navigate to the TestActor located in "WeaponMeshData/Testing"</p>

![image](https://github.com/Foe-Hammer/Attire-UI-Overhaul/assets/102454745/1f898c29-d63c-47f9-95a5-aadd24fc1758)

<p>
  Here you'll find the test scenario that, by default, displays the Dream Breaker and its Transform. <br>
  To Modify the display for your custom setup, you will only need to change the variables visible within the blueprint actor's Viewport Tab seen here.
</p>

![image](https://github.com/Foe-Hammer/Attire-UI-Overhaul/assets/102454745/da1748f3-cdc2-468e-b35c-4b56cbf36f92)
<p>
  The Details panel on the right can be ignored unless a variable has been selected.<br>
  These four variables will dynamically update the scene to show changes as you make them.
  To update a variable, simply select the thing you want to change and change the "Default Value" to reflect the desired change. <br>
  For example if you wanted to change the Dream Breaker to your custom mesh, simply select the variable on the left, and then select the dropdown on the right to change it to your custom mesh like so.
</p>

![image](https://github.com/Foe-Hammer/Attire-UI-Overhaul/assets/102454745/2e938d9b-3f87-438c-9d2d-134668abbd41)
