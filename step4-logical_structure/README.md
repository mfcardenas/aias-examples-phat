# Preparing the scenario to be added to the simulation

---
### Create Logical Entities
---

Define the logical entities

In the previous step, a JME3 project was created to edit the properties of the house that has been modelled. It is necessary to create a structure of nodes that allows organizing all the elements that exist inside the house: furniture, walls, decorations, etc..

The objective of this step is to position in space (coordinates) all the objects in the scenario that are grouped in each area, for example:

<table>
<tr>
<td>
<b>LivingRoom</b><br>
- Sofa<br>
- TV<br>
- Table1<br>
- Chair1<br>
</td>
<td>
<b>Kitchen</b><br>
- Table2<br>
- Sink<br>
- Chair2<br>
- Refrigerator<br>
</td>
</tr>
</table>

This step is necessary to identify the cue points by which each object can be accessed. In the same way, other important points should be established such as the centre of the object, the access points, the light point and the perimeter.

#### Center
The centre of the object is a reference point that defines, as its name indicates, where the midpoint of the whole object is.

#### Access point
Access points are the coordinates that allow access to an object. In the case of a chair, the access point is unique and indicates where you can access it to sit. On a table, the access points will be all those points so you can get close to the table. On a sofa, each station will have an access point.

#### Perimeter
The perimeter is all the points that encompass an area. A square room will be made up of four endpoints. A less uniform room will have as many points as angles between walls.

#### Light points
The light points attribute to each area the location of the light in case it is activated on stage. It is very similar to artificial home lighting and represents the position of the bulb that illuminates the room.

Here's how to set the position of the objects.

- <b>Logical Entities</b>
    - SpatialCoordenates
        - <i>[NameArea]</i>
            - Center
            - Lights
            - Perimeter
                - P1 (point position)
                - P2 (point position)
                - ...


## Set the coordinates in the nodes

- Select the node, for example the center node.

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/jme3/img_selected_point.png" width="40%" heigth="40%" alt="Selected Point Node" style="border: 1"/>
</p>

- On the stage, double-click on the point where you want to position the center.

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/jme3/img_step_oi_position.png" width="70%" heigth="70%" alt="Point in scenario" style="border: 1"/>
</p>

- Move the course to this point with the "move selected item to cursor" button.

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/jme3/img_selected_buttom.png" width="50%" heigth="50%" alt="Buttom Move cursor" style="border: 1"/>
</p>

- Observe how the simple green date is exchanged for a three-axis point on the plane.

<table>
<tr>
<td>
<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/jme3/img_step_i_position.png" width="70%" heigth="70%" alt="Point in scenario" style="border: 1"/>
</p>
</td>
<td>
<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/jme3/img_step_ii_position.png" width="70%" heigth="70%" alt="Point in scenario" style="border: 1"/>
</p>
</td>
</tr>
</table>
<p align="center">
</p>

- Save your change.

## Generate NavMesh (Navigation Mesh)

The navigation mesh is an important element within the scene.  The meshes are areas drawn in the form of polygons that serve to visually mark the accessible areas within the scene. The marked areas tell the animated characters where it is possible to go and where it is not possible to go.

With the help of the JMonkey editor, the mesh is generated and added to the scenario. The steps to generate it are as follows:

- Right click on the Physical node
- Option "Add Spatial...", "NavMesh"
- Check that the mesh has been created in the scenario.
- Save your changes.

It is important that the screen connect all areas that are passable. In the case of areas that are passable but isolated from each other, the characters will not be able to walk around the stage.
In PHAT, isolated zones are not useful for positioning the character and do not activate Elder movement between different areas of the house.

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/jme3/img_generate_navmesh.png" width="70%" heigth="70%" alt="Point in scenario" style="border: 1"/>
</p>