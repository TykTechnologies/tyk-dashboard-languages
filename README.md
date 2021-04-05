# Tyk Dashboard Language Packs

*[As of v1.3 of the Dashboard]*

As of version 1.3 of the Tyk Dashboard, language packs are supported. Tyk Technologies have open sourced our initial translations so that others can update and add to the collection of languages supported by the Dashboard over time.

Currently, the languages that are supported out of the box are:

- English
- Chinese (Mandarin)
- Korean
- French
- Spanish (Spain)

## How to enable a language pack in the Dashboard

To enable a language pack, simply add the JSON file to the `langs/` folder in your Tyk Dashboard installation folder. It must end in `.json` and be a valid JSON file.

Then amend your configuration file to add a UI section:
    
    ...
    "ui": {
        "languages": {
            "English": "en",
            "Chinese": "cn",
            "Korean": "ko",
            "French": "fr",
            "Spanish": "es"
        },
        "default_lang": "en"
    },
    ...

Each element in the languages section must match the prefix of the JSON file you have added. You can set the default load language by setting the `default_lang` attribute.

You will need to restart, and reload your Tyk Dashboard for the changes to take effect.
