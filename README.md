# Color Function Preset for Boost Moodle Theme

![Preset Preview](https://raw.githubusercontent.com/raulgroig/preset-colorfunction/master/preview.png)

## Synopsis

The Boost theme for Moodle is a bootstrap based theme that allows to upload preset files with style rules. 

The Color function preset allows to change all the main colors of the theme just selecting a new brand color in the Boost settings page. It is possible because all the main colors are obtained by Sass functions over the brand color.

The preset is based on the default Boost preset with a few style rules added for increase the visual impact of the colors.

To see a comparison between the Boost color palette and the Color Function palette and some suggestions of brand colors to use with this preset [click here](http://www.raulgroig.com/preset-colorfunction/).  

Just changing the brand color to brown (#b16740) and the theme will looks like this ![Preset Preview](https://raw.githubusercontent.com/raulgroig/preset-colorfunction/master/preview-brown.png)  

The Function Color Preset is available at the [Boost Presets Repository](https://moodle.net/mod/data/view.php?d=13&rid=639)


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

- Download the Color Function Preset: [Boost Presets Repository](https://moodle.net/mod/data/view.php?d=13&rid=639) or [Raw File](https://raw.githubusercontent.com/raulgroig/preset-colorfunction/master/preset-colorfunction.scss)
- Go to the Boost settings page (Dashboard > Site administration > Appearance > Themes > Boost).
- Click to add Additional theme preset files and upload it.
- Save changes to view your new preset option in the Theme preset dropdown.
- Select the new preset in the Theme preset dropdown and change the brand color if you want.
- Save again and it's all done.


## API Reference

- Boost presets - [Link to Moodle Docs](https://docs.moodle.org/dev/Boost_Presets)  
- Sass Functions - [Link to Sass Documentation](http://sass-lang.com/documentation/Sass/Script/Functions.html)


## Contributors

Please let me know if you want to improve something in this preset. I will appreciate any suggestion and I'm able to help on new features. Contact me by e-mail: [raulgroig@gmail.com](mailto:raulgroig@gmail.com)


## License

GNU General Public License v3 (GPL-3)  

You may copy, distribute and modify the software as long as you track changes/dates in source files. Any modifications to or software including (via compiler) GPL-licensed code must also be made available under the GPL along with build & install instructions.
