# Kent C. Dodds - Epic Web. Ship Modern Full-Stack Web Applications part2

- 来源：[B站 BV1JcVxzREgs](https://www.bilibili.com/video/BV1JcVxzREgs)（up 主：lmt831，共 100 P）
- 说明：英文转录 + 中文翻译（机器翻译，仅供学习参考）

---

## 01. 25. Dad Joke Break Schema Validation

**原文**

All right, let's get ourselves a joke. We're going to have Cody read this one for us. Thanks, Cody. If the joke didn't make you chuckle, maybe Cody reading it did. Having some laughter is always a good thing, and I like taking these breaks. I like these random dad jokes. I hope you do too. I hope you really enjoyed these exercises and that you've been having just a wonderful time learning all of this stuff. So it's important for you to take a break. So this is a great time to get

**译文**

好了，我们来听个笑话吧。我们让 Cody 来给我们读这个笑话。谢谢，Cody。如果这个笑话没让你发笑，也许 Cody 读出来能让你笑一笑。能笑一笑总是好的，我喜欢这样休息一下。我喜欢这些随机的老爸式冷笑话。希望你也喜欢。希望你真的很享受这些练习，并且在学习这些知识的过程中一直过得非常愉快。所以，对你来说休息一下很重要。现在正是休息一下的好时机。

## 02. 26. Intro to File Upload

**原文**

Let's talk about file uploads. Before we get into this, I want to mention that Kelly, your coworker has done some pretty cool things to allow us to have images on our routes. So she made a resource route for us. Feel free to dive into this and look at that if you like. But again, you've learned about resource routes. It's just a route that does not export a default. And so here we've got the loader, we take the image ID, we look up that image in the database, which we're going to be

**译文**

我们来谈谈文件上传。在开始之前，我想提一下，你的同事 Kelly 已经做了一些很酷的事情，让我们可以在路由中显示图片。她为我们创建了一个资源路由。如果你愿意，可以随时深入研究并查看相关内容。不过，你已经学习过资源路由了，它只是一个没有导出默认值的路由。在这里，我们有一个加载器，它会获取图片 ID，然后在数据库中查找这张图片，而我们接下来要做的就是……

## 03. 27. File Upload Functionality

**原文**

Thank you so much Kelly the co-worker for doing a bunch of work for us. She's added some stuff to the edit page of our notes so that we can easily add file upload. So that's what your job is and when you're all done it should look something like this. So you should render a default image that to make it so people can add their image themselves. We can add some cute koala here and we say cute koala illustration by mid-journalist.

**译文**

非常感谢同事 Kelly 为我们做了大量工作。她已经在我们的笔记编辑页面中添加了一些功能，以便我们可以轻松地添加文件上传。这就是你的任务，当你完成所有工作后，页面应该看起来像这样。你需要渲染一张默认图片，以便人们可以自己添加图片。我们可以在这里添加一只可爱的考拉，并注明“由 mid-journalist 创作的可爱考拉插图”。

## 04. 28. Image Upload with Form Data and Memory Upload Handling

**原文**

Let's open up the edit route and here in the action we're going to handle the file upload. But let's do the UI side of this first. I think that'll make it all make a little bit more sense. So we have this new component called the image chooser. This was built for us by Kelly. You can feel free to dive into how all of this works, but it's pretty cool. It just handles all of the styling stuff. So you don't have to worry about doing this and also previewing the image and stuff like this.

**译文**

我们来打开编辑路由，然后在这里的 action 中处理文件上传。不过，我们先来做 UI 部分。我觉得这样会让整个流程更清晰一些。现在我们有一个名为 image chooser 的新组件。这是 Kelly 为我们构建的。你可以随时深入研究它的工作原理，但它确实非常酷。它能处理所有的样式相关逻辑，所以你就不必自己操心这些，还要预览图片之类的了。

## 05. 29. TypeScript Integration

**原文**

This step we're not actually going to change any behavior. Everything's going to work exactly the same as it did before. But now we're going to make TypeScript happy. And if TypeScript is happy, then Lily, the life jacket is happy. And if that emoji is happy, then I'm happy and our users will be happy because TypeScript, again, it's not making your life terrible. It's just showing you how terrible your life is. So we're going to listen to TypeScript. We're going to fix all of these issues, add the file to our schema. There's a little bit of

**译文**

这一步我们实际上不会改变任何行为。一切都将与之前完全相同地运行。但现在，我们要让 TypeScript 满意。如果 TypeScript 满意，那么 Lily（救生衣）就会开心。而如果这个表情符号开心，那么我也会开心，我们的用户也会开心，因为 TypeScript 并不会让你的生活变得糟糕，它只是向你展示了你的生活到底有多糟糕。所以我们要听从 TypeScript 的建议，修复所有这些问题，并将文件添加到我们的模式中。这里还有一点……

## 06. 30. Validating File Uploads with Zod Schema in a Web Application

**原文**

So we're going to need to update our schema to account for the image ID in the file and the alt text fields. So let's add an image ID. That's simple enough. It's a string. It's optional because there may not be an image yet. The alt text also a pretty simple thing. That's also optional. You might want to say alt text should always be required, but that's not super realistic. And so we're not going to make it required. Yeah.

**译文**

所以我们需要更新模式，以包含文件中的图片ID和替代文本字段。那我们先来添加一个图片ID。这个很简单，它是一个字符串类型。由于可能还没有图片，所以它是可选的。替代文本也相当简单，它也是可选的。你可能会说替代文本应该始终是必填项，但这并不太现实。所以我们不会把它设为必填项。是的。

## 07. 31. Dad Joke Break File Upload

**原文**

So this one actually stings a little bit, but here we go Americans can't switch from pounds to kilograms overnight that would cause mass confusion. I really wish that this would happen though. Please it's such a nightmare. I am sorry. We also use the wrong term for football. It's not soccer, but there's an interesting history there. Americans didn't mess that one up. You blame our good friends the English. But anyway

**译文**

说实话，这句话听起来有点扎心，但咱们还是得说：美国人不可能一夜之间就从磅换成公斤，那样会造成大规模的混乱。不过我真的希望这一天能到来。拜托了，这简直是个噩梦。抱歉。另外，我们在足球这个词上也用错了。它不叫“soccer”，不过这背后有一段有趣的历史。这一点美国人可没搞错，要怪就怪我们亲爱的英国朋友吧。不过，不管怎样。

## 08. 32. Intro to Complex Structures

**原文**

Complex structures. This is a question that I get a lot when people are talking about making forms because it's not always super obvious how you accomplish this and a lot of it has to do with just the way that the web platform handles forms. So let's talk about that. If you were to do like an array of elements, like let's say we had an array of to-dos, you might do something like this where you'd say, hey, this is a to-do array, but that's not going to work. You're not going to be able to get things by the to-do.

**译文**

复杂的结构。当人们在讨论如何创建表单时，我经常被问到这个问题，因为要实现这一点并不总是那么显而易见，而且这在很大程度上取决于 Web 平台处理表单的方式。那么，我们就来谈谈这个话题。假设你想创建一个元素数组，比如一个待办事项数组，你可能会这样做：嘿，这是一个待办事项数组。但这样是行不通的。你将无法通过“待办事项”来获取这些元素。

## 09. 33. Grouping and Managing Related Fields in Form Objects

**原文**

Pretty often you want to be able to group related fields together as part of like an object, especially once we add support for multiple image uploads. We want to be able to group all of the properties for each individual image in their own little object. And so it would be really nice to take these three properties and put them as a sub-object of image, and then they're going to each be a part of that. But we need to make Zod happy with that, and then we need to make our form

**译文**

很多时候，你希望将相关的字段组合成一个对象，尤其是在我们支持多图上传之后。我们希望能为每张单独的图片将其所有属性都组织成一个独立的小对象。因此，如果能将这三个属性作为 `image` 的子对象来组织，那就再好不过了，这样它们就都会成为该对象的一部分。不过，我们需要确保 Zod 能接受这种结构，然后还需要让我们的表单……

## 10. 34. Implementing Image Field Set with Conform and TypeScript

**原文**

So let's go to our edit route and we'll start with our Zod schema. We're going to make a image field set schema. That's an object that has these fields. So it's z shape or object thinking of prop types again. And then we've got our ID, which is optional. And the file is going to be just this thing. So let's grab that. We'll just bring this up here. Copilot could have done that too, but we're just going to copy and paste. There we go. Okay, great. So we've got our field.

**译文**

那我们进入编辑路由，从 Zod 模式开始。我们要创建一个图像字段集模式。这是一个包含这些字段的对象。所以它是 z 形状或对象，再次参考 prop 类型的概念。然后我们有 ID，它是可选的。而文件将只是这个东西。那我们把它拿过来。我们直接把它移到这里。Copilot 也能做到这一点，但我们还是直接复制粘贴吧。就是这样。好的，很好。这样我们就有了这个字段。

## 11. 35. Multiple Image Uploading

**原文**

Kelly the co-worker added some error validation and stuff for us. So thank you Kelly. We are going to now change our schema to support an array of images rather than just a single image. Once you're done, it will actually behave exactly the same as it does now because we're not actually going to add the add and remove buttons yet. But this is just like one more step until we get to actually being able to add multiple images, which will be really nice. So that is your task for this step is to change the, you're going to change the

**译文**

同事 Kelly 为我们添加了一些错误验证之类的功能。所以，感谢 Kelly。现在，我们将修改模式以支持图片数组，而不仅仅是一张图片。当你完成之后，它的实际表现将与现在完全相同，因为我们暂时还不会添加“添加”和“删除”按钮。但这只是迈向能够实际添加多张图片的又一步，那将会非常棒。因此，你这一步的任务就是修改……你将修改……

## 12. 36. Dynamic Image Lists with Field Sets

**原文**

We're not going to be making any user experiences differences here, but we are going to be making a number of developer experience differences here. So we're going to change this to images and that's going to be a Z array of the image fields that schema. And then that means that this is now going to be images. And this is now simply images. So we're full circle. We're now just here all the images. That's awesome. And then down here, we're going to rename our default value from

**译文**

我们在这里不会带来任何用户体验上的差异，但我们将带来一系列开发者体验上的差异。因此，我们将这里的内容更改为 images，它将是一个包含该模式中图像字段的 Z 数组。这意味着现在这里将是 images，而这里就只是 images。这样我们就闭环了。现在我们这里就全是 images 了。太棒了。然后在下面，我们将把默认值从

## 13. 37. Interactive Image Management

**原文**

Let's add a delete button and an add button. So here's the solution. This is what you're working toward. We've got our delete. We've got our add image. We can add as many of these images as we like and delete them as well. And on top of that, all of the rest of this stuff will still continue to work. And so if I add two images and we have alt text for them, so soccer and cuddle, and we submit that. And if we take a look at our alt text, that cuddle is still there and soccer is right there. So that is working perfectly.

**译文**

我们来添加一个删除按钮和一个添加按钮。以下是解决方案。这就是你努力要实现的效果。我们已经有了删除功能，也有了添加图片的功能。我们可以添加任意数量的这些图片，也可以将它们删除。此外，其余的所有功能仍将继续正常运行。例如，如果我添加两张图片，并为它们设置了替代文本，分别是“soccer”和“cuddle”，然后点击提交。如果我们查看替代文本，“cuddle”仍然存在，“soccer”也还在那里。这说明一切都在完美运行。

## 14. 38. Dynamically Delete and Add Buttons

**原文**

Let's start with our delete button. So we're going to go to the edit route and right here we want to have a delete button on each one of these images just right there. And we don't have an icon yet so we're just using emojis. Icons will come later, no worries. All right, so what we're going to do is add a button right here and inside of this button we're going to have a span for what we want the screen readers to hear. So a delete image and then the icon, the or our fake icon, our emoji for

**译文**

我们先从删除按钮开始。我们要进入编辑路由，就在这一处，我们希望为每张图片都添加一个删除按钮，就放在这里。目前我们还没有图标，所以暂时先用表情符号代替。图标稍后会加上，别担心。好的，接下来我们要在这里添加一个按钮，按钮内部我们会用一个 span 元素来指定屏幕阅读器需要朗读的内容，比如“删除图片”，然后再加上图标——也就是我们的虚拟图标，一个表情符号。

## 15. 39. Dad Joke Break Complex Structures

**原文**

Why do you never see elephants hiding in trees? Because they're so good at it. Cody does not like that joke very much. As a koala that does hide in trees and is found a lot, Cody still hasn't figured out how the elephants are so good at hiding in trees. So well done. This is a really great opportunity to get up, take a break, walk around, give somebody a high five because you're doing awesome. So keep it up. We'll see you after the break.

**译文**

你为什么从来没见过大象躲在树上？因为它们太会藏了。Cody 不太喜欢这个笑话。作为一只真的会躲在树上、而且经常被人发现的考拉，Cody 至今还没搞明白大象是怎么做到那么擅长躲在树上的。所以，做得很好。这真是个绝佳的机会——站起来休息一下，四处走走，跟别人击个掌，因为你表现得非常出色。所以，继续加油吧。我们休息后见。

## 16. 40. Intro to Honeypot

**原文**

Honeypots are not as sweet as they sound. So sometimes spam bots will go all over the web and submit as many forms as they possibly can. They do this for SEO purposes. So like they'll maybe try to get onto a form and post a link that back links to their own site or whatever. That actually, there's a fair good return on that investment, unfortunately. They will also sometimes just check for sites that are vulnerable, report back and say, hey, these sites are vulnerable.

**译文**

蜜罐并不像听起来那么美好。因此，垃圾邮件机器人有时会遍布整个网络，尽可能多地提交各种表单。它们这样做是为了 SEO 目的。例如，它们可能会尝试进入某个表单，发布一个指向其自身网站的反向链接之类的东西。不幸的是，这种做法的投资回报率其实相当高。它们有时还会专门寻找存在漏洞的网站，然后报告说：“嘿，这些网站存在漏洞。”

## 17. 41. Adding a Honeypot to Protect Against Spam Bots

**原文**

On our signup page, we want to add a honeypot so that random spam bots can't just fill in the email and have us sending emails to a bunch of people all over the place to get them to sign up for our service. That would be really bad for the people. It would be super annoying for them. Really bad for us because we would get marked as spam and then our deliverability would be bad, all of that stuff. So for that reason, we need to have an input that only a bot would fill out on here. So you're going to need to add an input and then

**译文**

在我们的注册页面，我们希望添加一个蜜罐（honeypot），这样随机的垃圾邮件机器人就无法简单地填写邮箱地址，导致我们向各地的大量用户发送注册邀请邮件。这对那些用户来说会非常糟糕，会给他们带来极大的困扰。对我们来说也非常不利，因为我们的邮件会被标记为垃圾邮件，进而导致邮件送达率下降，等等。因此，我们需要添加一个只有机器人才会填写的输入框。所以，你需要添加一个输入框，然后

## 18. 42. Honeypot Fields in Sign Up Forms

**原文**

Let's go to our sign up form right here and we can get rid of this. We're going to be using our form data and in our sign up route we want to render a hidden div within which we will place our label and our input. So let's make a div and these bots, these spam bots are really most of the time not very sophisticated in there. It's too expensive to run them at their scale and actually evaluate the JavaScript on the page so they don't do a whole lot of parsing.

**译文**

我们直接来到这里的注册表单，然后可以把这个删掉。我们将使用表单数据，在注册路由中，我们需要渲染一个隐藏的 div，并在其中放置标签和输入框。那么，我们先创建一个 div。这些机器人，也就是垃圾邮件机器人，大多数时候其实并不怎么高级。以它们的规模运行并实际评估页面上的 JavaScript 成本太高了，因此它们并不会做太多解析工作。

## 19. 43. Honeypot Fields for Form Security

**原文**

Let's go to our sign up and we'll come here and swap out this section with the Honeypot inputs from Remix Utils. And if we take a look at this now, we'll see we've got this div now has an ID and are you hidden true and style display none. It also has a label that says please leave this field blank that is customizable. And we also have the input that's the actual Honeypot. It also includes an autocomplete nope so that the browser

**译文**

让我们前往注册页面，然后来到这里，将这部分内容替换为 Remix Utils 提供的 Honeypot 输入项。如果我们现在查看一下，就会发现这个 div 现在有了一个 ID，并且具有 `are-you-hidden="true"` 和 `style="display: none"` 属性。它还有一个可自定义的标签，上面写着“Please leave this field blank”（请留空此字段）。此外，我们还有作为 Honeypot 主体的输入框。它还包含 `autocomplete="off"` 属性，以防止浏览器...

## 20. 44. Honeypots for Form Security

**原文**

There are more features that the Honeypot utility can give us, but we need to send some data from the server onto the client. We're also going to want to have this applied to all Honeypots in all forms on our website. We don't want to have to do this from the server to the client for every single one of the Honeypots. So what we're going to do is do this one time in our root, in that root loader, and then we'll have a provider that provides those values. And then the Honeypot inputs will look for that provider and use those values.

**译文**

Honeypot 实用程序还能提供更多功能，但我们需要从服务器向客户端发送一些数据。此外，我们希望将这些功能应用到网站上的所有 Honeypot 的各种形式中。我们不希望针对每一个 Honeypot 都单独执行从服务器到客户端的此类操作。因此，我们将在根目录中的根加载器里仅执行一次该操作，然后创建一个提供这些值的提供者。之后，Honeypot 输入将查找该提供者并使用这些值。

## 21. 45. Honeypot Protection

**原文**

Let's start out by going to our root and we have something new from Kelly the co-worker here. So before we had export default on the app, now we need to render our app within a provider so that everything in our app has access to that. And we could definitely put the provider around the document to know all of that stuff, but that would just be a lot of work. And so instead, we're going to make another component called app with providers. That's the thing that we will default export. And then we can just wrap the app and then we don't have to worry about it.

**译文**

我们先回到根目录，这里有一个来自同事 Kelly 的新内容。之前我们在 `app` 上使用了 `export default`，现在我们需要将应用渲染在一个 `provider` 中，这样我们应用中的所有东西都能访问到它。我们当然可以把 `provider` 包裹在 `document` 周围来实现这一点，但那会非常麻烦。因此，我们将创建另一个名为 `app with providers` 的组件，并将其作为默认导出。然后我们只需包裹住 `app`，就再也不用担心这个问题了。

## 22. 46. Consistent Encryption with Honeypot Server

**原文**

There's one last consideration with our Honeypot server, and that is if we don't have this configured or it's set to undefined as it will be in production, we'll have these fields in here. And the interesting thing is that one server could send the form and then another server could handle the form. So if we distribute our app into multiple regions or have multiple instances of our app running, then generating the form with one server and then submitting the form to another server, there will be a problem.

**译文**

我们的蜜罐服务器还有一个最后的注意事项，那就是如果我们没有配置这个选项，或者在生产环境中将其设置为 undefined，那么我们这里就会出现这些字段。有趣的是，一个服务器可以发送表单，而另一个服务器则可以处理该表单。因此，如果我们将应用部署到多个区域，或者运行多个应用实例，那么用一台服务器生成表单、再将表单提交给另一台服务器的做法就会出现问题。

## 23. 47. Setting Up Honeypot Security for Server Environment Variables

**原文**

First, let's go over to our ENV server and we're going to add a honeypot secret Z dot string to our validation to make sure that we have the honeypot secret environment variable set up because if that environment variable is not set up, then we're going to be in a bit of a bind. So that we're going to have set up. We do this validation in this init, which is going to be called inside of our server entry. So once that has been validated, we can then use that in here with the

**译文**

首先，让我们转到我们的 ENV 服务器，并在验证中添加一个蜜罐密钥 Z 字符串，以确保我们已设置好蜜罐密钥环境变量。因为如果该环境变量未设置，我们就会陷入困境。因此，我们需要将其设置好。我们在这个 `init` 函数中执行此验证，它将在我们的服务器入口点内部被调用。一旦完成验证，我们就可以在这里使用该变量了。

## 24. 48. Dad Joke Break Honeypot

**原文**

What's red and bad for your teeth? A brick! I don't know about you, but like just the thought of a brick, like using a brick to brush your teeth or something, I can almost feel it just thinking about that. I'm sorry if that is a terrible feeling for you as well. But yeah, anyway, don't brush your teeth with a brick, I guess. So hopefully you had a great time with that. Let's go ahead and take a break, get up, walk around, get a drink of water, use a bathroom, whatever you need to do.

**译文**

什么东西是红色的，而且对你的牙齿不好？砖头！我不知道你怎么样，但光是想到砖头——比如用砖头来刷牙什么的——我几乎都能想象出那种感觉。如果这也让你感到不适，那很抱歉。不过总之，还是别用砖头刷牙了。希望刚才那段内容让你看得开心。现在我们休息一下，站起来走动走动，喝点水，上个厕所，做点你需要做的事吧。

## 25. 49. Intro to CSRF

**原文**

So check this out. I've got this note and I love it so much. It's my favorite note. Also, I got this email from somebody who said that all I have to do is click on this button and I will get a free iPad. I'm so jazzed about this so I'm gonna click on this and get a free iPad. Wait, what? What just happened? Where did my note go? What? Ah! What happened to my note? Oh no! I just fell victim to a cross-site request forgery attack. It is so sad.

**译文**

快来看这个。我有一张便签，我超爱它。这是我最喜欢的便签。另外，我收到一封来自某人的邮件，他说我只需要点击这个按钮，就能免费获得一台 iPad。我对此兴奋不已，所以我要点击这个按钮，去领一台免费的 iPad。等等，什么？刚才发生了什么？我的便签去哪儿了？什么？啊！我的便签怎么了？哦不！我刚刚遭遇了一次跨站请求伪造攻击。真是太难过了。

## 26. 50. CSRF Protection with Cookies

**原文**

For this first step, we're going to get a little bit of a peek into using cookies to persist some data so that we can associate this authenticity token with the particular client so that when they submit their forms, we can check from between the cookie that the client has and the token that was submitted in the form. So there's going to be a little bit of that. We're not going to dive too deep into the cookies until a future workshop. Once we talk about authentication, so you are going to be creating a cookie, you're going to be creating a

**译文**

在这第一步中，我们将初步了解一下如何使用 Cookie 来持久化一些数据，以便将该身份验证令牌与特定客户端关联起来。这样，当客户端提交表单时，我们就可以检查客户端持有的 Cookie 与表单中提交的令牌是否匹配。因此，这里会涉及一些相关内容。不过，在后续的研讨会中讨论身份验证之前，我们不会深入探讨 Cookie。届时你将需要创建一个 Cookie，你将要创建一个

## 27. 51. Creating and Managing CSRF Tokens With Node.js

**原文**

So the first thing we're going to want to do is create a utility for managing the CSRF utility. So CSRF.server.ts in our Utils here. And the CSRF utility is created with new CSRF coming from Remix Utils CSRF server. And then we've got a couple options that we can provide here. So cookie being the primary one, and we need to create a cookie object. So we're going to create a

**译文**

首先，我们要创建一个用于管理 CSRF 工具的实用程序。因此，在 Utils 文件夹中创建 CSRF.server.ts 文件。CSRF 工具通过 `new CSRF` 创建，其中 CSRF 来自 Remix Utils 的 CSRF 服务器。然后，我们可以提供一些选项，其中最主要的是 cookie，因此我们需要创建一个 cookie 对象。所以，我们将创建一个

## 28. 52. Authenticity With Token Protection

**原文**

So you'll remember our objective here is to prevent nefarious actors from like causing our users to accidentally delete their notes. So we're going to be working in that particular form to add our authenticity token. But before we can add the authenticity token, we need to provide that token to all of the forms on our page so that we can render this authenticity token component in the forms that we want to do this checking on. So your job is in the root

**译文**

所以你要记住，我们在这里的目标是防止恶意行为者导致用户意外删除他们的笔记。因此，我们将在特定的表单中工作，添加我们的真实性令牌。但在添加真实性令牌之前，我们需要将该令牌提供给页面上的所有表单，以便我们可以在希望执行此检查的表单中渲染这个真实性令牌组件。因此，你的任务是在根组件中完成。

## 29. 53. Security with Authenticity Token and CSRF Validation

**原文**

Let's go ahead and start in the note ID route where we have that delete button. So the what we really are our objective here is to add the authenticity token input and if I just add that and then we pull up our Delete button in here, then we'll see we've got our form, but it's not rendering anything The reason it's not rendering anything is because we haven't actually provided that token here We have loaded it in the root, but we need to provide it. So let's go to the root

**译文**

让我们从笔记 ID 路由开始，那里有那个删除按钮。我们在这里的主要目标是添加身份验证令牌输入框。如果我直接添加它，然后在这里调出我们的删除按钮，我们会看到表单已经出现，但它没有渲染任何内容。没有渲染任何内容的原因是我们实际上没有在这里提供该令牌。我们已经在根目录中加载了它，但需要将其提供出来。因此，让我们转到根目录。

## 30. 54. Dad Joke Break CSRF

**原文**

My friend sent to me what rhymes with orange. I said no it doesn't Okay, now is a good time for you to take a little bit of a break. Maybe get yourself an orange snack Have a good time. We'll see you in a bit

**译文**

我朋友给我发了一个和“orange”押韵的词。我说不对，不押韵。好啦，现在正是你稍微休息一下的好时机。或许可以拿个橙子当零食。祝你玩得开心，我们待会儿见。

## 31. 55. Intro to Rate Limit

**原文**

Getting attacked by a nefarious actor is never a fun time. And it's especially not fun if they're like brute forcing to get access to a specific account or they're making your server send a bajillion emails and so it's destroying your deliverability or they're just a number of things that an attacker can do to make your life pretty miserable. And they like increase your server hosting costs and all that stuff, especially if you have auto scaling enabled and stuff like that. So it's a good idea to add a little bit of

**译文**

遭受恶意攻击者的攻击从来都不是什么愉快的经历。如果他们试图通过暴力破解的方式访问特定账户，或者让你的服务器发送海量的电子邮件从而导致你的邮件送达率被毁掉，又或者他们能做其他各种事情让你的生活变得相当痛苦，那就尤其令人头疼了。他们还会增加你的服务器托管成本等等，尤其是当你启用了自动扩展之类的功能时。因此，添加一点点……是个好主意。

## 32. 56. Optimizing Your Express Server with Rate Limiting Middleware

**原文**

There's no situation in the world where it would make sense for somebody to sit here and go refresh about a bajillion times in a minute. That just wouldn't make any sense. They're probably trying to do a denial of service attack or something. And the fewer resources we can allocate to somebody doing something like this, the better. So I'm just going to keep going because we haven't implemented this yet. So what we're going to be doing in this exercise is adding a single rate limit configuration so that we can

**译文**

在世界上没有任何一种情况，会有人坐在这里一分钟内刷新几十亿次。这根本说不通。他们很可能是在尝试进行拒绝服务攻击之类的操作。而我们能为这类行为分配的资源越少越好。所以我将继续进行下去，因为我们还没有实现这个功能。因此，在本次练习中，我们将要做的就是添加一个速率限制配置，以便我们能够……

## 33. 57. Safeguarding Your Server- Adding Rate Limit Configuration

**原文**

Because we want this rate limit to apply before we even get into our remix code, so we want to use as few resources as possible to handle these rate limits before we get into our remix stuff, this is all going to happen before remix is even called. So this will happen in our server index file right here. So this is our express server. We have a couple of static files stuff where we're compressing the responses, all this stuff. This is all stuff that is like, it's really fast. It's not a problem. And in fact, users will be making requests to get static

**译文**

因为我们希望这个速率限制在我们进入 remix 代码之前就生效，所以我们希望在处理这些速率限制时尽可能少地消耗资源，然后再进入我们的 remix 相关逻辑。这一切都会在 remix 被调用之前完成。因此，这部分代码将放在我们的服务器索引文件中，也就是这里。这是我们的 express 服务器。我们有一些静态文件相关的处理，比如压缩响应等操作。这些都是非常快速的部分，不会造成问题。实际上，用户发起的请求正是为了获取这些静态资源。

## 34. 58. Tiered Rate Limiting with Custom Middleware

**原文**

There's a really big difference between a user on the home page just refreshing a bunch of times hoping they see their notifications or whatever they're looking for and a user going to the sign up page or the login page and entering some bogus stuff and trying to guess a user's password, right? I'm okay with the user trying to refresh and get their notifications that does happen sometimes. But if a user tries to sign up like 30 times in a minute, there's probably something fishy there. Or if a user tries to log in like 100 times in a minute, that yeah, that's probably

**译文**

在主页上，用户只是不断刷新页面，希望能看到通知或他们想找的内容，与那些前往注册页或登录页、输入虚假信息并尝试猜测用户密码的用户之间，存在着非常大的区别，对吧？用户尝试刷新以获取通知，这种情况有时会发生，我对此是可以接受的。但如果一个用户在短短一分钟内尝试注册30次，那很可能有些不对劲。或者如果一个用户在短短一分钟内尝试登录100次，那毫无疑问，这很可能就是异常情况。

## 35. 59. Applying Rate Limiting

**原文**

So let's open up our server and we're going to take this config and make a variable called our rate limit default. Stick that right there. And then we're going to create three different rate limit middlewares. So these are the three and it's going to be rate limit will pass our config and each one of them will have basically the same thing. So we'll have the rate limit default. But then for the strongest rate limit, we're going to say you only get 10 of these kinds

**译文**

那么，我们先打开服务器，然后获取这个配置，并将其创建一个名为 `rateLimitDefault` 的变量。把它放在这里。接下来，我们将创建三种不同的限流中间件。就是这三种，它们都会传入我们的配置，而且每个中间件的内容基本上都相同。因此，我们会使用 `rateLimitDefault`。但对于最强的限流规则，我们会规定你只能获得 10 次此类访问。

## 36. 60. Dad Joke Break Rate Limit

**原文**

A horse walks into a bar. The bartender says, hey, the horse says, sure. So that is that. You get to pet yourself on the back for doing such a good job, get yourself a drink, get yourself a treat. Go tell your dog the wonderful thing that you just did or your significant other or whoever. Just shout it from the rooftops. Look, I did this awesome thing. But yeah, now's a good time to take a little quick

**译文**

一匹马走进一家酒吧。酒保说：“嘿。”马说：“好啊。”就这样。你可以为自己干得这么出色而拍拍肩膀，给自己倒杯饮料，再弄点好吃的。去告诉你的狗你刚才干了件多么了不起的事，或者告诉你的另一半，或者任何你想告诉的人。尽管从屋顶上大声喊出来吧。瞧，我干了一件超棒的事。不过嘛，现在正是快速休息一下的好时机

## 37. 61. Outro to Professional Web Forms Workshop

**原文**

Hey, you did it. Well done. Awesome job. We've got really, really awesome error handling and really great form authoring experiences that our users are going to love using. We have protection for ourselves with rate limiting. And our users are going to love the CSRF token stuff, even though they don't know what that is. And they probably don't actually care. But they really do because we're protecting our users' data. And they like the honeypots. Well, hopefully they never know about the honeypots either. But we like the honeypots because we're not getting

**译文**

嘿，你做到了。干得漂亮。太棒了。我们拥有了非常非常出色的错误处理机制，以及非常棒的表单编写体验，我们的用户一定会喜欢使用这些功能。我们通过速率限制保护了自己。而我们的用户也会喜欢 CSRF 令牌相关的东西，尽管他们并不知道那是什么。他们可能也根本不在乎。但实际上他们很在意，因为我们正在保护用户的资料。他们也喜欢蜜罐。嗯，希望他们也永远不知道蜜罐的存在。但我们喜欢蜜罐，因为我们不会收到

## 38. 01. Intro to Data Modeling Deep Dive Workshop

**原文**

Hello, we're going to be doing some database stuff. We're finally getting off of our in-memory database thing, and we're going to be doing real database things. So let's take a look at the finished version of all this stuff. We've got a user search page. We can look for different users. We can dive into those users, and those users now have images, and it's awesome. And those images can be edited, and everything is sweet. We can change this. We can add a Koala cuttle.

**译文**

你好，我们接下来要处理一些数据库相关的东西了。我们终于要告别那种内存数据库的方案，开始使用真正的数据库了。那么，让我们来看看这些功能的最终版本吧。我们有一个用户搜索页面，可以搜索不同的用户。我们可以深入查看这些用户，现在这些用户还有了图片，效果非常棒。而且这些图片还可以编辑，一切都完美无缺。我们可以修改这个内容，还可以添加一个“Koala cuttle”。

## 39. 02. Intro to Database Schema

**原文**

In this exercise, we're going to create a database schema where we can insert users. And that's actually all we're going to be able to do is just do users. But this is going to get us introduced to the idea of creating a new database with Prisma. We're going to definitely be looking at some SQL too. So look forward to that. So just to give you kind of an idea around what database schemas are and why they're so great, this is what it would take to create a series of tables in a database that

**译文**

在本练习中，我们将创建一个可以插入用户的数据库模式。实际上，我们只能处理用户相关的操作。但这将帮助我们初步了解如何使用 Prisma 创建新数据库。同时，我们肯定也会涉及一些 SQL 内容，敬请期待。为了让你对数据库模式及其优势有个大致了解，以下是在数据库中创建一系列表所需的操作：

## 40. 03. Setting Up the Database with Prisma

**原文**

Let's get our database set up with Prisma. We're going to be running a couple of Prisma scripts to get things going to initialize our schema, and then we're going to add a couple of things to our schema. So most of this is going to be new files that we're creating and stuff. So you're going to want to follow the instructions that kind of outlays the files that you're going to be creating and the scripts that you're going to be running. We're actually not going to be pulling up the application for a little while until we get everything all situated

**译文**

让我们用 Prisma 来搭建数据库。我们将运行几个 Prisma 脚本来完成初始化工作，包括初始化我们的模式，然后我们会在模式中添加一些内容。因此，这部分内容主要涉及我们创建的新文件和相关操作。你需要按照说明来了解将要创建的文件以及要运行的脚本。在一切准备就绪之前，我们暂时还不会启动应用程序。

## 41. 04. Database with Prisma and SQLite

**原文**

To get us started, let's run npx prisma init and we're going to provide the flag url so that it knows that we want to make a SQLite database and we want it at file colon dot slash data dot db. That dot slash is going to be relative to the prisma schema that it's going to create for us, which will live inside of prisma, the directory. And so it's telling us, yeah, don't like we already have a dot get ignore file. Don't forget to add the dot env. You'll notice we actually don't have the dot env in our

**译文**

首先，让我们运行 `npx prisma init`，并提供 `url` 标志，这样它就会知道我们想要创建一个 SQLite 数据库，并将数据库文件指定为 `file:./data.db`。这里的 `./` 是相对于它将为我们创建的 Prisma 模式文件的路径，该文件将位于 `prisma` 目录下。然后它会提示我们：是的，我们已经有 `.gitignore` 文件了。别忘了添加 `.env` 文件。你会发现我们当前实际上并没有 `.env` 文件。

## 42. 05. Dad Joke Break Database Schema

**原文**

Bad at golf? Join the club. I actually am bad at golf and I don't even enjoy it that much, but my son likes it, my father-in-law likes it, so I go golfing sometimes. But I know there are a lot of people who love golf and I think that's awesome that you love golf. If that's what you like to do, go out and play some golf right now and then come back and get back to the exercises. If you're not into golf, go do something else. But it's important for you to get up, take a break, let your brain process the stuff that you're learning, and then get back

**译文**

高尔夫打不好？欢迎加入这个行列。我其实也打不好高尔夫，甚至不怎么喜欢这项运动，但我儿子喜欢，岳父也喜欢，所以我偶尔也会去打几杆。我知道有很多人热爱高尔夫，我觉得你能热爱高尔夫真是太棒了。如果这就是你喜欢做的事，那就现在出去打会儿高尔夫，然后再回来继续练习吧。如果你不感兴趣高尔夫，那就去做点别的。但重要的是你要站起来休息一下，让大脑消化一下正在学习的内容，然后再继续。

## 43. 06. Intro to Data Relationships

**原文**

How is your relationship? I hope it's awesome. We're going to talk about database relationships here. So we're going to do three of the most common database relationships, one to one, one to many, and many to many. And so I want to show you a couple of examples before we get started, specifically in Prisma schema language. So here we have a person, a single person can have a single social security number here in the US. And that social security number is going to be separate.

**译文**

你的关系怎么样？希望很棒。我们接下来要讨论的是数据库关系。我们将介绍三种最常见的数据库关系：一对一、一对多以及多对多。在开始之前，我想先通过几个示例来展示这些关系，具体使用 Prisma 模式语言。比如这里有一个“person”（人），在美国，一个单独的“person”只能拥有一个“social_security_number”（社会安全号码）。而这个社会安全号码是单独存在的。

## 44. 07. One-to-Many Relationships

**原文**

Now we're going to create our note model. So the note model is kind of interesting because it has a relationship with the user. So a single user can own multiple notes. And so we can make another note over here. And this note is owned by the user and so on. The interesting thing here though is that we can't have a single note that's owned by multiple users. That's not allowed. So each user has their own note. And also what's interesting is in a one to many relationship like we have here where

**译文**

现在我们要创建我们的笔记模型。笔记模型有点意思，因为它和用户之间存在一种关系。也就是说，单个用户可以拥有多个笔记。我们可以在这里再创建一个笔记。这个笔记由该用户拥有，依此类推。不过，这里有趣的一点是，我们不能让单个笔记被多个用户同时拥有。这是不允许的。因此，每个用户都有自己独立的笔记。此外，像我们这里这样的一对多关系中，还有一个有趣的地方是：

## 45. 08. One-to-Many Relationships in Prisma

**原文**

Let's head over to our schema.prisma file and right down here we're going to create our note model. So we'll say model note and this is going to have all the typical fields even co-pilot can fill this in for us. So we've got our ID just like we have for our user model. We have a title and content and then created at an updated at all of that pretty standard stuff. And then we have a relationship. So let's talk about the relationship.

**译文**

让我们转到 schema.prisma 文件，就在这里创建我们的 note 模型。我们输入 model note，它会包含所有典型的字段，甚至 co-pilot 都能帮我们填好。这里有 ID，就像我们在 user 模型中那样；还有 title 和 content，以及 created at 和 updated at，这些都是很标准的字段。然后是一个关系。我们来谈谈这个关系。

## 46. 09. Database Design

**原文**

We've got to get these images in here now. And now we're actually going to add images to users as well. So nodes have images, users have images. When I originally put this together, I thought, you know, like, there's a lot of different kinds of files that you could potentially create in an application. You got PDFs and CSVs and images, of course, and all sorts of different types. So why don't we do like a file type that's like just a generic thing where you stick a blob of stuff, and then we can have an image

**译文**

我们现在必须把这些图片加进来。现在，我们实际上还要为用户添加图片。也就是说，节点有图片，用户也有图片。当初我设计这个功能的时候，我想，你知道的，一个应用程序里其实可以创建各种不同类型的文件。比如有 PDF、CSV，当然还有图片，以及许许多多其他类型。那为什么不设计一种通用的文件类型呢？这种类型可以简单地存储一坨数据，然后我们就能用它来存放图片了。

## 47. 10. One-to-One and One-to-Many Relationships in Prisma

**原文**

So let's come down here, we'll make the user image first. So say model, user image. And here, Copilot's going to fill this stuff in. Let's just check its work. That's an important part of AI assisted programming. It is assisted. It is not the programmer yet. So here we have our ID. It's going to be just like the other IDs that we've had so far. So that works fine. Our alt text is going to be optional. And so an optional string, our content type. So this is like whether it's an a PNG

**译文**

那我们到这里来，先创建用户图片。所以写成 model, user image。然后，Copilot 会自动补全这些内容。我们来检查一下它生成的结果。这是 AI 辅助编程中非常重要的一环。它只是辅助工具，还不能完全取代程序员。这里我们有 ID，它会和我们之前见过的其他 ID 一样，所以没问题。alt 文本是可选的，因此是一个可选字符串。还有内容类型，比如它是否是 PNG 格式。

## 48. 11. Dad Joke Break Data Relationships

**原文**

I saw an ad in a shop window, television for sale, $1, volume stuck on fall. I thought, I can't turn that down. Ha ha. All right, hopefully you had a good time with that one. It's a good time to take a break now, get up, get a drink, walk around, do some jumping jacks, whatever you need to do to get your body moving so that your brain has the blood flow that it needs. And take some notes, whatever, to make sure that you solidify in your mind the things that you've been learning. Maybe start writing a blog post

**译文**

我在商店橱窗里看到一则广告：电视出售，售价1美元，音量卡在“关”的位置。我想，我可没法把音量调低啊。哈哈。好了，希望你们刚才玩得开心。现在是时候休息一下了——站起来，喝点东西，走动走动，做几个开合跳，或者做任何能让你身体动起来的事情，这样大脑才能获得所需的血液流动。也请做些笔记，不管用什么方式，确保把你学到的东西牢牢记在脑子里。或许可以开始写一篇博客文章。

## 49. 12. Intro to Data Migrations

**原文**

Let's talk about migrations. So making changes so far, what we've done is we just run NPX Prisma DB push. And that just says whatever the database is right now, the schema is going to be pushed up to the database. And that works okay for non-breaking changes. So let's talk about that. Here we have an order, and then we decide we want to have reviews on the order. So the order table doesn't actually get changed with this. In fact, we're only creating a new table.

**译文**

我们来谈谈迁移。到目前为止，我们进行的更改只是运行了 NPX Prisma DB push。这条命令会将当前的数据库模式推送到数据库中。对于非破坏性更改来说，这种方法效果不错。我们来具体看看。这里我们有一个订单，然后我们决定要为订单添加评论功能。因此，订单表本身并不会因此发生改变。实际上，我们只是创建了一个新的表。

## 50. 13. Creating Migration Files for Database Management with Prisma

**原文**

Let's go ahead and make our migration file. So we want to be able to spin up a new database every single time we like to play to a new environment or whatever. And then as we make changes over time, we want to be able to apply those changes to our existing databases so that we can create new tables or rename properties or whatever we're going to be doing. So in this exercise, you're going to be creating your migration file that will end up in the Prisma folder right here.

**译文**

我们开始创建迁移文件吧。我们希望每次想尝试新环境时，都能随时启动一个新的数据库。然后，随着时间的推移，当我们做出更改时，希望能够将这些更改应用到现有的数据库中，以便创建新表、重命名属性，或者执行其他操作。因此，在本练习中，你将创建一个迁移文件，该文件最终会保存在这里的 Prisma 文件夹中。

## 51. 14. Database Migrations with Prisma

**原文**

Let's create our migration. We're going to say npx prisma migrate dev. So we're creating our first migration here. It's going to warn us that we're going to lose all of our data and drop all of our tables and all that stuff. So it's just saying, hey, just so you know, and that's fine for us because we're generating this data anyway. So I'm going to say yes, and we're going to enter a name for the migration. So I'll say init. And that generates our migration also generates our prisma client. So here it's

**译文**

我们来创建迁移。输入 `npx prisma migrate dev`。这样我们就在这里创建第一个迁移。它会警告我们，这将导致所有数据丢失，并删除所有表等。它只是提醒我们一下，这对我们来说没问题，因为我们本来就要生成这些数据。所以我选择“是”，然后为迁移输入一个名称。我输入 `init`。这会生成我们的迁移，同时也会生成我们的 Prisma 客户端。所以现在这里就是

## 52. 15. Dad Joke Break Data Migrations

**原文**

I ordered a chicken and an egg from Amazon. I'll let you know. If you don't get, I'm not gonna tell you that one. Think about it a little bit. That one's actually pretty clever. That's a good one. All right, so I know that was a pretty quick exercise, but we're gonna make you take a break anyway, because breaks are important in your life. You need to get up and walk around and take some notes, whatever you need to do to really solidify this in your mind and give yourself the self-care

**译文**

我从亚马逊订购了一只鸡和一个鸡蛋。我会告诉你的。如果你没收到，我就不会告诉你那一题。仔细想想看。那一题其实挺巧妙的。那道题不错。好了，我知道刚才的练习进行得很快，但我们还是要让你休息一下，因为休息在你的生活中很重要。你需要站起来走动一下，记些笔记，做任何你需要做的事情，以便真正把这些内容巩固在脑海里，并照顾好自己。

## 53. 16. Intro to Seeding Data

**原文**

All right, let's let it grow with seeding data. So manual creation of data inside of Prisma Studio, not fun. I don't want to do that. Whenever I mess up data, I've got to like reset it. That would be so, so annoying. So instead, we automate stuff because we're software engineers. We're going to make this automatic. And so that is what seeding is. It's just a script that will create data in the database, deletes it, then creates it a new anytime you need to get that new data.

**译文**

好的，让我们用种子数据来让它增长起来。在 Prisma Studio 中手动创建数据可一点都不好玩，我可不想这么做。每当我把数据搞砸时，就得把它重置一遍，那简直太烦人了。所以，作为软件工程师，我们应该自动化处理这些事情。我们要让这个过程自动完成。而这正是“种子数据”的作用所在。它只是一个脚本，可以在数据库中创建数据、删除数据，然后在你需要新数据时随时重新创建。

## 54. 17. Configuring Prisma for Seed Script Execution

**原文**

So we've got our seed script that we made earlier to insert some images in the database. I want you to update the seed script so that it works without having anything in the database. In fact, I want it to delete everything in the database before we actually load new things in the database. This way we can just do like a refresh of our database and all of the data. We're going to stick in a couple pieces of data here, including the images and things. And then I want you to reset the database to be

**译文**

所以我们已经有了之前创建的种子脚本，用于向数据库中插入一些图片。我希望你更新这个种子脚本，使其在没有数据库内容的情况下也能运行。实际上，我希望它在向数据库中加载新内容之前，先删除数据库中的所有数据。这样我们就可以像刷新一样更新整个数据库及其所有数据。我们将在其中添加一些数据，包括图片等。然后我希望你将数据库重置为...

## 55. 18. Creating and Managing Data with Prisma Seed Scripts

**原文**

Our first step is to make it so that Prisma can actually run our seed script as part of the seed command and the things that it generates and things. So we're going to go down here to the bottom and we're going to add a section in here for Prisma and we'll say seed. We're going to say npx tsx prisma seed dot ts. And with that now, we should be able to run npx prisma db seed and that will execute our seed script. And the seeding command has been

**译文**

我们的第一步是让 Prisma 能够在执行 `seed` 命令时实际运行我们的种子脚本，以及它生成的相关内容。因此，我们将滚动到底部，在这里为 Prisma 添加一个部分，并写上 `seed`。然后输入 `npx tsx prisma seed.ts`。这样之后，我们应该就能运行 `npx prisma db seed` 来执行我们的种子脚本了。而种子命令也已经

## 56. 19. Optimizing Queries with Nested Mutations in Prisma

**原文**

So we talked about nested queries a little bit. We've got these images that we're creating at the same time we're creating this note. So what's cool about this is it allows us to automatically handle foreign keys like we're having to handle this foreign key right here. We've got codey and dot ID. We're specifying that on our ID. But these images on the note, they rely on the note ID, but we're not actually having to specify that because we don't even have it yet because we're in the process of creating it.

**译文**

我们之前稍微聊了一下嵌套查询。我们在创建笔记的同时，也会创建这些图片。这样做的好处是，它允许我们自动处理外键——就像我们现在需要处理的外键一样。这里有 `codey.id`，我们正在为它的 ID 做指定。但这些图片依赖于笔记的 ID，而我们实际上并不需要显式地指定这一点，因为此时笔记还在创建过程中，我们甚至还没有它的 ID。

## 57. 20. Nested Queries in Database Operations

**原文**

All right, let's nest the heck out of this thing. So I'm going to take all this create stuff from our note create, and we're going to add notes and create. And here we can provide an array of notes. And I'm just going to stick all that right there. And now we no longer need to provide the owner ID. We don't need that. And we don't need this. Tada. That's it. We're done. And so we can double check that this works with NPX Prisma DB seed. And that will run our seed script.

**译文**

好的，让我们把这个东西彻底嵌套起来。所以我要把我们笔记创建部分的所有创建代码都拿过来，然后添加 notes 和 create。在这里我们可以提供一个笔记数组。我直接把这些代码都粘贴进去。现在我们就不再需要提供所有者 ID 了，不需要那个了。这个也不需要了。搞定。就是这样。我们完成了。然后我们可以通过 NPX Prisma DB seed 来再次确认一下是否有效。这会运行我们的种子脚本。

## 58. 21. Dad Joke Break Seeding Data

**原文**

Dad, I'm cold go stand in the corner. I hear it's 90 degrees That's uh, yeah that I've never actually heard that one before that one was pretty pretty good. All right, let's take a break. Let's get up Let's walk around go high five somebody tell somebody that they're awesome and and why something specific Not generic you're awesome But like give them a genuine compliment and then you will feel better and they will feel better and everybody like if we all did that then like the world would be such a nice place so go

**译文**

爸爸，我冷，去角落里站着。我听说那儿有90度。呃，是啊，这个我倒是从来没听过，这个真的挺不错的。好了，我们休息一下。站起来，到处走走，去跟别人击掌，告诉某个人他们很棒，而且要具体说明为什么。不要只是笼统地说“你真棒”，而是要给出一个真诚的赞美。这样你感觉会好些，对方也会感觉好些。大家都会如此——如果我们都能这样做，那世界就会变得特别美好。所以，去吧。

## 59. 22. Intro to Generating Seed Data

**原文**

I don't know about you, but I don't want to have to create every single user that I want in my database, like every single hard code, all of that data. That just doesn't sound fun to me at all. And so you'd end up with a seed file that was enormous. And what if you wanted to do some performance testing? So you want to create 6,000 users or something like that. Yeah, that would be awful. And so we're going to randomly create some data. You create some fake data using a library called Faker.

**译文**

我不知道你们怎么样，反正我可不想在数据库里逐个创建我想要的每一个用户，比如把所有数据都硬编码进去。这听起来一点都不好玩。这样一来，你的种子文件会变得非常庞大。那如果你想做一些性能测试呢？比如想创建 6000 个用户之类的。是的，那可就惨了。所以，我们要随机生成一些数据。你可以使用一个叫做 Faker 的库来生成一些假数据。

## 60. 23. Generating Fake Data for Efficient Testing

**原文**

Hard coding, creating one user at a time is, yeah, not the best, not awesome. I don't want to have to think about what my title and content should be for all the notes that I want to create and test around and stuff, or even like the name of the users and stuff like that too. I don't want to have to do that. And so you're not going to have to do that. I'm going to show you how you can use awesome tools to generate fake data that looks realistic enough to actually work with on a day to day. So that's what you're going to do in this exercise. Have a good time.

**译文**

硬编码、一次只创建一个用户，嗯，这确实不是最佳方案，也一点都不酷。我可不想在为所有想要创建和测试的笔记思考标题和内容，甚至还要考虑用户名之类的东西。我可不想做这些。所以你也不用做这些。我将向你展示如何使用一些很棒的工具来生成足够逼真的模拟数据，以便日常使用。这就是你在这次练习中要做的。祝你玩得开心。

## 61. 24. Generating Random User Data with Faker.js for Database Seeding

**原文**

Let's jump into our seed script and we'll bring in Faker, just like Marty the Moneybag wants us to. And then we can use that to help us create a user that has like random information. So we'll await Prisma user create. And here we're going to have our data. And then our data is going to include a couple of things. We're not going to provide like necessarily the ID and stuff like that for this user, because this one's going to be totally random anyway. So we've got our user email.

**译文**

让我们进入种子脚本，引入 Faker，就像 Marty the Moneybag 希望我们做的那样。然后我们就可以用它来创建一个包含随机信息的用户。因此，我们将使用 `await Prisma user create`。这里我们将提供数据。数据将包含几个部分。我们不需要特意为用户指定 ID 之类的信息，因为这个用户本来就是完全随机的。所以我们有用户的邮箱。

## 62. 25. Dynamically Generating Data

**原文**

All right, Kelly did a lot of work for us and I just want to review some of that for you before we add the ability to have dynamic amount of data. So we want more than just a couple of notes and a couple of users. We want to have as many as we want to make it really easy. So Kelly organized things for us a little bit. First of all, she made this create user utility that handles creating this user and even makes the username resemble the name of the user that we created. So first and last name can

**译文**

好的，Kelly 为我们做了很多工作，在添加动态数据量的功能之前，我想先带大家回顾一下其中的一些内容。我们希望拥有的不仅仅是几条笔记和几个用户，而是能够根据需要添加任意数量的数据，让整个过程变得非常轻松。因此，Kelly 帮我们整理了一些东西。首先，她创建了这个“创建用户”工具，它能够处理用户的创建，甚至能让用户名与我们创建的用户姓名相匹配。因此，我们可以输入名字和姓氏，然后

## 63. 26. Generating Dynamic Seed Data

**原文**

Let's improve this seed script. So we have dynamic number of users. So right down here, we're going to say for loop and index is fine. Then we've got our array of actually, it's not an array, it's a total users. And so what's cool about this is once we move this into here, then we can make a change to our total users from five to 5000 if we wanted to and then now we've got 5000 users we're creating.

**译文**

让我们来改进这个种子脚本。现在我们有动态数量的用户。所以就在下面这里，我们写一个 for 循环，使用索引也没问题。然后我们有一个数组——实际上它不是一个数组，而是用户总数。这段代码的妙处在于，一旦我们把它移到这里，就可以将用户总数从 5 改成 5000（如果我们愿意的话），这样我们就能创建 5000 个用户了。

## 64. 27. Creating Unique User Data with Enforce Unique Library

**原文**

You know how we have a unique constraint on both the username and email? This is very good. It will help our queries to email and username be a lot faster. And just like from a pure product standpoint, it makes a lot of sense for those things to be unique. In fact, we're going to log the user in with their username or email as well. So we need to have those be unique. The problem is in our seed data, we're not actually generating unique values quite yet. Like we're generating random values and it's possible that two of these users could end up with the same

**译文**

你知道我们对用户名和邮箱都设置了唯一性约束吗？这非常好。它将大大加快我们针对邮箱和用户名的查询速度。而且，从纯粹的产品角度来看，这些字段具有唯一性也合情合理。实际上，我们还会让用户通过用户名或邮箱登录。因此，我们必须确保这些字段是唯一的。问题在于，在我们的种子数据中，我们目前还没有真正生成唯一的值。比如，我们生成的是随机值，这就可能导致两个用户最终拥有相同的值。

## 65. 28. Generating Unique and Valid Usernames in Seed Data

**原文**

Before I actually enforce this uniqueness, I'm going to come down here and we're going to add a catch right here because if there is a problem creating one of these users, this isn't all that critical that we actually fail everything. I'd rather just have some seed data created rather than blowing up the whole seed script. This is especially useful if you're creating a lot of users and it takes a while and you're waiting and you're waiting and then the second to last user, it blows up and you're like, that's so annoying.

**译文**

在我真正强制执行这个唯一性之前，我先往下走，在这里添加一个捕获处理。因为如果在创建这些用户时出现问题，我们其实不必让整个流程都失败。我宁愿只创建部分种子数据，也不愿让整个种子脚本崩溃。这一点尤其有用，特别是当你创建大量用户时——整个过程需要花费一些时间，你一直在等待，结果倒数第二个用户创建时突然失败，那种感觉真的非常烦人。

## 66. 29. Dad Joke Break Generating Seed Data

**原文**

Did you know Albert Einstein was a real person? All this time I thought he was just a theoretical physicist. All right, so this is a good time to take a break. I feel pretty good about the work that we've done so far. You should just pat yourself on the back. Do one of these victorious shakes. I don't know what you call this, but people do that sometimes. But you've done a good job. So take your break, get up, walk around, whatever, and then come on back and let's continue.

**译文**

你知道吗？阿尔伯特·爱因斯坦是个真实存在过的人。一直以来，我以为他只是个理论物理学家。好了，现在正是休息的好时机。我觉得我们到目前为止所做的工作相当不错。你应该给自己点个赞。来一个这种胜利的庆祝动作。我不知道这个动作叫什么，但人们有时就是这么做的。不过你干得确实不错。所以，去休息一下吧，站起来，走动走动，随便做点什么，然后再回来，我们继续。

## 67. 30. Intro to Querying Data

**原文**

Let's query some data finally finally we can pull up the real app and start talking to our database So first before we do that as we're going to be migrating from our existing in-memory database into our new database that is actually from like the real database and so here if I go to Cody's notes and I go to the first one you'll notice it's actually already gone and that's because I Have deleted that note from the in-memory database, but it's showing up in here

**译文**

最后，我们终于可以查询一些数据，调出真正的应用程序，并开始与我们的数据库进行交互。首先，在我们这样做之前，我们需要从现有的内存数据库迁移到新的数据库，而这个新数据库实际上来自真正的数据库。所以，如果我这里进入 Cody 的笔记，然后查看第一条笔记，你会发现它实际上已经不见了，这是因为我已经从内存数据库中删除了这条笔记，但它现在却在这里显示出来了。

## 68. 31. Connecting to a Real Database with Prisma and SQLite

**原文**

We're finally able to actually start working in our app again. So we still have our in-memory database. That's like still a thing that's happening here. But now we can actually start working with the real data in our database that we've just created with SQLite. So we are going to be migrating over time. It's going to be kind of funny, but we want to start with creating our Prisma client so that we can start interacting with that database. So you're going to be working in the

**译文**

我们终于又可以开始在我们的应用中实际工作了。因此，我们仍然保留着内存数据库。这仍然是当前正在运行的一个部分。但现在，我们终于可以开始使用通过 SQLite 刚刚创建的数据库中的真实数据了。所以，我们将逐步进行迁移。这会有点有趣，但我们希望从创建 Prisma 客户端开始，以便能够开始与该数据库进行交互。因此，你将要在以下位置进行操作：

## 69. 32. Optimizing Prisma Client for Efficient Database Operations

**原文**

We've actually already done a little bit with the Prisma client. If you recall in the seed script, we created a new Prisma client there. So you might think, well, okay, so that's just as easy as export, const Prisma, Prisma client. And then of course we need to bring that Prisma client in. And that would be the case except for the fact that we have HMR going on and HDR, that's hot data reloading or revalidation. And what that means is when we make server side changes, we don't shut down the server and then start it up.

**译文**

我们其实已经对 Prisma 客户端做了一些初步操作。如果你还记得，在种子脚本中，我们在那里创建了一个新的 Prisma 客户端。所以你可能会想，好吧，那不就是像 `export const Prisma = new PrismaClient()` 这么简单吗？然后当然我们需要引入这个 Prisma 客户端。如果不是因为我们有 HMR（热模块替换）和 HDR（热数据重载或重新验证）在运行，那确实就是这样。这指的是当我们在服务器端进行修改时，并不会先关闭服务器然后再重新启动它。

## 70. 33. Transitioning to Real Database with Prisma API

**原文**

Right now on this page, we're loading our data from our in-memory database. We want to start loading it from the real database and the user avatar would actually show up when you're done. So there's actually not a whole lot to do. We're just switching from one database to another, but you're going to be actually querying the real database using Prisma APIs. So you may need to take a look at some of the docs and stuff, how to do that efficiently and make sure that you include your select statement because you don't want to include all of the user data, just the data that's relevant for this page.

**译文**

目前在这个页面上，我们是从内存数据库加载数据的。我们希望开始从真实的数据库加载数据，这样在加载完成后，用户头像就会实际显示出来。因此，实际上需要做的事情并不多。我们只是从一种数据库切换到另一种数据库，但你将实际使用 Prisma API 来查询真实数据库。因此，你可能需要查看一些文档等资料，了解如何高效地执行此操作，并确保你只包含必要的 `select` 语句，因为你不想加载所有用户数据，而只加载与此页面相关的数据。

## 71. 34. Using Prisma to Retrieve User Data from a SQLite Database

**原文**

Let's go to our username and here we're going to swap out our in-memory database for our Prisma actual SQLite database. So Prisma and so now we're going to say Prisma, and this is async now. So we're going to add a wait, Prisma user, and we're going to do find unique because we have that unique constraint. We are still going to keep a warehouse. So it is a little bit similar. But instead of this equals thing, we're just going to say where the username is equal to

**译文**

让我们转到我们的用户名，这里我们将把内存数据库替换为实际的 Prisma SQLite 数据库。所以使用 Prisma，现在我们要写 Prisma，而且现在是异步的。因此我们要加上 await，使用 Prisma user，并且要执行 findUnique，因为我们有一个唯一性约束。我们仍然要保留一个仓库。所以结构上有些相似。但不再是这种等于号的形式，我们直接写 where 条件，让 username 等于

## 72. 35. Database Queries and Migrating to Prisma

**原文**

So on the notes page right here, we are actually making multiple queries from our in-memory database right now. That's why Kodi's image isn't loaded properly. And one of those is to query the owner, and then the other is to query the notes. I want you to combine these into a single query so that we have that optimization there. That would be nice. And of course, to migrate this over to Prisma. That way we load the proper stuff from the real database. So go ahead and give that a whirl. We'll see you when you're done.

**译文**

那么，就在当前的这个笔记页面，我们目前实际上正在从内存数据库中执行多个查询。这就是为什么 Kodi 的图片无法正常加载的原因。其中一个查询是获取所有者信息，另一个则是获取笔记内容。我希望你将这两个查询合并为一个，从而实现优化。这样会好很多。当然，我们还需要将这部分逻辑迁移到 Prisma 上。这样一来，我们就能从真正的数据库中加载正确的数据了。所以，现在就开始动手试试吧。等你完成后再见。

## 73. 36. Efficient Data Retrieval with Prisma and Subselects

**原文**

Let's start out by swapping this with Prisma and then we're going to say await, Prisma, user find first. No, not find first anymore. This is find unique. And then that needs to change the syntax a little bit because our Prisma query engine is a little bit different. And then we want to select the notes for this user. So we're going to say select. And here we're going to have a couple of

**译文**

让我们先把它换成 Prisma，然后我们会写 await Prisma.user.findUnique。不，不再是 findFirst 了，这次是 findUnique。然后语法需要稍微调整一下，因为我们的 Prisma 查询引擎略有不同。接着我们想为该用户选择笔记。所以我们会写 select。这里我们会有几个

## 74. 37. Dad Joke Break Querying Data

**原文**

Why do we tell actors to break a leg? Because every play has a cast! Ha ha ha! Yeah, that definitely definitely qualifies as a dad joke. There you go. So well done on that exercise. This is a lot of work and so you need to take a lot of breaks. Your brain needs it. It's learning is hard. If it's not hard or somebody tells you it's not hard, they are misleading you because it is absolutely a lot of work. And so you've got to stop, take breaks, write down notes,

**译文**

我们为什么要祝演员“Break a leg”（祝你好运）呢？因为每出戏都有一个“cast”（演员阵容）！哈哈哈！没错，这绝对绝对算得上是一个“老爸式笑话”了。就是这样。所以，你刚才那个练习完成得很好。这需要付出很多努力，因此你需要经常休息一下。你的大脑需要休息。学习的过程很辛苦。如果有人说学习不辛苦，那他们就是在误导你，因为这绝对是需要付出大量努力的。所以，你必须停下来，多休息，记下一些笔记，

## 75. 38. Intro to Updating Data

**原文**

We're going to make it so that you can delete records and you can update records and do all sorts of things to all these records when it's working with Prisma. And that is definitely something that we want to do. We don't want to continue working with our in-memory database thing. So in databases with SQL, you have a couple mechanisms for making mutations. So you have insert into table name and then the columns you want to update and here are the values. There's a little level of indirection here.

**译文**

我们将实现删除记录、更新记录以及对这些记录执行各种操作的功能，当它与 Prisma 配合使用时。这绝对是我们想要实现的功能。我们不想继续使用那种基于内存的数据库。在 SQL 数据库中，你有几种机制可以执行变更操作。比如，你可以使用 `insert into` 加上表名，然后指定要更新的列以及对应的值。这里存在一定程度的间接性。

## 76. 39. Mutating Data with Prisma

**原文**

Let's make this delete button actually work. So we're loading the data properly, but when we delete, it does redirect us, but that data is not actually deleted because we're just deleting it from the in-memory database. You need to do this mutation to the actual database. This one's going to be pretty simple. It's a pretty quick one. But the next steps in this exercise will be a little bit more on the complicated side. So we're going to throw you a softball for this one to do your first mutation with Prisma.

**译文**

我们来让这个删除按钮真正发挥作用。目前我们正确加载了数据，但当我们执行删除时，虽然页面会跳转，但数据并未真正被删除，因为我们只是从内存数据库中删除了它。你需要对实际的数据库执行这个突变操作。这个步骤会相当简单，处理起来也很快。不过，接下来练习中的步骤会稍微复杂一些。因此，这次我们会给你一个“软球”（简单任务），让你用 Prisma 完成第一次突变操作。

## 77. 40. Deleting Data with Prisma

**原文**

Like I said, it's going to be kind of easy. So once you know ID here, come down to delete. And instead of DB, it's going to be Prisma. And you're going to wait. And we're going to use the syntax or the API from Prisma here. And that's it. We're done. We can remove the DB from here now. And now delete will work. Boom, it's gone. Awesome. So that is delete with Prisma. You literally just say Prisma. Here's my model that I want to delete from

**译文**

如我所说，这会相当简单。所以一旦你知道了这里的 ID，就往下找到 delete。然后，这里不再是 DB，而是 Prisma。接下来你需要等待一下。我们将使用 Prisma 的语法或 API。就这样，大功告成。现在我们可以把这里的 DB 移除了。现在 delete 就能正常工作了。砰，它不见了。太棒了。这就是使用 Prisma 进行删除操作。你只需要直接说 Prisma，然后指定你想要从中删除的模型即可。

## 78. 41. Updating Page Mutations for Images and Notes with Efficient Cache Control

**原文**

Now we want to be able to update this page so that those mutations will go through. This one's a little bit more complicated though because we do have the note, but we also have all these images and you can delete images, you can add images, you can update images. So there's a fair bit of challenge with this one, but it's going to be fun. We're going to be doing a couple mutations as part of this and I think you're going to have a good time. The one thing that I'm going to call out for you for this first step of the exercise that may be a little bit confusing,

**译文**

现在我们希望这个页面能够被更新，以便这些变更能够生效。不过，这一部分要稍微复杂一些，因为我们不仅有笔记内容，还有所有这些图片——你可以删除图片、添加图片，也可以更新图片。因此，这一部分确实存在相当大的挑战，但过程会很有趣。我们将在此过程中执行几项变更，我想你会玩得很开心。对于练习的第一步，有一件事我需要特别指出，因为它可能会让你感到有些困惑：

## 79. 42. Efficiently Updating and Deleting Data in a Form with Prisma

**原文**

All right, so let's uncomment this bit. This is just pulling stuff out of our form submission. And the first bit of this is pretty easy. We're going to await Prisma note update and where the ID matches the ID of that which is in the params, so that ID. And then we're going to pass as our data the title and the content. So whatever they passed that, that is the new title and content. So that's it for updating the note itself. That's pretty straightforward. We can be very excited.

**译文**

好的，那我们来取消注释这段代码。这段代码的作用就是从表单提交中提取数据。第一部分相当简单：我们将调用 `await Prisma note update`，并通过 `where` 条件匹配 `params` 中的那个 ID，也就是这个 ID。然后，我们将用户提交的标题和内容作为数据传进去。也就是说，用户提交的内容将成为新的标题和内容。这就是更新笔记本身的全部操作，过程非常直接。我们可以为此感到兴奋了。

## 80. 43. Implementing Transactions for Reliable Data Operations

**原文**

Let's say you're building a banking app and so you have this transaction thing, right? You've got one user over here and one user over here and they want to transfer money. So user one transfers money out of their account and then you're going to transfer money into user twos account, but then there's a failure. And so user one already lost the money and now you're stuck here holding money. Maybe that's actually fine. Just kidding. Unless you're a thief, don't do that. That's bad. So the problem is we need to have something, some sort of transaction that like

**译文**

假设你正在开发一个银行应用，所以你有一个这样的交易功能，对吧？你这边有一个用户，那边也有一个用户，他们想要转账。那么用户一会从自己的账户转出钱，然后你会把钱转入用户二的账户，但此时出现了一个故障。于是用户一已经失去了这笔钱，而你现在却卡在这里，钱被滞留了。也许这样其实也没关系——开个玩笑。除非你是小偷，否则可别这么做，那是很坏的行为。所以问题在于，我们需要有某种机制，某种能够确保交易……

## 81. 44. Implementing Transactions with Prisma for Atomic Database Operations

**原文**

This is a little bit easier and also a little bit trickier than you might expect. So the the easy part of it is we simply add prisma dot transaction and Copilot wants us to do the array syntax. I don't want to do that. We're gonna have an async function and it's gonna take an argument. I'm gonna call dollar prisma. This is how I can differentiate between the regular prisma and the transactional prisma. A lot of people will also use tx to represent a transaction, but I don't know dollar

**译文**

这比你想象的要简单一点，也有点棘手。简单之处在于，我们只需添加 `prisma.transaction`，而 Copilot 希望我们使用数组语法。我不想这样做。我们将创建一个异步函数，它会接收一个参数。我会将其命名为 `$prisma`。这样我就可以区分普通的 `prisma` 和事务性的 `prisma`。很多人也会使用 `tx` 来表示事务，但我不知道 `$`

## 82. 45. Optimizing Database Calls with Nested Queries in Prisma

**原文**

As cool as that transaction thing is, it actually would be even better to not make so many calls to the database and just let Prisma optimize the calls that are going to be made. And so we're going to use nested queries for our updates. It turns out you can actually take all four of the different things that we're doing with the database and put it all in a single query. So that is your task. And we actually, Kelly already got rid of the transaction stuff. So you don't need to worry about getting rid of that. Just update all those queries to be in a single one.

**译文**

虽然事务处理的功能很酷，但实际上，如果我们能减少对数据库的调用次数，并让 Prisma 自行优化将要执行的调用，效果会更好。因此，我们将使用嵌套查询来进行更新操作。事实证明，我们其实可以将当前对数据库执行的所有四种操作整合到一条查询中。这就是你的任务。另外，Kelly 已经移除了事务相关的代码，所以你不需要再处理这部分内容。只需将所有这些查询更新为一条即可。

## 83. 46. Efficient Database Updates with Prisma's Nested Queries

**原文**

Let's combine these queries. So right here we've got our note update. Let's do the delete many first. So we're going to add images. And here we'll have a delete many. And that's simply going to actually be very similar to this. So we just provide the where clause. And and that will be scoped to our particular note anyway. So we don't need to have the note ID here anymore. All we need is this part of the where clause. And look, that looks pretty darn familiar. Thanks, co pilot. And so we've taken care of the delete many.

**译文**

让我们把这些查询组合起来。那么，这里我们有一个笔记更新。我们先执行“批量删除”。所以我们要添加图片。然后这里我们会使用“批量删除”。实际上，这个操作会和这个非常相似。我们只需要提供 where 子句即可。而且无论如何，它的作用范围都会限定在我们特定的笔记上。所以我们这里不再需要笔记 ID 了。我们只需要 where 子句的这部分内容。瞧，这看起来相当眼熟。感谢，Co Pilot。这样我们就处理好了“批量删除”。

## 84. 47. Dad Joke Break Updating Data

**原文**

What do you call fake noodle and impasta? All right, that was a good exercise. It's time to take a break. So get up, get moving, write down the things that you learned so you don't forget about them, and go do something nice for somebody or I don't know, just make the world a better place. And then when you are all rested and ready to move on to the next, then come on back because I'll be ready for you and we can keep on going.

**译文**

你管“假面条”和“意面”叫什么？好吧，这真是一次不错的练习。现在是时候休息一下了。所以，站起来，活动一下，把你学到的东西记下来，以免忘记，然后去做一些好事，或者，我不知道，总之就是让世界变得更美好一点。等你休息好了，准备好继续学习下一个内容时，再回来吧，因为我会在那里等你，我们可以继续前进。

## 85. 48. Intro to SQL

**原文**

Even though we have an ORM, sometimes you need to reach in and do some raw SQL. So I have a real project and the search page is pretty complicated. There are a lot of filters and things. And this is a query from that real project that I've got. So we're selecting Starships and brand models and a bunch of other things. This is the search page that allows the user to say,

**译文**

尽管我们使用了 ORM，但有时你仍然需要直接编写原始的 SQL 语句。我有一个真实的项目，其搜索页面相当复杂，包含了许多筛选条件和其他元素。以下就是来自那个真实项目的一个查询语句。我们正在选择星舰、品牌型号以及许多其他内容。这个搜索页面允许用户输入：

## 86. 49. SQL Queries for User Search in Prisma

**原文**

We still have one more place where we're still using the in-memory database instead of the actual database, and that's our user search page. So that is your job. You need to add the SQL query that is going to search users. This is going to be a little bit more complicated because you can just use regular Prisma to query the way that we're doing, but our product manager has a couple of interesting requirements that they want us to do. So we're going to actually write raw SQL in this exercise.

**译文**

我们还有一个地方仍然在使用内存数据库，而不是真正的数据库，那就是我们的用户搜索页面。所以这就是你的任务。你需要添加用于搜索用户的 SQL 查询。这会稍微复杂一些，因为你本可以直接使用常规的 Prisma 来执行我们当前的查询方式，但我们的产品经理提出了一些有趣的额外要求。因此，在本次练习中，我们将实际编写原始的 SQL 语句。

## 87. 50. User Search with Prisma and SQL

**原文**

So this is our user index page. Let's pull that up. And we're going to swap out this get rid of that nonsense. And we'll come up here switch this for Prisma. And then we can say our users cost users equals await Prisma query raw. And here we go, we've got our raw query going. And what we're going to do is first select ID username and name from the table called user

**译文**

这就是我们的用户索引页面。我们来把它打开。然后我们要替换掉它，把那堆没用的东西删掉。接着我们到这里，把它换成 Prisma。然后我们可以写：我们的 users 常量等于 await Prisma.query.raw。好了，现在我们的原始查询已经运行起来了。我们要做的第一件事就是从名为 user 的表中选择 ID、username 和 name。

## 88. 51. Handling TypeScript Errors and Runtime Type Checking with Prisma and Zod

**原文**

So what are we going to do about these typescript errors? The problem is that data.users is, yeah, it's not available on here. The reason it's not available is because this is going to be unknown. We don't know what's going to come back from this Prisma query raw. There are query builders that you can use other tools to interact with your database that could definitely perform this type of a query and make it type safe. But there are a lot of trade-offs associated

**译文**

那么，我们该如何处理这些 TypeScript 错误呢？问题在于，是的，`data.users` 在这里不可用。它之所以不可用，是因为这个值将是 `unknown` 类型。我们不知道这个 Prisma 原始查询会返回什么内容。你可以使用其他查询构建器或工具来与数据库交互，这些工具当然可以执行这种类型的查询并确保类型安全。但这也伴随着许多权衡取舍。

## 89. 52. Runtime Type Checking and Parsing in Prisma with Raw Queries

**原文**

So let's make a schema for a individual user here, we're going to call this our user search results schema. And we'll just do an individual search results. So each one of these individual users, we're going to bring in Z from Zod. This is going to be an object. And it's going to have an ID, it's not a number copilot, I don't know why copilot really wants IDs to be numbers, but they're super duper not. And then we've got our username and our name is nullable, because our name is

**译文**

那么，我们来为单个用户创建一个模式，我们将其称为用户搜索结果模式。我们直接创建一个单个搜索结果即可。对于每个这样的单个用户，我们将从 Zod 中引入 Z。这将是一个对象。它将包含一个 ID，它不是数字——Copilot，我不知道为什么 Copilot 总想把 ID 设为数字，但它们绝对不是数字。然后我们有用户名和姓名，其中姓名可以为空，因为我们的姓名是

## 90. 53. Working with Joins in SQL

**原文**

For this next exercise, we want to display the user's profile photo and that information is stored in a different table. So we're not going to get it from the user. We need to somehow get this other table in the same query. Now, we could do a separate query and say, OK, select all the user's images that match and that would be highly inefficient. I do not recommend this. And so what we're going to need to do is what's called a join in SQL. And so let's talk about joins. When I was looking for something

**译文**

在接下来的练习中，我们希望显示用户的头像照片，而该信息存储在另一个表中。因此，我们无法从用户那里直接获取。我们需要在同一个查询中 somehow 获取这个其他表。现在，我们可以执行一个单独的查询，例如选择所有匹配的用户图片，但这种方式效率非常低，我不推荐这样做。因此，我们需要在 SQL 中使用一种称为“连接”（join）的方法。下面我们来谈谈连接。当我在寻找某个东西时

## 91. 54. Left Joins with Prisma and SQLite

**原文**

Alright, so let's add our image ID to our Zod schema first. And then we'll come down to our UI and account for that. So now it's no longer a image object that's on the user. That is a little bit trickier to do with Ross equal, we're just going to do it as a property on the result. And so it's going to be called image ID. If I save that, we're going to get a parsing error because our query doesn't support the image ID yet. So now we're going to add our left join, we're going to left join the user table on the

**译文**

好的，我们先在 Zod 模式中添加图片 ID。然后我们会转到 UI 部分来处理这个新增字段。现在用户对象上不再是图片对象了。用 Ross equal 实现这一点稍微有点复杂，我们直接将其作为结果中的一个属性来处理。这个属性将命名为 image ID。如果我保存这个改动，我们会得到一个解析错误，因为我们的查询目前还不支持 image ID。接下来我们要添加左连接，对用户表执行左连接，连接条件为

## 92. 55. Sorting Users by Recent Entry with Raw SQL

**原文**

Well, now our product manager is doing the product manager thing and wants to make sure that these users are sorted by their recent activity. And we determined recent activity based on how recently they updated any of their notes, right? So we need to have some sort of way to sort these users by the notes that they are taking and when they've last updated their note, which adds a fair bit of complexity to our query. But

**译文**

嗯，现在我们的产品经理正在履行产品经理的职责，希望确保这些用户能按照他们的近期活动进行排序。而我们判断近期活动的依据是，用户最近一次更新其任意笔记的时间，对吧？因此，我们需要一种方法来根据用户正在记录的笔记以及他们上次更新笔记的时间来对用户进行排序，这给我们的查询带来了相当大的复杂性。但是

## 93. 56. Leveraging AI Assistance for Writing SQL Queries

**原文**

So there have been a couple of times as we've been working that I've used an AI assistant to help me fill out the different bits of code and things and I've had to correct it sometimes for some reason it really wants my IDs to be numbers for example. But for the most part it's actually super duper helpful and I want you to use AI assistance in your programming as well. So we're going to use an AI assistant to help us write this order by. So I'm going to copy this I'm going to pull up GitHub co-pilot in VS code. I'm going to say I need to fill in this

**译文**

在我们工作的过程中，有好几次我都使用 AI 助手来帮助我补全代码的各个部分，但有时我不得不对其进行修正，因为不知何故，它总是希望我的 ID 是数字。不过总体而言，它真的超级有用，我也希望你在编程时同样使用 AI 助手。因此，我们将借助 AI 助手来完成这个 `order by` 的编写。现在我要复制这段代码，然后在 VS Code 中打开 GitHub Copilot，接着告诉它我需要补全这里的内容。

## 94. 57. Dad Joke Break SQL

**原文**

What kind of dinosaur loves to sleep? A stegocenorus. Haha, I gotta tell my kid that one. My son really likes dinosaurs, or at least he used to. He's growing, you know. He just learned how to do a backflip yesterday on the trampoline by himself. It's awesome. Proud of him. So I'm gonna tell him that he's awesome and also tell him this joke. And you should tell somebody this joke because it's great. Connect with somebody. This is a good time to take a break and go do that and then come back and let's keep going.

**译文**

哪种恐龙喜欢睡觉？是“腕龙鼾龙”（stegocenorus）。哈哈，我得把这个笑话告诉我孩子。我儿子特别喜欢恐龙，或者至少以前是这样。他正在长大，你知道的。昨天他刚自己学会在蹦床上后空翻。太棒了。我为他感到骄傲。所以我要告诉他他很棒，还要把这个笑话告诉他。你也应该把这个笑话讲给某个人听，因为它真的很棒。跟别人建立连接吧。现在正是休息一下、去做这件事的好时机，然后再回来，我们继续。

## 95. 58. Intro to Query Optimization

**原文**

We're going to optimize the query that's on this page. So we're going to add just a silly number of users to our database, and we're going to figure out how to optimize that query. We're also going to be optimizing queries in general by adding some foreign key indexes that you probably be doing by default. But first, let's talk about optimization of queries. So people have this choice of spending a ton of money on hardware and caching to make things fast.

**译文**

我们将优化这个页面上的查询。为此，我们会向数据库中插入一个夸张数量的用户，然后找出优化该查询的方法。我们还将通过添加一些外键索引来优化各类查询——这些索引你通常应该默认就配置好。不过，首先我们来谈谈查询优化。人们通常有两种选择：一种是投入大量资金购买硬件和缓存系统来提升速度。

## 96. 59. Optimizing Query Performance with Indexes in Prisma

**原文**

For this exercise, we're going to be optimizing a query of the notes by a owner ID. And you're going to be adding an index for foreign keys to all of the models that have foreign keys, where those foreign keys are not unique. If they're unique, they already have an index that was created for us by Prisma. But if they're not unique, then we need to add an index. So your job is to first understand what's going on. And so you're going to be using explain query, whether that's using

**译文**

在本练习中，我们将优化通过所有者 ID 查询笔记的查询。你需要为所有包含非唯一外键的模型添加索引。如果外键是唯一的，Prisma 已经为我们创建了索引；但如果外键不唯一，我们就需要手动添加索引。因此，你的首要任务是理解当前的情况。为此，你将使用 `explain query`（无论是通过哪种方式）。

## 97. 60. Optimizing Database Queries with Indexes

**原文**

So I'm going to use the CLI will say SQLite 3 and point it to Prisma data DB. And then I'll paste in our explain query. And here's that explain query plan select star from note where owner ID equals one. And our query plan is to scan the note. So scans not always a terrible thing like it's not instantly Oh, it's a scan. It must be bad. But as in our particular case, we're going to be getting lots and lots of notes. And so if anytime we wanted to find the note for a single

**译文**

所以我将使用 CLI，输入 `SQLite 3` 并将其指向 Prisma 数据数据库。然后我会粘贴我们的解释查询。这就是那个解释查询计划：`SELECT * FROM note WHERE owner_id = 1`。我们的查询计划是扫描 `note` 表。扫描并不总是件坏事，比如不能立刻就说“哦，这是扫描，肯定不好”。但在我们当前的情况下，我们将获取大量笔记。因此，如果我们任何时候想查找单条笔记时

## 98. 61. Optimizing User Search Query Performance with Indexing

**原文**

I'm on my user search page and if you notice when I refresh this is taking like longer than you might expect. And that's because I filled my database with a ton of users. We can take a look at our logs here. We'll see that these queries are taking 900 milliseconds to run this query. What is happening? This is so bad. So what I did was we're projecting ourselves out into the future a little bit. And you can feel free to do this as well if you like. Just keep in mind it takes a little while to seed the database with this.

**译文**

我正在我的用户搜索页面，如果你注意到的话，当我刷新这个页面时，它花费的时间比预期的要长。这是因为我的数据库中填充了大量的用户。我们可以看看这里的日志。我们会发现这些查询需要 900 毫秒才能执行完。到底发生了什么？这情况太糟糕了。所以我做的方法是，我们稍微把时间线投射到未来一点。如果你愿意，也可以随意这样做。只是要注意，用这些数据填充数据库需要花费一些时间。

## 99. 62. Query Performance with Indexes in SQLite

**原文**

To be able to optimize this query, we need to explore it a little bit and have SQLite explain this to us. So I'm going to run SQLite 3 on my Prisma data DB file, and I'm going to copy the explain query plan from the instructions. So we have explained query plan. Here's our query. We filled it in with some pre-filled values. And here's the query plan that SQLite is planning on for this particular query. So let's

**译文**

为了能够优化这个查询，我们需要对它进行一些探索，并让 SQLite 为我们解释查询过程。因此，我将针对我的 Prisma 数据数据库文件运行 SQLite 3，并从说明中复制该解释查询计划的命令。现在我们有了查询计划。这是我们的查询语句，我们已经用一些预填充的值进行了填充。而这就是 SQLite 针对这个特定查询所规划的查询计划。那么，让我们……

## 100. 63. Dad Joke Break Query Optimization

**原文**

What did the doctor say to the gingerbread man who broke his leg? Try icing it. Haha. Actually, I'm kind of could go for a gingerbread man with icing on after that exercise. So now is a great time to get up and take a break and make sure you write down the stuff that you learned so that doesn't just like fall right out of your head because that does happen. So you do need to find some mechanism for solidifying the things in your mind that you are learning. So yeah, writing it down.

**译文**

医生对摔断腿的姜饼人说了什么？试试用糖霜敷一下吧。哈哈。其实，做完那些练习后，我现在还真想来一个带糖霜的姜饼人。所以现在正是起身休息一下的好时机，一定要把你学到的东西记下来，不然它们可就会从脑子里溜走——这种情况真的会发生。所以，你需要找到一种方法来巩固你正在学习的内容。没错，就是把它写下来。
