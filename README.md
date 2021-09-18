MarkdownSharp - With Github style code blocks
=========================================

The original MarkdownSharp can be found on google code here [https://code.google.com/p/markdownsharp/](https://code.google.com/p/markdownsharp/)


This is basically a fork of that, that has been slightly modified to support github style code blocks.

If you're unfamiliar with MarkdownSharp, it's a markdown parser, which was ported from the original perl markdown parser.  I believe it is what StackOverflow uses.

My light modifications allow this

<pre lang="no-highlight"><code>
```cs
public void Main()
{
  Console.WriteLine("Github Style Code blocks");
}
```
</code></pre>

Which will be transformed to the following html

```html
<pre><code class='language-cs'>
public void Main()
{
  Console.WriteLine("Github Style Code blocks");
}
</code></pre>
```

Then you can use a library like [HighlightJS](http://highlightjs.org/) to sytnax highlight that code block, and since we added the class ``language-cs``, it will be highlighted as c# code.

Whatever is after the 3 ticks will be put in the class name

so 
<pre lang="no-highlight"><code>```mylanguage
</code></pre> 
would transform to 
```html
<pre><code class='language-mylanguage'>
```

If anyone wants to add any of the other Github flavored stuff, feel free to pull request.  Or, fix my mediocre implementation of the the Github Flavored Codeblocks

### Syntax Highlighting Language support

| Language | Available language mode(s) |
|---|---|
| ASP.NET |	asp, aspx |
| C	| c |
| C++ |	c++, cpp, cplusplus |
| C# |	cs, csharp |
| Clojure |	clj, cljc, cljx, clojure |
| CSS |	css, less, sass, scss, styl, stylus |
| cURL |	curl |
| D |	d |
| Dart |	dart |
| Diff |	diff |
| Docker |	dockerfile |
| Erlang |	erl, erlang |
| Go |	go |
| Groovy |	gradle, groovy |
| Handlebars |	handlebars, hbs |
| HTML/XML |	html, xhtml, xml |
| HTTP |	http |
| Java |	java |
| JavaScript |	coffeescript, ecmascript, javascript, js, jsx, node |
| JSON |	json |
| Julia |	jl, julia |
| Kotlin |	kotlin, kt |
| Liquid |	liquid |
| Markdown |	markdown |
| Objective-C |	objc, objectivec |
| Objective-C++ |	objc++, objcpp, objectivecpp, objectivecplusplus |
| OCaml |	ocaml, ml |
| Perl |	perl, pl |
| PHP |	php |
| PowerShell |	powershell, ps1 |
| Python |	py, python |
| R |	r |
| React |	jsx |
| Ruby |	jruby, macruby, rake, rb, rbx, ruby |
| Rust |	rs, rust |
| Scala |	scala |
| Shell |	bash, sh, shell, zsh |
| SQL |	cql, mssql, mysql, plsql, postgres, postgresql, pgsql, sql, sqlite |
| Swift |	swift |
| TypeScript |	ts, typescript |
| YAML |	yaml, yml |
