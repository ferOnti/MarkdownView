## What is it?
MarkdownView is an Android webview with the capablity of loading Markdown text or file and display it as HTML, it uses MarkdownJ and extends Android webview. 

##How to use it? 

- To add MarkdownView to your project, include the jar, or the source code. 
- Simple usage is to set the whole activity to a MarkdownView by Adding the following to your onCreate method

`MarkdownView markdownView = new MarkdownView(this);  
setContentView(markdownView);`
 
- You can also add it to your layout by using `<us.feras.mdv.MarkdownView android:id="@+id/markdownView" />` 
and referance it in your activity: 

`MarkdownView markdownView = (MarkdownView) findViewById(R.id.markdownView);`

##Loading MarkDown text, local or online file : 

- **loadMarkdownData(String text)**

Using this method will result in loading md string to the MarkdownView and displaying it as HTML. 

 
- **loadMarkdownUrl(String url)**

You can use this method to load local or online files. 

To load a locale file, you have to add it to your assets folder and pass a url that start with "file:///android_asset/" : 
`markdownView.loadMarkDownData("file:///android_asset/myFile.md");`   

To load a file on the web you need to pass the full url :
`markdownView.loadMarkDownData("http://www.my-site.com/myFile.md");`
