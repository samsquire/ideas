One Hundred Ideas for Computing
===

This is a vision for how computing could be. I began writing down ideas down a number of years ago, this is a selection of ideas old and new. My theme is integration.

## 1. [Email Metadata](id:email-metadata)

Emails could contain comprehensive metadata about the human readable content depending on the sort of email it is. This machine readable information could be interpreted metadata to:
 
 * display specialised interfaces for certain information
 * integrate and collect information together
 * enable contextual computing

For example:

 * subscribe and unsubscribe to email newsletters from one interface
 * get notified of when a product will be delivered and when it is dispatched
 * receive an invoice? it is added to your accounting software
 * get cross platform desktop and mobile notifications, tailored to whatever device you are on
 * set up complex rules to react to different situations
 * get notified when someone replies to your forum or blog posts
 * receive notifications of what you bought, how much it cost
 * given permission to use a service? added to your personal keyring
 * receive a reply to a customer service ticket? it's added to your personal vendor relationship interface amongst all your other interactions with companies

Potential Integrations

 * HATEOAS for determining actions on an email: 'Unsubscribe' a mailing list email, 'Accept Invitation' for an invite, 'Reject Request'. We should be able to do more than just 'Reply' or 'Forward' an email.
 * [Life Engine](#life-engine)
 * [Living document](#living-documents)
 * [Email as social networking transport](#email-as-social-networking-transport)
 * Vendor Relationship Management

Existing:
 
 * [OpenEmailMetadata](https://github.com/samsquire/OpenEmailMetadata) - my very much incomplete exploration
 * [MailXML](http://www.idealliance.org/specifications/mailxml)
 * [Candle](http://candleapp.blogspot.co.uk/2011/06/why-i-invented-candle-i.html)

## 2. [Use Email as a Social Networking Transport](id:email-as-social-networking-transport)

The industry lacks an open social network. A social network can be build ontop of email: the user interface can  be a specialised email client with email as the transport mechanism. Everybody has an email address and web frameworks can easily communicate using mail protocols.

Email can be used as a common denominator protocol. A flexible and federated social network would abstract the protocol used for communication and upgrade to a better or efficient protocol when appropriate such as realtime  applications or when sharing files.

 * Users can send invitation requests in a regular email that includes a public key.
 * All shared content remains stored on the user's computer but can be hosted elsewhere.

Potential Integrations

 * [Email metadata](#email-metadata)
 * [Life Engine](#life-engine)
 
 Existing:
 
  * [Diaspora](https://joindiaspora.com/), [BuddyCloud](http://buddycloud.com/), [Status.Net](http://status.net/), [SockNet](http://socknet.net/w/The_Socknet), Appleseed
 
## 3. Community Idea: [Design This](id:design-this)

Developers need designers to give websites viable designs. This community brings developers with complete website backends and matches them with designers to give the backend a design.

 * Developer: "I have written the business logic, the backend API and a rudimentary frontend but I need a real design for a website."


## 4. [Living Documents](id:living-documents)

Blogs, forums, wikis and social networks solve variations of the same problem. Unfortunately they are not integrated enough. A blog post is not dynamic and flexible as it could be. Writing a post should allow me to take advantage of:

 * Collecting arbitrary structured data from the recipient rather than just a freestyle comment box at the bottom of a document. Information can be collected *within* the article such as small call to action button buttons that when clicked add form fields for the user to contribute to.
 * Allow users to provide corrections such as spelling (wiki functionality)
 * Split up the document into reusable components (wiki like transclusion)
 * Rendering display data in multiple ways
 
Examples:

```
A blogger is reviewing a number of products on an ongoing basis. The
blogger creates a post for a given product category and headings for
each offering. Attributes and ratings are placed in a bulleted list. The
blogger endeavours to update the blog post whenever information changes
regarding a product or when a new product is to be reviewed.


	- Ideally the blogger wants to display product attributes consistently and update them from one place.
	- Creating a summary of reviews at the bottom (without having to duplicate the information)
	- Ask users for product suggestions, perhaps with an embedded form.
	- The blogger wants to track the price or offers over time.
	- Allow users to make comments regarding particular products or ratings. Allow users to give their own ratings for an attribute.

This blogger uses a HTML strikethrough to indicate that information has
been updated in a blog. This is not transparent to the user. For
information such as the price or a rating of a product over time, it
will be difficult to see what the value was in the past and when it was
changed. They may want to show a graph of the product ratings over time.
``` 

Existing:

 * [LightTable](http://www.lighttable.com/)
 * Google Wave

## 5. [Life Engine](id:life-engine)

Life engine is a dashboard that attempts to collect information about your life and display relevant data on a single screen.

 * pension performance
 * bank account balances
 * upcoming birthdays for friends
 * dream diary
 * family, friend member statuses
 * important emails
 * to-do list, goals, reminders, calendar integration
 * lent possessions
 * alerts: hard disk space
 * active contractual obligations: apartment complex, mobile phone

Existing:

 * business dashboards
 
 
## 6. Community Idea: Ethical Me

A tool to track the decisions of consumers to register their buying decisions in a thoughtful way.

 * I didn't buy X because Y
 * I chose product X rather than Y because attribute Z

## 7. Peer to Peer Blocking

Block by default is inconvenient to users. Community driven blocking reduces risk. Configuration options should be shareable and synchronizable to increase security. The following configurations could be distributed to users who take part:

 * Firefox Request Policy
 * Host file blocking
 * Firewall rules
 * Application behaviour such as 'disable scripting/macros'
 
Potential Integrations:

 * web of trust, trust score for a people you know
 
Existing:

 * cloud based security providers, Site Advisor

## 8. Command Auto-complete

Command auto-complete could be implemented by:

 * indexing the man pages to extract documentation for the arguments of every command
 * typing a command begins a searches the index for arguments and either displays completion of the argument and/or provides a documentation panel for that argument.
 * or applications expose what they provide (see [representational computing](#representational-computing))

For example, if the user types `grep -v`, they may get an auto-complete for `--invert-match`. We could also provide transformations using knowledge from the index:

 * converting between long options and short options - useful for self-documenting shell scripts
 * sort arguments so they always appear in the same order

Potential integrations:

 * Use doclifter and parse resulting DocBook XML

## 9. [Elements Represent Themselves](id:elements-represent-themselves)

A rendering of data should stand-in and represent itself.

 * If you have an open program and see a filename in the title bar next to that file's icon, you should be able to interact with that name or icon in the same as you can elsewhere. For example, you should be able to move the file or rename it. You should be able to drag it into an open email.

 * If an application displays an IP address, a hostname, a filesize or some unit measurement, the user should be able to interact with these things with a tool that accepts these as arguments. Clicking a filesize may show where that space is being taken on the filesystem. Clicking an IP address may offer actions such as 'ping'. Clicking a unit measurement may show unit conversion tools.
 
When data is rendered, its type information should be preserved so that the user can interact with it.

Potential Integrations:

 * [the environment has knowledge](#the-environment-has-knowledge), [representational computing](#representational-computing)
 * types in the desktop environment
 
## 10. [The Environment has Knowledge](id:the-environment-has-knowledge) / Context-Aware Computing
 
Running applications expose information on what information they can provide and what they will accept. Bring type systems up into the desktop environment. Everything - including programs, have a type and have typed parameters. A system should help you fulfil type arguments for running programs. For example:

 * You have window open that is requesting an IP address.
 * Your machine exposes an IP address and your work VPN provides an IP address. Your online friends provide an IP address for a game server in a window.
 * You can pick the IP address from the available sources without having to type it in.
 * You have an email open in a browser which is listing attachments. In essence, this window is 'offering' you files. You should be able to see these files listed in file selection dialogs.

 
Potential integration:

 * drag and drop is no longer handled by clumsy drag and drop APIs

## 11. [Representational Computing](id:representational-computing)

Completing a task has a representation, such as 'render image' and if requested will select a program to do so depending on criteria. If the input data is in PNG format then it must pick a program representation that can render PNG. The inputs and outputs of programs are representations themselves so the type matching works upon programs themselves.

 * If an operation on a particular format has not been implemented but can be readily converted into a format that supports the operation, the system can follow a chain of conversions that allow an operation to be satisfied transparently. 
 * RC is akin to a program requesting a library that provides 'X' or 'can do X to Y' and having that library injected in. (see [representations are tests](#representations-are-tests))
 * There are many different ways of completing a task and they can be approached from different perspectives. Given a set of inputs and the intended goal, mappings or wrappers can provide for treating one representation as another but in a more formal way than industry practice. What something wraps and what programs are wrappers is in the heads of people and not known by the machine.
 * There needs to be some form of proof that two libraries will be interoperable. Representations as tests could provide this promise as a developer will import the representation of a task and any library promising to satisfy this representation would have to pass the tests dictated by the representation.

Existing:

 * Negotiation protocols
 * [Aspect oriented programming](http://en.wikipedia.org/wiki/Aspect-oriented_programming) 
 * Type systems, Type systems in the operating system and desktop environment
 * Dependency Injection
 * Testing in the field (production code that runs tests to make decisions, such as [Modernizr](http://modernizr.com/))
 * Weaving code into binaries by purpose

 
## 12. The Package Manager-Package Manager

There are multiple package managers that have to be controlled with separate programs. Setting up a machine involves installing various package managers. It seems a hierarchy of package managers would permit installing any number of packages.

 * package managers have consistent standard command-line API that lets them be driven by other programs to avoid special cases for package managers
 * can namespace packages of package managers
 
For example, if you were installing Typo, a blog platform:

 * you'll need RVM which is installed by script
 * Ruby which is installed by RVM
 * RubyGems which is installed by a Ruby script
 * Ruby on Rails
 * MySQL

By the end of this process, we've used two custom scripts and two package management systems. First the environment manager (RVM) and a language specific package manager (rubygems) and before we can even think about installing Typo3 with bundle. We still have not actually configured the software.

This could look something like this, where each package manager is namespaced:

```
mpm install script/https://get.rvm.io \
	rvm/1.9.3 \
	script/git@github.com/rubygems/rubygems/setup.rb \
	gem/rails \
	apt/mysql-server \
	apt/mysql-client \
	bundle/http://typosphere.org/stable.tgz
```

Potential integrations:

 * Infrastructure as code

## 13. Package Driven Development

Software complexity prohibits quick and repeatable set-ups. Software should be written to be packageable and repeateable from the beginning.

 * Not only does software need testing but the packages do too.
 * Installing the package should be enough (minus configuration) to begin running software

Existing:

 * [Vagrant](http://www.vagrantup.com/)
 
## 14. Configuration Spider
 
Infrastructure is complicated and the relationships between hosts, paths, ports and servers create a web of complexity. Tools like Chef and Puppet help generate configuration files that programs can read. A configuration spider would allow detecting and connecting the relationships between these configuration files.

The spider would scan for configuration files, identify port numbers, paths and hostnames to insert into a graph. When the spider detects a reference to the same value, it creates an edge from both usages to the actual data. This graph then becomes a reprsentation of system configuration, the edges link the configuration values are live and synchronized, an administrator can change the data in a single location and cause the usages to update. This could be rendered to the screen as a graph.

## 15. Community Idea: [Create This](id:create-this)

This is like the [Design This](#design-this) but in reverse. Designers create a design and a developer creates a backend for the site. Ideally suited to open source projects.

## 16. "We Want This" (The Reverse Kickstarter)

A group of people want to create something but do not have the time or energy to create it. They collaboratively decide what they want and raise funding.

 * users form committees to oversee the development effort
 * committees create 'open positions' as roles to fulfil
 * users who possess the required skills for a role offer to work
 * experts get paid, committee gets idea implemented

This is like a 'reverse kickstarter' or a petition.
 
Existing:

 * Kickstarter, in reverse

## 17. Clientside Bubble Routing

Bubble routing is an approach to detecting and handling events on the clientside. Most frameworks do not use bubbling to its full potential, they create a handler for each area where an event needs to be handled and stop propagation once it has been handled. Bubble routing uses a single event handler by taking advantage of the natural structure of the DOM and bubbling. Each element the event passes through enhances the information of the request before it gets to the topmost level where the event is actually handled.

 * Example: http://fiddle.jshell.net/SWrX5/17/


## 18. Shortcut Format

Keyboard shortcuts are configured differently in each program. Shortcut configuration should be in a standard format. This way you can load them and share them between operating systems and share configurations between applications.

 * A user should be able to use the same shortcut configuration in one browser as another.
 

## 19. Separating Frontends and Backends

Good design separates the frontend and the backend. This should be the case on the desktop too. If frontends and backends were separated, one could use the same underlying mail or instant messenger client but switch between frontends. Backends and Frontends would communicate according to some protocol.

Existing:

 * Node Webkit
 * [Tablizer's SCGUI](http://www.geocities.com/tablizer/scgui.htm)

## 20. Desktop Windows and File Management Features

These are some features for file exploring programs I have always wanted. Some already exist.

When I right click a [representation of a file](#elements-represent-themselves) (such as an icon or a filename), I should be able to interact with the file or folder in a many different ways:

 * `Put in New Folder` asks the user for a folder name and puts the selected files into this folder. The user does not have to create a new folder and manually move the files across. ([existing as Files 2 Folder](http://skwire.dcmembers.com/fp/?page=files-2-folder))
 * `Pull out of Folder` move the files in a folder out of the directory
 * `Copy Path` I shouldn't need to open a properties dialog to copy the path from or construct the path myself.
 * `Storage Usage` right click and view disk usage of the file in relative to everything else on the storage device
 * `Outsource` move the storage of the file elswhere but keep a link to the file here
 * `Compress`, `Convert`
 * `Security Settings` Add file permissions, encryption and enforce rules.
 * `Share` Make this file available to another person or machine.
 * `Add To Backup` You have a backup configured and you want to add this file or folder to your existing backup procedure.
 * `Tag`
 * `Merge Folders` 
 * `Resize` for images, videos
 * `File History` View changes of the file over time.
 * `Usages` Find references to this file from elsewhere in the file system such as in email attachments or as referenced paths.
 * `Search` Search the contents of the file.
 * `File Structure` Inspect the high-level structure of the file (such as a archived file) and any nested file systems or learn about underlying file format.

In the detailed list view for a folder, I should be able to see the following:

 * `File Indicators` A file or folder that is being used or processed by another running program should be obvious from the file explorer. If a file is open in another program - show an icon of that program. If a long running process is running involving the file, progress bars should appear near the file such as a progress bar for files being downloaded, copied, scanned or backed up.
 * If the file is not physically present on this machine, show icons that represent the storage services or rmeote machines that the file is available under.
 * Add arbitrary columns in file viewer. Columns can be loose - the columns displayed a the top do not necessarily have to be filled by every file. What would be better is if files that have custom files show another column header.

From open windows, I should be able to:

* `Share Window` share an open program with another machine.
* `Mute Audio`

Existing:

 * Some of the above are available in [KDE Services](http://kde-apps.org/content/show.php/?content=147065)
 
## 21. If you can see it, you can use it (SIUI)

This is the principle that if you can see some data on the screen, even in different window, you should be able to use it in your active program. On the command line, 'use it' means 'refer to it', such as the path of a file icon or a file path on the shell.

Take the output of git status for example:

```
# On branch master
# Changes to be committed:
# (use "git reset HEAD ..." to unstage)
#
# modified: file.ext
#
# Changes not staged for commit:
# (use "git add ..." to update what will be committed)
# (use "git checkout -- ..." to discard changes in working directory)
#
# modified: file2.ext
#
# Untracked files:
# (use "git add ..." to include in what will be committed)
#
# file3.ext
```

If you want to refer to a file name in the above, you could type it out and use your shell's auto-complete functionality. You could copy and paste it with the mouse or your terminal multiplexer. You should be able to refer to paths mentioned directly.

 * A program puts the paths into environment variables. The output of the program is adjusted to add numberings such as:
 
```
# modified: file.ext [1]
```
 Now I should be able to refer to the 1 in some way, perhaps `$m1` now stands for 'the first modified file on the list' which is 'file.ext'.

 * Hint mode places an overlay over the interface and numbers various things on the screen to be clicked. (see vimperator hint mode)

Existing:

 * [Plan 9 ACME](http://doc.cat-v.org/plan_9/4th_edition/papers/acme/) (clicking certain strings has behaviour)
 * TermKit
 * Vimperator / [Pteradactyl](https://en.wikipedia.org/wiki/Pentadactyl_(extension)
 * SCM Breeze or similar programs - this is limited to Git but its functionality should be part of the desktop environment and the shell

## 22. Shell as REPL

An invocation of a program on the terminal and its output could be interpreted as an assignment to variables in the current scope. The output of the program should be useable to the user. The developer should be able to interact with the shell or the output in a language of choice.

For example,

```git status -s```

Gives me the status of each file and the filename. If I want to use this data in Javascript or in Ruby I have to parse this text manually. Ultimately the structural output of this command is this same every time. There is a list of structure data with a consistent format that could be idiomatically represented in many languages. In Javascript this could be:

```
{"file": "hello.py", "status": "modified"}
```

The output of the Git command should be treated like an object that has already been parsed and interactions are already possible.

```
output.modified[0].file
```
This could be implemented lazily so that the effort to parse the output is not made until the user attempts to access fields.

Shell operations may be simpler as programming constructs. This way one could use the shell programmatically, in different languages.

```
wget http://example.com/ |  
(require '[cheshire.core :refer :all])
(require '[clj-http.client :as client])
(let [input (parse-stream (io/reader *in*))]
	(client/post "http://localhost:8383/" {
		:query-params {(input "m") (input "l")}
	} )
)
```

Existing:

 * [Haskell shell scripting (Shelly)](http://www.yesodweb.com/blog/2012/03/shelly-for-shell-scripts)
 * TermKit

## 23. Live Data

The display of data - perhaps through widgets or in documentation should be synchronized when the underlying data is updated. When something is changed in one location, all views of that information should be updated.

For example:

 * You change a keyboard button setting in an application, the documentation should automatically update to show the active shortcut.
 * An application is customized to change its appearance. The `screenshots` in the documentation should update accordingly.
 * Applications that want something but cannot function such as an internet connection or are waiting input should know and continue when the desired state is restored.
 * If the user has a window minimized for a while and the window has changed since it was last viewed, there may need to be a visual indication that something has happened or changed, such as a green or red fade effect.
 * The data on the screen should never be stale.


Existing:

 * When a folder is open and a file is added, the file should appear in the folder.
 * Observables


## 24. Error to Issue Tracker Linkage

If every compiler error is automatically converted into an issue and then automatically closed when it is absent, this would give visibility to problems that were solved and which still remain. This could be integrated with a build system.

There should also be some kind of mapping between the product's error state and a potential issue number. Currently the connection between an error condition and an issue in a tracking system is completely human - someone has to manually enter the error into an issue tracker and update the program to refer to it. Bug reporting should either be intregrated into an application or interpreted by the desktop or container environment. The error state should be detectable and linked to the issue tracker.

 * An graphical application facing an error condition typically reports errors a dialog. This dialog should display the known cases that cause this error. This is possible because Error Condition X was mapped to Issue Y which had associated Reason Z.

``` 
Error copying files: drive removed. Typically caused by:

 * Unplugging drive during copy 		[I didn't unplug it]  
 * Internet connection lost				[Diagnose internet connection]
```
```
 Compiler error: undefined is not a function (line 13)  
 	> A variable on Line 13 is undefined
 ```
 
 Potential integrations:
  
  * [Software metadata for the error reporting servers](#software-metadata)

## 25. Error Heuristics

Errors have numerous causes. Once an error becomes common enough and becomes common knowledge, it may not be justified to adjust the program to provide a better error mesage because the error is human. Separate tools can take advantage of heuristics can provide better insight to the problem. For a compiler error, this heuristic knows where to begin its search. These tools do not necessarily need to check if the error exists, they merely provide heuristics that help narrow down the problem. For example:

```
Line 13: user.mailboxes()[selectedMailbox].preferences: undefined is not a function
	> `user`, `mailboxes` could be `undefined`.
```

```
Error: install is not defined
 > This was reported as fixed in version 1.3	[Open update manager / run package-manager update x]
```

```
Expected ; saw }
 > Function expressions should be followed by a ;
 > Mismatching curly brackets, counted 4 {{{{ and 3 }}}
```

Existing:
 
 * Windows Reliability Problem and Reports
 * Brew Doctor
 
## 26. System-wide Data interpeters

There are many data patterns that are not explicitly marked up.

 * phone numbers
 * addresses
 * line numbers
 * units of time, standard measurements
 * paths, filenames, extensions, port numbers
 * system commands
 * standardized reference numbers
 * SHA, MD5 hashes
 * URLs
 * System or network usernames, hostnames

Data classification algorithms can be ran against the text displayed on terminals or within graphical programs. This could be deferred until the user interacts with the information, perhaps on mouse hover or clicking on the information.

Existing:

 * Mailto links
 * Protocol handlers
 * Contextual computing / Representational computing

## 27. Applications Expose Data Visually and Programmatically

The data that is being rendered by an application can be inspected and used as a datasource for another interface. This should also be programmatically accessible.
 
 * An open folder manager window has a folder open. Amongst other things, this can be interpreted as a list of dates and times (for the files in the folder). A calendar program can read and display the sequence of dates and times to show when files were created/modified along a timeline. This may be useful with photographs.
 
 * A spreadsheet program is opened and contains a sequence of dates. When the user views a date in a different application or on a web page, the environment refers to the spreadsheet filename.
 
 * An application or form on a website is requesting a piece of data. Data of the same type is also being displayed in another user interface. Selecting the input field will display a list of potential sources of this information, one being the active application.
 
This functionality would be user driven as to avoid performance issues. If I want to see what an application is using or doing:

 * I should be able to 'inspect' a program to view various aspects of the program. This could be a tree view that shows resources the application is using, what components have been loaded, the data loaded into each widget the modules are loaded. I should be able to see the internals of the application but in a high-level way. This should be queryable programmatically and useable in a distributed setting. ([explorable context](#explorable-context))

Similar:

 * [lennier's comment on desktop environments](http://tech.slashdot.org/comments.pl?sid=2585722&cid=38456084)

Existing:

 * Process Viewers, Sysinternals
 * Object Linking and Embedding
 * Registry editor
 * Microsoft SnapIns, Windows Management Instrumentation
 * procenv
 

## 28. [Representations are Tests](id:representations-are-tests)

A representation dictates what something is and what you can do with it. A PNG file, a JSON document, C sourcecode or a HTML file are accepted as inputs by different applications and operations. How do we know that that applications are interoperable and compatible? Representations can be inferred by the tests that they pass. This is similar to a type inferring programming language: we can build tests that represent high level qualities about applications and data formats. These are some high level examples that reason about the outputs or characteristics of programs or representations:

 * An sort algorithm that is stable or unstable.
 * Benchmarks to estimate space and time complexity. ([similar to cost aware computing](cost-aware-computing))
 * A library that accepts files at different levels of compliance.

If programs are representations too, they could even be interchangeable. For example, a HTTP client can execute HTTP methods taking various body data with request headers and return response headers and data. The client could be implemented in many different languages but this described interface is the same regardless of the language. If I import the 'HTTP Client' representation and use HTTP methods, this will result in calls to the underlying HTTP library. This would require wrappers that wrap the real library with a generic interface. Alternatively I was hoping that test cases themselves help describe the interface because test cases for libraries inevitably involve calling the libraries. For examle Apache HttpClient and the connect library in node each have an interface to GET a page by URL which will probably be a string. A sufficiently structured test case may even be able to create a picture about the expected inputs, the interface and the outputs. This could even use mocking or stubbing libraries to 'record' calls to library functions. Essentially we want to map our subset of data and outputs to a real library.


## 29. Community Idea: API Competition

Libraries compete on performance and API design. The statement of the problem stays the same but can be solved in multiple ways. For example:

 * an API for making HTTP requests
 * a query language for data
 * database backend query implementation
 * widget APIs
 * sort algorithms
 * client side web frameworks

APIs proposed should be voted and discussed. Implementations can be attempted.

Existing:

 * Js Perf
 * Benchmarks


## 30. [Widget Servers](id:widget-servers)

([see graphic](widgetservers2.png))

It should be possible for design and development workflows to co-exist and to work lockstep. Modern architecture splits web applications into layers and separates data, presentation and logic. This separation is inadequate for designers. This can manifest as designs being implemented top-down into the presentation layer. Depending on the architecture, aesthetic or functional changes require development effort. A triple architecture separates and provides tools for the tasks:

 * Creation of the design and style of pages and their components complete with dummy data and all the different states that the widget can be in. (Design, User Experience/Design)
 * Specifying what kinds of data the widget 'wants' to display. (Analysis, Design)
 * A service that when requested, returns the widgets that need to be on the page
a service that turns widgets into data requests. (Widget Server)
* A backend service stores and returns data. (Storage)
* A backend service that handles business logic. (Business logic)
* The association of 'stories' or 'criteria' or 'situation' with widget and widget state (Management)

Different people can work on the above in parallel because they are working with interfaces.

 * Backend business logic
 * Creating widgets or website components
 * Organizing and placing widgets onto pages


Potential integrations:

 * Explorable Context/What can I use 
 

## 31. Mounting Sourcecode

Sourcecode we compile or execute need not be the same as that rendered to the screen. Developers should be able to work on the same code base but view sourcecode in different ways. Mounting a source directory means we can apply bidirectional transformations between the stored sourcecode and what is opened in a text editor.

Coding style preferences can be configured on the mounted source code so that it appears according to the developer's taste. Developers can choose indention rules and spacing settings without affecting other developers. This is is like mapping between two [EditorConfig](http://editorconfig.org/) configurations automatically.

Personal preference also changes how people like to organize sourcecode by directory. Directory structures can be equivalents:

```
 - src
  - models
  - controllers
  - views
 - docs
``` 
```
 - modules
  - users
   - controller
   - model
  - products
   - controller
   - model
 - public

```


Potential integrations:

 *  Branching libraries

## 32. The Built-In Enemy

Users are not informed about security issues waiting to happen unless they:

 * read documentation properly
 * read start-up warnings
 * check mailing lists or online communities
 * update packages frequently

The 'Built-In Enemy' is a suite of heuristics that find security problems on a machine. Examples:
 
 * versions of libraries or running software
 * permission problems, the permissions of running applications (user, group)
 * exploit frameworks that run expoit attempts locally
 * looks for known in known versions of software
 * looks for weaknesses in the SSL certificates

Existing:

 * anti-virus software
 * [Secunia PSI](http://secunia.com/vulnerability_scanning/personal/)

## 33. Personal Infrastructure

Individuals lack personal infrastructure for photographs, videos, email or other services. User data is locked into assorted individual applications from vendors and service providers. A personal infrastructure is a set of machine instances or distribution of software that create a useful and serviceable infrastructure.

 * email server
 * catalogue, photograph management
 * backup provision
 * synchronization

Personal infrastructure providers could take the same approach as business hosting or cloud providers. They sell use of the infrastructure but provide value added services.
 
Personal infrastructure providers should start a trend where they provide not only the front end applications or web clients but provide direct access to the backend machinery hosted in the cloud. This would cater for power users and casual users.

PI could be distributed as a virtual machine that includes:

 * VPN software for securely logging on
 * file server
 * file synchronization tools
 * collaborative text editor (such as etherpad)
 * certificate authority, key management for security

Existing:

 * 'personal cloud' providers such as [Tonido](http://tonido.com/) and [OwnCloud](http://owncloud.org/)
 
## 34. Bluetooth Friend Mesh

Modern mobile phones are powerful and possess large unutilized CPU power. The resources available to a phone such as images, videos, maps, software and cached websites should be shareable in a mesh when people get physically close to one another.

 * People in the work place. Family members. Friends at a restaurant or a meetup.


## 35. Edit Servers: Team Active File Visualization

People working in the same area of software can cause problems where integrating changes is difficult. Decentralised source control systems mitigate integration pain but they do not actively help prevent it. As a user enters a file, the user's position, the following information is announced:

 * File level: file name, path, line number and column
 * Language level: method name, class, symbol name, module
 * Project level, functional area

Users can therefore be warned when a user attempts to update something that has also been changed by someone else. For example:   
 
 * A user opens a HTML template or XML file, this triggers an announcement that the file is open by a given user. If any other users then open this file, there is a list of users that also have this file open.
 * The current cursor position is indicated in the editor, perhaps in a certain color.
 * No warnings are raised unless changes are made.
 * When the user enters makes a change to a node in the HTML/XML file, this registers a change at this position in the file.
 * Any users who also enter this node will be warned about conflicts when they attempt to change the file.
 
This should permit multiple users editing the same file without tripping eachother up.

Existing:

 * any collaborative text editor such as Etherpad

## 36. Documentation Linked Code

Documentation and wikis are prone to fall behind a code base. Creating documentation from sourcecode or embedding documentation in the sourcecode are approaches to keeping documentation. Documentation and code should be linked together in such a way that it is difficult for it to fall out of date.

 * When code is visible in an IDE or in a text editor, the **relevant** documentation for this area should be quickly available to edit. This could be a panel, a tab or a split view that updates to always display documentation.
 * Documentation acts as a specialised test case. When example code in the documentation no longer compiles the build should fail.
 * Documentation should be linked to refactoring operations. When variables are renamed or code is moved, all the references to variables and methods should automatically update.

## 37. [Code Overlays](id:code-overlays)

Code overlays can make sourcecode more like a document and easier to read. Source code editors make poor use of space when rendering code. For example:

```
someLongMethodName	(type identifier, type identifier, type identifier,
					type identifier, type identifier type identifier
					type identifier, type identifier, type identifier)
```
Code quality problems aside, an IDE does not necessarily need to display this exactly the way the source is. There is wasted space below the method name. An auto-indenter could align the source perfectly but this seems like catering to the plaintext format of sourcecode rather than the expressive power of a user interface. 

This could be rendered like a table:

`someLongMethodName`

Type |	Argument	| type	| identifier | type | identifier
---	 | --- | --- | --- | --- | ---
type | identifier	| type | 	identifier | type | identifier
type | identifier	| type | 	identifier | type | identifier
type | identifier	| type | 	identifier | type | identifier

This tabular widget would permit moving cells up and down or lett and right to manipulate the ordering of the arguments list. This would update the ordering of the underlying sourcecode without using a refactoring dialog.


## 38. Code as a Wiki

Code is inherently linked and related. This is similar to wikis and the nature of hyperlinks and the web.

 * Code can be navigated as a wiki.
 * Edit code in the same style as a wiki.
 
## 39. Data Trails

The data on your screen has a trail of influence. Multiple sections of code are touched before output is displayed.

 * There is data displayed in a widget. Viewing the influences of this widget would show the source of the data such as the file, the API that was used, the connected database, the query that was executed.
 * An error is displayed, viewing the influences of this data will show what component the error was raised in and the configuration of that component.

## 40. [Input Services](id:input-services)

The embeddable widgets that platforms provide should be interchangeable and interoperable. Currently the choice of widget libraries is made by application developers rather than the user.

 * Text input edits should be configurable. It should be possible to choose what text editor to use for your applications. Perhaps you want to use advanced text editors or. 
 * Pick a calendar field editor.
 
## 41. Drill-down Interface

A widget represents data on the screen. It has a limited amount of space because it must co-operate with other widgets on the screen to give the entire screen meaning. Widgets are constrained horizontally and vertically. The amount of data that widgets should display depends on the current geometry. A drill down interface would allow to the user to inspect a particular facet of the interface and give it more importance, perhaps by double clicking it. This would trigger a resize of all the widgets on the screen to accommodate the user's change of focus. This would result in widgets disappearing and others appearing.

 * User Interfaces should not be considred merely the output of a program, they are an interactive program separate to business logic that the user drives and is in full control.

Examples:

```
An email client shows a panel of folders, an email preview pane and a detailed table of emails

 - Drilling down into the preview pane would make it much larger and provide a small reply box.
 - Drilling down into the folder view would show you all your folders, the rules associated with each folder and email addresses.
 - Drilling down into a contact's name on the detailed table would show various contact details of that contact, the emails and attachments that you have sent and received from this contact.
```

By pulling information relevant to the facet being inspected, user interfaces can become more useful.

This could be implemented as a zoom effect where the focal widgets are scaled upwards and less relevant widgets disappear as if they were to go past and behind the user.

A drill down interface is unlikely to be easy to design for because combinations and relevance would have to be determined in advance.

Similar:

 * Hypertext and embedded Hyperlinks within web applications can be considered a drill-down interface but is disjointed because the interface can change drastically between pages.
 * Dialogs that pop-up when clicking in order to provide more relevant functionality. Edit, summary buttons and 'more information' are examples as they often trigger popups or foldout panels to handle a user's change of focal point.

Potential Integration:

 * Designers can use an [explorable web](#explorable-context) as a way to decide what facets of the interface are important. They can then create various designs for different facets of data.
 
Existing:

 * [Eagle Mode](http://eaglemode.sourceforge.net/index.html), [Server monitoring demo](http://eaglemode.sourceforge.net/servmonvideo.html)

## 42. [Context As an Explorable Web: What can I use?](id:explorable-context)

The context available in a given situation should be easily accessible and discoverable. A context tells a story and gives way to opportunity. This information is cucrrently discoverable through consulting documentation, asking questions or using debugging tools. Development environments should present what has already been calculated and what is available in an easy way.

 * **Controllers** A web application request involves fetching data, processing and other tasks. What has the user provided? Where were they trying to go? There can be an element of duplication to this data and processing in a complex application. Cached data from previous queries can be taken advantage of.
 * **Templating Languages** the various data available to the request such as inferred information about the user or the user's current position in a flow. Already rendered widgets can also be re-used.

For example, a request is made, the server knows what user is making the request and the user is in a particular stage of the workflow. Information about the previous stages of the workflow is part of the context of this request. This data can be rendered in an interface to show what really is available - seeing the data available makes it easier to find out what you want to use when you don't know what you're looking for.

## 43. [Cost Aware Computing](id:cost-aware-computing)

Algorithm complexity and hardware specific characteristics could mean that a given algorithm or library is more optimal for certain configurations. An algorithm used on a desktop may not always be the best on a mobile phone. A library used on a server may not be useful on a laptop.

The operating system or host environment could pick the best algorithm depending on various conditions:

 * resource pressure (memory, system load, network throughput)
 * hardware specification
 
 Existing:
 
  * database query optimizers

## 44. [Interface Defined At Authorship: Meaning Added Later](id:idaa)

You want to create a document. You want:

 * videos, images, audio
 * outputs from web services, database query results
 * files from the filesystem or remote storage 

Traditional content management tools define rigid input formats and inflexible GUIs for inserting content.  Exacerbating this inflexibility is the tight coupling of this input interface to its display. There is a one to one mapping of input to output. This model is at odds of how well people understand tools: while writing a document, I do not care or even know how I'll integrate other content into my article. What's important to me is that I can insert placeholders for content and have these placeholders be processed later. In fact, I might not even be the same person who integrates the content together because I might be a content producer, marketer, designer or a journalist. 

I might not know how everything should look or act in my article until later. A tool should allow me to:

 * **Specify the Placeholder (or Intention)** When I want to include something on the page, I should specify what I am adding. This could be, 'gallery', 'price of item X in database', a reference to a Twitter hashtag or a presentation. This could be textual description, a tag, a RDF/N3 or some kind of relationship that identifies the added content in some way. This could even be a description of what the content creator wants to include - a note or requirement for consuming by a developer or the designer behind the website.
 * **Embed the Known (Data)**: This is the actual content known at the moment of authorship. Likely this will have a known format and meaning. This may be a file path, URL, description of a HTTP request, hostnames, port numbers, actual sourcecode and arbitrary XML elements. Sometimes there will be no data and the intention is data, in this case the intention is simply a transclusion point.
 * **View the transclusion points** This is the most important part. This is an interface that displays all the places where particular intentions/placeholders have been used. This is like a workflow system that shows all the 'unresolved' placeholders. Some placeholders/intents are implicit, such as URLs which you may wish to handle specifically depending on the address.
 
By treating the transclusion points as independent items to be tracked and controlled, we have better control of content that can evolve over time and stay consistent between pages. The transclusion points are 'holes' to be filled by some arbitrary process defined in the future or not at all.

 * **Handling a transclusion point** We can define `content handlers` to handle transclusion points. This is a mapping or function that takes the `intention`, the `data` and the `context` to produce `output` for  transclusion. (`handler(intention, data, context) → output`)


For example, this is an excerpt from such a user interface:

Description | Handler | Uses
---	| --- | ---
`<video/>` XML element | YouTube, Vimeo URL handler | Used on 4 pages |
`<gallery` XML element | 2 handlers: Slideshow handler, Embedded Flickr handler | Embedded Flickr: 5 pages<br/> Slideshow: 1 page |
`#` | Hashtag | Twitter link | 
`[bbcode][/bbcode]` | BB Code handler | Used on 1 page |
`<sql>` XML element | No handler registered | Used on 2 pages |
`<code>` HTML element | No hadler registered | Used on 5 pages |

Interface defined at authorship is similar to mail merge except the user does not care about the 'field format' and how the fields are transformed can be customized. IDAA can make web development simpler as content creators, designers and programmers stay in their respective domains working in parallel.

The interface part refers to how a developer did not actually specify how data should be input to give the data meaning. Detecting potential meaning is possible providing there are generic handlers such as XML elements.

Potential Integrations:

 * Microformats, microdata, semantic data
 * [Living Documents](#living-documents)

Existing:

 * Mail merge
 * MarkupControl
 * The Semantic Web
 * static site generators
 * Wiki transclusion
 * Word processors, Master documents and transclusion
 
## 45. Community Idea: Secure Configuration Distribution

Many applications ship with default configurations that are more likely to be vulnerable. A communiy could discuss the security of configuration options and offer files or patchers that ensure that common applications have proper settings. Examples would be preconfigured settings for Firefox, Chrome, Adobe Reader and Word.

## 46. RESTful Living Documents

The semantics of (`handler(intention, data, context) → output`) described by [IDAA](#idaa) could be handled by REST architecture where every inclusion is actually the definition of a HTTP request.

For example, an image is frequently needed in multiple resolutions, sizes and quality. Typically these variants are named based on size or purpose and uploaded separately. A IDAA REST architecture would map the intention  to the HTTP protocol. For example, a website logo with a single name (http://example.com/logo) that appears in the header of the website might have a content type of `header logo` while the logo for the footer has a content type of `footer logo`. From a consumption point of view, this is might be easier to understand than having a header-logo and a footer-logo file and keeping these files up-to-date. How these resources are actually fetched depends on the handler - it may be preferable for the designer to refer the intention of a logo but have developers map the content-type to plain directories.

Potential integration:

 * [Triple/Widget architecture](triple-architecture)
 * MIME
 * HATEOAS

## 47. Group and move sections lists easily

Moving around blocks of text through online rich text editors and default browser text editors is painful compared to dedicated tools.

Existing:

 * Outliner software
 * Mind Mapping

Potential integrations:

 * [Input services](#input-services)

## 48. Branching Libraries

Many frameworks and application architectures simply provide common abstractions for branching on input data, such as, given X then do Y. For example:

 * web frameworks that provide a routing and middleware APIs allow tying code to HTTP requests
 * command line argument processing libraries allow tying code to combinations of options and positional arguments.
 * browsers provide allow creation of event handlers that allow one to tie code to DOM elements that handle user inputs such as click or mouseover events
 * agent, actors that respond to messages
 * git hooks tie code to source control actions

Sometimes we want to use X as if it is a Y. Principles in one area can be used to tackle something in a completely different area using a non-traditional style.

 * Read or query a document or expose a SQL database as a file system as if it is a file system. (xmllint shell, SQL FUSE drivers)
 * Expose a web application API as a command line application.
 * Convert FUSE calls to REST semantics
  
A branching library allows the branching conventions of one ecosystem to be used in another which can potentially speed up development and permit reuse. Of course these have to be specifically implemented.

Existing:

 * [Zapier](http://zapier.com/)
 * FUSE, Ferris, component object models, web frameworks like Express and Sinatra
 * [Camel](http://camel.apache.org/)


## 49. Linked Representations

A file can typically be converted between formats. Sometimes it is necessary to keep a file available in multiple formats, such as a HTML file and a PDF. In this case it is desirable that:

 * whenever the HTML changes, the PDF is updated
 * when the PDF changes, the HTML is updated

Linked representations would be useful when files that are combined to create others or its converse when files are split to create others.

 * an sprite file, game tile
 * web designs that are split into assets

A linked representation would automatically split the files when a source file is changed or trigger a combining action when the components are changed. If software is written from composable actions or through [data `views` on the underlying data](#data-views), this could even be bidirectional. This would mean that editing the source image or the individual pieces would cause the other to be updated.

Existing:

 * Everything is a file (Plan9)
 * Saving a web page completely results in resource directory that appears adjacent to the HTML, even when moved.
 * Makefiles, compilation, linkage


## 50. Renderers

In a [living document](#living-documents) it is infeasible to manually markup all semantic information. It may be nicer to scan or interpret documents and automatically insert meaning.

Example | Handler | Uses
 --- | --- | ---
`555-555` | Phone number handler | Used on 1 page | 
`744` | UNIX Permissions handler | Used on 3 pages |
`~/known.file` | Known folder | Used on 5 pages |

This can be accomplished through dedicated programs and regular expressions.

 * detect phone number: clicking might cross reference to the number's owner in the user's address book or offer a telephone dialling service
 * Using a keyword from a programming language may link the keyword to relevant documentation or known location in the codebase.

Existing:

 * Mail clients that interpret phone numbers, dates and times for calendar integration.

## 51. Native Web Libraries

Web libraries are natively implemented versions of Javascript libraries. The interface of a web library is actually Javascript. A web library is always written in Javascript first. When performance problems need to be resolved, the moving parts can be implemented in a non-Javascript language and installed in the browser.

The idea is that native libraries can be added to stand-in for Javascript-libraries purely for performance reasons. These native versions would be able to act directly on the browsers internals as if the API calls were native. There should be no difference in functionality between the Javascript library and the web library.

```
navigator.require('http://example.net/library')
```
Where `library` is a URL to a Javascript file that is used as a key to find an installed web library. The Javascript version is used as fallback.

Usecases:

 * jQuery vs document.querySelectorAll
 * number abstractions
 * video and audio codecs
 * encryption

Potential integration:

 * Automated aspect oriented development - mapping particular Javascript function calls to native calls while leaving the rest in the Javascript engine. (cut points in Javascript)
 * Component loader frameworks

## 52. Account Management Protocols

Manging digital accounts is tedious as each account provider has its own graphical interface and no machine readable API. An account management protocol would allow the following:

 * changing of password
 * updating of email address and personal details

This would allow a user to change an email address or personal details once and have it take effect everywhere.

Potential Integration:

 * Password databases

## 53. Web State Machines for Testing

A web page can expose a state machine to indicate multitudes of state in the web application. The state transitions can be updated incrementally as things happen or as an on-demand introspection. A testing tool can therefore verify behaviour between interactions.

```
pageobject: {
	"warning.visible": true,
	"searchterm": "buckets"
}
assertions: {
	"warning": {
			visible: true
		},
	"search": {
		"value": "buckets"
	}
}
```

A page in a web application can be modelled as its own API of user behaviour.


## 54. [Community Idea: Tech Stack Slice](id:tech-stack-slice)

There is no website that allows the comparing different technology stacks. There would be a page for every permutation of technology, for example the following might be common technology pairs:

 * MySql and PHP
 * Node and MongoDB
 
These pairs can included in complete technology stacks such as linux, apache, MySQL and PHP (LAMP). This may go increasingly in depth to particular database abstraction layers, web frameworks and libraries. Each page will have a list of advantages and existing projects using this stack. As projects are added, the stacks will become more specific. Attributes from individual technology interactions will rise up to the entire stack.

As a user of this site, I may begin by exploring:

* Pick [ programming topic | programming language | technology | category of technologies ]
* Pick a [ programming problem | constraint | target platform ]
* Drill down into a technology and stack combination.
* Show existing projects or products that used this [ technology | category of technologies | architecture ]

Existing:

 * WikiMatrix, ForumMatrix, Alternative.To

## 55. [High Level Project Overview](id:high-level-project-overview)

When joining a project, there are high level asserted approaches to solving problems adopted by the project. This can be choice of technology stack and style of architecture. I should be able to see this in a single page.

 * This could be a series of lists in sections with headings such as 'Data Storage', 'Protocols', 'Architecture', 'Code Conventions' and 'Project Style'.

This overview should be an easy to update and shareable.

## 56. Use Microservices in Projects (Microtools)

We do not always need a heavyweight system for maintaining data. Wikis and document files are frustrating to update and typically fall out of date. Microtools are very specific tools unlike Wikis and management software, they serve a single purpose and make keeping track of data as simple as possible.

 * **updating a list of servers in different environments**: Server X has hostname Y and IP Z and is in environment A.
 * **important project contact details**
 * **project setup instructions**: A special to-do list specifically for maintaining setup instructions.

To be lightweight but useful, these examples could be implemented:

 * as simple command line utilities that operate on plain text files
 * as simple web based single page applications
 * with simple APIs to add items and fetch items programmatically


## 57. Acceptance Criteria Issue Tracker Intregration 

```
WHEN I click the search box
AND this is my first time I've used the search box
THEN the text should be cleared
```

This acceptance criteria follows the convention for `WHEN` and `THEN` in BDD style. Developers or testers may write automated tests with BDD tools and copy these strings into sourcecode. This is introducing a gap between where the ACs are defined and the place where they are tested. Ideally the testing should occur against the story and the AC from the story is the souce of truth. The following has taken the AC from the control of non-developers through copying AC into code:

```
var ac = {
"I click the search box": function () {
	searchbox.click();
	},
"this is my first time I've used the search box": function () {
	return searchbox.hasBeenUsed() === false;
	},
"the text should be cleared": function () {
	return searchbox.isEmpty() === true;
	}
}
```

```
ac("I click the search box");
ac("this is my first time I've used the search box") &&
ac("the text should be cleared")
```
If the story and AC changes in the issue tracker, the above test will still pass.


Strings may not be the ideal representations of acceptance criteria for they could change. AC may have similaraties with other stories and duplication creates maintainability problems. These may need a more robust link against the code that tests them.

Builds now run acceptance criteria tests so that functionality is not broken through future changes.

Potential integration:

 * Existing BDD frameworks.
 * Feature toggles

## 58. Microtests: Cross-Project Test Suite

Many bugs have common symptoms. These symptoms could be collected into a suite of tests that apply to all projects as a form of sanity testing. The following should trigger errors:

 * keywords such as 'undefined', 'null', 'nil' appearing in HTML
 * an element on the page containing no children
 * javascript error on page load
 * XHR requests that contain keywords like 'undefined' or 'null'
 * server responses that contain keywords such as 'null', 'undefined'
 * presence of strange or meaningful numbers such as '-1', '32768'
 * saving a file with accidental junk data at the end (such as vim :wq)
 * empty drop down boxes on a web site
 * throbbers that never stop throbbing
 * random symbols at the end of lines (after ;)
 


## 59. [Security Proxy](id:security-proxy)

The internet has made it easy to leak sensitive or confidential information. A dedicate web proxy could scan all traffic for keywords that match known sensitive information and reject it. This requires users define what they deem sensitive.

This is especially important as data is always being passively collected by web pages in Javascript.

Potential integration:

 * Password databases
 
## 60. Operating System Field 'Firewall'

Form fields and widgets are sanitized for sensitive information before being made available applications. This prevents information being pasted accidentally. This is like [security proxy](#security-proxy) but for input fields.

## 61. Visual Git Release Management

The branches of Git projects can be visualized as connected circles where branches are created and merged back. It would be nice to generate a live version of this diagram horizontally so one can follow development of a project and understand the release structure.

Existing:

 * Gitk but readonly

## 62. Salary Structure as a Program

An open source program could determine your salary. There may be various criteria that the program records and tracks so you are paid properly. There would be chains of verification of facts to prevent abuse. This could be tested and should maximize transparency in an organization.

Similar:

 * Tax as a transparent open source program
 
## 63. Website Annotation

Adding notes to websites can function as a form of memory aid. It should be possible for me to add and save notes to a web page in case I come back later.

## 64. Peer to Peer Backup

Backing up files to family and friends makes sense as a form of distributed off-site backup. This has been done by numerous services such as:

 * [Crashplan](http://crashplan.com/)
 * [Wuala](http://wuala.com/)

Security could be enhanced by ensuring files are broken up into pieces in the style of Bit Torrent.

Potential Integration:

 * [OneSwarm](http://www.oneswarm.org/)
 * BitTorrent / BitTorrent Sync
 
## 65. Open Source Subscription and Bounties

Open source projects benefit from contributors and financial contributions. Donations have more impact when they are larger and by multiple people. A open source subscription would be a monthly payment that combines donations from multiple people into one large donation for a project of choice each month. The community would vote what projects to donate towards. Donations have no expectation of special requests or work to be completed.

Open source bounties would be to implement a new feature or fix a bug.

Existing:

 * [BountySource](https://www.bountysource.com/)
 
## 66. Wizards and Forms Request Data

Many website forms and native applications with wizards request data across multiple pages. These applications should expose the entirety of the data they are asking for through a scriptable interface.


## 67. Hardware Review

A hardware reiew process shows how powerful your current set of detected hardware is.

 * show which components are letting your machine down
 * show approximate value at release vs current value
 * show benchmark results
 * shows release date and hardware generation
 * shows what applications might struggle with this configuration

Existing:

 * Windows Experience Index

Potential integration:

 * benchmarking applications


## 68. Right Click Outsource

Task management between computers is an unsolved problem in desktop environments. Many users have multiple devices. Sending tasks, inputs or outputs to different computers is painful. Usually sending audio to be played through another computer, taking control of an application running on another computer, sharing files or streaming data to other machines requires special software. 

 * I should be able to right click a running application and select `Outsource`. This will move the application to another computer. The frontend will probably be connected to the current machine but the processing will be moved elsewhere.
 * I right click the an indication of audio playback such as the volume control of my desktop environment or in an application, I select `Outsource` and select another device to play audio through.
 * I right click a directory on my machine and select `Outsource`. These files will now be moved to another device but still be available in the current directory.
 

## 69. Internal and External Configuration

There are two kinds of software configuration. Internal configuration is that application directly uses such as a browser and its own settings. External configuration is configuration that has been applied by the application's working environment. Both should be editable through a common interface.

## 70. Proximity Sharing

When you want to share files or content to people surrounding you physically, transfer is not that intuitive. With fixed workstations, it might be useful to drag files to the edges of the screen for the file to be 'dropped' into the adjacent workstation.

## 71. Gaming Interfaces for Work

Resource management, planning and configuration in video games provide simplified but effective and understandable controls and visibility over progress and process. Commercial software would benefit from visualizing the process and progress of work.

 * Visualizes the state of resources: spare capacity, tied up and bottlenecks.
 * A skill tree diagram of competitors, employees and suppliers.
 * Avatars showing the state that a procedure is in where animation indicates change over time.
 * The movement of individuals and resources around a graph.
 * Gamers take specific and sometimes complicated actions and witness the outcome. When employees take action, the digital representation is a side effect such as an email or logging something in CRUD applications. If instead the 'doing something' is implemented as an action and witnessing the action, everything becomes more transparent.

Gamification as currently realized by industry is not the same as using game interface design in business. The appeal is not making work feel like a game but to make work as clear and useable as a video game.

Examples:

```
A clinic has 3 general practicioner rooms, a waiting room, staff (receptionists, GPs, nurses) and stock of medicine. These are some of the resources being managed:

 * timing of appointments and staff tasks
 * physical space for procedures
 * available personnel
 * financial
 * happiness of staff and patients

With a gaming style interface, we can see at a glance whether or not the clinic is performing effectively:

 - we would see a visualization of the clinic layout, geospatial representations of the world make things more interesting as we can observe what is going on
 - we would see the staff counts and locations
 - we can see medicine expiry dates and stock levels
 - we can see the concurrency of the system if we lay out truly cohesive integrated timelines of when things are meant to happen
 - we can ensure that tasks are distributed fairly

We can answer questions:

 - are there too many patients waiting?
 - are GPs spending too much time with patients?
 - are cancelled appointments causing wasted physical space?
 - are doctors able to provide adequate personalised treatment in addition to performing paperwork?
 - is there a risk to the current combination of waiting patients that could pose a health risk?

We can adapt the rules of the game and check the results:

 - a room becomes unavailable for use by patients perhaps due to a tecnical fault. How will we assign patients and GPs to rooms now?
 - can we predict what repeat patients will need in terms of medicine so we can order less frequently?
 - can we detect when staff members are in demand to minimize waiting?
 - how can we make patients feel they are not being rushed and waiting endlessly?
 - what kind of data can we learn from a patient's habits: are they always late and can we fit another patient in quickly?

```

Potential integration:

 * [Real-time business intelligence](http://en.wikipedia.org/wiki/Real-time_business_intelligence)
 * [Workflow management systems](http://en.wikipedia.org/wiki/Workflow#Workflow_management_system)
 * Virtual realities, simulation games

## 72. [Best Practice Q&A Feeds](id:practice-qa-feed)

Good practices are a social construct and not given visibility in computer systems. Desktop and application help are too static to indicate the most up-to-date industry best-practice. A 'best practice feed' tool would be a peer reviewed support mechanism to provide advice and feedback when machines are being used.

 * People specify what they consider bad practice and why.
 * People suggest what they should do instead. (the `good practice`)
 * A user can subscribe to a `best practice feed`.
 * Users answer questions on the feed.
 * User is given feedback from the answers they provide.
 * Some decisions can be programmatically determined. (Doing X is potentially bad.)
 * This can be used as a form of checklist for action. They may be generic such as 'do you have backups?' to specific topics within a field.

To accommodate the variety of opinions, organisations and individuals can publish their own BPF. When an application is installed, the authors may bundle a BPF to help users starting out.

There are similar existing implementations. As a standard this could be created and completed with standard tools and visualizations. This can be a [microtool](#microtools) where Q&A are provided in a standard format.

Similar:

 * [Securing Web Application Technologies Checklist](http://www.securingthehuman.org/developer/swat)
 * [Web Developer Checklist](http://webdevchecklist.com/)

## 73. Web Of Trust Recommendations

Recommendations can be decentralised. You add people that you know and share your position on a concept. This could be:

 * entertainment such as a book, a website, a movie, music, restaurants
 * a practice (see [practice-feed](#practice-qa-feed))
 * software, shops, services
 * map routes

Opinions toward concepts can be distilled to how people classify or categorise something **and** the order and the weight that they give those categories. When asked why people like, approve, dislike and disapprove of something, there is likely to be determining factor. A web of trust recommendation system attempts to find shared categories and weights rather than those that have similar ratings. Categories can have weights and weights can have categories so that users can reinforce held views.

Users could also be asked to provide explicit recommendations. They are asked to consider similar content within their own collections.

```
If you like X then you might also like Y.
```

## 74. Mounted Email Attachments

Email attachments can be exposed as a file system. Opening a mail client and downloading an email attachment is tedious. It should be possible to grab attachments from the file system.

```
ls /mnt/mail@example/john/
attachment1.doc		attachment2.jpg
```

Alternatives:

 * Cloud storage providers (such as Dropbox, Box, Copy, AeroFs) could automatically pull attachments from a connected mail account into storage. This way there is no need for a separate download attachment step.


## 75. Competition Streams

Organisations offering products or services should permit access to a stream or feed that provides data about their offerings. This data could then be aggregated by browsers or third party services to optimize the offers to display.

## 76. Voluntary Data Mining

A user should be able to contact a retailer, supplier or manufacturer and ask for product recommendation given criteria. The organisation requests specific pieces of information that it will use to correlate to past purchases and offer suggestions given the target market. The customer gets a tailored recommendation from the retailer and the supplier gets accurate information about the customer and what they were looking for.

## 77. [Data Disclosure Tracking](id:disclosure-tracking)

Accessing a service or transmitting data reveals metadata and deliberate information. The knowledge of such disclosure should be trackable by the disclosing party.

 * revealing location through web browser
 * revealing email address or personal details via a web page
 * files that have been transmitted by email and the metadata within these files

People can then understand what information they are revealing to different parties. Inferences can also be made upon this information. For example, it is possible to infer that if an address is known, a postal code can be determined.

 * X knows Y

```
Your [email address, IP address, location, phone number] has been revealed to the following actors:

 * the web server amazon.co.uk on IP xxx.xxx.xxx.xxx
 * the noreply@amazon.co.uk email account
 * your mail provider, example.com

```

## 78. Cohesive Integrated Timelines

Calendars can help connect relations between activities and act as a memory aid. The information from a user's interactions across multiple devices and with multiple applications could be combined into a single view. A calendar view of my system log could show:

 * when I created new directories, moved or renamed files: to help remember a folder I moved
 * when I updated my system, when I received an error: to help correlate an error with an update
 * when I last transferred a file to this computer
 * when I last made a purchase
 * when I last logged into a service
 * starting up a program, closing a program
 * a file system or web search

The calendar can serve as a workspace if activities can be segregated by task or goal. Tasks can be spread over days, weeks, months and years where ability to view past activity would be contextually useful such as:

 * recurring tasks such as managing finances, mortgages, managing insurance, utility bills, large purchases
 * switching between different tasks with completely different contexts (home and work)

For example, when you are looking to buy a new vehicle, you can look at your time line for this task:

 * which car dealers you visited and contacted (emails, phone calls, GPS location)
 * the files you created and where you put them
 * your financial state at this point in time
 * the websites you visited as part of the research (looking at specific car models)

Potential integrations:

 * [Topic map engines](http://www.topicmaps.org/)

## 79. File Wires

Kepeing the data within and between files is difficult to keep synchronized. It should be possible to 'wire' up portions of files with other portions or other files so that they stay synchronized. This would be useful:

 * in configuration files and in documentation: being able to include a port number that always updates when the configuration file changes
 * in a large document where there are phrases, proper nouns, numerical or bibliographical references that one would like to keep synchronized.

The file wire infrastructure would:

 * Provide an interface that lets you select text or content and take a reference to it.
 * This data can then be placed elsewhere and will stay synchronized with wherever it is put.
 * Let you know when file wires break and the connection can no longer be maintained. This might happen if you edit a file in such a way to invalidate a reference. File wires should be generic enough that they can survive files that change.

The 'wire' is the binding of data between two locations. Depending on the format, this could be anything from:

 * a line number
 * a regular expression
 * a column position
 * a meaningful element in the file such as a heading or XML element
 * a reference to a marker or reference point in the document

Essentially, file wires turn every decomposable part of a file into a mail merge field source and destinaton but the field references are out of band and need not be stored in the file.

Potential integration:

 * Existing mailmerge formats
 * Text editor algorithmns: Ropes, [B-tree](http://codemirror.net/demo/btree.html): a special file system driver could intercept writes and reads from files with known formats to make file wires more efficient


## 80. "Playhouse": Repeatable Prototyping

Most rapid application development tools force developers to work within the confines of the tool and make it difficult to graduate to a realistic environment. Setting things up and configuring software is an impediment to prototyping ideas. A developer playhouse would take many different technologies and let them be experimented with from one interface without wrapping up the underlying technologies with proprietary code:

 * Provide a simple 'view' of a project's complex directory struture by showing panels for the most important files. For exampe, JSBin and JSFiddle show HTML, Javascript and CSS panels - all that are needed to write a simple prototype.
 * REPLs for many different languages
 * Prototyping with frameworks: Express, Sinatra, Flask
 * Provision of servers.

Examples:

```
When Playhouse is installed, you point it at a folder.

 * You click 'Express' and are given a panel for your app.js, your NPM dependency file.
 * You select 'Chef' and are given a tab for 'Infrastructure' and are given a tab for a new recipe file and a SSH terminal.
 * User submitted recipes are browseable on one side to get started with common applications or stacks.
```

Existing:

 * [Repl.it](http://repl.it/)
 * JsBin, JsFiddle

Existing Examples:

 * Yeoman, client side generators
 * Vagrant, Docker


## 81. Widget Studio

A widget studio is a content management system for the repetitive sections or widgets that are used on a website or web application and are managed as assets in addition to the web site. The widget studio is is like a model editor for designers. Every single state a widget supports should be explicitly specified by the widget studio.

Potential integrations:

 * [Widget servers](#widget-servers)

## 82. Inline HTTP Microservice Compilation

When writing a controller we can interact with a library directly or we can interact with a remote service and offload the work to another machine. For example, Facebook uses RPC internally so that various microservices collaborate to fulfil a request. Inline HTTP microservice compilation would require a developer to always interact with a library through a HTTP interface. This would involve a single web request fanning out to many requests. If performance problems become an issue, the backend server behind the HTTP service can be 'inlined' or 'pulled into' the code base and replace the HTTP calls. That a HTTP interface is used should not cause overhead if a compilation or transformation step is used that avoids the network stack altogether. By using HTTP as the common interface, functionality can be pulled into the application layer or offloaded to a remote server on demand.

Inlining code may require integration code that understands the project or sourecode of various web frameworks, such as a ruby on rails or nodejs project and knows how to pull in the code into the codebase. The possibility of rewriting code at compile time could further be used to improve efficiency.

If this could be implemented dynamically, servers could become truly elastic: when resources are plenty, the microservices run locally. When resources become constrained, the microservices run on separate machines. 

Potential integration:

 * [Widget servers](#widget-servers): fetching a rendered version of every widget that is to be displayed on web page would be expensive, as one request could quickly translate into hundreds of widgets. This functionality could be 'pulled into' the application layer for efficiency while maintaining flexibility.


## 83. Data Dependency Injection

When a web server handles a request, it inevitably fetches and processes data to fulfil and display a response. In a complicated web page, data may be used by multiple widgets and there may be overlap. This should not result in duplicate requests or needless processing.

 * There can be overlap between data requested or generated by business logic and that needed for display.
 * If a query made for a widget shares a subset of data needed by business logic, then the two queries can be replaced with a single more generic query that allows the data to be fetched once and used twice.

Inversion of control (IoC) containers could be used for widgets and the data they need. A widget should not be directly instantiated with information - it should pull the data it needs from its environment.
 
## 84. Cache Timeout Read-in

The statelessness of HTTP means that data is requested multiple times in order to fulful a request. For example, a multiple page form will typically involve queries to return the logged in user, the state of the form and the fields that have been completed. This data loaded by a web server in a controller may be useful across multiple requests. Memory caches keep data from expensive requests in memory until the next request. These caches need to be explicitly requested for the data to come available. A predictive cache read would associate a timeout with each HTTP request for when the data should be re-loaded into memory. When a user submits a form there will be a predictable delay until the next request. This lump of data - potentially representing the output of many queries - can then be associated with the user HTTP request. This data will only be read back into memory when the time delay elapses as a way of pre-empting the user's next request.

Potential integrations:

 * Memcached, Redis

## 85. [Software Metadata](id:software-metadata)

The infrastructure required to support software is spread across disparate services, servers and protocols. This information could be kept together in a metadata file that represents that piece of software:

 * the source control servers
 * a description of what the application does
 * the bug tracking system
 * versioning 
 * upgrade schedule
 * the authors, maintainers
 * contact details, commercial support details, if available
 * installation technique: package, script
 * mailing lists, online chat, official community discussion
 * dependencies

With this information it might be possible to:

 * submit bug reports from the desktop environment when an application has crashed
 * easy to create a mirror for a local network or for use by a guest virtual machine
 * download sourcecode for an binary
 * plot a timeline showing the predicted upgrades for a machine

Existing:

 * [Portable Application Description files](https://en.wikipedia.org/wiki/Portable_Application_Description)

## 86. Friend Pipe

Sending a file or giving things to other technical users is harder than it needs to be. It should be possible to pipe things to friends and have the transport mechanism be determined behind the scenes:

```
file | friendname
```

This can be combined with a 'friend package manager'.

```
friend add <email>
```

Existing:

 * [Filegive](http://freecode.com/projects/filegive)

## 87. Interface Colescing

When similar events occur in succession where each in isolation would have displayed a dialog, there is a risk that they block and have to be dealt with separately or they stack on-top of one another. Examples of where this is often a problem:

 * copying or transferring files
 * error mesage dialogs 
 * desktop environment notifications
 * wizard dialogs

Interface colescing means that a singular dialog can 'colesce' with future dialogs to provide a better suited interface for handling multiple items.

Examples:

 * You select a group of files to copy or move to another folder. This opens a file transfer dialog. You move another set of files. This transfer joins the first dialog which collapses to handle multiple cases.
 * You select a single item in a list to edit and an form appears. You select multiple items to edit and you receive a form better suited for editing multiple items.

## 88. Batching Notifications

Desktop environment notifications such as email or instant messages can be distracting. Events do not always require immediate attention and can be delayed and delivered in batches.

 * Email notifications could be set to once an hour, instant message alerts to 10 minutes and social networking to once a day.
 * The notifications should be rendered slowly and ordered to avoid overwhelming users. In the Windows notification area (nicknamed the system tray), icons can indicate notifications.


## 89. [Code Journey](id:code-journey)

Learning a code base should be easy to start and supportive. An interactive code base exploration tool can:

 * display the codebase with accompanying narrative to create an interactive walkthrough such as discussing the architecture and the various modules of a code base
 * step-by-step REPL playback that the user can pause and continue at any time (without affecting the tutorial)
 * annotations, diagrams, screencasts, voiceovers
 
Existing:

  * The [`Try Redis` demo](http://try.redis.io/)
  * [LightTable](http://lighttable.org/)

## 90. [Views of Data](id:data-views)

Applications such as wiki or ERP applications are typically monolithic where the full application is absolutely necessary to interact with the underlying data. Data conversion is needed to move data between ecosystems. Conversion is less useful than a view over data. When we have a view over data, we can use multiple tools to interact with the same data.

 * If complex filtering or sorting behaviour cannot be shifted to a database, it would be preferable if the data retrieved could still be queried as if it was. It is likely a dedicated querying module would give better performance than writing custom sorting and filtering. The same APIs for sorting and filtering used both the client and server.
 * Running database queries over a CSV/JSON/XML file
 * The data being displayed on a user interface in one window is useable by the user. The user can run a query against the list of emails or interpret the email body as a document in a different format.

Using views may be less efficient because data is not in an optimized data structure. For example, running a join query over a CSV file is likely to be slow. A view architecture could support this in the following ways:

 * write handcrafted code that can support basic SQL functionality over text files
 * write a mapper that converts JSON/CSV/XML into insertions into a newly spun up database server or in-memory database

The user should not care what format or representation the data is in - only that they can interact with the data in multiple ways. It should be possible for many applications to operate on the same data structure.

Existing examples:

 * [NeDB](https://github.com/louischatriot/nedb) compatible with MongoDB
 * Templating on the client and on the server
 * LINQ: functional queries over objects
 * [Bidirectionalization](http://en.wikipedia.org/wiki/Bidirectionalization)
 * [Automatic conversion with representational computing](#representational-computing)
 
## 91. Template Virtual Machine

At its basic level, templating can be considered a block of memory split into dynamic and static regions:

 * A single instance of the website is kept in memory.
 * The static data and dynamic sections in-memory template are indexed.
 * Widgets or common components are shared different pages or nested views.
 * When a request comes in for a given page the .
 
All this does is replace the generation of the contiguous block of bytes [static, dynamic, static, …] with a higher level representation of the output. Servlet layers and templating engines map the output page structure from many nested function calls and branching - the Template Virtual Machine essentially directly maps the blocks to the output. There may be the following benefits:

 * The clientside can subscribe to the backend blocks and be notified when they change.
 * Dynamic blocks are essentially `holes` that must be filled by programs.
 * DB performance can be measured and checked for errors.
 * Blocks can be shared between pages.
 * Potential parallelization of dynamic blocks. Non-static data can be streamed immediately and all future dynamic blocks can run at the same time providing there are no dependencies.
 
Similar: 

 * [rendr](http://rendr.com/)
 * The idea of [String Templates](http://www.stringtemplate.org/) where all substitutions must be known in advance.

## 92. Personal Data API

Rather than supply a collection of personal data to remote services, data should be requested from the user's machine or data custodian through an API by the remote service. This would keep all the data in a single location and ensure that data is kept in synchronization. This could be implemented by browsers.

This also allows a user to track what data was disclosed to which parties.

Potential integration:
 
 * [Disclosure tracking](#disclosure-tracking)
 * Account management protocols
 * Formats for common personal data
 * Vendor relationships management

## 93. Shell Output Pinning

The output of one command can be useful while running further commands. For example, a search of a directory would give a list of files. It may be nice to pin this list to the top of the shell and allow the user to work their way through the list. 

Examples:

 * You search a directory (grep) and pin the results to the top of the terminal. You mark off each file you process as you go.

## 94. Policy Tracking

Digitally serving legal agreements, policies and terms and conditions has become industry practice without any tools for users to manage, track and interrogate legal documents. A policy aware system can display policy relevant used contextually when people use computer systems as a way of encouraging users to understand.

 * notifications when policies change
 * accessing a service shows what terms are applicable in a given context such as those for a website
 * see at a glance what conditions apply to the user such as idenmification clauses

Legal documents that state a valid action

Existing:

 * [EULAnalyzer](http://www.brightfort.com/eulalyzer.html)
 * [TOS Back](http://www.tosback.org/timeline.php)
 * [Platform for Privacy Preferences Project](http://en.wikipedia.org/wiki/P3P)

## 95. Community Idea: Distributed Development

A pool of developers can collaborate to build a system if the individual pieces of code are well defined enough.

    Developer 1 logs in and picks feature A to implement.
    Feature A requires features B and C to exist.
    Developer 1 describes B and C at a high level and creates an imaginary interface how these features might be used if they existed with input data corresponding to outputs.
    Developer 1 implements feature as much of feature A as possible.

    Developer 2 logs in and sees that Feature B and C are still to be implemented with the imaginary interface defined by Developer 1. Developer 2 implements features B and C, ensuring that the interfaces needed by Feature A is maintained. 
    
Developers collaborate by breaking up problems and shifting other ones to others. A developer operates on a small portion of the code base at any given point so that ramp-up time until productivity is low. Developers jump between features frequently.

Potential integration:

 * API competition: competing for the best API (not the implementation)

## 96. [Encyclopedic Literate Desktop](id:encyclopedic-literate-desktop)

Computer systems and interfaces are obtuse and do not describe what they are doing or how they function. A desktop environment should explain and describe software as if it was a living encyclopedia. Computers can be more easily understood if they allowed what's on screen to be functionally decomposed and explained.

 * Select a window, click the 'flip' button to see what is 'behind' the window, as a metaphor to see what he application is doing.
 * This gives us a description of the application and facts about the author, version and contact details.
 * Use cases and scenarios of the application from a high level.
 * A list of features.
 * The current status of the application, such as what features are currently being used and how it is configured.
 * A list of dependencies and what each dependency is used for.
 * Where the application is stored, where it is configured
 * What files the application opens
 * The data being transmitted by a program. ([Wireshark Dissectors](http://www.wireshark.org/docs/wsdg_html_chunked/ChapterDissection.html))
 
These would be displayed as a overview style format in a similar style to that of a landing page for a product or service online. Each section above might be expandable (such as select a feature and learn how it works.) and linked to further information to learn more.

An advanced user should be able to view the sourcecode of an application in a literate interface. The emphasis is of a readable view of the sourcecode as opposed to an editing environment to help the users understand how this particular application functions.

 * When I inspect a running application, I want to know all the technologies that are being used. The architecture, how the application is split into modules. What each thread is actually doing. I want to see state diagrams and workflows. I want to see the queryable services that the running aplication provides: perhaps those provided by IPC or over the network and the protocols. I want to see what widgets are currently on the screen and what they are populated with. I should be able to jump to the sourcecode, application side and library side when clicking these items. I want to see what algorithmns are being used and visualizations of how the algorithmns work, perhaps leading to a [code journey](#code-journey).
 * Encyclopedic entries are programs that take a state and generate a document describing the state of the widget, perhaps written by that representation's author. For example, a widget author understands the internals of the widget and knows how to create a visualization of how the widget functions. This content would be transcluded into the parent encyclopedic entry for the program.

Goals:

 * Desktop environments become dynamic textbooks
 * Make everything discoverable.
 * Click and explain


Potential integrations:

 * [Code as wiki](#code-as-wiki), [Code overlays](#code-overlays), [Code journeys](#code-journeys), [high level project overview](#high-level-project-overview)
 * Application comparison with [tech slice](#tech-stack-slice)

## 97. Community Idea: "Tracked Reasoning"

Viewpoints of a discussion can be identified, related and analysed independently. When a user writes a post, the user can break up the post into separate viewpoints or assertions. These assertions may be ordered logically such as, A implies B then C. Posts will then be cross referenced to see the relationship of each viewpoint and what would need to be true or false to counter an argument.

## 98. The Desktop is an Integrated Development Environment

A desktop environment is a development environment except windows and widgets are the files and the user's inputs are the lines of code. A desktop environment should be malleable to change in a similar way that the contents of the DOM (Document Object Model) of a web application can be easily changed. A web developer does not need to re-compile sourcecode to change how an application appears.

If applications were designed to separate:

 * decision what widgets should be displayed given application state
 * deciding what data each widget should display
 * deciding which widgets should be displayed together (logical groupings such as 'menubar', 'toolbar')
 * deciding how to lay these widgets out (ordering, orientation)
 * deciding how detailed these widgets will be (responsive design)

Then the desktop environment and the user can override parts of the above behaviour of the application without damaging internal state of running applications. 

 * a user could select an interesting region of a complex interface and 'send it to the notification area' or 'promote it to the titlebar' so that they can cut and splice the user environment how they like. This would be provided by the environment - not specifically coded. ([How can I display a live screenshot of a piece of another application?](http://blogs.msdn.com/b/oldnewthing/archive/2013/05/13/10417964.aspx))
 * the user can interrogate and inspect the information underlying information a widget is displaying and add behaviour to it
 * right click a 'disk usage' indicator and select 'monitor' and create a notification when disk usage reaches a threshold. The desktop environment is smart enoguh to know it is not the widget itself that is being monitored but the underlying data the widget is displaying.

```
Example: A configuration file 

 - A simple visualization of a configuration file is a plaintext editor.
 - The next layer may be a tree structure to navigate the blocks of the file.
 - The next step would be to provide proper widgets for every value.
 - The next step may be wizards to generate certain blocks of the configuration file.
 - The next step may be to provide a dashboard and interpretation of what the configuration file is doing from a high level. Such as a nginx dashboard with icons for proxying. (see [representational computing](#representational-computing) and [data views](#data-views))

```
 * Interfaces are written to visualize and edit representations.
 * Writing interfaces to interact with data needs to be as cheap as possible. It should be possible to knock up a configuration interface for a configuration file. For example, if the parse tree of a configuration file was exposed as a representation by an application, this would be much easier.

Deployed applications on desktops preside in an impoverished environment compared to the environment that was used to create them. This makes installed desktop software inconsistent between installations and brittle. Various products bundle full-stack servers traditionally used on the server-side. These include web servers and databases. The provision and configuration of these servers should be no different to that used in cloud environments or in development. The desktop environment should be using provisioning tools such as Docker, Vagrant, Chef or Puppet behind the scenes. For example, installing a product that needs a MySQL database would use an existing running if installed and is of the correct version or will install a new copy. It's a complex engineering problem to make this possible, efficient and simple.

Example:

Title bars

The top of every window in a desktop environment could be broken down like so:

![Everything is composable](https://raw.github.com/samsquire/ideas/master/paneling.PNG "Everything is composable")

A desktop environment essentially becomes a website in the sense there is a link between what is being displayed and how the user can interact with it or edit it. Every on-screen component can be customized, re-ordered and adjusted. Desktops become living infographics.

Integration:

 * [Encyclopedic literate desktop](#encyclopedic-literate-desktop)

Existing:

 * [Aurajs](http://aurajs.com/)
 * COM/OLE Linking
 * Firebug, Chrome development tools
 * Microsoft MMC Snapins


## 99. Directories Are Portals

A directory can be domain specific and relevant to the types of files displayed. The layout and grouping of icons should be customisable.

![Bubble back grouping](https://raw.github.com/samsquire/ideas/master/file_view.PNG "Bubble back grouping")

![Application portal](https://raw.github.com/samsquire/ideas/master/systemviewer_mergedisplay.PNG "Application portal")

 * In many file managers where folders appear first and there are many folders, no files can be seen. Folders and files could be arranged in a way that makes files and folders obvious immediately. Directories could be positioned along the top and down the right-hand side to make a `-|` shape to avoid the situation where only folders can be seen without scrolling down. This could then be sticky as the user scrolls down so that the user can always access folders.
 * Icons are scaled according to relative importance in the directory.
 * The background colors are arbitrary coloured to group certain files, perhaps with titles. A packing algorithm can a ensure that certain icons get arranged together in a pleasant way without breaking the uniform apperance of the icons.


Existing:

 * [Stardock Spaces](http://www.stardock.com/products/fences/)

## 100. Personal Integration Framework

Online tools like Zapier and drag-and-drop workflow systems enable users to mix up online services - this is something that should be possible across devices.

 * A user wants to do accomplish a task - these tasks should be directly browseable. The desktop environment should provide an interactive How To system that allows configurations to be created.
 * A user wants 1 feature in a product that offers 5. They do not necessarily care about the application. They have all the applications they want intalled but they want them to interact in a certain way.
 * User can apply conditions to differernt tasks.
 * These configuration and underlying services and applications required for these tasks could span across multiple devices and machines.
 * Adding behaviours or integrating behaviours between running services and applications should be like a marketplace for features rather than applications.
 * Developers who scratch configuration itches can wrap up simple configuration permutations as 'offering task X'
 
This is like a package manager for normal users except that full applications are not being packaged - behaviour and configuration are.

 * when I log into my laptop, close applications on phone to save power, reopen when laptop becomes inactive
 * when I save a presentation to any device, syncronize it to all of my devices immediately
 * when I take a photo or video, add it to my photo album
 * keep this folder synchronized with this device
 * keep this folder available remotely to this device
 * always keep this window to this side of the window
 * if I start this application, close another (perhaps to save resources)
 * when I login to this application, turn on this machine
 * tell me when I spend X money (determine from email parsing or [open email metadata](#email-metadata))

Existing:

 * Applescript and Services
 * [Zapier](http://zapier.com/)
