## Installation
``npm install kinakoneko``

## Example(s)
**NodeJS:**
```javascript
// kinakoneko //
const kinakoneko = require('kinakoneko');

async function yourFunctionName() {

  // Get SFW Neko Images, uwu //
  console.log("SFW Neko: " + await kinakoneko.neko());

  // Get Lewd Neko (NSFW), owo //
  console.log("Lewd Neko:" + await kinakoneko.lewdNeko());

  // Lewd Bomb me onii-san~~ //
  console.log("Lewd Bomb: " + await kinakoneko.lewdBomb(5));

  // Get other NSFW Images //
  console.log("BDSM: " + await kinakoneko.nsfw.bdsm());
  console.log("Maid: " + await kinakoneko.nsfw.maid());
  console.log("Hentai: " + await kinakoneko.nsfw.hentai());
}

// Call your Function! //
yourFunctionName();
```

## Legacy Function(s)
Example:
```javascript
kinakoneko.function() // Format
kinakoneko.lewdNeko() // Example
kinakoneko.lewdBomb(5) // Meow, I'm Example 2
```
Function | Description
---|---
lewdNeko | NSFW Neko Girls (Cat Girls)
lewdBomb(n) | Sends (n) amount of lewds! :3

## SFW Function(s)
Example:
```javascript
kinakoneko.function() // Format
kinakoneko.foxgirl() // Awoo!~ Another example!
kinakoneko.neko() // Meow! An Example!
```
Function | Description
---|---
neko | SFW Neko Girls (Cat Girls)
foxgirl | SFW Fox Girls

## NSFW Function(s)
Example:
```javascript
kinakoneko.nsfw.function() // Format
kinakoneko.nsfw.hentai() // Example
kinakoneko.nsfw.feet() // Another Example
```
Function | Description
---|---
ass | I know you like anime ass~ uwu
bdsm | If you don't know what it is, search it up
blowjob | Basically an image of a girl sucking on a sharp blade!
cum | Basically sticky white stuff that is usually milked from sharpies.
doujin | Sends a random doujin page imageURL!
feet | So you like smelly feet huh?
femdom | Female Domination?
foxgirl | Girl's that are wannabe foxes, yes
gifs | Basically an animated image, so yes :3
glasses | Girls that wear glasses, uwu~
hentai | Sends a random vanilla hentai imageURL~
netorare | Wow, I won't even question your fetishes.
maid | Maids, Maid Uniforms, etc, you know what maids are :3
masturbation | Solo Queue in CSGO!
orgy | Group Lewd Acts
panties | I mean... just why? You like underwear?
pussy | The genitals of a female, or a cat, you give the meaning.
school | School Uniforms!~ Yatta~!
succubus | Spooky Succubus, oh I'm so scared~ Totally don't suck me~
tentacles | I'm sorry but, why do they look like intestines?
thighs | The top part of your legs, very hot, isn't it?
uglyBastard | The one thing most of us can all agree to hate :)
uniform |Military, Konbini, Work, Nurse Uniforms, etc!~ Sexy~
yuri | Girls on Girls, and Girl's only!<3
zettaiRyouiki | That one part of the flesh being squeeze in thigh-highs~<3

## Wallpaper Function(s)
Example:
```javascript
kinakoneko.nsfw.function() // NSFW Format
kinakoneko.nsfw.mobileWallpapers() // NSFW Example
```

Function | Description
---|---
kinakoneko.mobileWallpapers() | Fetch a random SFW Wallpaper! (Mobile)
kinakoneko.wallpapers() | Fetch a random SFW Wallpaper! (Desktop)
kinakoneko.nsfw.mobileWallpapers() | Fetch a random NSFW Wallpaper! (Mobile)
kinakoneko.nsfw.wallpapers() | Fetch a random NSFW Wallpaper! (Desktop)


## How to Resolve Promises
```javascript
// Just Calling my dear child, kinakoneko //
const kinakoneko = require('kinakoneko');

// Option 1, using and calling an asyncronous function //
async function yourFunctionName() {
  console.log(await kinakoneko.nsfw.maid()); // Output: Some weird long link that you probably will definitely try to open //
}

// Don't forget to call your function! //
yourFunctionName();

// Option 2, Using ".then" //
kinakoneko.nsfw.maid().then((imageURL) => {
  console.log(imageURL);
})
```


##
Discord Bot Example
```javascript
const Discord = require('discord.js');
const kinakoneko = require('kinakoneko');

// Create New Client //
const client = new Discord.Client();

// Bot Settings //
const settings = {
  prefix: "YOUR_BOT_PREFIX",
  token: 'YOUR_BOT_TOKEN'
}

// On "Message" Event! //
client.on('messageCreate', async (message) => {

  // Checks if message channel is NSFW! //
  if (!message.channel.nsfw) return message.channel.send('Sorry! Not NSFW Channel!');

  // Create New Embed //
  const embed = new Discord.MessageEmbed();

  // Defines Command //
  var command = message.content.toLowerCase().slice(settings.prefix.length).split(' ')[0];

  // Onii-chan, don't reply! //
  if (!message.content.startsWith(settings.prefix) || message.author.bot) return;

  if (command == 'lewdneko') {

    // For Embed //
    embed.setImage(await kinakoneko.lewdNeko());
    return message.channel.send({ embeds: [embed] });

    // For Plain Text //
    return message.channel.send(await kinakoneko.lewdNeko());

  } else if (command == 'maid') {

    // For Embed //
    embed.setImage(await kinakoneko.nsfw.maid());
    return message.channel.send({ embeds: [embed] });

    // For Plain Text //
    return message.channel.send(await kinakoneko.nsfw.maid());
    
  }

}


});
```

## Support
[DONATE](https://saweria.co/KazeDevID)
