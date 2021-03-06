## Workshop 2: Responsive Design and Bootstrap

####What is Responsive Design?
Designing your website to look good across multiple screen sizes and therefore multiple devices.
- If you want to read more about it, the concept was introduced in 2010 in [this A List Apart Article](http://alistapart.com/article/responsive-web-design)

#####Examples of Good Responsive Design
 - https://responsivedesign.is/examples

####Bootstrap
[getbootstrap.com](getbootstrap.com)

*“Bootstrap is the most popular HTML, CSS, and JS framework for developing responsive, mobile first projects on the web.”*

#####Use Bootstrap in your personal website
1. Go to the ["Getting Started"](http://getbootstrap.com/getting-started/) section of the website
2. Scroll down to where it says 'Bootstrap CDN' and copy and paste that snippet of code into your index.html file header
  * this is the quickest way to do it, but in terms of performance, you may want to eventually download the files and save them in your website's directory
  * for now referencing the CDN is good enough

#####Components - Navbar
Bootstrap provides many reusable components that you may find useful for your website, such as dropdowns and navbars

1. Go to the ["Components"](http://getbootstrap.com/components/) section of the website. Here you can see examples of all of Bootstrap's reusable components
2. We will start with a [navbar](http://getbootstrap.com/components/#navbar) because this is a common component of any website
3. For this example, our navbar will link to an "About Me" page and a "Projects" page.
4. Paste the following code inside the body of your html file:

  ```html
    <!-- Navigation Bar -->
    <nav role="navigation" class="navbar navbar-default">
        <!-- Brand and toggle get grouped for better mobile display -->
        <div class="navbar-header">
            <button type="button" data-target="#navbarCollapse" data-toggle="collapse" class="navbar-toggle">
                <span class="sr-only">Toggle navigation</span>
                <span class="icon-bar"></span>
                <span class="icon-bar"></span>
                <span class="icon-bar"></span>
            </button>
            <a href="#" class="navbar-brand">Brand</a>
        </div>
        <!-- Collection of nav links and other content for toggling -->
        <div id="navbarCollapse" class="collapse navbar-collapse">
            <ul class="nav navbar-nav">
                <li><a href="#">Home</a></li>
                <li><a href="#">About Me</a></li>
                <li><a href="#">Projects</a></li>
            </ul>
        </div>
    </nav>
  ```
5. Replace 'Brand' with your name or whatever you would like to really
6. On the list element for each page change ```<a href="#">``` to link to the corresponding html file ex. ```<a href="aboutme.html">``` 
  * This means your 'aboutme.html' file is in the same directory as your 'index.html' file (it should be). If not, you need to provide the relative path
  * This is assuming you have a file called 'aboutme.html' make sure the name of your file for your "About Me" page matches the name you link to in the ```href```
7. Now once you have the html files for your other pages, you have a responsive navbar that will link to them :)
8. Browse through the other reusable components bootstrap provides and try to implement some more in your website

#####Bootstrap's Grid System
It is easy to make your website responsive to different screen sizes with Bootstrap's responsive, mobile first fluid grid system http://getbootstrap.com/css/#grid

Bootstrap uses a 12 column system to make it easy to format your site. This means that your column width sizes inside any row should add up to 12. For example, if you wanted three equal sized columns in one row, you would have three columns of size 4 (because 4+4+4=12). If you wanted three columns, but for one to be twice as large as the others, you could have one column of size 6, and the other be size 3 (because 6+3+3=12).

You can also optimize your site for different screen sizes! When defining a column, you assign it 'xs' 's' 'm' or 'lg' which corresponds to the size of the smallest size browser that will display the content in columns, any browser smaller will just stack the columns.

######Example code for 3 equal columns to be only displayed as columns on a medium device or larger
 ```html
 <div class="row">
   <div class="col-md-4">Content for your first column</div>
   <div class="col-md-4">Content for your second column</div>
   <div class="col-md-4">Content for your third column</div>
 </div>
  ```

To get a better understanding of what this all means, try resizing your browser with this link open: https://getbootstrap.com/examples/grid/ to understand the column system.
