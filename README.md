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
"STOREMAT" materials can just use the path to the file while "JSON" materials have to have some JSON data associated with them. The big signifigance between "JSON" and "STOREMAT" is that JSON does not store image and shader data directly into the file. First thing we want to establish is the shader and the path to the json data 
```json
{
  "material":"materials/myName/material.json",
  "shader":"materials/myName/shader.shader"
}
```
for each assigned uniform on a shader we can employ the tactic known as naming them
```json
{
  "material":"materials/myName/material.json",
  "shader":"materials/myName/shader.shader",
  "uniforms" : {
    "myUniform":[
      1,0,1,1
    ]
  }
}
```
