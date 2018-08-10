## Create the plane with SweetHome 3D

---

The first step is to create the scenario you want to use in the simulation. For this, it is necessary to use an editor that allows the construction of this scenario in an easy and fast way. The tool we use for this case is SweetHome 3D. In addition to being open source, any user without any knowledge of modeling can use the tool.

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

All the objects on the stage can be clapped into two groups:

- Objects whose only function is to <b>decorate</b> the environment
- <b>Interactive</b> objects that, in addition to decorating, can be interactive within the simulation: a door that opens, a chair that moves the user, a tap that opens, a light that lights up, etc.

Decorate | Interactive | Both
--- | --- | ---
<img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/img_decorate.png" width="300px" heigth="300px" alt="Decorate"/> | <img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/img_interactive.png" width="300px" heigth="300px" alt="Interactive"/> | <img src="https://github.com/mfcardenas/aias-examples-phat/blob/master/assets/img/img_both.png" width="300px" heigth="300px" alt="Decorate or Interactive"/>

This classification is necessary because for each interactive object it will be necessary to define a behaviour and qualities that the decorative objects will not have.
<i>In this first section we will only focus on the decorative objects and the construction of the staircase.</i>