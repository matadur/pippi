# Ginger
_'Cuz gingers have freckles._

Basic command line tool for logging hours in [let's freckle](http://letsfreckle.com). Uses the excellent [freckle api bindings](https://github.com/tbranyen/nodefreckle) from the Node.js library created by Tim Branyan [@tbranyen](http://twitter.com/tbranyen)

## Setup
Currently you need to manually edit ./lib/cli.js and uncomment this line:
`// freckle( "<your subdomain here>", "<your token here>" );` modifying it with your subdomain and token.

## Use
```
Usage: ginger [command] [options]

[Commands]
list            List project associated with your subdomain.
                  ex: ginger list

log             Log time entries using various options.
                  ex: ginger log -p 101814 -m "quick update" -t 15m

[Options]
-h, --help      Display this help page.
                  ex: ginger -h

-t, --time      Time entry in freckle specified format.
                  ex: ginger -t 15m
                  ex: ginger -t 1.5h

-p, --project   The project ID.
                  ex: ginger -p 101814

-m, --message   Post a message to yammer
                  ex: ginger -m "I'm working on ginger"
                  ex: ginger -m "tag, tag, tag"

-d, --date      Optional date formated in YYYY-MM-DD. Defaults to today.
                  ex: 2012-07-20
```

## Todo
* I'd like to use a basic config tool that will keep variables like api-key, subdomand and email in a separate file.
* I'd like to be able to input a project name instead of id.
* I'd like to have tab completion for project names and tags.
