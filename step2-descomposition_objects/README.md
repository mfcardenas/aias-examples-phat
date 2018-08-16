# Descomposition objects

---
### Define the objects that will participate in the simulation
--- 

#### Decorative objects or interactive objects.

The objects included on the stage can be decorative or interactive. The stage and the decorative and interactive objects can be built simultaneously, but it is recommended that the interactive objects be included after the stage base has been created.
 
This separation makes it possible to assign the interactive behavior of the objects, using the corresponding animation techniques.

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/img_step2_full_plan.png" width="80%" heigth="80%" alt="Full Plan"/>
</p>

### Create the scenario and the decorative objects
When the stage is created, the different elements that adorn it are embedded in it. As you can see from the picture below, all the furniture in the house has been put in place. The more detailed this process is, the more realistic the house used in the simulation will be. 

View 1 | View 2| View 3
--- | --- | ---
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/img_step2_full_view_i.png" width="300px" heigth="300px" alt="Full view 1"/> | <img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/img_step2_full_view_ii.png" width="300px" heigth="300px" alt="Full view 2"/> | <img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/img_step2_full_view_iii.png" width="300px" heigth="300px" alt="Full view 3"/>


#### The furniture
The initial installation of SH3D includes only a gallery of basic furniture. To expand this gallery, there are free resources that third parties make available for your use. 
In the section of <a href="http://www.sweethome3d.com/importModels.jsp" target="_blank">SweetHome3D Galleries</a>, you can find different collections of furniture that will allow you to decorate the house with the objects that exist in it.

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/img_sh3d_models.png" width="80%" heigth="80%" alt="models gallery"/>
</p>

#### Summary

- Open Sweet Home 3D and build the full plan of the Ausilioteca (or the scenario you want).
- The work area in Sweet Home 3D should be similar to the one shown in the following image:

<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/img_step2_scenario_02.png" alt="Full Scenario" />
</p>

## Exporting the Scenario

In SH3D use the menu "3D view" and the option "Export to OBJ format".
<p align="center">
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/img_export_obj.png" alt="Scenario" />
</p>
This process does not generate a single file. It is possible to generate one or more image files containing the textures that have been applied to certain objects on the stage, such as walls, floor or ceiling. All generated files must remain together.

In the directories of this step you will find:
- models/: the SweetHome3D work files with the basic plan of the house and the outside area.
- obj_export/: an export of the scenery in OBJ format.

<b>Note:</b><i> The map of the outside area has not been exported to the obj format because it is very large. Please generate it on your own computer by following the steps above.
</i>

At this point, you will have modeled the full scenario and will have the necessary files to create the simulation.

Congratulations!