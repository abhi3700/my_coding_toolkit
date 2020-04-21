## GitHub Repo
* Markdown Extended Higlighting - https://github.com/jonschlinkert/sublime-markdown-extended
* Markdown TOC - https://github.com/naokazuterada/MarkdownTOC

## NOTES
* One can try editing a file on __Github__ or __Sublime Text 3__ enabling this above extensions.
* Always use indentation using tabs, NOT spaces.
* Indentation size can be 2, 3, 4..anything. [2 recommended]

## Shortcuts
* ##### **Bold** - Bold
* ##### _italic_ - Italics
* ##### `<ins>underline</ins>` - underline a statement
* ##### Collapsible: Expand text with title
  <details>
  <summary><b>Expand: </b></summary>
		
	<h2>Abhijit is a good boy</h2>
	<p>Humand is a village in Chashm Rural District, Shahmirzad District, Mehdishahr County, Semnan Province, Iran. At the 2006 census, its existence was noted, but its population was not reported. </p>
		
  </details>
* ##### Collapsible: Expand code snippet/block with title
	> NOTE: give a line break after summary tag

	<details>
	<summary><b>View code: </b></summary>

	```cpp
	std::cout << "With Iterator:" << std::endl;
	for (std::vector<string>::iterator i = v.begin(); i != v.end(); ++i)
	{
		std::cout << *i << std::endl;
	}
	```
	</details>

* ##### Single line code snippet - `code`
* ##### Multiple-line code snippet - 
  ```cpp
  std::string s = "hello";
  ```
* ##### Image from HTTP link
  - 1
  ```
  <p align="center">
    <img src="https://github.com/DrifeCommunity/Documentation/blob/master/Images/DRIFE-Governance.png" alt="DRIFE_governance" width="550" height="510">
  </p>
  ```
  - 2 with no width or height <br/>
  `![eos_image](http://url/to/img.png)`
  
* ##### Image from local folder
  Within a git repository, it is done like this:
  
  > NOTE: It is a relative path 
  ```markdown
  ![auto_fetch Image](./images/Fork/auto_fetch.png)
  ![Repository Image](./Sessions/Session%201/images/repository.jpg)
  ```
  Try <kbd>alt+m</kbd> from inside a ST3 application to view if it is shown.
  
  __Example: Look at the relative path in the image link__ <br/>
  The directory is like this:
```console
  |-- libs
  |   |-- Dash
  |   |   |-- dash.md
  |   |   |-- examples
  |   |   |   |-- 1_demo.py
  |   |   |   |-- 2_hello.png
  |   |   |   |-- 2_hello.py
  |   |   |   |-- 3_children.py
  |   |   |   |-- kill_port.bat
  |   |   |   `-- practice.py
  |   |   `-- images
  |   |       |-- console.png
  |   |       `-- console_open_url.png

```
  Now, in `dash.md` file, the image - `console.png` will be referred as this:
```markdown
	<p align="center">
	  <img src="./images/console.png" alt="console Image" width="" height="">
	</p>
```
  > NOTE: the image link is `./images/console.png`, NOT this - `./libs/Dash/images/console.png`. So, it's a relative path w.r.t `dash.md` file (where the image is referenced).
  
* ##### Highlight console
```console
foo@bar:~$ whoami
foo
```
* Highlight shell
```sh
wc -l en_US.twitter.txt 
```
* ##### New page
```markdown
<div style="page-break-after: always;"></div>
```
* Embed Videos
```md
[[embed url=http://www.youtube.com/watch?v=6YbBmqUnoQM]]
```

