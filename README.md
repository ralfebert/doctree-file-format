# doctree-file-format

`.doctree` is a pragmatic textual file format for 'table of contents' documents that is

* easy to generate
* easy to parse for both humans and machines
* fast to scan/search

As an example, a `.doctree` for the table of contents of the Wikipedia entry "[Book](https://en.wikipedia.org/wiki/Book#toc)":

	Book - Wikipedia, the free encyclopedia
		1 Etymology -- {"href":"#Etymology"}
		2 History of books -- {"href":"#History_of_books"}
			2.1 Antiquity -- {"href":"#Antiquity"}
				2.1.1 Tablet -- {"href":"#Tablet"}
				2.1.2 Scroll -- {"href":"#Scroll"}
				2.1.3 Codex -- {"href":"#Codex"}
				2.1.4 Manuscripts -- {"href":"#Manuscripts"}
				2.1.5 Middle East -- {"href":"#Middle_East"}
				2.1.6 Wood block printing -- {"href":"#Wood_block_printing"}
				2.1.7 Movable type and incunabula -- {"href":"#Movable_type_and_incunabula"}
			2.2 Modern world -- {"href":"#Modern_world"}
		3 Book manufacture in modern times -- {"href":"#Book_manufacture_in_modern_times"}
			3.1 Current processes -- {"href":"#Current_processes"}
			3.2 Finishing -- {"href":"#Finishing"}

## Spec

* `.doctree` files are UTF-8 encoded
* The structure of the document is formed by the indentation using single tab characters `\t`
* Optionally, additional attributes can be specified optionally as a JSON string after the title: `title -- { ... }`
* A line may not be indented more than +1 tab character than the line before
* Every line is a title of a document entry, `\n` is used as line break character
* Empty lines, line breaks in the title/JSON or ` -- {` in the title: forbidden
* The document may have only one root node: The first line may not be indented and all the following lines must be indented

## License

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />This document is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.
