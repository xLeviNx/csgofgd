Located in steamapps\common\Counter-Strike Global Offensive\game\csgo, these are fixes for Counter-Strike 2 courtesy of users and Source2ZE

Some entities are missing from hammer .fgd files, but they can be made to work again after substituting them from CS:GO. These entities are:
filter_activator_team
env_sun - this entity will be removed in the near-future. The current alternative method used by Valve is to have a 'sun mesh' in the 3D skybox at a very far away distance from the map origin.
The following section will explain how to re-enable filter_activator_team.

The entity is missing in hammer from base.fgd. The .fgd for this entity can be copied directly from CS:GO .fgd, or alternatively can be copied from below:
@FilterClass base(BaseFilter) size(-8 -8 -8, 8 8 8) = filter_activator_team :
	"A filter that filters by the team of the activator."
[
	filterteam(choices) : "Filter Team Number" : 2 : "The team number to filter by.  If the filter mode is Allow, only entities whose "+
		"team number matches the given team will pass the filter. If the filter mode is Disallow, "+
		"all entities EXCEPT those whose team number matches the given team will pass the filter." =
	[
		2 : "Terrorist"
		3 : "Counter-Terrorist"
	]
]
For consistency, this block can be pasted in near other filter_* entities in the base.fgd. If you have no idea what this means and would rather play it safe, then place this block at the end of base.fgd.

Also added a fix for light_barn using color temperature instead of color. These are reflected in this file
