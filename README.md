Located in steamapps\common\Counter-Strike Global Offensive\game\csgo, these are fixes for Counter-Strike 2 courtesy of users and Source2ZE

Some entities are missing from hammer .fgd files, but they can be made to work again after substituting them from CS:GO. These entities are:
filter_activator_team
env_sun - this entity will be removed in the near-future. The current alternative method used by Valve is to have a 'sun mesh' in the 3D skybox at a very far away distance from the map origin.
Also added a fix for light_barn using color temperature instead of color. These are reflected in this file
