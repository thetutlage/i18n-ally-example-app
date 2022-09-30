# Example project for i18n-ally
An example project using the i18n-ally VSCode to work with translations inside edge templates.

## Setup

- Clone the repo
- Run `npm install` to install dependencies

## Custom framework config file

This repo contains the config file to enable extension for AdonisJS template engine called Edge inside `.vscode/i18n-ally-custom-framework.yml`

```yaml
languageIds:
  edge

usageMatchRegex:
  - "[^\\w\\d]t\\(['\"`]({key})['\"`]"

refactorTemplates:
  - '{{ t("$1") }}'
  - t("$1")
```

## Enabling namespaces
AdonisJS uses namespaces for translations and hence this option must be enabled for the extension to work properly.

## Testing
Open `resources/views/welcome.edge` file to see the extension in action. Search for `{{ t("messages.title") }}` for example.

You might also need the AdonisJS official extension so that VsCode can assign the language id to all `.edge` files. The official VSCode extension https://marketplace.visualstudio.com/items?itemName=jripouteau.adonis-vscode-extension
