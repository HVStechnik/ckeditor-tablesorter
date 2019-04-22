# ckeditor-tablesorter

Adds sorting functionality to CKEditor

## How to install: 
1. Add the tablesorter directory to the ckeditor/plugins directory
2. Then edit the config.js file and add "tablesorter" to the extraPlugin list (config.extraPlugins = 'xyz,tablesorter,xyz';)
3. Reload the editor, that's it :-)

Currently tested with CKEditor version 4.7.0 and 4.10.1
Currently supported languages: en,de,ru,uk

## Adding your own language:
In order to add your own language, please fork this repository, navigate to tablesorter/lang, copy the en.js file, rename it to your own ">>>language-code<<.js" (e.g. ru.js) and change the content:

```
CKEDITOR.plugins.setLang( 'tablesorter', '>>> place your language code here, e.g. ru <<<', {        
        contextAsc: 'Sort ascending',   // label for ascending sorting
        contextDesc: 'Sort descending', // label for descending sorting
} );
```
Please create a pull request with the new language to this repository!

If you try to install tablesorter with a non-supported language, you may encounter one of the following errors:
 - Cannot read property 'contextAsc' of undefined
 - editor.lang.tablesorter is undefined
