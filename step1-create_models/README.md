# Create models

---
### Create the plane with SweetHome 3D
---
The first step is to create the scenario you want to use in the simulation. For this, it is necessary to use an editor that allows the construction of the scenario in an easy and fast way. The tool we use in this case is SweetHome 3D. In addition to being an open source, any user without any knowledge of modelling can use the tool.

The construction of the stage is a manual task that should be done by consulting information such as:
- Drawings or plans previews
- Pictures of the accessories contained in the drawings
- Photos of textures
- Measurements of the elements that exist in the scenario

Walls | Furniture | Decorations
--- | --- | ---
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/img_walls.jpg" width="300px" heigth="300px" alt="walls examples"/> | <img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/img_furniture_iii.jpg" width="300px" heigth="300px" alt="walls examples"/> | <img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/img_furniture_i.jpg" width="300px" heigth="300px" alt="walls examples"/>

Bedroom | Kitchen | Interactive Object
--- | --- | ---
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/img_bedroom.jpg" width="300px" heigth="300px" alt="walls examples"/> | <img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/img_kitchen.jpg" width="300px" heigth="300px" alt="walls examples"/> | <img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/img_objects.jpg" width="300px" heigth="300px" alt="walls examples"/>

The useful measurements of the scenario are as follows:
- Height, width and thickness of walls
- Height, width and thickness of furniture
- Height, width and thickness of moving objects

The objects on the stage can be classified into two groups:

- Objects whose only function is to <b>decorate</b> the environment
- <b>Interactive</b> objects that, in addition to decorating, can be interactive within the simulation: a door that opens, a chair that is moved by the user, a tap that opens, a light that lights up, etc.

Decorate | Interactive | Both
--- | --- | ---
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/img_decorate.png" width="300px" heigth="300px" alt="Decorate"/> | <img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/img_interactive.png" width="300px" heigth="300px" alt="Interactive"/> | <img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/img_both.png" width="300px" heigth="300px" alt="Decorate or Interactive"/>

This classification is necessary because for each interactive object it will be necessary to define a behaviour and qualities that the decorative objects will not have.
<i>In this first section we will only focus on the decorative objects and the construction of the staircase.</i>

#### Ausilioteca

Based on all the information gathered from the scenario, the next step is to build the plan that represents all the areas we want to include in the simulation.
To simplify this task, it is possible to create a foreground shot with only the basic structure of the stage: walls, doors, windows, floor and ceiling, without including any decorative or interactive elements.

In the case of the Ausilioteca, the result obtained is shown in the image below.

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/img_ausilioteca_10.png" width="70%" heigth="70%" alt="First Plan" />
</p>

In this foreground, it is possible to see all the important areas of the house: main entrance, living room, kitchen, corridors, bedrooms and other accesses.
For this first exercise, we will only use these areas of the house.

#### Summary

- Open Sweet Home 3D and build the initial plan of the Ausilioteca (or the scenario you want).
- Use the minimum amount of objects on the stage (doors, door frames, windows, etc.).

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/img_ausilioteca_01.png" alt="Ausilioteca" width="70%" heigth="70%"/>
</p>

- The work area of Sweet Home 3D is similar to the one shown in the following image.
<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/img_scenario_01.png" alt="Scenario" width="70%" heigth="70%"/>
</p>

## Export the Scenario

Finally, the entire scenario that has been modelled must be exported to a generic format. In this case, the format is "obj", which is a common format used by many modelling and animation applications.

In SH3D use the menu "3D view" and the option "Export to OBJ format".

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/img_export_obj.png" alt="Scenario" width="70%" heigth="70%"/>
</p>

This process does not generate a single file. You may even generate an image file containing the textures that have been applied to certain parts of the stage such as walls, floor or ceiling. All generated files must remain together.

In the directories of this step you will find:
- models/: the SweetHome3D work files with the basic plan of the house and the outside area.
- obj_export/: an export of the scenery in OBJ format.

At this point, you must have modelled the entire scenario and have the necessary files to create the simulation.

Congratulations!