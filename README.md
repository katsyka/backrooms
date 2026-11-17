# Backrooms

A first-person exploration game set in an endless maze of yellow rooms, written as a single HTML file with three.js.

## Gameplay

You wake up somewhere you shouldn't be. Explore the procedurally generated rooms, avoid the entity that hunts you, and find the exit door.

## Technical notes

- **Infinite world.** The level is generated in chunks around the player, so it never ends.
- **Lighting.** Ceiling lights come from a shader-driven lamp grid rather than real light sources, which keeps hundreds of lamps cheap to render.
- **Ambient occlusion.** Contact shadows are faked with decals.
- **Enemy AI.** The entity chases the player using breadth-first pathfinding through the maze.
- **No assets.** All textures, including the striped and patterned wallpaper, are generated in code.

## Running

The game is one file. Serve the folder over HTTP:

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

## Controls

| Key | Action |
| --- | --- |
| `W` `A` `S` `D` | Move |
| Mouse | Look |
| `Shift` | Run |
| Click | Lock the mouse pointer |
