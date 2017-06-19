## Favorites

Plugin for [fman.io](https://fman.io) that gives you the ability to setup a list of favorite directories to go to.

Install by uploading "Favorities" to your [data directory](https://fman.io/docs/customizing-fman)`/Plugins/ThirdParty`.

After restarting **fman**, you will have the ability to set favorite directories, go to them, set path shorteners, remove path shorteners, and remove favorites.

### Usage

#### HotKeys Set

<Shift+f>  - Set a new Favorite directory

<Ctrl+f> - Remove a Favorite Directory.

<Ctrl+0> - Go to a Favorite Directory.

#### Commands

`Go To Favaorite` - This command will display a list of favorites by their assigned names for the user to choose from. As you type letters in the name, the list is shortened. Once one is selected, the current panel is moved to that directory.

`Remove Favorite Directory` - This command will remove the selected favorite directory.

`Set Favorite Directory` - This command sets the currently highlighted directory as a favorite. If the path contains a shortener's path, then it will be shortened to that shorener's name in double brackets.

`Set Shorten Directory` - This command asks the user for a shortener name and creates a new shortener to that directory.

`Remove Shortener Directory` - This command removes a shortener directory from the shortener list. It then expands the shortener in all the favorites that had that shortener.

#### Files Created and Used

`~/.favoritedirs` - This file contains all of your favorite directories. Each line is the assigned name, a "|" symbol, and the path to the directory. If the path contains a directory in the `~/.shorenerdirs` file, then the path is removed and a placeholder is inserted instead.

`~/.shortenerdirs` - This file contains all the shortener directories and their names. It is in the same format as the `~/.favoritedirs` file. Once you create this file, copy it to your Dropbox location and link it back to this location. Now you can share your favorites between systems.

#### Suggested Usage

Once you install the plugin, set up your shortener directories. I setup one for each of my Dropbox locations. Then, create your favorites in the shorteners subdirectories. Once you have the favorites setup, move your `~/.favoritedirs` to your Dropbox location you want and  link to the original location and name. On the second system, setup the same shortener file using the same names and link the synced favoritedirs file to the normal location. Now you can go to the favorite directories inside these shortener directories easily! They also automatically update when you add new ones.

### Features

- The ability to set a favorite directory.
- The ability to go to a favorite directory.
- Remove a favorite directory.
- Set up directories as shorteners with a name. Then all paths under that directory will be set to the shortener's name and expanded to that path when going to it. This gives the ability to share favorites between system just using the paths in common.