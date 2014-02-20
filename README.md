diacritic-annotator
===================

Plugin for annotator that allows diacritic mark (images) to be placed at a given baseline of a highlighted piece of text

#Installation

To use the tool you need to install the [Annotator plugin](https://github.com/okfn/annotator/) to annotate text.

In addition, add diacritic-annotator.min.js and diacritic-annotator.min.css CDN distributed file to your head tag, like this:

```html
	<head>
		<!-- Annotator -->
		<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.7/jquery.min.js"></script>
		<script src="http://assets.annotateit.org/annotator/v1.2.7/annotator-full.min.js"></script>
		<link rel="stylesheet" href="http://assets.annotateit.org/annotator/v1.2.7/annotator.min.css">

		<!-- Diacritic Mark Plug-in -->
		<script src="src/diacritic-annotator.js"></script>
		<link href="src/diacritic-annotator.css" rel="stylesheet">
	
	</head>
```

Furthermore, you will need to create an instance of Annotator with the plugin, as follow:

```js
	<script>
		var 
    	var optionsdiacritic = {
    		tag:{diacriticname;urlofmarkimage;baseline,diacriticname2;urlofmarkimage2;baseline2}
		};
    	$('#div_id').annotator().annotator('addPlugin','Diacritics',optionsdiacritic);
    </script>
```

Change #div_id for the real id where the Annotator is and "optionsdiacritic" should include the name you'd like the users to see appear, the url for the location of the image (should be 10px by 10px unless it's changed in the CSS with a transparent background), and the baseline for the image (options: "top", "middle", "bottom").
