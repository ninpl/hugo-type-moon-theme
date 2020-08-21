<h1 align="center">
  <br>
  <a href="https://github.com/moonantonio/hugo-type-moon-theme"><img src="https://github.com/moonantonio/hugo-type-moon-theme/blob/master/images/logo.png?raw=true" alt="LogoRepo" width="100"></a>
  <br>
  Hugo Type Moon Theme
  <br>
</h1>

<h4 align="center">Theme for <a href="https://gohugo.io/" target="_blank">hugo</a>, light and with different features.</h4>

<p align="center">
  <a href="https://gohugo.io/">
    <img src="https://img.shields.io/badge/hugo-v0.50-brightgreen"
         alt="Hugo">
  </a>
  <a href="https://pages.github.com/">
    <img src="https://img.shields.io/badge/Static-%20Web-blue">
  </a>
</p>

<p align="center">
  <a href="#about-the-project">About The Project</a> •
  <a href="#how-to-use">How To Use</a> •
  <a href="#download">Download</a> •
  <a href="https://github.com/moonantonio/hugo-type-moon-theme/blob/master/README.es.md">Spanish</a> •
  <a href="#contributors">Contributors</a> •
  <a href="#license">License</a>
</p>
<p align="center"><img src="https://github.com/moonantonio/hugo-type-moon-theme/blob/master/images/fondo.png?raw=true" width=600 alt="Screenshot of Example"></p>

<p align="center"><em>Image of the general cover of the theme. Check it out at <a href="https://themes.gohugo.io/">hugo.themes</a>.</em></p>

## About The Project

<img src="https://github.com/moonantonio/hugo-type-moon-theme/blob/master/images/info.png?raw=true" align="right"
     alt="Info" width="200" height="320">
     
A free and open-source ~~Jekyll~~ Hugo theme. Great for blogs and easy to customize. This theme is a port of the original [Type theme](https://github.com/rohanchandra/type-theme) made by [Rohan Chandra](https://github.com/rohanchandra). Noteworthy features of this Hugo theme are the integration of a comment-system powered by Disqus, Google Analytics and localization (l10n) support.

* **Google Analytics** - System that easily connects with Google Analytics to **record your website data in a metric**. Following all the traffic flow that is generated.

* **Localization** - All the information of type-moon-theme is in a file, if you don't want a website in English, you can **change to the language** you want easily. Editing the file that contains all the strings related to the topic.

* **Portraits** - You can customize the different **article entries with the portraits** you want. Just loading them from the root of the image files. Slightly modifying the vision in each of the entrances.

* **Descriptive Icon** - Icons at the top of the title, which define the content of the post for the reader. For example, if there is code inside an entry, you can warn using this option. There are also options for **documents, music, files**, among others.

* **Comments** - Comments via Disqus. It is a **global blog comment hosting service** for websites and online communities using a network platform.

## How To Use

I assume you've **Git installed**. Inside the folder of your Hugo site run

		$ hugo new site blog
    $ cd blog
		$ git init
    $ git submodule add https://github.com/moonantonio/hugo-type-moon-theme.git themes/hugo-type-moon-theme
		$ echo 'theme = "hugo-type-moon-theme"' >> config.toml
		$ hugo server

You should see a folder called `hugo-type-moon-theme` inside the `themes` directory that we created a few moments ago.
Now we have to replace some files and do a little configuration of the web.

 * **exampleSite** - Copy the **data folder** that is in exampleSite and paste it in the root of the blog (./). Copy the file **config.toml** that is in exampleSite and paste it in the root of the blog.

> To turn the exampleSite folder in a standalone demo site the themesDir property has been set to ../... This way you can preview this theme by running hugo server inside exampleSite folder.
> Due to the customized themesDir path Hugo will fail to find themes if you copied the config.toml into the root directory of a regular Hugo website. Make sure you comment out the themesDir property if you use the theme in production.

 * **The config file** - Now, let us take a look into the **config.toml**. Feel free to play around with **the settings**.

---

| Parameter | Description |
| :-------: | :----------:|
| `baseurl = "https://replace-this-with-your-domain.com/"` | Change for your domain. |
| `languageCode = "es-es"` | Language of the web |
| `title = "Type moon theme"` | Title of the web |
| `theme = "hugo-type-moon-theme"` | Theme that the web contains |
| `disqusShortname = "spf13"` | The optional comment system is powered by Disqus. Enter your shortname to enable the comment section under your posts. With the **disableComments** frontmatter parameter you can disable the comment section for each page individually. |
| `googleAnalytics = ""` | The same applies to the activation of Google Analytics. Enable it by entering the tracking code for your website. |
| `paginate = 10` | Post that each page will have. |
| `themesDir = "../.."` | Uncomment it to lift a temporary site from the template folder, comment it for production. |
| `author = "Your name"` | Author of the web. |
| `description = "Add a description of your website"` | Description of the web. |
| `keywords = "keyA,keyB,keyC..."` | Keys to find the web. |
| `avatar = "img/avatar.png"` | Avatar of your user, appears in each publication. |
| `gravatar = "your@email.com"` | In case you have your avatar in gravatar, you can access it through your email. |
| `headerText = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.<br><br>Remove all header text in **config.toml** to disable this feature."` | Header text that appears in front of the background. |
| `headerImage = ""` | Image of the header that appears on the home page. |
| `copyright = "Released under the MIT license<br>Powered by [Hugo](//gohugo.io/) with the [Type Moon Theme](//github.com/moonantonio/hugo-type-moon-theme)"` | Copyright that is written at the end of the web. |
| `title = "Type moon theme"` | Set title for Hugo's opengraph template |
| `mainSections = []` | Define which types of content shall be displayed on the homepage. |

---

* **The archetypes file** - Every time you create **a new post**, you will get various options to fill in.

---

| Parameter | Description |
| :-------: | :----------:|
| `featureimage = "img/bg.png"` | Define a thumbnail by entering the relative path to the image in the parameter of the post, this way you can store them either next to the content file or in the `static` folder. |
| `portraitimage = "img/portrait/portrait0000.png"` | Define a portrait by entering the relative path to the image in the parameter of the post, this way you can store them either next to the content file or in the `static` folder. |
| `title = "{{ replace .TranslationBaseName "-" " " | title }}"` | The title of the post. |
| `date = {{ .Date }}` | The date of entry. |
| `draft = true` | Determines if the input is in draft mode and therefore will not be processed. |
| `tags = ["type"]` | Tags separated by commas. |
| `categories = ["type"]` | Categories separated by commas. |
| `menu = "nav"` | You can define menu entries as you like by linking a post or any other site. First, let us link a post that you've written. We can do this in the frontmatter of the post's content file by setting `menu` to `nav`. That's it. |
| `type = "fa fa-file"` | Type of information found within the entry. |
| `disableComments = "true"` | Turn off comments. |

---

In order to see your site in action, run Hugo's built-in local server.

    $ hugo server

Now enter [`localhost:1313`](http://localhost:1313) in the address bar of your browser.

---

 <img src="https://github.com/moonantonio/hugo-type-moon-theme/blob/master/images/info.png?raw=true" align="left"
     alt="Info" width="190" height="290">

## Download

You can [download](https://github.com/moonantonio/hugo-type-moon-theme/releases) the latest installable version of **Hugo Type Moon Theme**.

## Contributors

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

The project is now maintained by [Moon Antonio](https://github.com/moonantonio), created by [Rohan Chandra](https://github.com/rohanchandra), port by [digitalcraftsman](https://github.com/digitalcraftsman) and fix by [Andy Grunwald](https://github.com/andygrunwald) with the help of collaborators ([list](https://github.com/moonantonio/hugo-type-moon-theme/graphs/contributors)).

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore -->

| [<img src="https://avatars3.githubusercontent.com/u/7427480?s=460&u=6c19110c744836fd6265dd1b4781e6ddd22dd20a&v=4" width="100px;"/><br /><sub><b>Moon Antonio</b></sub>](https://moonantonio.github.io/)<br /> | [<img src="https://avatars2.githubusercontent.com/u/816965?s=460&u=cfac03d73d63c2f1f61e0ed4f88a8bfb88f24274&v=4" width="100px;"/><br /><sub><b>Rohan Chandra</b></sub>](https://github.com/rohanchandra)<br /> | [<img src="https://avatars0.githubusercontent.com/u/7010165?s=460&v=4" width="100px;"/><br /><sub><b>digitalcraftsman</b></sub>](https://github.com/digitalcraftsman)<br /> | [<img src="https://avatars1.githubusercontent.com/u/320064?s=460&u=9a53426eee768d13406cabcead926211cd3343a0&v=4" width="100px;"/><br /><sub><b>Andy Grunwald</b></sub>](https://github.com/andygrunwald)<br /> |  | | |
| :-----------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------: |

<!-- ALL-CONTRIBUTORS-LIST:END -->


## License
[MIT](https://github.com/moonantonio/hugo-type-moon-theme/blob/master/LICENSE.md)

---

> [moonantonio.github.io](https://moonantonio.github.io/) &nbsp;&middot;&nbsp;
> GitHub [@moonantonio](https://github.com/moonantonio) &nbsp;&middot;&nbsp;
> Twitter [@AntonioMoonNull](https://twitter.com/AntonioMoonNull)
