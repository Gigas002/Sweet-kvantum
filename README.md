# Sweet-kvantum

Fork of [Sweet kvantum](https://github.com/EliverLara/Sweet/tree/nova/kde/Kvantum) theme

Two [Kvantum](https://github.com/tsujan/Kvantum) themes for Qt applications:

- `Sweet`
- `Sweet-transparent-toolbar`: the same, with no background behind the menu bar and toolbars

## Install

On Arch Linux, the AUR package `sweet-kvantum-git` installs both to `/usr/share/Kvantum`.

Otherwise, Kvantum looks for a theme in a folder named after it, holding its `.kvconfig` and `.svg`:

```sh
for theme in Sweet Sweet-transparent-toolbar; do
    mkdir -p ~/.config/Kvantum/$theme
    cp src/$theme.kvconfig src/$theme.svg ~/.config/Kvantum/$theme/
done
```

Then choose the theme in Kvantum Manager (Change/Delete Theme), or:

```sh
kvantummanager --set Sweet
```

Qt applications use it with Kvantum as their style: in Plasma, System Settings -> Colors & Themes -> Application Style -> kvantum; elsewhere, `QT_STYLE_OVERRIDE=kvantum`.

## Editing

The two SVGs are the same picture: change both. The themes differ only in their `.kvconfig`, where `Sweet-transparent-toolbar` draws the menu bar and toolbars with `_menubar`, an element that isn't in the SVG, so nothing is drawn.
