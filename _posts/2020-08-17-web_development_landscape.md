---
layout: post
title: ⭐️ Choosing a tech stack and making sense of the web devlopment landscape (from a bootstrap entrepreneurial perspective)
permalink: web-development-landscape
image: /images/default.jpg
categories: entrepreneurship
---

I've wanted to learn how to develop proper web apps for several years now. But what has stopped me so far is that there are so many options, and I was never sure what exactly I should learn. In particular, what I've been missing is a proper overview of the various players in the field and how they interact.

Now that I've read and tried a lot, I've decided to write such an overview myself. My goal is primarily to organize my own thoughts and save them for the inevitable case that I'll be confused about the same things again. 

Everything that follows is heavily biased by my perspective as an inexperienced bootstrap entrepreneur. Naturally, the perspective of, say, an engineer at a big company will be very different. Hence, if you're an experience web developer, you can safely ignore this article. But if you're a beginner or an aspiring bootstrap entrepreneur, you might find my overview helpful.

With that out of the way, let's dive in. 

## Common vs. Custom Apps

The first thing you need to get clear about is what you're really trying to achieve. Obviously, your stack for building an iPhone or a Desktop app while be very different from your website development stack. However, when it comes to different kinds of websites, the lines get blurrier. 

There are so many types of web apps that it would be delusional to say that there's one ideal way to build all of them. In particular, there are certain types of websites that are so common that amazing specialized tools have been developed. Extremely common website categories are:

- Wikis (knowledge bases)
- Forums.
- Content sites (blogs, documentation, purely informational websites for offline businesses)

 If your website project falls into one of these categories, it's usually a good idea to use a specialized tool for the job. 

- Great choices if you want to build a Wiki are [Dokuwiki](https://www.dokuwiki.org/dokuwiki) and [Mediawiki](https://www.mediawiki.org/wiki/MediaWiki).
- A popular choice for a forum is [Discourse](https://www.discourse.org/).
- For content sites there are three broad categories:
    - **Static site generators** such as [Jekyll](https://jekyllrb.com/) and [Hugo](https://gohugo.io/). Here the key idea is that you put text or markdown in a specific directory in a version-controlled codebase (e.g. GitHub). Then the software starts a build process that outputs static HTML files that contain your content within a consistent layout. The websites that are built this way are extremely fast, secure and can be hosted cheaply or even for free in many cases. If you're not afraid of a bit of code, this is arguably the best option for pure content sites.
    - **Traditional content management systems** (CMSs) like [WordPress](https://nehalist.io/why-im-not-the-biggest-wordpress-fan/), [Drupal](https://drupal.org/), and [Ghost](https://nehalist.io/why-i-dont-like-the-ghost-blogging-platform-anymore/). Here the idea is that you have a visual backend that you can use to manage your site. Within the backend, there's a button that says "New Post". If you click it, type some text and hit another button labelled "Published", your text is stored in a database and retrieved from there when users visit your site. CMS sites can either be self-hosted (on a virtual private server or some shared hosting) or hosted by specialized managed hosting services.
    - **Headless content management systems** like [DatoCMS](https://www.datocms.com/) or [ContentFul](https://www.contentful.com/) that aim to combine the best parts of the two other categories. Most people don't feel comfortable updating code repositories, as it is necessary if you're using Jekyll or Hugo. Hence if you're using a headless CMS you can write your content as you would do it using traditional content management systems. Then this content gets crunched by a static site generator like [Gatsby](https://www.gatsbyjs.com/). The result is a fast and secure website that only consists of static HTML and CSS files.

While tools that were invented to build custom web apps are capable of creating, say, pure content sites, this is a lot more work and the results typically will not be as half as good. A proper analogy is that it's like trying to carve a miniature wood figure starting from a mammoth tree.

On the other hand, it's also possible to use a tool that was built for a particular, common type of website and use it to build something completely different. For example, while it's possible to build a custom web app with a tool like WordPress, this usually isn't a wise choice. A proper analogy is that this is like delivering a package from Europe to China on a unicycle. Possible? Yes. But not very pleasant. Moreover, your customers will probably complain and you won't be happy about the result yourself. 

Lastly take note that even if you want to build a custom web app, it often makes a lot of sense to use a specialized tool at some point. For example, many apps use something like Jekyll for their documentation. 

With that said, let's talk about proper ways to build custom web apps in more detail. 

## Building Custom Web Apps — Tools of the Trade

When it comes to custom web apps, there are three important type of tools:

- No-Code Tools
- Traditional Tools
- Serverless Tools

Let's talk about no-code tools first

### The No-Code Approach

I think the following prediction by [Pieter Levels](https://twitter.com/levelsio/status/1170258907232493574) is not too far-fetched given that 30% of the web runs on WordPress (which is essentially a no-code tool): 

> In the future writing actual code will be like using a pro DSLR camera, and no code will be like using a smartphone camera
Some pros will keep doing work with DSLRs (and need them), but most basic apps will be built with no code. Just like most photos now are shot on a phone.

So far, primarily content sites were built using no-code tools. However, using tools like Google Sheets, Airtable, Zapier, Typeform, and Bubble, many simple [CRUD](https://en.wikipedia.org/wiki/Create,_read,_update_and_delete) applications can be built without a single line of code. An example would be a tool that allows users to get their luggage picked up from the airport by contractors. You could easily build this kind of tools using Typeform, Zapier, and Airtable. 

However, I'm not buying completely into the current no-code hype. Yes, no-code tools are great if you want to validate an idea quickly. However, once the idea is validated you'll most likely want to build your properly using more traditional tools. With a no-code stack you'll always be limited in what you can do and many things will just not work the way you want it. Additionally, you'll be extremely dependent on all tool providers and if one of them makes dramatic changes or goes out of business your entire site becomes unusable overnight.

A great comparison are tools that people use to create documents. At one of the spectrum, we have no-code tools like Microsoft Word, while at the other end we have LaTeX. In this space, almost any use case you can imagine can be realized using no-code tools. But you know what? People (in particular professional publishers) still use and love LaTeX. 

A proper analog is maybe that no-code tools are akin to Legos. Theoretically, you can build a complete factory using Legos. But that doesn't mean that you should do it. 

So in short: use no-code tools for simple CRUD-style apps and to validate ideas quickly. 

Next, let's talk about traditional tools that are commonly used to build custom web apps. 

### The Traditional Approach

This is the largest and most confusing category. There are just so many choices. 

The two key elements of a web app are a backend and a frontend. The backend is where all the magic happens while the frontend is responsible for making it visible and accessible to the user. 

For example, the backend decides what happens when your users visit a particular URL at your site, or submit a form, or click a button. The backend is also responsible for retrieving and transforming data from your database and other data sources. Traditionally, the backend is software code that is executed on a server.

In contrast, frontend code is interpreted and executed by each user's browser individually. Moreover, the frontend is responsible, for example, for how the data that was retrieved by the backend is shown to users. 

A different way to put it is that the frontend is the presentation layer, whereas the backend is the business and database layer.

{:.centered}
![](/images/frontend_backend_diagram.svg)

For both, frontend and backend development, you have to make a choice whether you want to use a [Vanilla programming language](http://en.wikipedia.org/wiki/Vanilla_software) or a framework. Most developers prefer to use a framework. Using a vanilla programming language is like building a factory by starting from limestone, sand and water while using a framework is akin to starting with concrete. 

In either case, we have to talk about programming languages. But before we dive in, I feel it's important to point out that there's no right or best choice. Choosing a programming language is largely a matter of personal preferences and you can do amazing things with any one of them.

**Choosing a Backend Stack**

For the backend, some of the most popular programming languages used by bootstrap entrepreneurs are

- PHP - owes much of its popularity to the prevalence of WordPress which is written in PHP. Hence, everyone who wants to develop themes or plugins or simply wants to customize their WordPress site has to learn PHP. Another huge advantage of PHP is that it's incredibly easy to deploy PHP apps. You just have to upload your PHP file to some hosting service or server and direct your URL to it. For all other languages, lots of more complicated intermediate steps are necessary before your app is available on the web. Nevertheless, if you can choose freely, PHP probably shouldn't be at the top of your list. It's not a very well-designed, enjoyable language and full of [inconsistencies and surprises](https://eev.ee/blog/2012/04/09/php-a-fractal-of-bad-design/).
- Python - a great choice because of the amazing ecosystem and its simple syntax. There is a package for almost any use case, ranging from machine learning to scientific calculations.
- Ruby - another great choice thanks to its expressiveness and its focus on [programmer happiness](https://rubyonrails.org/doctrine/). Moreover, as for Python, there's a huge ecosystem with packages (called gems in this context) for many use cases. The main difference is that most Ruby packages are intended for web apps, while Python has packages for more diverse use cases.  Deploying a Ruby app is thanks to Heroku almost as easy (if not easier) than deploying a PHP project.
- Elixir and Clojure - in contrast to Python and Ruby (which are object-oriented), these are functional languages. I'm not an expert on these matters but my impression is that the learning curve is much steeper and it takes more time to write in a functional style. However, eventually it pays off because your code is less error-prone and easier maintainable. Here's a [talk](https://www.youtube.com/watch?v=vK1DazRK_a0) that explains nicely the difference between object-oriented and functional programming. There are also many [talks by Rich Hickey](https://github.com/tallesl/Rich-Hickey-fanclub), the inventor of Clojure, like [this one](http://www.infoq.com/presentations/Are-We-There-Yet-Rich-Hickey), that are awesome and help to understand the motivation behind functional programming. Additionally, [Paul Graham's essay on Lisp](http://www.paulgraham.com/avg.html) is worth reading in this context since Clojure is a Lisp dialect.
- Node.js -  strictly speaking it's not a programming language but a piece of software that makes it possible to use JavaScript for the backend. This is attractive for many people because it means that you can use the same language for the frontend and the backend.

Above, I've already mentioned that it rarely happens that developers — solo-developers in particular — use a vanilla programming language to develop web apps. (A rare exception is [Pieter Levels](https://levels.io/how-i-build-my-minimum-viable-products/) who developed all of his highly successful apps in vanilla PHP.) Instead, it makes in many cases sense to use a framework that hides many cumbersome details behind another layer of abstraction.

{:.centered}
![](/images/abstraction_layers.svg)

So let's talk about some of the most popular **backend frameworks**.

- Popular PHP frameworks are Laravel and Symfony. Laravel is far more modern, feature-rich and easier to learn for beginners. A notable advocate of Laravel is [Mubashar Iqbal](https://www.producthunt.com/@mubashariqbal/made). Here's an [app](https://podhunt.app/) that was built with Laravel.
- When it comes to Ruby everyone shouts immediately Rails as the number one framework. (Here's a cool [Rails-Laravel dictionary](http://jimmylocoding.com/a-laravel-rails-dictionary/). The mere existence of such a dictionary already demonstrates how similar the two frameworks are.) A notable advocate of Ruby on Rails is [Jon Yongfook](https://twitter.com/yongfook/status/1223086371025276928). Here's an [app](https://www.bannerbear.com/) that was built with Rails. A popular lightweight alternative is Sinatra.
- The most popular web development framework for Python is Django.  A notable advocate is [Sergio Mattei](https://twitter.com/matteing/status/1275658405445865475). Here's an [app](https://getmakerlog.com/) that was built with Django. A lightweight alternative is Flask.
- Phoenix is for Elixir what Rails is for Ruby. A notable advocate is [Derek Sivers](https://sive.rs/rails2php). Here's an [app](https://papercups.io/) that was built using Phoenix.
- The most popular Node.js framework is Express.js. Here's an [app](https://www.apstudynotes.org/) that was built using Express.js.

Something that has helped me a lot is to have a look at sites that were built by solo developers  using different frameworks. By doing this, you notice quickly how buggy or smooth an app that was built using a particular framework typically is. This is why I've added a link to an example app for each framework. After doing a bit of research I decided to learn Ruby on Rails although, for example, Laravel would've been certainly an equally good choice. My main reason for going with Rails is that almost anyone seems to agree that Rails is the best choice if you want to get from idea to usable product quickly. It doesn't scale as well as other frameworks and has certain disadvantages. But for me, as an aspiring bootstrap entrepreneur it seems like the perfect choice. 

In case you need further decision help, here's a [nice comparison](https://www.craighewitt.me/rails-vs-django-vs-laravel-an-analysis-of-web-frameworks-from-a-non-technical-founder/) of Rails, Django, and Laravel. An important difference I've noticed that lots of Laravel stuff is heavily monetized whereas in the Rails community there is a lets-help-each-freely other spirit. This isn't necessarily an argument against Laravel since it's great if there is lots of high-quality stuff you can use. However, if you're a bit short on cash or just don't feel comfortable spending a hundred bucks here and there, Rails seems like a better option.

Having talked about the backend, we next need to decide how we're going to present our app to the users. 

**Choosing a Frontend Stack**

The quintessential frontend "programming languages" are

- HTML - used to define the basic structure of sites. For example, using HTML you define that Page 1 should include a headline and box containing text and two buttons, while Page 2 should include only a headline and text.
- CSS  - used to define the basic look of sites. Using CSS you can define how the various elements (headlines, text, buttons, boxes) look like at each page and where they're located on the page.
- JavaScript - used to define the behavior of site elements. For example, using JavaScript you can define that a given button should start dancing whenever it is pressed. A more sensible use case is that JavaScript can be used to modify site elements without reloading the page. For example, when you press an upvote button, the total votes counter should change. With JavaScript, you can make sure that the counter updates immediately and no page reloading is necessary.

There's no way to get around these three web languages because they are what web browsers understand. As mentioned above, backend code is executed on our server and thus we can use any language we like. After all, the server is our computer and hence we can install software that makes sure it understands PHP or Ruby code. The frontend code, however, is executed by each user's computer and since we can't control what kind of software a user has installed, it always has to boil down to HTML, CSS, and JavaScript. 

Nevertheless, people have developed many ways to make frontend development more effective. The key idea to make this possible is to more sophisticated languages which are then "compiled" on the developers' computer so that the result is HTML, CSS, and JavaScript that our user's computers understand.

For example, for CSS there are preprocessors like SASS and LESS. These are extensions of CSS that introduce new features like variables that make it easier to style websites consistently. Once the SASS or LESS files are finished, they are used to built proper CSS files which are then served to users. 

Similarly, there are HTML preprocessors (also known as templating languages) like Haml and Slim. One of the main selling points of these preprocessors is that they allow you to define so-called partials that you can insert and reuse at different pages. (In some sense, this is the same idea as for the variables the CSS preprocessors introduce.) The preprocessor files are then compiled on the developers' computer and the result are proper HTML files. 

Last but not least, there are "[JavaScript flavours](https://2019.stateofjs.com/javascript-flavors/)" like TypeScript, Svelte and ClojureScript that introduce a simpler syntax plus new functionalities and compile to standard JavaScript. (Note that my classification of Svelte is far from the standard. More commonly Svelte is classified along the same lines as JavaScript frameworks like Vue and React that are discussed below. However, since Svelte files are complied to vanilla JavaScript, I've included it here.)

{:.centered}
![](/images/prepocessor_logic.svg)

Now just as there are backend frameworks, there are frontend frameworks that make it easier to develop nice looking, smooth sites. 

- The [most popular CSS frameworks](https://2019.stateofcss.com/technologies/css-frameworks/) are Bootstrap, Bulma, and Tailwind. These frameworks are simply CSS files that you can include in your site that include many class definitions. For example, once you've included the Bootstrap.css file, you can simply add the code "class="btn btn-primary" to a given button and it will immediately start looking nicely. Tailwind takes a somewhat different ("utility first") approach that is explained in more detail [here](https://adamwathan.me/css-utility-classes-and-separation-of-concerns/).
- Popular JavaScript lightweight frameworks (commonly called utility libraries in this context) that make it easier to solve common tasks in JavaScript are [jQuery](https://jquery.com/) and Alpine, and Stimulus. Additionally, there are somewhat more heavy JavaScript frameworks (commonly just called libraries) like React and Vue that make it easier to update site elements based on user behavior. A big selling point is that these libraries allow you to write HTML in JavaScript and thus you can control the structure of your site from a common source. One of the main use cases of these frameworks are single page applications (SPAs). A SPA is loaded only once and afterwards, everything is updated dynamically using Javascript. An example of a SPA application is Gmail.
- Moreover, as for the various backend languages, there are also more heavy-weight frontend frameworks like Ember and Angular. These frameworks introduce a specific, opinionated organization of your files and thus can help to stay organized as a project grows.

While most people agree that using a backend framework is a smart choice for most use cases, there is no such consensus regarding frontend frameworks. In particular, for solo developers it's easily possible to develop well-functioning, nice-looking sites without ever touching heavy stuff like Vue, React, or Angular. A lightweight CSS framework plus some jQuery (or one of its more modern alternatives) are often absolutely sufficient.  With that said, there are of course certain advantages to using a fully-fledged frontend framework. However, in particular for aspiring bootstrap entrepreneurs it's important to note that they aren't as essential as a proper backend framework. I decided to stick to Tailwind.css and jQuery until I feel the need for a more complex frontend approach.

**Combining the Puzzle Pieces**

Now that we've talked about various puzzle pieces, let's discuss shortly how they are commonly combined. In this context, it's conventional to invent acronyms for popular full-stacks.

- Arguably the most popular full-stack (again thanks to the popularity of WordPress) is the **LAMP stack**. LAMP stands for Linux, Apache, MySQL, and PHP respectively. In practice this means that you use a Linux server that runs Apache to redirect request to the suitable backend code files. The backend code is written in PHP and data is stored in a MySQL database. Note that there is nothing that indicates any frontend choice. The reason for this is that the LAMP stack comes from a time when sophisticated frontend development wasn't a big thing. You just used HTML, CSS, and maybe a bit jQuery. Since this was the standard, it was not necessary to point it out explicitly. There are many popular variants of the LAMP stack. For example, Apache is often replaced by Nginx and the stack is then called LEMP stack since Nginx is pronounced "engine X". Moreover, MySQL is sometimes replaced by Postgres. The resulting stack goes by the name LAPP. For small projects such details usually don't matter and LAMP, LEMP, and LAPP work equally well.
- Another full-stack that has become increasingly popular recently is the **MEAN stack**. MEAN is an acronym for MongoDB, Express.js, Angular.js and Node.js. Hence here the idea is to do everything, from the frontend to the backend in JavaScript. For the backend we use Express.js (which is a Node.js framework) that stores data in a MongoDB database. The frontend is written in Angular.js. The MEAN stack is particular popular among frontend developers who already know JavaScript very well and are thus happy to also use it for the backend. As for the LAMP stack there are lots of variants, like the MEEN stack where Angular.js is replaced by Ember.js. Note that since Linux has nowadays become the standard, people no longer feel the need to include it in their stack names.
- Another popular "stack" that doesn't have an acronym name is **Rails**. Even though Rails is a backend framework, it's also, in some sense, a complete stack since it allows you to build an integrated system that addresses all common issues, from the frontend JavaScript that you need to make live updates to the site, to Database changes, to the business logic in the backend. (With that said, it's important to note that it often can make sense to use a CSS framework and JavaScript libraries in Rails projects. However, since they play minor roles in this context, they aren't explicitly included in the stack name.) Since it's so standard to use Heroku to host Rails apps, there is no need to point this out. If people talk about the Rails stack, they usually mean a Rails monolith hosted at Heroku. The monolithic approach of Rails is, of course, ideal for solo-developers because it means that you just have to master one thing and don't need a team consisting of server, database, frontend, and backend specialists.
- Lastly, there is the **[JAMstack](https://kymellis.co/jamstack-marketing-headless-cms/)**. JAM is an acronym for JavaScript, APIs, and Markup. I still don't understand completely what the JAMstack is supposed to be. I remember listening to a [Podcast episode](https://www.codingblocks.net/podcast/jamstack-with-j-a-m/) in which three experienced web developers talked for two and a half hours about the JAMstack. However, despite multiple attempts they weren't able to pin down what the JAMstack really is and what it should be used for. Moreover, just have a look what the [official site](https://jamstack.org/) answers to the question "What is the Jamstack?". Well, there is no answer. They only thing they feel confident to say is that "the thing that [Jamstack sites] all have in common is that they don’t depend on a web server." But that's, by definition, the serverless approach, right? So what makes the JAMstack different? The best answer I can give is that JAMstack sites are analogous to sites that are created by static site generators like Jekyll, Hugo or Gatsby but additionally have certain dynamic features that are included via API calls. The simplest example would be adding a commenting section to a Jekyll blog using [Disqus](https://disqus.com/). Hence, the JAMstack doesn't seem ideal for complex web apps. For example, you wouldn't want to build something like Amazon using the JAMstack. But if your goal is to build a site that is primarily content focused with just a few dynamic elements sprinkled in here and there, the JAM approach may make sense.

Since I've just mentioned the serverless approach, it makes sense to discuss it in a bit more detail. 

## The Serverless Approach

The key idea behind the serverless approach is that you don't run your own server (not even virtually). Instead, you outsource things that are traditionally handled by the backend to specialized services. So serverless doesn't mean that there's no server. It only means that you're utilizing someone else's server. However, instead of a renting model in which you virtually own a server someone else runs for you (which already has been the standard for the past 20 years), in the serverless approach you're using someone else's server only in an on-demand fashion. In practice this means that your app makes API calls in the background to provide the necessary functionality to the users and you're only paid for what you're actually using. In other words, your bill is directly proportional to the number of API calls your app made to the service.

For example, let's say your app enables social media managers to create optimized images they can use in their Instagram and Twitter posts. In a serverless approach, the image resizing and optimization procedures are handled through API calls to external services. 

The big advantage of the serverless approach is that you don't have to worry about your server infrastructure and scaling issues at all. Moreover, you only pay for what you really use. However, this isn't necessarily a good thing. While most serverless bills are extremely cheap in the beginning, they often start to grow rapidly as your app become more popular. And there is always the danger of a surprisingly large bill because you configured something wrongly. 

In contrast, in a server renting model, you have to pay a fixed flat fee per month. When the server crashes it's your fault and responsibility to get it running again. However, in particular for bootstrap entrepreneurs, it's often sufficient to just restart the server and upgrade it, which can be down with a few mouse clicks. Servers have become incredibly cheap and a server that costs as little as $20 per month can handle large traffic spikes without problems.

In this context, it makes sense to talk about deployment abstractions before we dive deeper into the whole serverless world. 

### Deployment Abstractions

At one end of the spectrum, we have servers that you run yourself, for example, in your basement. These are known as "bare metal servers". At the other end of the spectrum, we have serverless architecture providers. In between these two extremes we have virtual private servers (VPS), and platform-as-a-service (Paas) providers. (Additionally, there are infrastructure-as-a-service (Iaas) providers that live somewhere in-between VPS and Paas but since the lines are quite blurry I've not included them in the discussion below. For example, a VPS is an example of an infrastructure-as-a-service.  As another aside, software-as-a-service (Saas) is what is often built using VPS, Iaas, Paas, or serverless architecture.)

{:.centered}
![](/images/deployment_abstraction.svg)

- No sane solo developer uses bare metal servers.
- Virtual private servers are, for example, commonly used for the LAMP and related stacks. By renting a virtual private server, you're getting full access to a computer that runs in someone else's data center. You can then install on the server software like Apache or Nginx to turn it into a proper web server and upload your website files to make them available on the internet. Popular providers are Linode, Digital Ocean, and Vultr and entry-level servers start at around $5 per month. Many of them provide one-click-installations of common full-stacks. Advantages of the virtual private servers are that they're incredibly cheap, fast, and you have full-control over everything. The downsides are that you're responsible for managing the server. You have to install updates regularly, secure it to make sure you won't get hacked, and respond to emergencies manually.

{:.rightaligned}
![](/images/development_hoster_user.svg)

- Platform-as-a-service providers are extremely popular for Rails apps with Heroku as the prime example. You just push your app to the Paas provider, and they do all the heavy lifting for you and makes it almost magically available on the web. Naturally, Paas providers charge quite a bit more than VPS providers. Typically, you pay around $7 per app. (Take note that a VPS can handle lots of different apps at once so a Paas approach is significantly more expensive if you're tinkering with lots of different apps.) An interesting [compromise](https://content.nanobox.io/moving-from-heroku-to-linode/) is to [host Paas-style software on your own VPS](http://dokku.viewdocs.io/dokku/).
- Last but not least, there are serverless architecture providers. As mentioned above, a complete serverless app consists of just a bunch of static HTML, CSS, and JavaScript files that are usually hosted on some content delivery network like Netlify or Vercel. All functionality is provided by utility APIs. For example, user registration and authentication can be handled by using Auth0, Firebase Authentication or Amazon Cognito. Payments can be handled by Stripe and search functionality can be added via [Algolia](https://www.algolia.com/). Data can be stored and retrieved in cloud databases like Cloud Firestore, DynamoDB or in at MongoDB Cloud. These kinds of services are also sometimes called backend-as-a-service providers. Moreover, files can be hosted in Amazon S3 buckets or using Firebase Hosting. And if you want to crunch data using custom code, you can just use something like [AWS Lambda](https://aws.amazon.com/lambda/) functions, Google Cloud Functions, or Azure Functions that allows you to run self-contained snippets of JavaScript or Python in the cloud. This is known as Functions-as-a-Service (Faas). (By the way, here's a [nice website](https://expeditedsecurity.com/aws-in-plain-english/) that explains the various Amazon Web Services (AWS) in plain English.)

A nice analogy for all of this are cars. You can either buy a car (=bare metal servers), rent a car ( =virtual private server), use Uber (=platform-as-as-service) or use a care sharing service (=use serverless architecture). In the latter two cases, you don't have to worry about car inspections and related issues. But this comfort comes at a price because these solutions become quite expensive if you use them a lot.

It's worth mentioning that deployment abstraction is not a black and white issue. It can make a lot of sense to build an app the traditional way and then use serverless functions wherever it makes sense. For example, the [Indiehackers site](https://www.indiehackers.com/about) uses an Ember.js backend that is hosted on a Paas provider ([AWS Elastic Beanstalk](https://aws.amazon.com/elasticbeanstalk/)) and uses Firebase for the database and user authentication. Another good use case is to delegate CPU-intensive jobs to serverless providers since this takes the memory/CPU load off your main app. This is what [Bannerbear](https://www.bannerbear.com/) uses which is a Rails app that utilizes serverless functions for image rendering.

If want to learn more about serverless architecture, here's a [great free resource](https://serverless-stack.com/). Moreover, you might want to look at dedicated frameworks like the [serverless framework](https://www.serverless.com/) (Node.js, Express.js), [Laravel Vapor](https://vapor.laravel.com/) (PHP, Laravel), [Lamby](https://lamby.custominktech.com/) (Ruby, Rails), and [Zappa](https://github.com/Miserlou/Zappa) (Python). 

Something I've noticed myself about the serverless approach is that it still suffers from the new hotness problem. This term describes, to quote Michael Hartl, a situation in which a "dizzyingly complex set of technologies seems to change every six months". In practice this means that most of the tutorials you find online are already outdated since everything changes quickly. Hence, a lot of your development time is dedicated to hunting tiny bugs that are due to some changes in the API or elsewhere. Another important aspect is that there's always a certain element of vendor-lock-in. This means that you'll become extremely dependent on the serverless architecture provider since it's a lot of work to change to a different provider. Hence, should the provider decide to raise its prices dramatically or shut down, you could run into big problems. 

## A few Warnings

Let's end this already far too long article with a small warning. 

You shouldn't trust blindly anything I wrote above. I'm not an expert and you should definitely do your own research. 

However, be careful who you listen to. Most advice that you'll find online is coming from people who have a very different background and different goals than you. For example, if your goal is to build complete web apps as a solo-developer the recommendations by an engineer at Google will probably not be particularly helpful. Most best practices in large or even small software teams are simply not practicable for a solo-developer. 

So my strategy is to find advice and recommendations from people who are just one or two steps ahead of me, from people who do what I want to do, and I ignore all the rest. 

I play around with different options until I find something that I like. Then I'll stick to it until I've built what I've wanted to build. If I didn't find the experience enjoyable, I move on to the next thing. 

Once you've found an approach that is enjoyable and works, it rarely makes sense — in particular as a bootstrap entrepreneur — to switch to something completely different. As long as you're able to make your ideas a reality, this is all that matters. Your users don't care about your tech stack.
