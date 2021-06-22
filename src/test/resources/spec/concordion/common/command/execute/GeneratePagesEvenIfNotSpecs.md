# Be able to create pages in any valid format that aren't specs

## User Story

As a specification writer, I want to be free to create pages in my specification that aren't specs, in markdown, Excel or HTML/XHTML, so that I can structure supplementary information in any way that I think my readers would find most clear and organized, while at the same time being able to take advantage of the convenience and readability of markdown syntax or Excel spreadsheets over HTML.

## Example: Convert Markdown File

*Given* markdown file **RandomFile.md** in the spec directory that **does not have a matching Fixture**.

*When* Concordion runs.

*Then* RandomFile.md should be **converted to HTML file RandomFile.html**.

## Example: Link to Another Markdown File Should Link to Correct HTML

*Given* markdown file **RandomFile.md** that does not have a corresponding fixture, and **has a relative link to markdown file TheOtherFile.md**:

```[link to the other file](TheOtherFile.md)```

*When* Concordion runs.

*Then* the link should now point to the generated HTML page **TheOtherFile.html**:

`<a href="TheOtherFile.html">link to the other file</a>`

## Example: Convert Excel File

*Given* Excel file **SomeFile.xlsx** in the spec directory that **does not have a matching Fixture**.

*When* Concordion runs.

*Then* SomeFile.xlsx should be **converted to HTML file SomeFile.html**.