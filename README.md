# Tyk Dashboard Language Packs

As of version 1.3 of tyk Dashboard, language packs are supported. Tyk technologies are open sourcing our innitial translations so that others can update and add to the collection of langauges supported by the dashboard over time.

Currently, the lanaguages that are supported out of the box are:

- English
_ Chinese (Mandarin)
- Korean

## How to enable a language pack in the Dashboard

to enable a lanuage pack, simply add the JSON file to the `langs/` folder in yout tyk dashboard installation folder. It must end in `.json` and be a valid JSON file.

Then amend your configuration file to add a UI section:
    
    ...
    "ui": {
        "languages": {
            "English": "en",
            "Chinese": "cn",
            "Korean": "ko"
        },
        "default_lang": "en"
    },
    ...

Each element in the languages section must match the prefix of the JSON file you have added, you can set the default load langauge by setting the `default_lang` attribute.

You will need to restart, and reload your dashbaord interface for the changes to take effect.
