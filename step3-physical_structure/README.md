# Preparing the scenario to be added to the simulation

---
### Create JME3 project
---

JMonkey IDE as well as eclipse, netbeans or intellyJ, need their projects to have a certain structure to work with them. In the case of JMonkey, to work with modeled objects, scenes or animations, it is necessary that the project has the structure of a JME3 type project. When you create a new project of this type, the editor creates the structure necessary to work with all these objects.

Here's how, through a temporary use project, we can edit the previously created scene to include all the attributes you need to interact with the simulation.
    
- Create new project of category: JME3 and BasicGame, Next.

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/jme3/img_create_project_i.png" width="70%" heigth="70%" alt="Step 1: Create Project"/>
</p>

- Use the default project name. If you wish, change the location of the project but remember that it will only be for temporary use.

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/jme3/img_create_project_ii.png" width="70%" heigth="70%" alt="Step 2: Set Name Project"/>
</p>

- Note the structure of the project created. The directory of interest is the <i>assets/Scenes/</i> directory.

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/jme3/img_project_i.png" width="70%" heigth="70%" alt="Step 3: Review Content of the Project"/>
</p>

- From the file browser, copy all files generated with SH3D (Export to obj format) into the <i>assets/Scenes/Houses</i> directory.

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/jme3/img_copy_obj_file.png" width="70%" heigth="70%" alt="Step 3: Copy Content of the Project"/>
</p>

- Return to the JMonkey editor and refresh the project content. You can now view the previously copied files.

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/jme3/img_refresh_project.png" width="70%" heigth="70%" alt="Step 3: Refresh view in IDE"/>
</p>

- Try to open the file <i>'.obj'</i>. The editor will generate an equivalent file with its own format, whose extension will be <i>'.j3o'</i>.

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/jme3/img_generate_j3o.png" width="70%" heigth="70%" alt="Step 3: Generate j3o"/>
</p>

<b>Warning:</b> <i>Whenever you try to open the".obj" file, the editor will create the "j3o" file. Once created, copy the".obj" file to another directory to avoid generating the".j3o" file again and losing any modifications you make.</i>

- Open the created <i>".j3o"</i> file.

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/jme3/img_open_j3o.png" width="70%" heigth="70%" alt="Step 3: Open j3o file"/>
</p>

- Activate the light point to see the imported scenario.
- Display the <i>"Grid"</i> to size the position of the house.

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/jme3/img_config_ide.png" width="70%" heigth="70%" alt="Step 3: Use j3o file"/>
</p>

- Use the central button of the mouse to zoom in and out of the house. Use the left click to rotate the house and the right click to move it. If not, use the next buttons: Move, Rotate and Scale respectively.

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/jme3/img_option_ide.png" alt="Modify object in scenario"/>
</p>
    
---
### Resizing the model
--- 

When the scenario was built, a certain scale was used for the size of all the objects in the scenario. All these objects will now become part of the simulation environment so their scale will have to correspond with the scale of the other elements of the framework.

To comply with this part, the scenario that we included in JMonkey will have to be resized and brought to a standard size. The "Scale" option allows you to resize the entire scenario quickly. 

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/jme3/img_escalado_i.png" width="70%" heigth="70%" alt="Scale object in scenario"/>
</p>

When resizing the house, the size of the GRID must be taken into account to represent the size of the house. That is, the house owes the same or a smaller area than the GRID in the space.

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/jme3/img_escalado_ii.png" width="70%" heigth="70%" alt="Scale object in scenario"/>
</p>

This would be the ideal size of the house.

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/jme3/img_escalado_iii.png" width="70%" heigth="70%" alt="Scale object in scenario"/>
</p>

---
### Defining a physical structure
--- 

After setting the size of the house, the next step is to describe the composition of the stage and each of its internal areas, for example, living room, kitchen, bedroom, bathroom, etc.

Each of these areas must be tagged and represented by a spatial node. Nodes are entities on which some representation of an object or part of it hangs in the general space of the scene. All nodes hang from a top node.

To organize this whole hierarchy of nodes, in the scene explorer window, it is necessary to define three main nodes on which all the following nodes will hang. These three nodes are:

- Physical Entities (PhysicalEntities)
- Logical Entities (LogicalEntities)
- Structure  (Structure)

### Physical Entities
The physical entities group together the areas that make up the house. Each area of the house must have a node that represents it. Later, within each child node, the elements that compose or are part of the area will be grouped together, for example, Room: Sofa, Chair, Table, Television, etc.

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/jme3/img_structure_node_i.png" alt="Structure Node"  style="border: 1"/>
</p>

### Logical Entities
Logical entities also group together the areas that make up the house. Each area of the house must have a node that represents it. Just like the physical entities, in each area, you must define child nodes that group the elements that makeup or are part of the area, for example, Room: Sofa, Chair, Table, Television, etc.
Unlike physical entities, logical nodes indicate the points or coordinates in the plane where these areas and elements are located. These coordinates are the reference of where each element is and where it is located throughout the space.

The structure required for this node is as follows:

LogicalEntities
- SpatialCoordenates
    - [NameArea]
      - Center
      - Lights
      - Perimeter

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/jme3/img_structure_node_ii.png" alt="Structure Node" style="border: 1"/>
</p>

The creation of the logical nodes will be explained in the next step.

### Structure

All the objects that make up the house hang from this node.  When you want to assign a specific animation or behavior to an element, it must be moved to the physical entities node.
All other objects must be organized in the following node structure:

- Structure
    - Physics
    - Visual
    
<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/jme3/img_structure_node_iii.png" alt="Structure Node" style="border: 1"/>
</p>

### Create nodes of type Spatial

In the scene explorer window, place the cursor on the parent node and right-click on the "Add Spatial..." and "Node" options.

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/jme3/img_structure_node_iv.png" alt="Structure Node" style="border: 1"/>
</p>