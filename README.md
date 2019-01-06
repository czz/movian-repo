# movian-repo
movian repository


How to publish plugins

Starting with Movian 6.0 supports multiple feed of plugins. For more information how to add new feeds to Movian see this article.

Note: There is no longer a central plugin repository hosted at this site. See this article for more info

The easiest way to publish plugins is to commit each of them to a public repo at github.

See https://github.com/andoma/movian-plugin-modarchive for an example how this should look.

Then you can use the movian-repo tool found at https://github.com/czz/movian-repo to generate plugin feeds.

Currently this tool only work with github hosted plugins.

Edit a text file called repos.txt and fill it with one github repo name per line, for example:

/andoma/movian-plugin-sidplayer
/andoma/movian-plugin-xmpplayer
/andoma/movian-plugin-gmeplayer
/andoma/movian-plugin-modarchive

Run it like this:

python build.py -i repos.txt -o repo.json

Then you can upload this file on github pages or host it in any way you like. Then give the URL to your users.
