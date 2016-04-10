# Front-end-Practices
Describing what my best practices are.


# HTML Best Practice Coding Guidelines

### W3C Standards
All pages on the site should conform to W3C Standards which can be validated using the W3C Validator

https://validator.w3.org/

### HTML Layout
All of your HTML should be well formed using the relevant HTML5 tags available ie. <header>, <nav>, <main>, <article>, <section>, <aside>, <footer>.

### Javascript Files
Unless there is a valid reason, you should place all of the Javascript Files and Libaries just before the end </body> tag so they are the last files to run when the page loads.

### Comments
Always use comments in your code so if you get hit by a bus another developer can go in and read the comments so they know what the code actually does.

### Class and ID's
When using class names, make sure they are relevant to the component you are coding i.e. search-box, search-btn, search-block-link. **Don't** use colours for class names.

On using ID's make sure you only use one in a page and make sure you do not use it in a loop so it gets repeated.

If you are using classes and ID's for jQuery and Javascript then using prefix js- so other developers know what it is being used for.

### Source Order  
There has been various conversations over time saying content first for source ordering before secondary navigation. One of the reasons was due to Search Engine crawling which has now advanced to a level it does not matter when the main content is placed. From the Screen Reader point of view the user can skip between links and also skip to content if this has been placed in the code.

### Accessibility
All sites must conform to W3C Level 1 Standards although this does not mean you need to stop at this point. If you can make the site meet Level 2 or 3 then make it meet these levels. 

A reference guide is available on W3C - https://www.w3.org/WAI/WCAG20/quickref/

**Level 1**  
* Make sure all images have an alt attribute (1.1.1)
* Skip to Content Links (2.4.1)
* Site is Accessible by keyboard only (2.1.1)

**Level 2**  
If the site you are building has to conform to Level 2 then make sure the design foreground (text) and background colours pass the relevant tests. Discuss with the PM and Designer if it has been placed in the spec and the designs have already been signed off.

* Colour Contrast (1.4.3) - You can test the colour ratios - http://juicystudio.com/services/luminositycontrastratio.php
* Images of Text (1.4.5) - Do not use images of text unless essential i.e. Company Logo
* Consistent Navigation (3.2.3)


### Aria Roles  
You can use Aria Roles but it depends on what you are doing with the site. Aria Roles are not needed on Header, Navigation, Main, Aside and Footer tags as they are already covered.

### HTML5 Page example - This is a guide only

```html
<!DOCTYPE html>
<html>
    <head>
        <title>HTML5 Template</title>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">

        <!-- Adding HTML5 SHIV for fallback for older browsers -->
        <script src="https://cdnjs.cloudflare.com/ajax/libs/html5shiv/3.7.3/html5shiv-printshiv.js"></script>

    </head>
    <body>
        <header>
        	<!-- Header Content -->
        </header>
   
        <nav>
        	<!-- Main Navigation -->
        </nav>

		<nav class="secondary">
			<!-- Secondary Navigation -->
		</nav>

		<main>
			<h1>Title</h1>
			<!-- Main Content Area -->
			<article>
            	<h2>Title</h2>
				<!-- Article Content -->
        	</article>
		</main>

        <aside>
        	<!-- For Use for example a Right Column -->
        </aside>

        <footer>
        	<!-- Footer Content -->
        </footer>

		<!-- Javascript files and Libraries are the last thing before body tag -->
        <script src="http://code.jquery.com/jquery-1.10.2.min.js" type="text/javascript"></script>
        <script src="/assets/js/main.js" type="text/javascript"></script>

    </body>
</html>