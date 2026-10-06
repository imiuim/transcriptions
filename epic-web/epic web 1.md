# Kent C. Dodds - Epic Web. Ship Modern Full-Stack Web Applications

- 来源：[B站 BV1EAVxzWEt2](https://www.bilibili.com/video/BV1EAVxzWEt2)（up 主：lmt831，共 100 P）
- 说明：英文转录 + 中文翻译（机器翻译，仅供学习参考）

---

## 01. 01. Intro to Full Stack Foundations Workshop

**原文**

Welcome to the full stack foundations workshop of Epic Web Dev. My name is Kent C. Dodds and I am so excited that you've jumped into my spaceship so that we can take off into space and learn all about building full stack web applications. We're going to be doing the foundational stuff, the stuff that is going to be applicable to you, whatever technologies or tools that you're using that will be really valuable to you as a full stack web developer. We're going to start with the foundational stuff. And so we're getting into styling.

**译文**

欢迎来到 Epic Web Dev 的全栈基础工作坊。我叫 Kent C. Dodds，非常高兴你登上了我的宇宙飞船，我们将一起飞向太空，学习如何构建全栈 Web 应用。我们将学习一些基础内容，这些内容无论你在用什么技术或工具，都将对你作为一名全栈 Web 开发者非常有价值。我们将从基础开始。现在，我们进入样式设计部分。

## 02. 02. Intro to Styling

**原文**

All right, styling, it's going to be awesome. We're going to be learning all about how to link resources onto our page, not just styles, also favicon, but you can actually use the same approach for linking a bunch of different kinds of resources as well. And so the basic idea with HTML to link resources onto the page is by using the link tag. You can read all about the link tag on the Mozilla development network, the MDN web docs, and there are actually a lot of things

**译文**

好的，接下来是样式部分，效果一定会很棒。我们将学习如何将各种资源链接到页面上，不仅仅是样式表，还包括 favicon。实际上，同样的方法也适用于链接各种不同类型的资源。在 HTML 中，链接资源到页面的基本方法是使用 `<link>` 标签。你可以在 Mozilla 开发者网络（MDN 网页文档）上详细了解 `<link>` 标签，其实它涉及的内容非常多。

## 03. 03. Manage Asset Links in a Remix Application

**原文**

There's not much to our application and in fact if we look at our HTML right here then we'll see we don't even have anything in the head, we barely have anything in the body and then just some stuff here that's added by remix for the scripts and everything. So there's nothing in here but we do have a favicon and if we go to our network tab and do a refresh here we'll see that favicon is being requested right here. That favicon is inside of our public directory so public slash favicon.ico and that

**译文**

我们的应用其实很简单。事实上，如果我们看看这里的 HTML，就会发现 head 部分几乎没有任何内容，body 部分也几乎为空，只是有一些 Remix 为脚本等添加的内容。因此，这里几乎什么都没有，但我们确实有一个 favicon。如果我们打开网络（Network）选项卡并刷新页面，就能看到 favicon 正在这里被请求。这个 favicon 位于我们的 public 目录下，即 public/favicon.ico。

## 04. 04. Using Remix's Links Component

**原文**

To get things started, I'm actually going to ignore Cody the koala and Marty the money bag really quick because I want to show you what things look like without using the special remix API is first. So we're going to just stick this right here, say link. And the link is all going to be the exact same as what we have with the remix API. So we're going to have a rel is icon. And the type is image SVG XML and slash favicon SVG. Thank you co pilot.

**译文**

为了开始，我其实会暂时忽略考拉 Cody 和钱袋 Marty，因为我想先给大家展示一下不使用特殊的 remix API 时是什么样子。所以我们直接把它放在这里，写上 link。而这个 link 将与我们使用 remix API 时的完全相同。所以我们会设置 rel 为 icon，type 为 image/svg+xml，然后是 /favicon.svg。谢谢 co pilot。

## 05. 05. Asset Import Caching Issue

**原文**

All right, so we've got a new problem and that is what if we decided, you know what? I don't want it to be this purple color. I want it to be red. We're just gonna hard code it as red. And so now I'm going to refresh and the favicon isn't updated. I refresh over and over and over again. It's not being updated. And this is because of a cache. You'll see right here in our favicon request, we have this disk cache is what it's showing under the size. That's because it's not actually asking our server for the updated file for our favicon.

**译文**

好的，我们现在遇到了一个新问题：如果我们决定——你知道的——我不想要这个紫色了，我想要红色。我们干脆直接把它硬编码为红色。现在我来刷新一下，但 favicon 并没有更新。我一遍又一遍地刷新，它就是不更新。这是因为缓存的问题。你会看到这里，在我们的 favicon 请求中，大小这一栏显示的是“磁盘缓存”。这是因为浏览器并没有真正向我们的服务器请求更新后的 favicon 文件。

## 06. 06. Caching the Favicon

**原文**

So here we have our purple favicon and let's say that we wanted to change it to orange. All right, so I'm going to save that I hit refresh. Nothing happens. Not good. Not what I want at all. And so what we're going to do is we're going to copy this or we'll just move it. We're not going to need it here anymore. We're going to move it up into our app directory. So we're going to call this assets. This is just my decision. It's not really convention doesn't doesn't actually have any bearing on how things work. I just like to put my assets in a folder called assets.

**译文**

现在我们有了这个紫色的 favicon，假设我们想把它改成橙色。好的，我先保存一下，然后点击刷新。什么都没有发生。这可不行，完全不是我希望的结果。所以我们要做的就是复制这个文件，或者直接把它移动一下。我们以后就不再需要它放在这里了，要把它移到我们的 app 目录里。我们会把这个文件夹命名为 assets。这只是我自己的决定，其实这并不符合什么特定的惯例，也并不会对实际运行产生任何影响。我只是喜欢把资源文件放在一个名为 assets 的文件夹里。

## 07. 07. Add Custom Fonts to the Global CSS

**原文**

Now we want to have a CSS file that applies globally on our application and you add CSS file or style sheets, those resources via link tags. And so we've got this CSS file our font.css. That's under app styles font.css. And it configures all of our fonts that includes references to slash fonts, which we'll find in the public directory slash fonts and then our font name, and then all the fonts that are in here. So what we're going to do is we need to

**译文**

现在我们需要一个在全局应用中生效的 CSS 文件。您可以通过 link 标签添加 CSS 文件或样式表资源。我们这里有一个 CSS 文件 font.css，它位于 app/styles/font.css 目录下。该文件配置了我们所有的字体，其中包括对 /fonts 的引用——这些字体文件存放在 public/fonts 目录下，后面跟着字体名称以及该目录下的所有字体文件。接下来我们需要做的是：

## 08. 08. Adding Global Styles to a Remix App

**原文**

To get this CSS file on the page, we need to use a link. And so we're going to import our font style sheet URL from styles font. So here's our styles font.css. And with that, then we can add a rel of style sheet. And there's our href. That's our font style sheet URL here. Let's go ahead and console like that. So we can take a look at what that looks like in our console. And there it is.

**译文**

要将这个 CSS 文件引入页面，我们需要使用一个 link 标签。因此，我们要从 styles font 导入我们的字体样式表 URL。这里就是我们的 styles font.css。然后，我们可以添加一个 rel 属性为 stylesheet。这里就是它的 href，也就是我们的字体样式表 URL。现在我们按照这样的方式在控制台中输出，以便查看它在控制台中的显示效果。就是这样。

## 09. 09. Using PostCSS and Tailwind CSS in Remix

**原文**

Writing raw CSS is perfectly fine, but there are some differences between browsers and there are a couple of new features that you may want to use and have those features kind of be automatically rewritten for you to support older browsers, things like that. And so that's where tools like post CSS come in really handy. The ability to automatically transform the CSS code that you write into something that all your browsers can actually evaluate can be quite helpful. On top of that,

**译文**

直接编写原始的 CSS 是完全可行的，但不同浏览器之间存在一些差异，而且还有一些你可能想使用的新特性。如果这些特性能够被自动转换，以便兼容旧浏览器，那就再好不过了。而这正是 PostCSS 这类工具大显身手的地方。能够将你编写的 CSS 代码自动转换为所有浏览器都能实际解析的形式，这一点非常有用。此外，

## 10. 10. PostCSS and Tailwind CSS Configuration

**原文**

Let's start by creating a post css.config.js file right here and I'm going to copy our config that we had in our instructions and stick that there. This is going to give us a nesting in our tailwind classes and then the tailwind css plugin itself so that we can actually use apply and the other directives that are supported by tailwind and then auto prefixer so we don't have to worry about vendor prefixing anything regardless of whatever cool stuff

**译文**

我们先在这里创建一个 postcss.config.js 文件，然后我将把之前说明中的配置复制粘贴到这里。这样就能在 Tailwind 类中实现嵌套功能，同时引入 Tailwind CSS 插件，以便我们实际使用 `apply` 以及其他 Tailwind 支持的指令。此外，还会加入自动前缀处理工具（auto prefixer），这样我们就不必担心任何酷炫功能的前缀问题了。

## 11. 11. Bundling CSS in Remix

**原文**

Sometimes you need to use a library that comes with styles all baked in and you need to include those styles on the page. Other times you have some global CSS that you want to have applied on the page and there are various situations where maybe you'd be writing your own component and you want to have co-locate that component with its CSS but then you have to get that CS onto the page somehow and if you did a bunch of components like this then your links in that root is are going to get very

**译文**

有时你需要使用一个自带内嵌样式的库，并且需要将这些样式引入页面。有时你有一些希望应用到页面上的全局 CSS。此外，还有各种情况：比如你在编写自己的组件时，希望将该组件与其 CSS 放在一起，但又必须以某种方式将该 CSS 引入页面；如果你以这种方式创建了许多组件，那么根目录中的链接就会变得非常……

## 12. 12. Configure CSS Bundling

**原文**

To get this global CSS file included onto the page, we're actually already importing it. We're doing what is called a side effect import. And what that means is we're not actually using any of the values that are being exported by this particular file. And in the case of CSS, CSS doesn't actually export anything. Remix is adding some special meaning to these CSS imports. And in fact, you can't technically import CSS files anyway. So there's a little bit of magic going on here as well as here. But there's some different magic

**译文**

要让这个全局 CSS 文件包含在页面中，我们实际上已经在导入它了。我们执行的是所谓的“副作用导入”。这意味着我们并没有真正使用该文件导出的任何值。就 CSS 而言，CSS 本身并不会导出任何东西。Remix 为这些 CSS 导入赋予了一些特殊含义。事实上，从技术上讲，你本来就无法导入 CSS 文件。因此，这里和这里都有一些“魔法”在起作用。不过，这些“魔法”各有不同。

## 13. 13. Dad Joke Break

**原文**

Alright, so here's your dad joke. Did you hear about the scientist who had lab partners with the pot of boiling water? He had a very esteemed colleague. Hopefully that gives you a little bit of a laugh. It's important to take breaks between these exercises. So get up, do a little bit of a stretch, and then get right back to it. Let's learn the next thing.

**译文**

好的，下面给你讲个老爸式冷笑话。你听说过那位和沸腾的水锅做实验搭档的科学家吗？他有一位非常“受尊敬”的同事。希望这能给你带来一点笑声。在这些练习之间休息一下很重要。所以，站起来稍微伸展一下，然后再继续回来。我们来学习下一个内容吧。

## 14. 14. Intro to Routing

**原文**

I am really excited about routing. Routing is one of the coolest parts of the web. While other native platforms don't typically have any concept of a URL and they kind of have to come up with your own thing, the web has always had this URL that people can bookmark, they can send to each other, they can share on social media, they can without any special like attention as far as the developer is concerned, you just, there it is, they can share that URL. You can email them the URL and have them go exactly where

**译文**

我对路由真的非常兴奋。路由是网络中最酷的部分之一。虽然其他原生平台通常没有 URL 的概念，不得不自己想办法实现类似功能，但网络一直都有这种 URL——人们可以将其收藏、互发、分享到社交媒体，而且作为开发者，你几乎不需要做任何特殊处理，它就在那里，他们可以直接分享这个 URL。你可以通过电子邮件把 URL 发给他们，让他们精准地跳转到指定的位置。

## 15. 15. Routing in Remix

**原文**

For this exercise, you're going to be adding a bunch of files following the remix flat routes convention. And you're going to have all the instructions that you need in the instructions. You'll be following along Cody in the instructions here because you're creating new files are not going to find Cody in the code comments because those files don't exist yet. So just follow Cody's instructions. But I want to show you what things will look like when you're all finished. So you're going to have a slash users slash Cody route that will show Cody's name.

**译文**

在本练习中，你将按照 remix 扁平路由规范添加大量文件。所有必要的说明都已在“Instructions”中找到。你将按照这里的“Instructions”中的 Cody 的指引操作，因为你正在创建新文件，而目前代码注释中还没有 Cody（因为这些文件还不存在）。因此，只需遵循 Cody 的说明即可。不过，我想向你展示最终完成后的效果。届时，你将拥有一个 `/users/Cody` 路由，用于显示 Cody 的名字。

## 16. 16. Creating User Profile and Notes Pages with Remix Routes

**原文**

Let's start by running npx remix routes to get an idea of our current route layout. So we have our routes here is our root route. So that's that root TSX and then our route index. It's our index route for this URL segment, which is just slash and the files routes index TSX. So we don't have very many routes here. Let's get started with our user profile page. So that's going to be slash user slash username. We're

**译文**

我们先运行 `npx remix routes`，了解一下当前的路由结构。这里就是我们的路由，这是我们的根路由。也就是那个根目录下的 `TSX` 文件，然后是 `index` 路由。它是这个 URL 分段的索引路由，也就是根路径 `/`，对应的文件是 `files/routes/index.tsx`。目前我们的路由并不多。现在我们来开始处理用户个人资料页面。它的路径将是 `/user/username`。我们

## 17. 17. Adding Navigation Links

**原文**

As a user, it would be kind of nice to be able to navigate around this rather than having to update the URL all over the place. So I want to make the link for where the logo is at. I want that to send people back to the home page. That's a pretty common practice. Also the one in the footer. And then I want to have a link that will take me back to the user's profile page. So this, we need a link that'll take us back here. And then on this page, we need a link that takes us to the notes page. And then on here, I want to have a link that

**译文**

作为用户来说，能够方便地导航会比到处都去更新 URL 要好得多。所以我想为徽标所在的位置创建一个链接，让用户点击后可以返回首页。这是一种非常常见的做法。页脚中的链接也需要这样做。然后，我还需要一个能返回用户个人主页的链接。因此，这里需要一个能跳转回这里的链接。接着，在这个页面中，我们需要一个能跳转到笔记页面的链接。然后，在这里，我希望添加一个链接……

## 18. 18. Adding Absolute and Relative Links

**原文**

Let's start by making the epic notes in the header and footer link to the homepage. So we're going to change this div to a link and that's going to come from remix run react. And that's going to go to slash that's the homepage. And we'll do the same thing down here. And that's a link right here. And now if I click on that, boom, I go home. Awesome. And then we're going to need to have a link on the user profile.

**译文**

让我们先让页眉和页脚中的“史诗笔记”链接到主页。因此，我们将把这个 div 改为一个链接，这个链接将通过 remix run react 实现，并指向斜杠，也就是主页。下面的部分我们也会做同样的处理，这里就是一个链接。现在如果我点击它，砰的一声，我就回到了主页。太棒了。接下来，我们还需要在用户个人资料上添加一个链接。

## 19. 19. Adding Dynamic Parameter Support

**原文**

So we have more users than just the one Kodi user and our users are each going to have more than just the sum note ID. They're going to have a bunch of different notes. And so hard coding Kodi and some note ID right here is not really going to work out. And so your job is to make those things dynamic. And so when you're all finished, you should be able to go to any username here. And then also some note ID will still work, but you should be able to go to some other note ID.

**译文**

因此，我们的用户不止一个 Kodi 用户，而且每个用户都会有不止一个便签 ID。他们将拥有许多不同的便签。所以，在这里硬编码 Kodi 和某个便签 ID 显然是行不通的。你的任务就是让这些内容变得动态化。完成之后，你应该能够访问这里的任意用户名，然后输入某个便签 ID 仍然可以正常工作，同时你也应该能够访问其他便签 ID。

## 20. 20. Access Params with useParams

**原文**

For us to make this stuff dynamic, we're going to need to rename some of these things. So typically in a routing system, the dynamic portions of the URL are signified by a colon, but we can't use colons in the file system. And so instead we use the dollar sign because we like money a lot. Just kidding. Well, I mean, I kind of like money, but yeah, so we're going to say dollar and then username. That's the name of the param. And we'll have to do the same thing here to keep these

**译文**

为了让这些内容变得动态，我们需要重命名其中一些东西。通常在路由系统中，URL 的动态部分会用冒号来表示，但在文件系统中我们不能使用冒号。因此，我们改用美元符号，因为我们很喜欢钱。开个玩笑啦。好吧，我确实有点喜欢钱，但总之，我们要写成 dollar 然后 username。这就是参数的名称。我们在这里也需要做同样的处理，以保持这些

## 21. 21. Adding a Resource Route

**原文**

Sometimes you need to have some routes that are just there to serve data or to send some kind of response like a CSV or a generated PDF or all kinds of things. You can do all sorts of things with HTTP. And it's not just UI that you want to serve on HTTP. You're not just wanting to send HTML and JavaScript and those static assets. Sometimes you want to dynamically generate some assets. And so for what we're going to do is we're going to add what's called a health check endpoint

**译文**

有时，你需要一些仅用于提供数据或发送某种响应的路由，例如 CSV、生成的 PDF 等各种格式的内容。你可以通过 HTTP 实现各种各样的功能。HTTP 并不仅仅用于提供用户界面，你也不仅仅想发送 HTML、JavaScript 以及这些静态资源。有时你还需要动态生成一些资源。因此，接下来我们要做的就是添加一个所谓的“健康检查端点”。

## 22. 22. Example Resource Route Usage

**原文**

We want the URL for our resource route to be at resources slash health check. That's where we want this to go. Not for any particular reason that is important as far as the framework is concerned. We can have this literally be anywhere that we want. But I like putting my resource routes under resources just because it makes more sense. And especially since this is for automation purposes and the users are never really going to see this, I don't really mind having that kind of convention myself.

**译文**

我们希望资源路由的 URL 为 `resources/health-check`。这正是我们希望它所在的位置。就框架而言，这并没有什么特别重要的原因。我们实际上可以把它放在任何想要的位置。但我喜欢将资源路由放在 `resources` 下，因为这更符合逻辑。尤其是由于这是用于自动化目的，用户也根本不会真正看到它，所以我自己并不介意采用这样的约定。

## 23. 23. Dad Joke Break_2

**原文**

All right, you've been working hard. Let's get a dag joke in here. Don't trust Adams. They make up everything. Hopefully that gave you at least a little bit of a chuckle that's good for your body and for your brain to laugh a little bit and smile. So now you should probably get up and walk around a little bit, take some notes on some of the things that you've learned before you get yourself ready for the next exercise. So you've been working hard. You deserve this. You're doing awesome. Keep up the good work and let's

**译文**

好了，你一直都很努力。现在我们来讲一个 DAG 笑话。别相信亚当斯（Adams），他们什么都瞎编。希望这个笑话能让你会心一笑——笑一笑对身体和大脑都有好处。所以现在你最好站起来稍微走动一下，在准备下一个练习之前，把学到的内容记一记。你一直都很努力，应该得到这样的放松。你做得非常棒，继续加油！

## 24. 24. Intro to Loading

**原文**

Most apps wouldn't be apps without some data loading. We need some dynamic data. And so that's what we're going to be doing in this exercise, where we can actually load data for a particular user. And you can take a look at the network tab. And as we navigate between these, we're loading data as we go. So here's the note, the title and the content. And then we go to another one and boom, we've got a note with the title and the content. So we do dynamic loading as we navigate around the app. But then we also do full server rendering.

**译文**

大多数应用如果没有数据加载功能，就无法称之为应用。我们需要一些动态数据。因此，在本练习中，我们将实现为特定用户加载数据的功能。你可以查看网络（network）选项卡。当我们在这些页面之间导航时，数据会随之加载。比如这里，我们看到了笔记的标题和内容。接着我们切换到另一篇笔记，砰的一声，就加载出了带有标题和内容的笔记。因此，当我们在应用中导航时，会进行动态加载。但同时，我们也会进行完整的服务器端渲染。

## 25. 25. Loading Data to Your Database

**原文**

So Kelly, the co-worker has been at work again. And now we have a nicer designed page here, which is nice. But we have some work to do. We want to actually load the data right here for all of the users notes and load the actual note content itself. And the final version looks something like this. So that is a much nicer look. And it is doing exactly what we want it to do. Where this data comes from is a mock database implementation.

**译文**

那么，同事 Kelly 又来上班了。现在我们有了一个设计更精美的页面，这很好。但我们还有一些工作要做。我们想在这里为用户的所有笔记加载数据，并加载实际的笔记内容。最终版本大致是这个样子。这样看起来美观多了。而且它完全实现了我们的预期功能。这些数据来自一个模拟的数据库实现。

## 26. 26. Efficient Data Loading in a Remix App

**原文**

To get started on this profile route, we're going to import our DB file from app utils DB server. So that's the file that's right here app utils DB server. And with that, then we can add our loader export. So it's export a function called loader. And this is going to take our data function args. So we're going to use the params from data function args. And that's coming from remix run node. And that is a type. We'll just stick that up.

**译文**

要开始这个 profile 路由，我们将从 app utils DB server 导入我们的 DB 文件。也就是这里的这个文件：app utils DB server。然后，我们就可以添加 loader 导出。即导出一个名为 loader 的函数。该函数将接收我们的 data function args。我们将使用 data function args 中的 params。它来自 remix run node。这是一个类型，我们直接把它放上去即可。

## 27. 27. Handling Error Messages

**原文**

So this works fine until you decide you want to try something funny and then you get a big kablooey with an error message that really isn't all that useful. We'll take care of handling error messages and making them look nice in a future part of this workshop, a future exercise. But we do want to make things work a little bit nicer for us during our development time and that means making TypeScript happy. Again, I repeat

**译文**

所以，一切运行正常，直到你决定尝试一些有趣的东西，然后就会“砰”地一声，弹出一个其实没什么用的错误信息。我们将在本次工作坊的后续部分、也就是未来的练习中，学习如何处理错误信息并让它们看起来更美观。不过，我们还是希望在开发阶段让事情变得稍微顺利一些，而这也就意味着要让 TypeScript 满意。我再说一遍：

## 28. 28. Handling Error Responses with Remix

**原文**

So we've got a couple places that are missing data. We threw up this TS expect error that Lily the life jacket is super not into. So we're going to remove those here really quick so that we can reveal that. And basically the problem is this query to our database could potentially give us a null for the user because maybe the user doesn't exist. And so what we're going to do is add an if statement to say if there's not a user, then we're going to throw a new error. And that makes TypeScript happy.

**译文**

所以我们发现有几个地方缺少数据。我们抛出了这个 TypeScript 的 expect 错误，Lily（救生衣）对此非常不感冒。所以我们现在快速把这些地方移除掉，以便能揭示出这个问题。基本上，问题在于这个数据库查询可能会为我们返回一个 null 值，因为用户可能不存在。因此，我们要添加一个 if 语句，说明如果没有用户，我们就抛出一个新的错误。这样一来，TypeScript 就会满意了。

## 29. 29. Dad Joke Break Loading

**原文**

Here's a little levity for you. A red and blue ship just collided in the Caribbean. Apparently the survivors are marooned. So hopefully that gives you a little bit of a chuckle. So I want you to get up and just walk around in a circle at least or something. It's important for you to move your body as you're learning. That will help blood flow in your brain, which will make you more effective. So yes, make sure to take these breaks and then let's get back to it in the next exercise.

**译文**

给你讲个轻松的小故事。一艘红色的船和一艘蓝色的船刚刚在加勒比海相撞了。据说幸存者们都被困在了荒岛上。希望这能给你带来一点笑声。现在，我希望你能站起来，至少绕着圈子走一走。在学习的时候活动身体很重要，这有助于促进大脑的血液循环，让你学习效率更高。所以，一定要记得适时休息一下，然后我们在下一个练习中再继续。

## 30. 30. Intro to Mutations

**原文**

Applications need to mutate data. Users need to be able to interact with that data. And this is where building web apps can be really complicated unless you're doing things the way we're going to do it. And it's awesome. So we're going to talk about data mutations. So in this exercise, you're going to be able to make a change to one of the notes and it will apply and it will be awesome. You'll also be able to delete notes. And that will also work. So the and and that's a form submission that we're going to be doing. That is just a

**译文**

应用程序需要对数据进行修改。用户需要能够与该数据交互。而构建 Web 应用正是在这一点上变得非常复杂，除非你采用我们即将介绍的方式。这种方式非常棒。因此，我们将讨论数据修改。在本练习中，你将能够对其中一条笔记进行修改，修改后效果会立即生效，而且体验非常棒。你将还能够删除笔记，这同样也能正常工作。而这正是我们通过表单提交来实现的功能。这仅仅是

## 31. 31. Building Forms

**原文**

So Kelly, our coworker did some more work for us. She's so great. And what she did was add this bar down here with a non-functional delete button, which you will be responsible for implementing later. And this edit button, which takes you to this page, this is the solution. Your job is to make it look like this. You won't be able to submit the form. If you try, it'll just blow up. But you should create this form just to get things going here for where you're starting.

**译文**

那么，Kelly——我们的同事——又帮我们完成了一些工作。她真是太棒了。她在这里添加了这个横栏，里面有一个目前还无法使用的“删除”按钮（稍后需要你来实现），还有一个“编辑”按钮，点击后会跳转到这个页面，也就是解决方案页面。你的任务是让这个页面看起来像现在这样。你将无法提交这个表单——如果你尝试提交，程序就会崩溃。不过，你还是需要创建这个表单，以便为后续开发打下基础。

## 32. 32. Creating Form Components with Remix

**原文**

Our note edit route is not really doing too much. We're just rendering the data. So let's make it render a form instead. We're going to return a remix form. So capital FORM, and that's going to come from remix run react. And yes, we do want method post. So we're going to do all caps post here. But the method post is important because we don't want to put the data that's in the form in the URL. We want it in the body of the request. So we're not going to

**译文**

我们的笔记编辑路由目前并没有做太多事情。我们只是在渲染数据。因此，让我们让它渲染一个表单吧。我们将返回一个 Remix 表单。所以使用大写的 FORM，它来自 remix run react。是的，我们确实需要使用 POST 方法。因此，我们在这里使用全大写的 POST。但 POST 方法很重要，因为我们不想将表单中的数据放在 URL 中，而是希望将其放在请求体中。所以我们不会

## 33. 33. Handling POST Requests for Form Submission

**原文**

With our form all set up, we can now start handling these post requests. So our loader actually handles all the get requests, and then our action handles everything else. And so in particular, it handles these post requests. So forms can only be set to get or post as far as the browser is concerned. In remakes, you can actually set the method to all of the different HTTP methods. But I don't recommend doing this because the browser is only capable of supporting post and

**译文**

既然我们的表单已经设置完毕，现在就可以开始处理这些 POST 请求了。实际上，我们的加载器处理所有的 GET 请求，而我们的动作处理其余的一切。具体来说，它处理的就是这些 POST 请求。就浏览器而言，表单只能设置为 GET 或 POST 方法。在 Remix 中，你实际上可以将方法设置为各种不同的 HTTP 方法。但我并不推荐这样做，因为浏览器只支持 POST 和

## 34. 34. Handling Form Submissions and Mutations

**原文**

All right, so let's add our action. It's going to be very similar to our loader. It runs on the server. It accepts the params or these data function args. One of those args is the request, and then we can get the request data from the form data. So let's export a function called action. This will take our request, and that's our data function args, and then we can get our form data from request or await request.formdata. This is all regular HTTP

**译文**

好的，那我们来添加我们的 action。它和我们的 loader 非常相似，都是在服务器上运行。它会接受 params 或这些 data 函数的参数。其中一个参数是 request，然后我们可以从表单数据中获取请求数据。那我们来导出一个名为 action 的函数。它将接收我们的 request，也就是 data 函数的参数，然后我们可以通过 request 或 await request.formdata 来获取表单数据。这些都是标准的 HTTP 操作。

## 35. 35. Handling Form Errors and User Mistakes

**原文**

So we've got this TS expect error here and that's because the title and content could be something that we don't want them to be it is very possible that a user could change the DOM and then submit a file instead or they could hit this API directly without using the form at all so we can't really rely on the fact that our form is being submit properly and For those types of scenarios I actually don't care too much about their experience if they're using things wrong

**译文**

所以我们这里遇到了一个 TypeScript 的期望错误，这是因为标题和内容可能包含我们不希望它们出现的内容。用户完全有可能修改 DOM 后再提交文件，或者完全不使用表单而直接调用这个 API。因此，我们其实无法依赖表单能够被正确提交这一事实。对于这类情况，如果用户的使用方式有误，我其实不太关心他们的体验。

## 36. 36. Form Data Types and Validation

**原文**

To start, let's get rid of this comment right here. We're basically saying TypeScript, I know you're trying to let me know how terrible my life is, but I'm going to shut you up. No, we don't want to do that. TypeScript is only there to be helpful. So what it's saying is this update accepts data for the title and content. The title and content could be a couple of different values that are not allowed for what we've configured our database to be. So it's saying the type that we're passing is a form, data, entry value, or null.

**译文**

首先，我们先删掉这里的这条注释。我们基本上是在说：TypeScript，我知道你想让我知道自己的人生有多糟糕，但我要让你闭嘴。不，我们不想这么做。TypeScript 只是为了提供帮助而已。所以它的意思是，这个更新接受标题和内容的数据。而标题和内容可能是一些我们数据库配置所不允许的值。因此，它指出我们传入的类型是表单、数据、条目值，或者 null。

## 37. 37. Button Forms Data

**原文**

Now we've got a button that says delete and when you click on it nothing happens. That's because this button is yeah, nothing special. The capital button here, this component is really just something to make it look styled with this destructive variant that we have. But we need like some sort of on click or something to handle this. Now we're not going to use an on click because that does not progressively enhance. And what we're really trying to do is do a network request to actually

**译文**

现在我们有了一个写着“delete”的按钮，但当你点击它时，没有任何事情发生。这是因为这个按钮——是的，它本身并没有什么特别之处。这里的这个组件，其实只是为了通过我们现有的这种“破坏性”变体（destructive variant）来让它看起来有样式而已。但我们需要某种点击事件处理程序来处理这件事。现在我们不会使用 `onClick`，因为它无法实现渐进式增强（progressively enhance）。而我们真正想要做的是发起一个网络请求来实际……

## 38. 38. Form Submissions and Mutations

**原文**

There are a lot of cases to consider if we were to just add an on click and do a fetch request or whatever, you know, you know the drill. They're just an outrageous number of cases. Like what if the user is quick happy and then quick hit a bunch of times or what if that's actually useful, but then you have race conditions and coming back and like what if, what if, what if, how do you handle errors? All the so many, so many things that you have to consider. And on top of that, this, if you add an on click, this button won't work at all.

**译文**

如果我们只是简单地添加一个 `onClick` 并执行一个 `fetch` 请求之类的操作，需要考虑的情况有很多，你懂的，就是那一套。这些情况多到离谱。比如，如果用户操作很快，然后连续点击了很多次，该怎么办？或者如果这种连续点击实际上是有用的，但又会引发竞态条件，那又该怎么办？还有“如果……怎么办”、“如果……怎么办”、“如果……怎么办”——你该如何处理错误？有太多太多事情需要考虑了。更糟糕的是，如果你添加了 `onClick`，这个按钮就完全无法正常工作了。

## 39. 39. Handling Multiple Actions in a Single Action Function

**原文**

So right now our action is just doing one thing, it's just deleting, but it could be that we'll add another button in the future to favorite a note, for example. Or there are all sorts of things that we could add to this page that says, I want some more mutations that can be performed. Now there are a couple of ways to do this. There's something that I call full stack components that you can read about elsewhere. But most of the time that's not entirely necessary and we can just handle multiple actions inside of

**译文**

目前，我们的动作只做一件事，那就是删除。不过，我们将来可能会添加另一个按钮来收藏笔记，例如。或者，我们还可以在这个页面上添加各种功能，表示我希望增加更多可以执行的变更操作。现在有几种方法可以实现这一点。其中一种是我所说的“全栈组件”（full stack components），你可以在其他地方读到相关内容。但大多数情况下，这并非完全必要，我们只需在……内部处理多个动作即可。

## 40. 40. Leveraging Name and Value in Buttons for Multiple Form Submissions

**原文**

So the first thing that we're going to do is something that not a lot of people really know about, but that is that you can specify a name and a value on a button. And that will be serialized as if it were an input. And what's really interesting about this is if we had multiple buttons, you can have a different name and intent. And you can say favorite. And here, let's just do no variant there. Boom, favorite. So now we have a favorite button. And based on the name and

**译文**

首先，我们要做的这件事并不是很多人所了解的，那就是你可以在按钮上指定一个名称和一个值。它会像输入框一样被序列化了。这件事真正有趣的是，如果我们使用多个按钮，每个按钮都可以有不同的名称和用途。比如我们可以设置一个“favorite”（收藏）。这里我们暂时不设置变体。搞定，就是“favorite”。现在我们就有了一个收藏按钮。而根据这个名称和

## 41. 41. Dad Joke Break Mutations

**原文**

I got a new suit recently made entirely of living plants. I wasn't sure at first, but it's grown on me. Taking breaks is an important part of your learning. You need to get your body moving, so get up, take a break, and then come back and let's get to the next one.

**译文**

我最近得到了一套全新的西装，它完全由活体植物制成。起初我还有些不确定，但现在我已经越来越喜欢它了。休息是你学习过程中非常重要的一环。你需要让身体活动起来，所以快站起来休息一下，然后再回来，我们继续下一个吧。

## 42. 42. Intro to Scripting

**原文**

So far, everything that we've done in this workshop can be done without any client-side JavaScript whatsoever. Because Remix is focused on progressive enhancement, that means that a regular link click is going to do a full-page refresh, and it's going to do a server render of the next page. That works just fine. A submission of a form that also is going to do a full-page refresh, but Remix is able to convert that post request to a regular request that we don't have to work with.

**译文**

到目前为止，我们在本工作坊中所做的所有事情，都完全不需要任何客户端 JavaScript。由于 Remix 注重渐进式增强，这意味着普通的链接点击会触发整个页面的刷新，并由服务器渲染下一个页面。这种方式运行得非常好。表单提交同样会触发整个页面的刷新，但 Remix 能够将这种 POST 请求转换为一个我们无需额外处理的普通请求。

## 43. 43. JavaScript in Remix- From Optional to Essential

**原文**

You know what's interesting is because remix implements everything through a progressive enhancement means that means that we actually don't need JavaScript on the page. And so Kelly, the coworker actually removed all JavaScript from our page. So just took all the scripts and said, Nope, we don't need them. So if I refresh the page, we can see we have our document request, we can see our fonts, CSS file and our tail and CSS file, then the font files that the browser is going to use, and then our favicon. And that's it.

**译文**

你知道有趣的地方是什么吗？因为 Remix 通过渐进式增强的方式实现了所有内容，这意味着我们实际上并不需要页面中包含 JavaScript。所以，我的同事 Kelly 真的从我们的页面中移除了所有的 JavaScript。她直接删掉了所有的脚本，说：“不，我们不需要它们。”因此，如果我刷新页面，我们可以看到文档请求、字体、CSS 文件、我们的 Tailwind CSS 文件、浏览器将要使用的字体文件，以及我们的 favicon。就这样，没了。

## 44. 44. Improving User Experience with Client-Side JavaScript

**原文**

So we got full page refreshes and that's not like super terrible. Everything is working just fine. But there are some things that we can do with client side JavaScript that we can't do without preventing these full page refreshes and doing client side routing. So we got to add JavaScript to the page. Now we're responsible for everything that appears between the open HTML and the closing HTML tag. So that is to say everything on the page is our responsibility, which is really nice because it means that we can conditionally decide whether we want to include JavaScript on the page or not.

**译文**

所以我们得到了完整的页面刷新，这倒也不算太糟糕。一切运行都挺正常的。但有些功能，只有通过客户端 JavaScript 才能实现，而这需要防止完整的页面刷新并进行客户端路由。因此，我们需要向页面中添加 JavaScript。现在，HTML 开始标签和结束标签之间的所有内容都由我们负责。也就是说，页面上的所有内容都是我们的责任，这其实很好，因为这意味着我们可以根据条件决定是否在页面中包含 JavaScript。

## 45. 45. Page Navigation with Scroll Behavior

**原文**

Now that we have JavaScript on the page, there are a number of things that the browser was doing for us before that it's not doing for us anymore. And one of those is when you navigate and click on different links, the browser is going to do a full page refresh and it's going to stick you at the top of the page. And that is no longer the case because we're updating the URL. And so the browser doesn't know when to scroll you to the top of the page. So you'll notice when I navigate between these, then we're actually not scrolling up to the top of the page. That's actually desired behavior. I think that kind of makes sense for the way that this UI is

**译文**

既然页面上现在有了 JavaScript，浏览器之前为我们做的一些事情，现在就不再做了。其中之一就是：当你导航并点击不同链接时，浏览器会执行完整的页面刷新，并将你带到页面顶部。而现在情况不同了，因为我们正在更新 URL，所以浏览器不知道该何时将你滚动到页面顶部。因此你会发现，当我在这些页面之间切换时，我们实际上并没有滚动到页面顶部。这正是我们想要的行为。我认为对于这种 UI 来说，这样的设计是合理的。

## 46. 46. Enhancing Scroll Restoration

**原文**

So we need scroll restoration to happen automatically for us and we're going to use the scroll restoration component from remix run react. So bring in scroll restoration and this is going to control and keep track of our scroll position as we're navigating around. So once we navigate to another place, then the scroll restoration component will just keep track of where we were scrolled at that location. So if we go back or when we go forward, we can always make sure that we're

**译文**

所以我们需要让滚动恢复自动为我们生效，我们将使用来自 `remix run react` 的滚动恢复组件。引入 `scroll restoration` 后，它将在我们导航时控制并跟踪我们的滚动位置。一旦我们导航到另一个位置，滚动恢复组件就会跟踪我们在该位置时的滚动状态。这样，当我们返回或前进时，就能始终确保我们回到正确的滚动位置。

## 47. 47. Environment Variables for Client-Side and Server-Side

**原文**

For this exercise, there are a couple of things that I need to give you some background on for you to be successful. First of all, I'll say that the primary learning outcome of this exercise is pretty simple. You're simply going to add a script tag and properly set the inner HTML for that so you can have some dynamic script running in here. But there are a couple of things that for the particular use case, we're going to use that for where you need to understand a few things. So first of all, Remix has actually two builds. And in fact, we actually

**译文**

在本次练习中，我需要先为你提供一些背景信息，以便你能够顺利完成。首先，本次练习的主要学习目标其实很简单：你只需要添加一个 `<script>` 标签，并正确设置其 `innerHTML`，从而让一些动态脚本在这里运行起来。不过，针对我们即将使用的具体用例，你还需要了解一些其他内容。首先，Remix 实际上有两个构建版本。事实上，我们确实……

## 48. 48. Exposing Environment Variables in a Web Application

**原文**

Let's go to our root.tsx and here we're going to have to in our loader access all of the environment variables. So actually what I'm going to do is add a console.log. We need an L right there. Env. Save that. And I'm going to pull up our output from the playground here. So I refresh and we get our mode development. So that's the terminal output from the workshop.

**译文**

让我们转到 root.tsx，在 loader 中我们需要访问所有的环境变量。所以我实际要做的是添加一个 console.log。我们需要在那里加一个 L。Env。保存。然后我将调出 playground 的输出。刷新后，我们得到 mode development。这就是 workshop 的终端输出。

## 49. 49. Optimizing Resource Loading with JavaScript Prefetching

**原文**

One of the cool things that we can do now that we have JavaScript on the page that we could do before is we can kind of anticipate what the user is going to do and let the browser know of certain resources that we need to load ahead of time. So if I come down here and I click on notes, by this point, I think like we can pretty much assume that they're going to go to the notes page. But when we click on notes, that's going to load a couple of JavaScript files and some data. It could potentially load some CSC.

**译文**

现在，既然页面上有了 JavaScript，我们可以做一件很酷的事情——这是以前做不到的。我们可以大致预测用户接下来要做什么，并提前告诉浏览器我们需要加载某些资源。比如，如果我往下滚动然后点击“notes”，那么到这一步时，我们基本可以假设用户会跳转到 notes 页面。但当我们点击“notes”时，页面会加载几个 JavaScript 文件和一些数据，甚至可能还会加载一些 CSC。

## 50. 50. Enhancing User Experience with Prefetching

**原文**

All right, let's get this going. So I'm going to hard reload. We're going to clear this out and I'm going to go to our username route. And in here, that's this link right here, we want to prefetch when the user intends on clicking on it. So I'll say prefetch intent. And with that, now when the user hovers over it or they mouse down on it or whatever, they give us some sort of intent that they want to click on it, then we should get the

**译文**

好的，我们开始吧。我将执行硬刷新。我们先清空这里，然后进入我们的用户名路由。在这里，就是这个链接，我们希望在用户打算点击它时进行预取。所以我会写上 prefetch intent。这样一来，当用户悬停在上面、按下鼠标或者有任何表示他们想要点击的意图时，我们就应该获取到

## 51. 51. Improve the UX with Pending UI

**原文**

Remember how I talked about the fact that once you bring JavaScript in, it kind of makes some things good and other things worse and that pending UI is the thing that it makes worse? Yeah, that's definitely a problem. So here I can make this change and I can submit and it's super fast and it's awesome. But I don't always have an awesome network connection. So if we kind of simulate a bad network connection through this slow 3g preset, now like users don't typically have slow 3g, but they often have bad network connection. So we're going to simulate that with this. So if I remove those,

**译文**

还记得我之前提到的吗？一旦引入 JavaScript，它会让某些事情变得更好，也会让另一些事情变得更糟，而 pending UI 就是它变得更糟的那部分。没错，这确实是个问题。所以在这里，我可以做出这个更改并提交，速度非常快，效果也很棒。但我并不总能拥有出色的网络连接。因此，如果我们通过这个“慢速 3G”预设来模拟较差的网络连接——虽然用户通常不会使用慢速 3G，但他们经常会遇到糟糕的网络连接——我们就会用它来进行模拟。所以，如果我移除这些……

## 52. 52. Adding Pending State to Form Submissions with Remix

**原文**

When the user submits a form, they're actually performing a navigation, just like if they were clicking on these different links, submitting a form like clicking the Delete button takes them from one place to another. Now, that's not always the case. Sometimes you're going to like, favorite a post or something like that, and that's not going to result in navigating from one page to another. But in the context of what we're doing right now, we are navigating. There's only one navigation possible at a time. So I can navigate to this page and I can click on Edit. I can

**译文**

当用户提交表单时，他们实际上是在执行一次导航，就像点击这些不同的链接一样。例如，提交表单或点击“删除”按钮，都会将他们从一个位置带到另一个位置。当然，这并非总是如此。有时你只是想收藏一篇帖子之类的操作，这并不会导致页面跳转。但就我们当前的操作而言，确实是在进行导航。而同一时间只能进行一次导航。因此，我可以导航到这个页面，然后点击“编辑”。我可以

## 53. 53. Dad Joke Break Scripting

**原文**

All right, I got a good one for you here. What was the most important invention than the first telephone? The second one. Okay, now it's time to take a break. So let's get up, walk around, get a drink, go to the bathroom, whatever you need to do, and then come back and let's get back to it. But you do need to take a break. I'd require it. It's an important aspect of what you're doing is taking care of that brain of yours. So take care of the brain, then come back and let's get on to the next one.

**译文**

好的，我给你准备了一个好问题。比第一部电话更重要的发明是什么？是第二部电话。好了，现在是时候休息一下了。所以，请站起来，走动一下，喝点水，去趟洗手间，做你需要做的任何事情，然后回来，我们继续。但你确实需要休息一下。我要求你这样做。你所做的事情中，一个重要的方面就是照顾好你的大脑。所以，请照顾好你的大脑，然后回来，我们继续下一个。

## 54. 54. Intro to Search Engine Optimization (SEO)

**原文**

I know that some of you are seeing this and you're thinking, my app doesn't need SEO because I have some, you know, it's an internal app or something, but no, you definitely don't skip this exercise. This is important for you as well. It's not just about SEO. It's also about when you share things on like within your corporate network or if you like when the user is looking at your page, you're going to have some important metadata that you need to configure your application with.

**译文**

我知道你们当中有些人看到这段话时可能会想：我的应用不需要 SEO，因为它是内部应用之类的。但事实并非如此，你绝对不能跳过这个步骤。这对你来说同样重要。这不仅仅是为了 SEO，还涉及到当你通过公司内部网络分享应用内容时，或者当用户查看你的页面时，你需要为应用配置一些重要的元数据。

## 55. 55. Configuring Meta Tags

**原文**

You may have noticed by now that our title is pretty awful and there are a number of other things that we need to configure about our web page so that things, the browser behaves properly as we need for our application. So for this first step of this exercise, I want you to add some meta tags to the head so that we can configure our website to look nice, especially the title. What a garbage thing there. No, you don't want that.

**译文**

你可能已经注意到，我们的标题相当糟糕，而且我们还需要对网页进行一些其他配置，以便浏览器能按照我们应用程序的需求正常运行。因此，在本练习的第一步中，我希望你为 `<head>` 部分添加一些元标签，以便我们能够配置网站的外观，尤其是标题。那标题简直是一团糟。不，你肯定不想那样。

## 56. 56. Meta Tags for Better SEO and UX

**原文**

Everything between the opening HTML tag and the closing HTML tag is our responsibility. So if it's not showing up, that's our, our role. That's what we're supposed to do. And we do that in the root. So if we want something in the head, we're going to do that in our root route. So we just are going to put a couple of meta tags in here. We're going to have a title. This can be epic notes. We'll have a meta tag for the description. Um, and yeah, a note taking up, we do whatever makes sense.

**译文**

从 opening HTML 标签到 closing HTML 标签之间的所有内容都是我们的责任。所以如果它没有显示出来，那就是我们的、我们的职责所在。这正是我们应该做的事情。而我们在 root 中完成这项工作。因此，如果我们想在 head 中添加内容，就会在我们的 root route 中完成。所以我们只需在这里添加几个 meta 标签。我们会设置一个标题，可以是 epic notes。我们还会添加一个用于描述的 meta 标签。嗯，是的，在笔记中，我们做一切合理的事情。

## 57. 57. Dynamic Metadata for Different Routes

**原文**

It's pretty common that you want to have different metadata on different routes. And so here is the solution for this exercise where we show the profile and then the bar. That's, that's fairly common. And then Epic Notes. And then we have our description, check out this profile on Epic Notes. And then if I go to the homepage, those get automatically updated to be relevant for the homepage. So we have like kind of this default that will be applied to all the pages, but then we can opt in to changing it on specific pages. So that is your task today.

**译文**

在不同路由上拥有不同的元数据是很常见的需求。因此，这里给出了本练习的解决方案：我们先展示个人资料，然后展示信息栏。这种情况相当常见。接下来是 Epic Notes。然后是我们的描述，快来 Epic Notes 上查看这个个人资料吧。如果我返回首页，这些内容就会自动更新为与首页相关的信息。也就是说，我们有一个默认设置会应用于所有页面，但也可以在特定页面上选择覆盖它。这就是你今天的任务。

## 58. 58. Managing Meta Tags and Descriptions in RemixRunReact

**原文**

So to update our title and our description for this route, we need to go to that route. That's the username route. And we'll add a meta export. This is actually pretty similar to the links export, but there are a couple of important differences that we'll talk about. So we're going to export const meta, and this is a meta function, which we'll bring in from remix run react. And then we are going to return an array. So again, pretty similar to the way that links work. And each one of these will be a

**译文**

因此，要更新此路由的标题和描述，我们需要进入该路由，也就是用户名为 `username` 的路由。然后，我们将添加一个 `meta` 导出。这实际上与 `links` 导出非常相似，但有几个重要的区别，我们稍后会讨论。因此，我们将导出一个常量 `meta`，它是一个 `meta` 函数，需要从 `remix run react` 中引入。然后，我们将返回一个数组。所以，这与 `links` 的工作方式非常相似。而这里的每一个元素都将是一个

## 59. 59. Customizing Meta Tags with Dynamic Data

**原文**

It's very common to want to use some dynamic data in your meta export. So here's what we have so far. We just say profile. This is just hard coded for this route. But in the solution, we have the user's name. And if you take a look at the head for the solution, we have Cody and then the vertical bar, Epic Notes. And then the description will say profile of Cody on Epic Notes. So we want to be able to customize this based on the data for the page. And we can use this later on if you want to go further beyond this exercise.

**译文**

在元数据导出中使用一些动态数据是非常常见的需求。目前我们得到的结果如下：我们只是简单地写上了“profile”。对于这条路由来说，这只是硬编码的值。但在解决方案中，我们包含了用户的姓名。如果你查看解决方案中的 head 部分，会发现内容是“Cody | Epic Notes”。而描述则会显示为“Cody 在 Epic Notes 上的个人资料”。因此，我们希望可以根据页面数据来定制这些信息。如果你希望在本练习的基础上进一步深入，稍后也可以用到这些内容。

## 60. 60. Handling Dynamic Data with Remix's Meta Function

**原文**

So again, we're going to be in the username route, and we're going to enhance this a little bit so that we can get the user's information. So the meta function accepts a argument that is an object and has a couple of pieces of information that you might find very useful. And one of those is the data. And the issue with this, though, is that the data is typed as any because we actually don't have that type script isn't aware of the connection between this meta function

**译文**

因此，我们再次进入用户名路由，并对它进行一些增强，以便能够获取用户信息。`meta` 函数接受一个对象作为参数，其中包含一些你可能觉得非常有用的信息。其中之一就是 `data`。不过，这里的问题在于 `data` 的类型被定义为 `any`，因为我们实际上并没有这个类型，TypeScript 也无法识别这个 `meta` 函数之间的关联。

## 61. 61. Optimizing Metadata for User Info

**原文**

All right, so Kelly, the coworker did a little bit of nice work for us. And that is she added a little bit of metadata to our notes index page as well as our notes specific note ID page. On the notes index page, the best that she could do was add the username from the params because that note index page doesn't even have a loader. So there's no way to get that data to know which user it is. We have to create a loader for that, which seems kind of wasteful,

**译文**

好的，那么 Kelly 这位同事为我们做了一些不错的工作。她为我们的笔记索引页面以及特定笔记 ID 页面添加了一些元数据。在笔记索引页面上，她能做的最好的事情就是从参数中获取用户名，因为该索引页面甚至没有加载器。因此，没有办法获取数据来识别当前用户是谁。我们必须为此创建一个加载器，但这似乎有些浪费。

## 62. 62. Implementing Dynamic Meta Data for Routes in a TypeScript Application

**原文**

Let's start with the note ID route. So note ID. And we'll come down here and we've got a meta function that Kelly, our coworker built for us. And we also are using this matches thing. So let's go ahead and console log matches and see what that thing is at all. So look at our console here, we have that log. And there are three parts of this matches array. So there are three routes that are currently matching on the page. We have the route that's the root route.

**译文**

我们先从笔记 ID 路由开始。也就是笔记 ID。然后我们往下走，这里有一个元函数，是我们的同事 Kelly 为我们构建的。我们还用到了这个 matches 东西。那我们先来控制台输出一下 matches，看看它到底是什么。看我们的控制台，这里有对应的日志。这个 matches 数组有三个部分。也就是说，当前页面上有三个匹配的路由。其中一个就是根路由。

## 63. 63. Dad Joke Break - SEO

**原文**

I was shocked when I was diagnosed as colorblind. It came out of the purple. Get it? Blue came out of the purple. Okay. Anyway, hopefully that was a fun time for you and now it's time to take a break. So get up, walk around, get some exercise, take care of that brain of yours and then come back. You maybe grab something to eat, something healthy that your brain can munch on while you're doing all this learning. Once you got that, then come on back and let's do some more of these exercises. Have fun.

**译文**

当我被诊断出色盲时，我震惊了。这完全是出乎意料的。你明白吗？蓝色是从紫色里冒出来的。好吧。总之，希望刚才那段时光对你来说很有趣，现在是时候休息一下了。所以，站起来，走动一下，做点运动，照顾好你的大脑，然后再回来。你或许可以拿点东西吃，吃点健康的食物，让你的大脑在学习的同时也能“咀嚼”一下。准备好了之后，就再回来，我们一起多做些这样的练习吧。玩得开心。

## 64. 64. Intro to Error Handling

**原文**

Sometimes things happen that you don't really want to have happen. So sometimes we have errors and it's not always our fault, but sometimes it is. Sometimes the user submitted some bad data or the form was configured incorrectly or the service that we're depending on is down and it happens. And there are various status codes to communicate the status of an HTTP request as part of the response. And so there are

**译文**

有时会发生一些你并不希望发生的事情。因此，我们有时会遇到错误，这并不总是我们的错，但有时也确实是我们造成的。比如，用户提交了错误的数据，或者表单配置不正确，又或者我们依赖的服务宕机了，这些都可能引发问题。在 HTTP 响应中，有多种状态码用于传达请求的状态。因此，存在

## 65. 65. Improving Error Handling and UI on User Profile Page

**原文**

We've got a pretty ugly looking error on the user profile page. Let's go to username and Cody added a couple of error logs that we could add. So let's uncomment that and boom, we've got this loader error. This is an ugly error page. Do not like at all. So that's our loader and then our component same sort of business looks awful. No fun at all. So what your job is is to use some of the utilities available from remix to

**译文**

我们在用户个人资料页面上遇到了一个相当难看的错误。让我们转到用户名页面，Cody 添加了一些我们可以使用的错误日志。那我们就取消注释这些日志，然后“砰”的一声，我们就遇到了这个加载器错误。这是一个很难看的错误页面，完全不喜欢。所以这就是我们的加载器，然后是我们的组件，同样的问题，看起来也很糟糕。一点也不好玩。因此，你的任务是使用 Remix 提供的一些实用工具来

## 66. 66. Error Handling and Error Boundaries

**原文**

to handle errors in the username route, we're going to go to the username route. And let's add this right here. What a terrible, ugly looking error. So let's make it look nicer. We're going to export a function called error boundary. And here we're going to get the error from use route error. And that's going to come from remix run react right here. And then we can console error that error, because this can be literally anything, anything could throw this error

**译文**

要处理用户名路由中的错误，我们需要进入用户名路由。然后在这里添加这段代码。这错误看起来真糟糕、真难看。所以我们让它看起来更友好一些。我们将导出一个名为 error boundary 的函数。在这里，我们将从 use route error 中获取错误信息。它会来自 remix run react 的这里。然后我们可以用 console.error 输出该错误，因为这可能真的是任何东西，任何内容都可能抛出这个错误。

## 67. 67. Handling Expected Errors with Error Boundaries

**原文**

So we've got our error boundary set up. And one thing that we didn't mention was we have in our username right here, we've got this invariant response. Remember, we put that there. And what this invariant response does is throw a response object. Throne response objects will also get passed to our error boundary. So here we're saying, if there's a user, then things are good. If there's not, then send a user not found body in a response with the status of 404. So if I say,

**译文**

那么，我们已经设置好了错误边界。还有一点我们之前没有提到的是，在我们这里的用户名部分，有一个不变响应（invariant response）。还记得我们把它放在那里了吗？这个不变响应（invariant response）的作用是抛出一个响应对象（response object）。而所有被抛出的响应对象（response objects）也都会传递给我们的错误边界。所以这里我们这样写：如果存在用户，那么一切正常；如果用户不存在，就返回一个“用户未找到”（user not found）的响应体，状态码为 404。所以如果我说，

## 68. 68. Improving Error Messages for User

**原文**

Let's give users a much better error message here. So let's go to our username. We've got our invariant response that's throwing the error that's causing this. So we can come down here and I want to show them a message that says, hey, you went to this username that doesn't exist. So let's have a default right here. So this is our fallback if this was some other error. So I'm going to extract this to our error message. And we'll assign that to let because if

**译文**

让我们在这里给用户一个更好的错误信息。那我们来到用户名这里。我们有那个引发错误的不变量响应，正是它导致了这个问题。所以我们可以在这里往下走，我想向他们显示一条消息，内容是：嘿，你访问的这个用户名不存在。那我们在这里设置一个默认情况。这是我们在遇到其他错误时的备用方案。所以我要把这个提取为我们的错误信息，并将其赋值给 let，因为如果

## 69. 69. Streamlining Error Handling in Routes with a General Error Boundary

**原文**

Kelly the co-worker has come in clutch and made us a really nice abstraction for our error boundaries. So now we have this general error boundary that we can use to render errors all over the place in all of our routes because this is a pretty common thing that you're going to want in your routes. And we want it to be consistent. We want it to be easy to do. So you have this status handlers prop that will take a status code and then you provide a function that will be called to get what the error

**译文**

同事 Kelly 在关键时刻挺身而出，为我们构建了一个非常棒的错误边界抽象。现在，我们有了一个通用的错误边界，可以在所有路由中随时渲染错误信息，因为这是路由中一个非常常见的需求。我们希望它保持一致性，并希望实现起来简单便捷。你可以通过 `statusHandlers` 属性传入一个状态码，然后提供一个函数，该函数将在需要获取错误信息时被调用。

## 70. 70. Error Boundaries and Handling in Nested Routes

**原文**

All right, let's go to our username and we're going to swap this with the generic general error boundary. So like pretty much all this stuff can be removed in favor of the general error boundary. But you know what, I kind of removed that prematurely. Let's back it up a little bit because I want to get this right there. So let's put it all back. And then we'll say status handlers and for 404. Yep, that's kind of the idea. But we need to get the params right there.

**译文**

好的，我们转到用户名部分，然后把它替换为通用的错误边界。基本上，所有这些内容都可以被通用的错误边界所取代。不过，你知道的，我有点过早地把它删掉了。我们稍微回退一下，因为我想确保把它放对位置。所以，我们把所有内容都恢复回来。然后我们会说状态处理程序，用于 404。是的，差不多就是这个意思。但我们需要把参数放在正确的位置。

## 71. 71. Improving Error Handling with a Document Component

**原文**

We've got ourselves an error boundary on the root. Seems like a pretty good idea. You want to have that on that route for sure. But we've got a bit of a problem. So if I comment this out, we've got an error on the root loader and this looks really awful. Definitely not what I wanted. If we look at the elements tab, we'll see we have our div with the container and it's all styled and everything, but our head is completely empty. What is that? Let's look at the view source on this. What?

**译文**

我们在根组件上设置了一个错误边界。这看起来是个不错的主意。你肯定希望在那个路由上也加上它。但我们遇到了一个小问题。所以，如果我注释掉这段代码，根加载器就会出现一个错误，而且看起来非常糟糕。这绝对不是我希望看到的结果。如果我们查看“元素”选项卡，会看到我们的 `div` 带有容器样式，所有样式都应用好了，但我们的 `<head>` 完全是空的。这是怎么回事呢？我们来看看页面的源代码。什么？

## 72. 72. Refactoring App Components for Better Error Handling

**原文**

So instead of trying to move stuff out, this will actually be easier if we just call this document. And then we can have a new thing, export function app. And this is our new app component. And then we just move stuff into the app component that can't be in the document. For example, you cannot use use loader data inside of an error boundary because the loader might have failed to run. And so we're going to move this stuff up into our app component. And then yeah, this we want to keep there all that we want to keep there.

**译文**

所以，我们不需要尝试把东西移出去，直接调用这个文档反而会更简单。然后我们可以创建一个新的东西：export function app。这就是我们的新 app 组件。接着，我们把那些不能放在文档里的内容移到 app 组件中。例如，你不能在 error boundary 内部使用 use loader data，因为 loader 可能未能成功运行。因此，我们将这部分内容移到我们的 app 组件中。然后，是的，我们希望把这些内容都保留在那里。

## 73. 73. Handling 404 Errors in React Router with Splat Routes

**原文**

We are almost done handling a bunch of errors in our app. There's one more error that is a little different than the others. If I go to some route that doesn't exist, we don't even have a dynamic route that matches this URL. So we're going to get this 404 error, no route matches URL, yada, yada, yada. But the thing is that this is bubbling up to our root error boundary, and so that's fine. But we could do better, right? Because we can still render the header and the footer. Everything else still works. If the user is logged in,

**译文**

我们差不多已经处理完应用中的一堆错误了。还有一个错误和其他的有点不一样。如果我访问一个不存在的路线，我们甚至没有一个动态路由能匹配这个 URL。所以我们就会得到这个 404 错误，没有路由匹配 URL，云云。但问题是，这个错误会冒泡到我们的根错误边界，这倒也没问题。不过我们可以做得更好，对吧？因为我们仍然可以渲染页眉和页脚。其他一切都还能正常工作。如果用户已登录，

## 74. 74. Handling 404 Errors with Splat Routes in Remix

**原文**

All right, step one, we got to create that splat route. And with the remix flat routes convention, the way that we are going to do that is in the routes directory, we'll add a dollar dot TSX. So this is going to match all routes that don't match anything else. And with this, we can export a function called loader. And we're just going to return or we could throw either one will work, but we can return a new response that can be not found, and then status for

**译文**

好的，第一步，我们必须创建那个 splat 路由。按照 Remix 的 flat 路由规范，我们要在 routes 目录下添加一个 dollar.tsx 文件。这将匹配所有其他路由都无法匹配的路径。然后，我们可以导出一个名为 loader 的函数。我们直接返回一个响应即可——也可以抛出错误，两种方式都行——但这里我们返回一个新的“未找到”响应，状态码设为 404。

## 75. 75. Dad Joke Break_3

**原文**

I know this is our last exercise so you don't have another one to go to until the next workshop, but we're gonna give you a dad joke just as a good send-off. Don't tell secrets in cornfields too many years around. Get it? Here's a corn? Hopefully that's a good little bit of levity to leave you off with and that you enjoy this. So yeah, definitely get up and do a little bit of actual physical exercise or movement because that is important for

**译文**

我知道这是我们的最后一次练习，所以在下一次工作坊之前，你不用再参加其他练习了。不过，我们还是想用一个冷笑话作为美好的告别。不要在玉米地里说秘密——“too many years around”（谐音“too many ears around”，即“周围太多玉米棒子”）。你懂吗？这就是一个关于玉米的笑话。希望这个小笑话能为你带来一些轻松愉快的心情，也希望你喜欢。所以，一定要起身做一些实际的体育锻炼或活动，因为这非常重要。

## 76. 76. Outro to Full Stack Foundations Workshop

**原文**

Awesome job. You should feel so proud of yourself for finishing this first workshop of Epic Web Dev. There's a lot of stuff we did in here and I think that you have every right to feel like you've really accomplished something here. I hope that you take the things that you learned in this workshop today and apply it to what you're doing in whatever work that you're doing, whether it's side projects or projects at work. The things that we learned today are certainly tied to remix in many ways and tailwind and

**译文**

干得漂亮。完成 Epic Web Dev 的第一次工作坊，你应该为自己感到非常自豪。我们在其中做了很多内容，我认为你完全有理由觉得自己真正有所成就。我希望你能将今天在这次工作坊中学到的知识应用到你所从事的任何工作中，无论是个人项目还是工作中的项目。我们今天所学到的内容在许多方面都与 remix 和 tailwind 密切相关。

## 77. 01. Intro to Professional Web Forms Workshop

**原文**

Welcome to the Professional Web Forms Workshop. Congratulations on making it here. I'm excited for the cool things that we're going to be building together. Let's take a look at a couple of those things. So if we go to users code, and we still have our code route, and we've got all of these notes, but we also have an image upload component. So you can actually upload images and it's going to be awesome. You want to give proper alt text. So like illustration of koalas cuddling. There you go. That's proper alt text.

**译文**

欢迎来到专业网页表单工作坊。恭喜你坚持到了这里。我很期待我们一起构建的那些酷炫功能。让我们先来看几个例子。如果我们进入 users code，仍然可以看到我们的 code 路由，这里有所有这些笔记，但我们还有一个图片上传组件。所以你实际上可以上传图片，效果会非常棒。记得提供合适的替代文本。比如“illustration of koalas cuddling”（考拉拥抱的插图）。就是这样。这就是合适的替代文本。

## 78. 02. Intro to Form Validation

**原文**

Let's validate some stuff. We'll validate these forms. So when we're all done, we will get this nice validation logic when there is no JavaScript or when the JavaScript is slow, and that's like built-in browser behavior. And then when we've got JavaScript, we'll have our own custom job or rendering for error messages and stuff. We got to do this all on the server because we can't really trust the user's client, all of that stuff. And we still want to

**译文**

让我们来验证一些内容。我们将验证这些表单。这样，当我们完成所有工作后，就会拥有这套完善的验证逻辑：在没有 JavaScript 或 JavaScript 运行缓慢时，它会采用浏览器内置的行为；而当有 JavaScript 可用时，我们则能自定义错误消息等的渲染方式。所有这些都必须由服务器完成，因为我们无法真正信任用户的客户端环境。而我们仍然希望……

## 79. 03. Required Field Validation for User Input

**原文**

You know one cool thing about our users? We can trust them. We don't have to do any validation. Just kidding. We totally need to do a validation. And it's not just about not trusting the users to make a mess of our data or whatever, but it's also about helping them not make a mess of their own data. For example, what if the user accidentally deleted all this and submitted that, now their note is empty? Or even worse, what if they delete the title and submit that?

**译文**

你知道我们的用户有一个很酷的特点吗？那就是我们可以信任他们。我们根本不需要做任何验证。开个玩笑啦。我们当然需要做验证。这不仅是为了防止用户把我们的数据搞得一团糟，也是为了避免他们把自己的数据搞乱。比如，如果用户不小心删除了所有内容并提交，那他们的笔记不就空了吗？更糟糕的是，如果他们连标题都删掉再提交，该怎么办？

## 80. 04. Form Validation for Accessibility

**原文**

To validate this form, we're going to go to where that form lives in our edit route. And then we come down here to our form, and we can just provide regular HTML attributes for this. So both the title and the content are required. And the title has a min length or a max length, max length of 100. We don't want like ridiculously long titles. So then required on the content, and then a max length,

**译文**

要验证此表单，我们需要前往编辑路由中该表单所在的位置。然后向下找到表单部分，直接为表单添加常规的 HTML 属性即可。因此，标题和内容都是必填项。标题有最小长度和最大长度限制，最大长度为 100。我们不希望出现过长离谱的标题。内容同样是必填项，并设置了最大长度。

## 81. 05. Server-side Validation and Custom Error Messages

**原文**

Even though the browser supports built-in validation and you can even customize that validation with JavaScript, this is really easy to circumvent. Users can literally just open up the DevTools and go down to here and say, you know what, I think it should have a max length of thousands and then they can circumvent our validation that way. Or they could just hit the endpoint directly, just look at what the network is doing and do that same thing and do whatever they want to with it. So we absolutely always know

**译文**

尽管浏览器支持内置验证，你甚至可以通过 JavaScript 自定义这种验证，但要绕过它其实非常容易。用户完全可以直接打开 DevTools，定位到这里，然后说：“你知道吗？我觉得最大长度应该设为几千。”这样他们就能绕过我们的验证。或者，他们也可以直接调用后端接口——只需观察网络请求，然后如法炮制，对数据做任何他们想做的事情。因此，我们必须始终确保……

## 82. 06. Server-Side Form Validation and Error Handling

**原文**

Let's open up the editor route and our action is where server code runs. So the user cannot circumvent this no matter what they do. This server code is the code that they are calling and so it will run so we can do some validation here. So let's create an errors object and then we can say if the title is equal to an empty string, then we know that they did not submit the title. So we can say errors.title. Now here Copilot is saying hey, why don't you just set errors.title to this string.

**译文**

我们来打开编辑器路由，而我们的“操作”（action）正是服务器代码运行的地方。因此，无论用户做什么，都无法绕过这一步。这段服务器代码正是用户调用的代码，所以它会执行，我们可以在这里进行一些验证。那么，我们先创建一个 errors 对象，然后可以判断：如果 title 等于空字符串，那就说明用户没有提交标题。因此，我们可以写 errors.title。这时 Copilot 提示说，嘿，你为什么不直接把 errors.title 设置为这个字符串呢？

## 83. 07. Dynamic Error Validation with Hooks

**原文**

We've put together this error validation logic, but it actually isn't doing us any good because we have that no validate hook or attribute that we have to apply to our component to prevent the browser from doing its own validation. The problem with that is if the user submits the form before our JavaScript has a chance to load, then they're going to be able to submit something incorrect. And so we don't want to put no validate on our form unless the JavaScript is ready to take over.

**译文**

我们编写了这段错误验证逻辑，但实际上它并没有发挥作用，因为我们必须为组件添加 `novalidate` 钩子或属性，才能阻止浏览器执行自身的验证。问题在于，如果用户在 JavaScript 加载完成之前就提交了表单，那么他们就能提交错误的数据。因此，我们不想在表单上设置 `novalidate`，除非 JavaScript 已经准备好接管验证逻辑。

## 84. 08. Form Validation with Client-Side Hydration

**原文**

Let's open up our edit route and right here we've got a good place to put the use hydrated hook I figure you can probably write this yourself at some point. We're not here to learn react and so that's why I provided that for you and With use hydrated now basically I'll explain how this works. We start with the use state of false and so on the server render Use hydrated will return false the use effect never runs on the server and so when the client

**译文**

让我们打开编辑路由，在这里我们有一个合适的位置来放置 useHydrated 钩子。我想你以后大概可以自己写出这段代码。我们在这里不是为了学习 React，所以我才为你提供了这个。现在有了 useHydrated，我来解释一下它是如何工作的。我们从使用状态 false 开始，因此在服务器渲染时，useHydrated 将返回 false。useEffect 在服务器上永远不会运行，所以当客户端...

## 85. 09. Dad Joke Break From Validation

**原文**

Velcro, what a ripoff! Hopefully you get a little bit of a chuckle out of that. The idea is to give you a very nice stopping point for the work that you're doing because you need to take breaks as you go. So take a break, stand up, walk around, whatever, and then come back and let's keep going.

**译文**

“Velcro”（魔术贴），这玩意儿真坑！希望你听了能会心一笑。这么说的目的，是想让你有一个很好的停顿点来暂停手头的工作，因为你在做事的过程中需要适时休息。所以，去休息一下，站起来走动走动，做点什么都行，然后再回来，咱们继续。

## 86. 10. Intro to Accessibility

**原文**

Accessibility is a very, very big subject and it's very, very important in your applications for various reasons. So for one, the people who are already at a disadvantage don't need you making an inaccessible app to make their lives that much more challenging. So please, just like accessibility is about caring about people, especially those who are already living life in a disadvantage situation. It also makes people better for everybody.

**译文**

无障碍是一个非常非常大的主题，而且出于各种原因，它在你的应用程序中非常重要。首先，那些已经处于不利地位的人，不需要你再开发一个难以使用的应用，让他们的生活变得更加艰难。因此，请记住，正如无障碍关乎关爱他人——尤其是那些本已身处不利境地的人一样，它也能让所有人都受益。

## 87. 11. Fixing Form Reset Button and Accessibility Issues

**原文**

When we first made this form, we had this reset button that worked great, but that reset button not working anymore. So we've got some form association that has been broken there that you need to fix. We also have a bit of an accessibility problem here. If I click on the title or click on the content, those are labels. And when you have a label that's properly associated, then clicking on that label will focus the input that it's associated to. But that's not happening.

**译文**

当我们最初创建这个表单时，我们有一个重置按钮，它运行得很好，但现在这个重置按钮已经不起作用了。因此，表单关联出现了问题，需要您进行修复。此外，这里还有一个小小的无障碍访问问题。如果我点击标题或内容，这些元素本应作为标签使用。当标签被正确关联时，点击该标签应该会将焦点定位到其所关联的输入框上。但目前这种情况并未发生。

## 88. 12. Improving Accessibility and Form Associations

**原文**

So let's open up the editor here and we'll come over to our reset button. Now, I actually already kind of did this for you with the status button. Let's explain why the reset button isn't working. So we should be able to type in there hit reset and it should reset. The problem is with the way that the design is formatted, especially useful for these things that scroll a lot, we have this as a detached section of our scrollable content. So it's outside of the form. You'll see we've got that

**译文**

那么我们在这里打开编辑器，然后转到我们的“重置”按钮。实际上，我之前已经用“状态”按钮为你做过类似的操作了。现在我们来解释一下为什么“重置”按钮不起作用。我们本应该能够在这里输入内容，然后点击“重置”，然后它就会重置。问题在于当前的设计格式，特别是对于这类内容滚动较多的情况，我们将其作为可滚动内容的一个独立部分来处理。因此，它位于表单之外。你会看到我们已经这样做了。

## 89. 13. Error Messages and Accessibility with ARIA Attributes

**原文**

We have some more accessibility things to consider when it comes to our error messages. So once we get that title as required error message, we need to associate that error message with our input field so that screen readers can tell our users that there is an error. So if we take a look at the solution, what we're going to see when we have things properly associated is we'll have, well, let's enter, there we go. We have aria invalid is true and aria described by is the title error. That's going to be the ID of our errors.

**译文**

在考虑错误消息时，我们还需要注意一些无障碍方面的问题。因此，一旦我们获得“标题为必填项”这一错误消息，就需要将该错误消息与输入字段关联起来，以便屏幕阅读器能够告知用户存在错误。如果我们来看看解决方案，当各项内容被正确关联后，我们会看到——嗯，我们来输入一下，好了。此时，aria-invalid 为 true，而 aria-describedby 指向的是标题错误。这将是我们的错误信息的 ID。

## 90. 14. Accessible Forms with ARIA Attributes

**原文**

Let's pull up our editor and come over to our error list. So we're going to need to have an ID on this UL so that we can associate this list of errors with the inputs that it's making an error about or even the form. And so let's take an ID attribute, and that will be an ID of optional type string. And then here we'll say ID is the ID that we've been given. And that takes care of that.

**译文**

让我们打开编辑器，然后转到错误列表。因此，我们需要为这个 UL 设置一个 ID，以便将该错误列表与它报告错误的输入项甚至表单关联起来。那么，我们来添加一个 ID 属性，其类型为可选的字符串。然后在这里，我们说明 ID 就是我们被分配的那个 ID。这样就处理好了。

## 91. 15. Focus Management for Better User Experience

**原文**

So let's say I'm a user that's new to the app and I don't realize that the content needs to have some value into it. And so I go and submit this and we get this error. Now my focus is on the submit button. It was, but the submit button was disabled. But my focus stays down there. So I'm tapping around and now I have to go find, okay, where was the error? People using assistive technologies who cannot see the screen, experience this on the daily and it's awful. So what we really should do is autofocus

**译文**

假设我是一个刚接触这个应用的新用户，没有意识到内容需要包含一些实际值。于是我提交了表单，结果出现了这个错误。此时我的焦点原本在提交按钮上，但该按钮当时是禁用的。然而，焦点仍然停留在下方区域。我只好四处点击，然后还得重新寻找：“嗯，错误提示在哪儿呢？” 无法看到屏幕、使用辅助技术的用户每天都会遇到这种情况，体验非常糟糕。因此，我们真正应该做的是自动聚焦。

## 92. 16. Managing Focus for Form Errors

**原文**

Let's do the easy thing first. So the easy thing is to make it so that we autofocus on the input when we land on this page. So we'll add autofocus right here. That was it. Easy. Nothing going on there. Boom. Autofocus. Awesome. So that's good. So now let's do the little bit harder thing next. And that is we need to add a use effect. I know a use effect, but don't worry. This is actually exactly what use effects are intended for. Side effects on the

**译文**

我们先来做简单的事情。简单的事情就是，当我们进入这个页面时，让输入框自动聚焦。所以我们直接在这里加上 autofocus。就是这样。很简单。没什么复杂的操作。搞定。自动聚焦。太棒了。这样很好。那接下来我们来做稍微难一点的事情。那就是我们需要添加一个 use effect。我知道你可能听说过 use effect，但别担心。这实际上正是 use effect 的用武之地。处理副作用。

## 93. 17. Dad Break Joke Accessibility

**原文**

What do you do when your bunny gets wet? You get your hair dryer. Ha ha ha ha. Yeah, Cody didn't like that one so much. Look at that stoic expression. Yeah, no, just kidding. Actually, Cody's got a smile. You can't really tell, but Cody's always happy with you and your work. You should be happy with you and your work as well. You're doing an awesome job. Keep it up. We're going to take a quick break and then when you come back, you can get right back into it with the next series of exercises.

**译文**

当你的兔子弄湿的时候，你会怎么做？你会拿出吹风机。哈哈哈哈哈。是啊，Cody 不太喜欢那样。看看它那副一本正经的表情。好吧，不开玩笑了。其实，Cody 是在笑。虽然不太看得出来，但 Cody 总是对你和你的工作感到满意。你也应该对自己和你的工作感到满意。你做得非常棒。继续加油。我们稍作休息，等你回来之后，就可以接着进行下一组练习了。

## 94. 18. Intro to Schema Validation

**原文**

Scheme of validation. All right. So I don't know about you, but when I see something like this, I'm like, that would be awful if I had more than just two fields or even more complicated validation logic. And I have been down this road before and I have created utilities like this one. You know what? That's just about as awful. And so I don't really like having to write a bunch of these utilities. It'd be really nice if we had like a generic utility that had some nice

**译文**

验证方案。好的。我不知道你们怎么样，但当我看到类似这样的东西时，我就会想，如果字段不止两个，或者验证逻辑更复杂一些，那可就糟糕了。我以前也走过这条路，还创建过像这样的工具。但说真的，那也差不多糟糕透了。所以我真的不喜欢不得不编写一大堆这样的工具。要是我们能有一个通用的工具，带有一些不错的功能，那就太好了。

## 95. 19. Schema Validation

**原文**

So we've got some good validation going on here. The user experience is just fine, but I want to improve the developer experience a little bit. We're going to switch to schema validation with Zod. This is going to open up a bunch of other really cool things that we can do. So I want you to jump in, delete a bunch of our custom validation logic, switch it to schema validation with Zod. And then when you're finished with that, I'll take you through the way that I did it, and then we can move on and make things really, really cool.

**译文**

现在我们已经有了一套不错的验证机制。用户体验本身没有问题，但我希望稍微提升一下开发者体验。接下来，我们将切换到使用 Zod 进行模式验证。这将为我们带来许多其他非常酷的功能。所以，请你动手删除我们之前自定义的大量验证逻辑，并将其替换为 Zod 的模式验证。完成之后，我会向你展示我是如何实现的，然后我们就可以继续让事情变得更加酷炫。

## 96. 20. Schema Validation with Zod

**原文**

So let's go to the edit route and we'll come to the server side. That's where most of our stuff is going to happen. And we're going to create a new note editor schema. So this is going to come from Zod. And so let's import that from Zod. And then it's going to be an object. So this will have a title. This will be a string. And for this to be required, an empty string, as far as string is concerned, is considered valid. So we need it to be at least one

**译文**

那么我们进入编辑路由，然后转到服务器端。我们大部分逻辑都将在这里实现。接着，我们将创建一个新的笔记编辑器模式。这个模式将来自 Zod。因此，我们从 Zod 中导入它。然后，它将是一个对象。这个对象将包含一个标题，类型为字符串。由于该字段是必填项，而空字符串在字符串类型中仍被视为有效值，因此我们需要确保其长度至少为 1。

## 97. 21. Form Data Parsing with Conform

**原文**

Doing this is not my favorite thing. Turning our form data into an object that we can then pass to the note editor schema and all of that. In this form, that's not a huge deal. And in fact, in simple forms, we can do something like this. Here's my form, yeah, form body, form objects. And you say form or object from entries. And now you've got that object. And so we could do that. And that'll work for simple forms. But I don't really like that.

**译文**

做这件事并不是我最喜欢的。将我们的表单数据转换为一个对象，然后将其传递给笔记编辑器模式等等。在这个表单中，这并不算什么大问题。实际上，对于简单的表单，我们可以这样做。这是我的表单，没错，表单主体、表单对象。然后你可以通过 entries 将表单转换为对象。现在你就得到了那个对象。所以我们可以这样做，而且对于简单的表单来说，这样是行得通的。但我其实不太喜欢这种方式。

## 98. 22. Form Submission and Error Handling with Conform & Zod

**原文**

Let's pull open our editor and we're going to swap all this stuff for the conform parse utility from conform to Zod. So this is going to give us back a submission object. We're going to say parse and that's coming from conform to Zod. We're going to pass in our form data and our schema is going to come from our note editor schema right there. And with that now, instead of taking the results and all of that, we have this submission object.

**译文**

让我们打开编辑器，把所有这些内容替换为来自 `conform-to-zod` 的合规解析工具。这样会返回一个提交对象。我们调用 `parse` 方法，它来自 `conform-to-zod`。我们将表单数据传入其中，而模式则来自我们这里的笔记编辑器模式。这样一来，我们就不再需要处理结果和那些东西了，而是得到了这个提交对象。

## 99. 23. Type Safety with Conform

**原文**

Now that we've got Conform working on our server side, we can use some of Conform's React utilities to work in our UI. And it can apply some really awesome progressive enhancement pieces. And on top of that, it makes it so that we can have complete type safety from the UI all the way to the back end and back again. It's really fabulous. So there are a couple of things that you need to know about that I've left in information in the instructions. Take a look at that and then get on to this exercise and we'll see you when you're done.

**译文**

既然我们已经在服务器端让 Conform 正常运行了，就可以使用 Conform 提供的一些 React 实用工具来开发我们的用户界面。它能实现一些非常出色的渐进式增强功能。更重要的是，它还能确保我们从用户界面到后端，再到返回用户界面的整个流程中都具备完整的类型安全性。这真是太棒了。关于这一点，有几点注意事项我已经放在了说明中。请查看这些说明，然后开始练习，我们稍后见。

## 100. 24. Simplifying Form Handling with Conform and Schema Validation

**原文**

All right, let's delete a lot of code. So starting from our UI right here, we can delete the use hydrated hook because that's handled for us by conform. We no longer need the form ref. That's also handled by conform. The form ID also handled by conform. We can delete everything between here and there. My goodness, all handled by conform. So the errors, the hydrated state, the error IDs,

**译文**

好的，我们来删除大量代码。首先从我们的 UI 这里开始，我们可以删除 `useHydrated` 钩子，因为 Conform 已经帮我们处理好了。我们也不再需要 `formRef`，Conform 同样已经处理好了。Form ID 也是由 Conform 处理的。我们可以删除从这里到那里的所有内容。天哪，全部都由 Conform 处理了。所以，错误、已同步的状态、错误 ID，
