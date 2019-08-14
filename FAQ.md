# Frequently Asked Questions
Below we have gathered a collection of the most frequently asked questions.
Any questions answered below, will be ignored on various forums, personal messages, skype-requests or GitHub issues.

## Schematics

### How can I remove skySMP? (or any other schematic)
Make sure you add an appropriate section to the `config.yml` file, and simply list then as not enabled in the `island-schemes` section.
```yml
island-schemes:
  skySMP:
    enabled: false
```
If you simply remove the schematic, it will be re-created on next server-startup.

