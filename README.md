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
Sprites can be in one of three formats jpeg png and svg. sprites made without those formats will have to be converted. Sprites must also have an open liscense. For some good examples look at [OpenGameArt](https://opengameart.org/) for a good example of how this is done. Another thing to look out for is spritesheet data!. If your sprite has spritesheet data make sure to include it by using json instead of just a string
```json
{
  "spritePath":"sprites/myName/Sprite.png",
  "sheetData":"sprites/myName/Sprite.json"
}
```
