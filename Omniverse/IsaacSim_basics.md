# IsaacSim Basics

## Useful resources
- [IsaacSim Documentation Page](https://docs.isaacsim.omniverse.nvidia.com/latest/index.html) 
- [Omniverse Materials Workflows](https://docs.omniverse.nvidia.com/materials-and-rendering/latest/materials_workflows.html)

## Scene Creation

### Adding assets into a scene as reference
Assets imported as reference are present in the scene but any change you make on them is not reflected on the original asset.\
Follow this procedure to import an asset as a reference:
1. Select an xForm which will be the parent for the new asset.
2. Create a new child xForm: _Right click -> Create -> xForm_.
3. (Optional) Give a name to the new xForm.
4. Right click on the new xForm and do: _Add -> Reference_.
5. Look for the asset you want to import, click on it and then click on _Select_. The asset will be imported as a reference under the xForm you created.

### Adding semantic class to an prim
1. Select the prim you want to assign the semantic class to (recommended to select a Mesh prim).
2. Go to "Semantics Schema Editor" (if not present, check within the Replicator tab on the top bar).
3. As "New Semantic Type" write "class".
4. As "New Semantic Data" write the name of the class you want to use.
5. Once ready, click on "Add Entry On All Selected Prims".

### Manually setting a pose for a human asset
1. Activate "SKELETON JOINT" extension within IsacSim.
2. Now, when you select a "Skeleton" prim, you should be able to see a new tab in the "Property" section named "Animation and Pose Modes".
3. In that tab, select "Rest Pose".
3. Expand the Skeleton prim to reach the articulations you want to translate/rotate.
4. Rotate and translate the articulations as you wish.
5. Go back to the Skeleton prim and, inside the "Animation and Pose Modes" tab, press the "Save" icon next to "Rest Pose".
6. The pose you set is now saved and the human asset will keep that pose.

## Scripting

### Run IsaacSim from Python script (headless mode) - Windows
1. Identify the location of IsaacSim executable in your pc (you can check from Omniverse launcher).
2. Check that inside the same folder there is a file named _python.bat_.
3. Run your python script to launch IsaacSim in headless mode:
    
        .\python.bat <path_to_your_python_script>

