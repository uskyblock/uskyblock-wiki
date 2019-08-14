uSkyBlock has an API.

## Environment - Maven
First off, add the following to your `pom.xml`
```xml
<repositories>
  <repository>
    <id>ultimateskyblock</id>
    <url>https://www.uskyblock.ovh/maven/uskyblock/</url>
  </repository>
</repositories>
```
And in your dependency-section:

```xml
<dependency>
  <groupId>com.github.rlf</groupId>
  <artifactId>uSkyBlock-API</artifactId>
  <version>2.8.3</version>
</dependency>
```
Please check to make sure that you're using the latest release version (not ending in -SNAPSHOT).

## Environment - Gradle
Repository:
```gradle
repositories {
  maven {
    name "ultimateskyblock"
    url "https://www.uskyblock.ovh/maven/uskyblock/"
  }
}
```

Dependency:
```gradle
dependencies {
  compile "com.github.rlf:uSkyBlock-API:2.8.3"
}
```
Please check to make sure that you're using the latest release version (not ending in -SNAPSHOT).

If you are not using Maven or Gradle, grab the api-jar and put it in your classpath.

## Java Integration

Write some code along these lines:
```java
Plugin plugin = Bukkit.getPluginManager().getPlugin("uSkyBlock");
if (plugin instanceof uSkyBlockAPI && plugin.isEnabled()) {
  uSkyBlockAPI usb = (uSkyBlockAPI) plugin;
  player.sendMessage(String.format(
    "\u00a79Your island score is \u00a74%5.2f!", 
    usb.getIslandLevel(player)
  ));
}
```

## Event Integration
uSkyBlock fires events when it detects changes to the model, so if you want to integrate using the events, instead
of polling, you are welcome.

```java
/**
 * Listener for catching uSkyBlock Events
 */
public class uSkyBlockListener implements Listener {
    private static final Logger log = Logger.getLogger(uSkyBlockListener.class.getName());

    @EventHandler
    public void uSkyBlockEvent(uSkyBlockEvent e) {
        log.log(Level.INFO, "Received uSkyBlockEvent: " + e);
        if (e.getAPI() != null && e.getAPI().isEnabled()) {
            // Access API
        }
    }

    @EventHandler
    public void uSkyBlockScoreChangedEvent(uSkyBlockScoreChangedEvent e) {
        log.log(Level.INFO, "Received Score-Change Event: " + e);
        IslandScore score = e.getScore();
        if (score != null) {
            // Do some magic here
        }
    }
}
```

## Javadocs
Javadocs for the latest uSkyBlock-API release are available [here](https://www.uskyblock.ovh/javadocs/release/uSkyBlock-API/).
