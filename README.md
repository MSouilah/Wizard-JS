![Badge-glow](https://img.shields.io/badge/WizardJS-v1.6-blue?style=flat-square) [![jsDelivr hits (GitHub)](https://data.jsdelivr.com/v1/package/gh/AdrianVillamayor/Wizard-JS/badge)](https://www.jsdelivr.com/package/gh/AdrianVillamayor/Wizard-JS) ![GitHub repo size](https://img.shields.io/github/repo-size/AdrianVillamayor/Wizard-JS?style=flat-square)

# Wizard-JS - Wizard Vanilla JavaScript

A lightweight wizard UI component that supports accessibility and HTML5 in JavaScript Vanilla.


## Demo
Try it 


[![Codepen](https://user-images.githubusercontent.com/29653964/116972608-8f6bca80-acbb-11eb-98c1-8a3b19705de1.png)](https://codepen.io/adrianvillamayor/pen/VwWPVME)


## Installation 
Add this code. [cdn](https://www.jsdelivr.com/package/gh/AdrianVillamayor/Wizard-JS)

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/AdrianVillamayor/Wizard-JS@1.6/styles/css/main.css" integrity="sha256-fzh2SI0FhNBETzlD6atqnrNKf0m7g85OREoqtbdCuuM=" crossorigin="anonymous">
<script src="https://cdn.jsdelivr.net/gh/AdrianVillamayor/Wizard-JS@1.6/src/wizard.min.js" integrity="sha256-x8IFm01zeoF8EUDlpC5vaSvL0sSMkPhlrKD8xvhK3Hk=" crossorigin="anonymous"></script>
```

## Usage
```javascript
let args = {
	"wz_nav_style": "dots",
	"buttons": true,
	"navigation": 'buttons',
	"finish": "Save!",
	"blink": true,
};

const wizard = new Wizard(args);

wizard.init();
```

## Config Wizard
Options allowing to modify the behavior and actions
| Parameter      | Type   | Default          |  Definition / Value   |
| -------------  | ------ | ---------------- | --------------------- |
| `wz_class`     | String | .wizard          | Wizard main container class |
| `wz_nav`       | String | .wizard-nav      | Nav container class |
| `wz_nav_style` | String | dots             | Style of navigation steps / `dots`, `tabs`, `progress` |
| `wz_content`   | String | .wizard-content  | Body container class |
| `wz_buttons`   | String | .wizard-buttons  | Action button container class |
| `wz_button`    | String | .wizard-btn      | Class of Prev, Next and Finish action buttons |
| `wz_step`      | String | .wizard-step     | Class for both nav and body steps |
| `wz_form`      | String | .wizard-form     | Class of the form that contains the wizard |
| `wz_next`      | String | .next            | Class of Next action button |
| `wz_prev`      | String | .prev            | Class of Prev action button |
| `wz_finish`    | String | .finish          | Class of Finish action button |
| `current_step` | int    | 0                | Active wizard step |
| `steps`        | int    | 0                | Number of wizard steps |
| `navigation`   | String | all              | Allows you to change the navigation mode / `buttons`, `nav`, `all` |
| `buttons`      | Bool   | true             | Allows you to show or hide the action buttons |
| `next`         | String | Next             | Next button text |
| `prev`         | String | Prev             | Prev button text |
| `finish`       | String | Submit           | Finish button text |
| `blink`        | Bool   | true             | Way of highlight appear: link or persistent |

## HTML Tags
- Define the step type as a form, to validate the fields marked as required and change the wizard to form in case it is not defined.
  
	`[data-type]` => `form`, `default`	
	```html
	<div class="wizard-step" data-type="form"> 
	```
	If not defined, it is treated as `default`.




## Events Management
When any wizard button is used, it will generate an event.
```javascript
document.addEventListener("prevWizard", function (e) {
	alert("Prev Step");
});

document.addEventListener("nextWizard", function (e) {
	alert("Next Step");
});

//When it is a form
document.addEventListener("submitWizard", function (e) {
	alert("Form Submit");
});

//When it is not a form
document.addEventListener("endWizard", function (e) {
	alert("Wizard is finished");
});
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://github.com/AdrianVillamayor/Wizard-JS/blob/main/LICENSE)

### Thanks for your help! 🎉
