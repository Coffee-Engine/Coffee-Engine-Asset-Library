# Coffee Engine Asset Library!
The Coffee Engine Asset Library is a library of default assets that can be fetched and easily added to a project much like the ones of Scratch and Penguinmod.
For extension devs make sure to pack your extension

The different categories include

Sprites,
Materials,
Environments,
Models,
Sounds,
and Scripts

## Contributing
Before you start, you will want to create a folder for yourself in your own branch of the repo. If you are on the browser just create a new temporary text file.
Then you can go to the "creators.json" file in the root and add your name. In your creator folder add a file named "index.json".
You can view the "creators/DavidC" for an example creator folder.
### Sprites
Sprites can be in one of three formats “JPEG”, “PNG”, and “SVG”. Sprites made without those formats will have to be converted. Sprites must also have an open license. For some good examples look at [OpenGameArt](https://opengameart.org/) for a good example of how this is done. Another thing to look out for is sprite-sheet data! If your sprite has sprite-sheet data make sure to include it by using JSON instead of just a string
```json
{
  "spritePath":"sprites/myName/Sprite.png",
  "sheetData":"sprites/myName/Sprite.json"
}
```

###Materials
Materials Models and Shaders are undergoing changes to comply with the Sectorz branch of coffee's material system as it is much more managable and simple.

### Sounds
Sounds can be imported as "MP3", "WAV", or "OGG" file formats. You just have to specify the path to the sound file.

### Scripts
Scripts can be added by uploading the script file to your folder in any of the built-in script formats as of the 11th of January 2024, you can import Javascript("js"), Cappuccino("cappu"), and SugarCube("cescr") files. The language will be automatically processed by the file extension of the script. Please make sure your script doesn't have any easily encountered error cases and is made of a scriptedBehavior (SugarCube does this automatically). The script will also be scanned for security vulnerabilities due to the engine being scratch-like due to the block coding.

### Environments
Enviornments can be saved by going to the scene you want to save the environment of. This will save sun data, skybox data, fog, and particle data into one convenient file. All you need to do is specify the path.
