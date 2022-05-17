# Bookmarklet to clip webpages to google docs

(modified version of: https://gist.github.com/jbrown123/4c768495b21b03d5529f26ccd83bf69f)

Just create a new bookmark and make the text below (starting with javascript:) the URL of the bookmark.  Note that you will need to replace the "YOUR FOLDER ID HERE" string with the actual google docs folder ID you want to use. 

Copy the text below into your bookmark URL (be sure to substitute your folder ID):

```
javascript:(function(){var folder="YOUR FOLDER ID HERE"; var text=""; if(window.getSelection){text=window.getSelection().toString();}else if(document.selection && document.selection.type!="Control"){text=document.selection.createRange().text;}if(prompt("Press Ctrl+C, Enter", "Tags: \n\n"+location.href+"\n\n"+document.title+"\n\n"+text)) window.open('https://docs.google.com/document/create?usp=drive_web&folder='+folder+'&title='+encodeURIComponent(document.title))})()
```
