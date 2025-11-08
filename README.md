# SF2-Global-Fog
Fog it up when a boss spawns in.

Requires:
Slender Fortress 2 Modified - 1.8.0 Alpha 2 branch (https://github.com/Mentrillum/Slender-Fortress-Modified-Versions/tree/1-8-0-rewrite)

CBaseNPC (https://github.com/TF2-DMB/CBaseNPC)

How to use:
Place this into your scripting folder in addons/sourcemod in the server files
Compile with a compiler of your choice. I personally use Visual Studio Code
After this is compiled, the "global_fog" section will work with bosses. Documentation is below.

TODO:
Make a branch for 1.9.0 Alpha (1-8-0-alpha-3)

DOCUMENTATION

    "global_fog" // Section in a boss config. Most of these keyvalues mirror the options in env_fog_controller. All keyvalues seen here are their default values
    {
        "start" "1000.0" // How far away it starts
        "end" "1500.0" // How far away it reaches max density
        "density" "0.75" // Max density for the fog. Decimal percent, 0.75 = 75%
        "color_primary"    "255 255 255 255"
        "color_secondary" "255 255 255 255"
        "blend" "0" // Enables color blending in planar-based fog
	    "direction" "0 0 0" // Vector which the viewcam is checked against for blend colors
        "farz" "-1" // Anything beyond this distance is not rendered. -1 means no change in existing farz setting
	    "radial" "1" // Use radial fog added in a 2025 update. This is enabled by default
        "custom_sky_name" "" // This is set to nothing (no change in skybox) by default. If this is set, make sure to also add the corresponding downloads in "mat_download"
    }

