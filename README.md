# Creator

A playground for HTML, CSS, JavaScript, and Typescript with live preview. Create a project and give it a name. From that moment on, the project is saved! Completely locally, in your browser's indexedDB.
When you restart the tool, the most recently used project will open automatically.
All previously created projects can be easily found in a dropdown menu, as well as in the context menu (right-click -> Select Project).
To save your projects completely browser-independently, you can download all projects as a single ZIP file or one by one as JSON project file or as HTML. If you copy the contents of the ZIP file to the /creations subfolder, you can select the projects to be loaded with '...index.html?usedb=0' when opening the tool. Alternatively, click 'Import Project' and select the ZIP file itself. You can then also select which projects should be imported from the ZIP file.
Starting with ?usedb=0 means that no browser database is used. Instead, the tool searches for the 'creations.txt' file in the creations folder and loads the projects listed there from the /json folder. Projects can therefore no longer be backed up automatically! However, you can save all loaded projects as a ZIP file, or a single project as JSON. Everything else works normally.

## The Editors

The Creator is based on Cloud9's popular Ace editor.
There are a total of six individual editors, only one of which is visible at a time. The editor is conveniently selected via tabs directly above the editor.
The editors: HTML, JavaScript, Typescript, CSS, Images, and Assets.
Each editor checks the input for syntactical correctness, has undo/redo, a beautifier, a minifier, and makes input suggestions.

The first four editors are self-explanatory (HTML, CSS, JS, TS). The 'Images' and 'Assets' editors save content in JSON format.

### Asset Editor
When uploading files, you can choose how they should be processed: by file extension or as an asset.
If you select Asset, the uploaded files will be converted, depending on their content, either as a dataURI, as minified text, or into an 8- or 16-bit array buffer (this behavior can be influenced; more on this later).
The file contents are then converted to strings and added to the Asset Editor. When the project is rendered, the global constant '\_assets\_' is created, which contains all assets to make them accessible via JavaScript.

### Image Editor
Click 'Upload' and select the images to upload. These will be converted to dataURIs and saved as strings in the Image Editor. Each time the project is rendered, all image paths within the HTML and CSS source code are replaced with dataURIs, so the images are displayed normally. However, this does not apply to dynamic content, which is loaded at runtime.

The contents of the image and asset editors should only be edited manually if you know what you're doing! But if necessary, there's always the undo function. ;)

## The Editor Functions
