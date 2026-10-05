# Blender Car Suspension Animation with Spring Physics

This project provides a reusable Blender Python script that automatically builds a car suspension system with spring physics and tests it on procedurally generated rough terrain.

## Features

- Automatic car assembly with body, wheels, and suspension mounts
- Spring-based rigid body suspension setup using Blender physics
- Rough terrain generation with adjustable amplitude and seed
- Animation workflow that tests the car over uneven ground
- Reusable script that can be customized for different vehicle dimensions and stiffness values
- Simple setup for Blender users without requiring a model library

## Requirements

- Blender 3.0 or newer
- Python included with Blender
- 3D viewport enabled

## Files

- `car_suspension_setup.py` — builds the full scene automatically
- `README.md` — setup and usage instructions

## Quick Start

1. Open Blender.
2. Open the Scripting workspace.
3. Load `car_suspension_setup.py` in the Text Editor.
4. Click Run Script.
5. Press the Play button in the Timeline to view the suspension test.

You can also run it from the command line:

```bash
blender --background --python car_suspension_setup.py
```

## What the script creates

The script creates:

- A car chassis body as a cuboid
- Four wheel meshes and wheel assemblies
- Suspension arms and spring-like connection points
- A rough terrain mesh with displaced height variation
- Rigid body and constraint settings for suspension motion
- Animated motion to test the car traversing the terrain

## Customize the setup

At the top of `car_suspension_setup.py`, adjust settings such as:

```python
CAR_LENGTH = 4.0
CAR_WIDTH = 2.0
CAR_HEIGHT = 1.2
WHEEL_RADIUS = 0.45
WHEEL_WIDTH = 0.25
TERRAIN_SIZE = 30
TERRAIN_ROUGHNESS = 0.8
SPRING_STIFFNESS = 120000
SPRING_DAMPING = 0.8
```

These values affect:

- vehicle proportions
- wheel size and ground clearance
- terrain bumpiness
- stiffness and motion damping of the spring setup

## Animation workflow

The script is designed as a practical animation workflow:

1. Generate terrain and vehicle parts
2. Add suspension constraints and wheel collisions
3. Add keyframes for forward motion and wheel rotation
4. Simulate/preview the car traversing rough terrain
5. Render the animation from the camera

## Terrain generation

The terrain is generated procedurally using a height field. The roughness and scale can be tuned for:

- mild road undulation
- rocky trail testing
- rough off-road conditions

## Notes

This is intended as a reusable, script-driven Blender scene builder rather than a physically exact full vehicle simulation. It prioritizes a fast setup and clear animation behavior that can be iterated quickly in Blender.

## Troubleshooting

- If the wheels sink too far into the terrain, increase the wheel radius or raise the car body slightly.
- If the suspension bounces too much, increase damping.
- If the car falls through the terrain, make sure the terrain object has collision settings enabled.
- If the animation is too slow or too fast, adjust the frame range or keyframe spacing in the script.

## Suggested next steps

- Add a follow camera
- Add wheel steering animation
- Increase realism with more detailed suspension links
- Export a render sequence for presentation or review

---

This project is ready to be expanded into a more advanced Blender suspension rig or a more physically accurate rigid-body setup.
