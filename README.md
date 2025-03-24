# DNA-Engine
An UI library for cloning semantic templates

License:MIT npm Hits Build

dna-engine is a lightweight easy-to-use UI library enabling developers to rapidly build maintainable JavaScript applications.

A) Bookstore Example
Designate templates with the dna-template class, and put the templates directly into the HTML of your web page.  Use the element's id to indicate the name of the template.  Enclose data fields in double tildes ~~.

1. HTML for book template
<h1>Featured Books</h1>
<section class=books>
   <div id=book class=dna-template>
      <h2>~~title~~</h2>
      Author: <cite>~~author~~</cite>
   </div>
</section>
Then call the dna.clone() function to insert a copy of the template into the DOM.  The supplied JSON data object populates the fields of the template.

2. JavaScript call to add book node
dna.clone('book', { title: 'The DOM', author: 'Jan' });
The new clone element replaces the template.  The original template is detached from the DOM and kept for additional cloning.

3. Resulting HTML with clone
<h1>Featured Books</h1>
<section class=books>
   <div class=book>
      <h2>The DOM</h2>
      Author: <cite>Jan</cite>
   </div>
</section>
Need to clone the template multiple times?  Simply pass an array of data objects into the dna.clone() function.

B) Additional Information
https://dna-engine.org (see the "Try it out" section for an interactive example)
Sample To-Do Application (jsfiddle)
Introduction to dna-engine (YouTube)
Documentation
Release Notes
C) Contributor Notes
To be a contributor, fork the project and run the commands npm install and npm test on your local clone.  Make your edits and rerun the tests.

Pull requests welcome.  Since the pacakge version number is updated during the release process, you can leave the version number unchanged.

D) Build Environment
Check out the runScriptsConfig section in package.json for an interesting approach to organizing build tasks.

CLI Build Tools for package.json

🎋 add-dist-header:  Prepend a one-line banner comment (with license notice) to distribution files
📄 copy-file-util:  Copy or rename a file with optional package version number
📂 copy-folder-util:  Recursively copy files from one folder to another folder
🪺 recursive-exec:  Run a command on each file in a folder and its subfolders
🔍 replacer-util:  Find and replace strings or template outputs in text files
🔢 rev-web-assets:  Revision web asset filenames with cache busting content hash fingerprints
🚆 run-scripts-util:  Organize npm package.json scripts into groups of easy to manage commands
🚦 w3c-html-validator:  Check the markup validity of HTML files using the W3C validator
