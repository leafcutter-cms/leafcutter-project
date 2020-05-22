# Adding dependencies with Composer

Leafcutter is designed to manage its dependencies via Composer. For that reason, there are some considerations regarding the version constraints in your `composer.json` file.

In general, addons and themes should specify which versions of Leafcutter they are compatible with. They should also specify which versions of other themes or addons they require or are known to conflict with. This means that the best and most reliable way of specifying versions for them is *to not*.

The suggested method is to specify a version constraint for the main `leafcutter/leafcutter` package only, and allow Composer to sort out everything else by giving them `*` wildcard constraints.

For example, if you wanted to install the code highlighting addon, the suggested Composer command would be:

```bash
composer install leafcutter/addon-highlight:*
```

## Activating addons

Addons must be activated in order to actually do anything. This is done by adding them to the array of addon names in the config path `addons.activate`. In this template, this has been started for you in the file `config/addons.yaml`

## Activating themes

Themes will also not do anything across the board unless they are activated. For themes this configuration option is at `themes.activate`. Multiple themes can be activated at once, and will be applied in the order they appear in config. This allows you to make non-comprehensive themes that just tweak something.

The theme configuration in this template is already started in the file `config/theme.yaml`
