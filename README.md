# Color Function Preset for Boost Moodle Theme

![Preset Preview](https://raw.githubusercontent.com/raulgroig/preset-colorfunction/master/preview.png)

## Synopsis

The Boost theme for Moodle is a bootstrap based theme that allows the admin to upload preset files with style rules. 

The Color function preset allows to change all of the main colors of the site just selecting a new brand color in the Boost settings page. It is possible because all the main colors are obtained by Sass functions over the brand color.

The preset is based on the default Boost preset with a few style rules added for increase the visual impact of the colors.

You can see a comparison of the default Boost color palette and the default Color Function palette and some suggestions of brand colors to use with this preset [here](http://www.raulgroig.com/preset-colorfunction/) 


## Code Example

It is not necessary to code to use this preset, just install and change the brand color in the Boost settings page.  

The code bellow is the part of the preset that generate the main colors with some Sass functions over the brand color.

```scss
$brand-primary:     #4580B9 !default;
$brand-info:        adjust-color($brand-primary, $saturation: -15%, $lightness: 25%) !default;
$brand-success:     adjust-color($brand-primary, $hue: -115deg, $lightness: -10%) !default;
$brand-warning:     adjust-color(complement($brand-primary), $red: 50) !default;
$brand-danger:      adjust-color($brand-warning, $saturation: 50%, $lightness: -15%) !default;
```

## Motivation

This new preset feature is the simplest way to customize Moodle and works really fine. I'm very glad with this innovation and with the possibility of helping to improve it.


## Installation

- Download the Color Function Preset: [Link to raw file](https://raw.githubusercontent.com/raulgroig/preset-colorfunction/master/preset-colorfunction.scss)
- Go to the Boost settings page (Dashboard > Site administration > Appearance > Themes > Boost).
- Click to add Additional theme preset files and upload it.
- Click to Save changes to view your new preset option in the Theme preset dropdown.
- Select the new preset in the Theme preset dropdown and change the color if you want.
- Save again and it's all done.


## API Reference

Boost presets - [Link to Moodle Docs](https://docs.moodle.org/dev/Boost_Presets)
Sass Functions - [Link to Sass Documentation](http://sass-lang.com/documentation/Sass/Script/Functions.html)


## Contributors

Please let me know if you want to improve something in this preset. I will appreciate any suggestion and I'm able to help on new features. Contact by e-mail [raulgroig@gmail.com](mailto:raulgroig@gmail.com)


## License

GNU General Public License v3 (GPL-3)  

You may copy, distribute and modify the software as long as you track changes/dates in source files. Any modifications to or software including (via compiler) GPL-licensed code must also be made available under the GPL along with build & install instructions.
