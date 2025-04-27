# Creator
A playground for HTML/Javascript/Typescript/CSS. Stores all projects in the browaers indexedDB, or creates a single HTML file from a project.
<hr>
The creator's editor is based on the popular ace editor from Cloud9.
There are six individual editors included for HTML, Javascript, Typescript, CSS, Images and Assets.
<ul>
  <li>
    Assets
    <ul>
      <li>
        Whwn you upload files, you can choose, how they should be teeatet: Depending on the file extension or as an asset.
        In case that you choose asset, the uploaded files will be converted either to a dataURI, to minified text or to an 8 or 16 bit areay buffer, depending on the content (you can influence this behaviour, more on that later).
        The file data will then be stringified and added to the assets editor, which content is in json format.
      </li>
      <li>
        When the project is rendered, the global constant _assets_ is created, holding all the assets, in order to make them accessible by javascript.
      </li>
      <li>
        You should never edit the content of the assets editor by hand unless you know what you do (errors there will at least be shown by the ace editor).
      </li>
    </ul>
  </li>
  <li>
    Images
    <ul>
      <li>
        Some
      </li>
    </ul>
  </li>
</ul>

    

