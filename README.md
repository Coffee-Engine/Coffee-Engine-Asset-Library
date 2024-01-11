# Coffee Engine Asset Library!
The Coffee Engine Asset Library is a library of default assets that can be fetched and easily added to a project much like the ones of Scratch and Penguinmod.

The different categories include

Sprites,
Materials,
Enviornments,
Models,
Sounds,
and Scripts

If you are looking to contribute a plugin or an extension go to the plugins and extensions repository! (When its open)

## Contributing
Before you start you are going to want to make a folder for yourself in your own branch of the repo. If you are on the browser just create a new temporary text file.
Then you can go to the "creators.json" file in the root and adding your name. In your creator folder add a file named "index.json".
You can view the "creators/DavidC" for an example creator folder.
### Sprites
Sprites can be in one of three formats “JPEG”, “PNG”, and “SVG”. sprites made without those formats will have to be converted. Sprites must also have an open license. For some good examples look at [OpenGameArt](https://opengameart.org/) for a good example of how this is done. Another thing to look out for is sprite-sheet data! If your sprite has sprite-sheet data make sure to include it by using JSON instead of just a string
```json
{
  "spritePath":"sprites/myName/Sprite.png",
  "sheetData":"sprites/myName/Sprite.json"
}
```

### Materials
Materials are slightly more complicated due to the nature of their creation. There are two formats materials a standard "JSON", and "STOREMAT",
"STOREMAT" materials can just use the path to the file while "JSON" materials have to have some JSON data associated with them. The big significance between "JSON" and "STOREMAT" is that JSON does not store image and shader data directly in the file. The first thing we want to establish is the shader and the path to the JSON data associated with the material.
```json
{
  "material":"materials/myName/material.json",
  "shader":"materials/myName/shader.shader"
}
```
for each assigned texture on a shader we can employ the tactic known as naming them.
```json
{
  "material":"materials/myName/material.json",
  "shader":"materials/myName/shader.shader",
  "textures" : {
    "myTexture":"materials/myName/myTexture.png"
  }
}
```
One good tip is to make a folder to store each material in so instead of using
```js
"materials/myName/material.json"
```
you would use
```js
"materials/myName/myMaterial/material.json"
```

### Models
3D models can be added in the "DEA", "GLTF", or "OBJ" file formats. "OBJ" files can also have accomponying "MTL" files.
Models have to be specified as a JSON object so we can store their materials and and model data together.
In the example below "override1" is the name of a material in the model.
```json
{
  "model":"models/myName/myModel/model.obj",
  "MTL":"models/myName/myModel/model.mtl",
  "override1":"models/myName/myModel/override.png"
}
```

### Sounds
Sounds can be imported as the "MP3", "WAV", or "OGG" file formats. You just have to specify the path to the sound file.

### Scripts
Scripts can be added by uploading the script file to your folder in any of the built-in script formats as of the 11th of January 2024, you can import Javascript("js"), Typescript("ts"), Lua("lua"), and SugarCube("cescr") files. The language will be automatically processed by the file extension of the script. Please make sure your script doesn't have any easily encountered error cases and is made of a scriptedBehavior (SugarCube does this automatically). The script will also be scanned for security vulnerabilities due to the engine being scratch-like due to the block coding.

### Enviornments
Enviornments can be saved by going to the scene you want to save the enviornment of. This will save sun data, skybox data, fog, andomniparticle data into one convienent file. All you need to do is specify the path.
