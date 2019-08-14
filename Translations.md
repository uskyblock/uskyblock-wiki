![uSkyblock-Revived](http://i.imgur.com/JbSV18m.png)

The uSkyBlock uses gettext for generating translations for different languages.

This tool helps us to keep track of strings within the source-code, and extracts them for translation.

# Translating to another language

* Copy the keys.pot file, and rename it to `<language-code>.po`
  * The latest `keys.pot` can always be found in [src/main/po/keys.pot](https://github.com/rlf/uSkyBlock/blob/master/uSkyBlock-Core/src/main/po/keys.pot)
  * The language-code is the [ISO-639-1](http://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) code.
* Open the newly created .po file in a text-editor or a po-editor
* Edit the headers, to reflect the language and other state of the translation
```
msgid ""
msgstr ""
"Project-Id-Version: v2.3-HF3\n"
"Report-Msgid-Bugs-To: https://github.com/rlf/uSkyBlock/issues\n"
"POT-Creation-Date: 2015-04-17 08:45+0200\n"
"PO-Revision-Date: YEAR-MO-DA HO:MI+ZONE\n"
"Last-Translator: Mikey Mouse <Mikey.Mouse@Disney.Com>\n"
"Language-Team: LANGUAGE <LL@li.org>\n"
"Language: nl\n"
"MIME-Version: 1.0\n"
"Content-Type: text/plain; charset=UTF-8\n"
"Content-Transfer-Encoding: 8bit\n"
```
Of special concern is the `Language:`.

Now you can use your favourite po-editor to translate all the `msgstr` entries in the .po file.

**Good Suggestions:**
* [POEdit](http://poedit.net/) - Windows/Mac/Linux client
* [Loco](https://localise.biz/free/poeditor) - Free online po-editor
* [Gted](http://www.gted.org/) - Eclipse Plugin

*Note:* Never touch or translate the `msgid`s.

Once the .po file has been translated, post the .po file back to uSkyBlock, by either:
* create a [pull-request](https://github.com/rlf/uSkyBlock/pulls) to get it added to the official-release.
* paste it to [pastebin](http://pastebin.com/), and create an issue on [GitHub](https://github.com/rlf/uSkyBlock/issues) linking to it.
* paste it to [pastebin](http://pastebin.com/), and create a forum post on [DevBukkit](http://dev.bukkit.org/bukkit-plugins/uskyblock/) linking to it.
* paste it to [pastebin](http://pastebin.com/), and create a forum post on [Spigot](http://www.spigotmc.org/threads/uskyblock.38300/|Spigot) linking to it.
* create an issue on [GitHub](https://github.com/rlf/uSkyBlock/issues), and attach the .po file to it.

Once the .po file has been approved and merged to the uSkyBlock master, the translations will be available in the next release.

**Testing the translation**

Either place the newly created .po file in the `i18n.zip` file within the jar-file, or copy it to the `plugins/uSkyBlock/i18n` folder, once the plugin has been reloaded, the new translation should be available from the `/usb lang` command.

**Disclaimer**

We can not be held responsible for translations not made by us.
If in any case a translation is not correct you can contact us and we will deal with the matter as soon we can.
In case of an translation on purpose being rude or inappropriate we will remove the translation.
