# NFL-Computer-Vision
A custom computer vision model that identifies an offense's formation

This model takes in an all-22 image of an offense, pre snap, like the example below:

![wide_reciever 0028cdac-2188-11ee-b314-5a28ce701c8a copy](https://github.com/henrykra/NFL-Computer-Vision/assets/139408171/661355a5-24a7-40a6-a4e7-f2f408504c88)

Two models are applied to the image, one to detect the locations of the offensive players, and the other to detect the positions of the visible numbers in the image

Player detection:

![output1](https://github.com/henrykra/NFL-Computer-Vision/assets/139408171/ddfe77b0-33f0-461c-84ab-f3f5a1a632b3)

Number detection:

![output2](https://github.com/henrykra/NFL-Computer-Vision/assets/139408171/bd4d2e57-4683-4a1f-a333-ce4ed5201b0e)


Then, the model creates a section of the field using the locations of the numbers. The player locations are recorded in relation to the corners of the grid section. 

![output3](https://github.com/henrykra/NFL-Computer-Vision/assets/139408171/a08b11fb-fa17-40c9-a32b-1adf5f5ced47)

The script applies perspective transformation using the corners of the grid area to extract accurate locations of the players in comparison to the field

![output4](https://github.com/henrykra/NFL-Computer-Vision/assets/139408171/41ab7cf2-fa95-4a69-bcea-65f3687983ff)

Then using those locations, a diagram of the offense's pre snap alignment is created, similar to how it would be drawn up on a playbook

![output6](https://github.com/henrykra/NFL-Computer-Vision/assets/139408171/8955128c-6cc0-458e-bcb7-58bf63d3ec50)
