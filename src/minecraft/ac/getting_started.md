# Getting Started

## Installation
It's hard to get started with a library if you don't have it installed, so let's take care of that:

### Maven
To install AC in your Maven managed plugin, just insert these lines where appropriate, 
and update the version numbers:

```xml
<repository>
    <id>brettb-repo</id>
    <url>https://repo.brettb.xyz</url>
</repository>
```

```xml
<dependency>
    <groupId>xyz.brettb</groupId>
    <artifactId>ac</artifactId>
    <version>0.13.0</version>
    <scope>provided</scope>
</dependency>
```

### Gradle
Installing AC in you Gradle managed plugin is just as easy, insert these lines where they apply,
updating the version numbers when appropriate.

```Gradle
repositories {
    maven {
        name = 'brettb-repo'
        url = 'https://repo.brettb.xyz'
    }
}

dependencies {
    compileOnly group: 'xyz.brettb', name: 'ac', version: '0.13.0'
}
```

## Usage
Using AC in your plugin is also quite easy:

```java
package xyz.brettb.example;

import org.bukkit.ChatColor;
import xyz.brettb.ac.commands.CommandContext;
import xyz.brettb.ac.commands.CorePluginCommand;
import xyz.brettb.ac.commands.CorePluginCommandMeta;
import xyz.brettb.ac.plugin.CorePlugin;
import xyz.brettb.ac.plugin.CorePluginMeta;

// The prefix for chat messages
@CorePluginMeta(chatPrefix = "&l&8[&bAEX&8]&r")
public class example extends CorePlugin {

    @Override
    public void onModuleEnable() {
        // Register the command to the module
        registerCommand(new ExampleCommand());
    }

    // Example command definition
    @CorePluginCommandMeta(description = "Just an example", aliases = {"ex"})
    private static class ExampleCommand extends CorePluginCommand {
        public ApolloCoreCommand() {
            // Sets the command's name
            super("example");
        }

        // Called when the command is executed
        @Override
        public void handleCommandUnspecific(CommandContext ctx) {
            ctx.reply(ChatColor.translateAlternateColorCodes('&', getPlugin().getChatPrefix()) +
                    ChatColor.DARK_AQUA + " This is an example!");
        }

    }

}
```


## Help
If you need help with AC feel free to message me on Discord @ `apollo#9292`, or opening an issue on [GitHub][src]

## Further Documentation
At this time no further documentation exists, my best recommendation is to look at the [source code][src] and figure things out for yourself.
If you'd like to write better documentation for me, be my guest!    


[src]: https://github.com/GreatGodApollo/ac