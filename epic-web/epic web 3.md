# Kent C. Dodds - Epic Web. Ship Modern Full-Stack Web Applications part3

- 来源：[B站 BV1ajVxzyEDm](https://www.bilibili.com/video/BV1ajVxzyEDm)（up 主：lmt831，共 100 P）
- 说明：英文转录 + 中文翻译（机器翻译，仅供学习参考）

---

## 01. 64. Outro to Data Modeling Deep Dive Workshop

**原文**

Hey, great job. You should feel really proud of yourself. Like, look at this cool app that we've been working on. You've done such an awesome job making all of this stuff work just so beautifully. Well done. You should feel proud of yourself. Go tell somebody about this cool thing that you've built. Show it off to them and feel like you're just on top of the world because you are. You've done a great job. Keep up the good work and yeah, we'll look forward to seeing you in the next workshop. See ya.

**译文**

嘿，干得真棒。你应该为自己感到特别自豪。快看看我们一直在开发的这个酷炫应用吧。你把所有东西都配合得如此完美，表现得真是太出色了。干得漂亮。你应该为自己感到骄傲。快去告诉别人你打造的这个酷东西吧。向他们展示一下，让自己感觉仿佛登上了人生巅峰，因为你确实做到了。你干得非常出色。继续保持这种势头，我们期待在下一期工作坊再见到你。回头见。

## 02. 01. Intro to Authentication Strategies & Implementation Workshop

**原文**

All right, folks, hold on to your hats. We're going to do web authentication. And look at how many things there are. Oh, it's so much. Some people would look at this list and they'd say, you know what? That's why you use a third-party service to manage authentication for your application. I've got two responses to that, or three maybe. One, yeah, you might be right. Depending on how important it is for you to ship quickly and everything, it might be nice to just offload all these concerns to somebody else.

**译文**

好了，各位，请坐稳了。我们接下来要讲的是 Web 身份验证。看看这里有多少内容吧。哦，内容真多。有些人看到这个列表可能会说，你知道吗？这就是为什么你应该使用第三方服务来为你的应用管理身份验证。对此我有两个回应，或者可能是三个。首先，是的，你说的可能有道理。根据你是否需要快速上线等因素，把这些事情都交给别人来处理或许是个不错的选择。

## 03. 02. Intro to Cookies

**原文**

We're going to talk about cookies, and we're finally going to get dark mode on our app. Isn't that wonderful? And it's awesome, actually. We're going to be doing optimistic UI. So our theme requires some server side interaction to get server rendering of our theme. And you'll notice we're on a slow 3G network, but it is still lining fast. So how are we doing this? That's what we're going to be learning about cookies, rock. So first, I'm going to talk a little bit about the history of cookies. And then we'll talk about GDPR.

**译文**

我们来聊聊 Cookie，并且终于要在我们的应用中实现深色模式了。是不是很棒？实际上，这真的很酷。我们将要使用乐观 UI。因此，我们的主题需要一些服务器端交互来实现主题的服务器端渲染。你会注意到我们使用的是缓慢的 3G 网络，但页面仍然加载得很快。那么，我们是如何做到这一点的呢？这正是我们将要学习的 Cookie 相关内容。首先，我会简单介绍一下 Cookie 的历史，然后我们再聊聊 GDPR。

## 04. 03. Implementing Theme Switching with Conform and UseFetcher

**原文**

All right, we've got a theme switch finally, but every time I click on it, nothing's happening. The network tab's not submitting even though it's in a form. And the reason is because this is managed by Conform. So let's take a look at that. Right here is our theme switch. This is being rendered inside of our home page or our root component here in the footer. And we're passing along the user preference. We haven't actually set that to anything yet, so it does fall back to light. And we have two options. We have light mode and dark mode.

**译文**

好的，我们终于有了主题切换功能，但每次点击它时，都没有任何反应。即使它在一个表单中，网络标签页也没有提交数据。原因在于这是由 Conform 管理的。所以我们来看一下。这里就是我们的主题切换器。它是在我们的主页或根组件的页脚中渲染的。我们传递了用户偏好设置，但目前还没有将其设置为任何值，所以它会回退到浅色模式。我们有两个选项：浅色模式和深色模式。

## 05. 04. Creating a Theme Switcher with Form Submission and Fetcher in React

**原文**

Our first step here is going to be making it so that we actually render the theme that the user wants to have set in our form. So we're going to render a hidden input. So input type is hidden and the name is going to be theme and the value will actually be the next mode. So the value will be the value the user wants to set their theme to. That next mode is going to come from right here. So our next mode will be the opposite of the current mode. So here we're actually going to leave that comment

**译文**

我们的第一步是实现在表单中渲染用户希望设置的主题。为此，我们将渲染一个隐藏输入框。输入框的类型为 hidden，名称为 theme，其值将是 next mode。也就是说，该值就是用户希望设置的主题值。这个 next mode 的值将直接来源于此处。因此，我们的 next mode 将是当前模式的相反值。这里我们暂时保留该注释。

## 06. 05. Adding User Preference for Dark Mode

**原文**

So the app already does have the ability to have a dark mode. We just need to control the class and poof, it turns into dark mode. So what you need to do is handle the wiring of the cookie so that we can preserve the user's preference between light and dark mode. And then once we are updating that cookie based on clicking on this, then we should be able to wire that into the class name on the HTML element. So that's what you're going to be doing in this one.

**译文**

因此，该应用实际上已经具备深色模式的功能。我们只需控制类名，然后“啪”的一声，它就会切换为深色模式。所以，你需要做的是处理 Cookie 的绑定逻辑，以便在用户切换浅色和深色模式时能够保存其偏好设置。一旦我们根据用户的点击操作更新了该 Cookie，就应该能够将这一状态同步到 HTML 元素的类名上。这正是你在本次任务中要完成的工作。

## 07. 06. Implementing Cookies for Theme Selection

**原文**

So actually, I'm going to take things a little differently than what I had you do in the exercise because I want to kind of iteratively get to the point where we have this cookie happening. So we are going to go to our route. We're going to go to the action that's handling this form submission. And I'm going to add a set cookie header right here that says set cookie and the value is going to be theme equals dark. And if I come over to my network, we clear this out and I click on this, then we're

**译文**

所以实际上，我打算采取一种与练习中略有不同的方式，因为我希望逐步实现这个 Cookie 功能。因此，我们将前往路由，找到处理表单提交的 Action，然后在这里添加一个 Set-Cookie 标头，其值为 theme=dark。如果我切换到网络面板，清空内容然后点击这个按钮，那么我们就

## 08. 07. Implementing Optimistic UI for Theme Switching

**原文**

One of the drawbacks of our approach of requiring a network request to change the user's theme is that if their network is slow, their theme change is going to be slow. So let's go to a slow 3G. This is something that you just cannot control as a web developer. You don't get to control the user's network speed. So if I click on this, we're going to be waiting around for a little while before the request response finishes and now we get our theme. That is super duper not cool. Not a fan of that at all.

**译文**

我们这种方法的一个缺点是，每次更改用户主题都需要发起网络请求。如果用户的网络很慢，那么主题切换也会很慢。现在我们切换到慢速的 3G 网络。作为 Web 开发人员，你根本无法控制这一点——你无法掌控用户的网络速度。所以，如果我点击这里，我们就得等上一小会儿，直到请求响应完成，然后才能加载主题。这真的非常非常糟糕。我一点都不喜欢这样。

## 09. 08. Implementing Optimistic UI with Remix

**原文**

Let's get optimistic. So we're going to go to our root and right above the theme switch, we're going to make a function called use theme. And this is going to manage all of our optimistic UI stuff that we're going to be doing. So the idea here is we need to know what the user is submitting from this fetcher. So we can say fetcher dot form data dot get theme, right. And it's saying form data may not be defined because it it's possible that we're not submitting anything. So we can just add this. And so

**译文**

让我们保持乐观。所以我们要进入根目录，在主题切换按钮的正上方，创建一个名为 `useTheme` 的函数。这个函数将管理我们接下来要做的所有乐观 UI 相关逻辑。这里的核心思路是：我们需要知道用户通过 `fetcher` 提交的内容是什么。因此，我们可以这样写：`fetcher.formData.get('theme')`。但这里会提示 `formData` 可能未定义，因为我们有可能没有提交任何内容。所以我们可以直接添加这个判断。因此

## 10. 09. Dad Joke Break Cookies

**原文**

I dreamed about drowning in an ocean made of orange soda last night. It took me a while to work out. It was just a fantasy. Some of these are actually pretty, pretty clever. That one is one of those. Also terrifying. Some of these are very terrifying. All right, well done. This is a good time to take a break, get a drink of water and move on with your life. Do something for a second and then come on back because we got so much stuff to learn. So let's get back to it when, you know,

**译文**

昨晚我梦见自己沉入一片由橙味汽水构成的海洋中。我花了好一会儿才反应过来。那不过是一场幻想罢了。其中一些其实真的、真的挺巧妙的。那个就是其中之一。同时也挺吓人的。有些真的非常吓人。好了，干得不错。现在正是休息一下、喝杯水、继续过你生活的好时机。先去做点别的事情，然后再回来，因为我们还有好多东西要学。那么，等你准备好了，我们就继续吧。

## 11. 10. Intro to Session Storage

**原文**

Let's get into session storage. This is where we're going to start getting into a little bit of actual auth stuff. But this is another one of those underlying technologies that auth really relies on is session storage in the cookie. So cookies can be configured in a variety of ways. And three of them that are very important for auth are that the cookie is only accessible via HTTP. That means that only the browser has access to it. And it does not share that with any client-side JavaScript. And then it sends that cookie over.

**译文**

我们来了解一下会话存储。从这里开始，我们将真正涉及一些实际的认证相关内容。但这也是认证所依赖的一项底层技术——即存储在 Cookie 中的会话存储。Cookie 可以通过多种方式进行配置。其中三种对认证非常重要的方式是：Cookie 仅可通过 HTTP 访问。这意味着只有浏览器才能访问它，而不会与任何客户端 JavaScript 共享该 Cookie。然后，该 Cookie 会被发送出去。

## 12. 11. Toast Messages with Cookies

**原文**

So next we want to be able to show the user a toast message when they delete a note, for example. So if we go to root.tsx, we've got this new show toast thing. And we have also this toaster that was built for us by Kelly. So thank you, Kelly, the coworker. So the show toast allows us to call the show toast utility from this package that we're using. And if I come over here to this, let's just test this out to see what that looks like.

**译文**

接下来，我们希望能够在用户删除笔记时，向他们显示一个提示消息。例如，如果我们进入 root.tsx 文件，就会发现这里多了一个新的“显示提示”功能。此外，还有一个由 Kelly 为我们构建的提示框组件。所以，感谢我的同事 Kelly。这个“显示提示”功能让我们能够调用我们正在使用的这个包中的提示工具。现在，让我到这里来，我们测试一下，看看效果如何。

## 13. 12. Configuring Cookie Session Storage for Toast Messages

**原文**

We're going to manage this cookie in a utils. So let's come to our utils. We're going to make a new one called toast dot server dot ts. And in here, we're going to be using a create session cookie session storage from remix run node. And this is going to get us our toast session storage. We're going to export that. And here, we're going to configure our cookie with a couple of options. So we want the name to

**译文**

我们将在一个 utils 中管理这个 cookie。因此，我们来到 utils 文件夹。我们将创建一个新的文件，命名为 toast.server.ts。在这里，我们将使用来自 remix run node 的 createSessionCookie 和 sessionStorage。这将为我们提供 toast 的 sessionStorage。我们将将其导出。然后，我们将通过几个选项来配置我们的 cookie。我们希望名称为

## 14. 13. Adding Toast Notifications to Delete Functionality

**原文**

All right, now we're going to be able to get to one of these and hit delete and it should pop up a toast message. So what's involved here is going to the route that has the delete, the action that actually deletes the note. And then you're going to be using that toast session storage that you just created to set a toast message value in there and use that to create a cookie value, a set cookie header that you will send with the response. And then in your root loader, you're going to look for that cookie

**译文**

好的，现在我们将能够访问其中一个并点击删除，此时应该会弹出一个“toast”消息。这里涉及的操作是：前往包含删除功能的路线，即实际执行删除笔记的操作。然后，你将使用刚才创建的“toast”会话存储，在其中设置一个“toast”消息值，并利用该值创建一个 Cookie 值，即“Set-Cookie”标头，随响应一同发送。接着，在你的根加载器中，你将查找这个 Cookie。

## 15. 14. Managing Toast Messages with Cookie Sessions

**原文**

So to be able to get a toast message when I delete this, I need to go to the place that is responsible for deleting that. And that happens to be in our note ID route. And in here, what we're going to do is read the current state of our toast session storage cookie, and then set the value there. So here, to read the current state, we're going to go grab our cookie header from request.headers.getCookie. And that's all web standard stuff, request headers, that's standard web stuff, which

**译文**

因此，为了在删除此内容时能够收到一条提示消息，我需要前往负责删除该内容的地方。而这个地方恰好位于我们的 note ID 路由中。在这里，我们要做的是读取当前 toast 会话存储 cookie 的状态，然后设置其值。所以，为了读取当前状态，我们需要从 `request.headers.getCookie` 中获取 cookie 标头。这些都是标准的 Web 内容，`request.headers` 就是标准的 Web 内容，它

## 16. 15. Improving Note Deletion Functionality with Multiple Cookies

**原文**

I don't know a single product manager that would be okay with this problem as soon as you delete a note. You'll never hear the end of it. Yeah, not okay. So we're going to fix that. It is simpler and more complicated than you might think, but it's not a very big step of the exercise and just a couple pieces to change. We are going to be bringing in a utility because we're going to need to set two cookies at the same time. And you definitely can do that and we'll see how to do that in this exercise.

**译文**

我认识的产品经理中，没有一个会在你删除笔记后对这个问题表示接受。他们会一直跟你没完没了地抱怨。是的，这绝对不行。所以我们要解决这个问题。它比你想象的要简单，同时又更复杂一些，但这并不是一个很大的改动步骤，只需要修改几个部分。我们将引入一个工具，因为我们需要同时设置两个 Cookie。你当然可以做到这一点，我们将在本练习中看看具体该如何操作。

## 17. 16. Efficiently Updating and Serializing Cookies

**原文**

So let's go to our root and we'll come down here to our loader where we are loading the toast and we need to add the unset. So let's say toast cookie session unset toast and that might seem like all you need to do but we actually need to let the browser know that we no longer want this toast property inside that cookie. Now of course the browser doesn't know that there's a toast property all the browser sees is this big long weird string. We need to serialize

**译文**

那么，我们进入根目录，然后向下找到加载 toast 的加载器部分，我们需要添加 unset 操作。比如写成：toast cookie session unset toast。这看起来似乎就是你需要做的全部了，但实际上我们还需要让浏览器知道，我们不再希望这个 toast 属性保留在该 cookie 中。当然，浏览器并不知道存在一个 toast 属性，它看到的只是一个又长又奇怪的字符串。我们需要进行序列化。

## 18. 17. Implementing Flash Messages for Temporary Notifications

**原文**

Remembering to do the unset and everything is probably unnecessary for a toast because a toast is kind of like a flash in the pan, right? Like it's just a thing that happens in the instant and then it should be gone. And that's actually a pretty common pattern. In fact, it's so common that it's been encoded into a bunch of different libraries that help you manage sessions like this one. And so your responsibility is to switch from the set and get process to a flash and get, which is

**译文**

记住执行 unset 操作以及所有相关步骤，对于 toast 来说可能并不必要，因为 toast 有点像转瞬即逝的东西，对吧？它只是在某个瞬间发生，然后就应该消失。这其实是一种非常常见的模式。事实上，它已经变得如此普遍，以至于被编码进了许多不同的库中，这些库可以帮助你管理像这样的会话。因此，你的责任就是从“设置并获取”的流程切换到“瞬时获取”的流程，即

## 19. 18. Efficiently Removing Toast Messages with Flash API

**原文**

So this one's a pretty quick one. We just need to switch our get call that we did right here or our set call to flash. And now the next time that a get is called for toast, it will automatically be unset. So let's come over here to our route where we are doing that get call. And we can remove the unset. And that's it. We do still need to set the cookie. The browser needs to be made aware of the change in this session storage. But that's it. So I can come over here, hit

**译文**

所以这个改动相当简单。我们只需要将刚才这里的 get 调用（或者 set 调用）改为 flash 即可。这样下次当有人调用 toast 的 get 时，它会自动被取消。那我们来到执行这个 get 调用的路由处，把 unset 移除掉，就完成了。我们仍然需要设置 cookie，因为浏览器需要知道这个 session storage 的变化。但仅此而已。所以我现在可以来到这里，执行

## 20. 19. Dad Joke Break Session Storage

**原文**

What's the leading cause of dry skin? Towels! All right, well, that actually maybe you should go for a swim really quick. This is a good time to take a break and let your brain kind of think about the things that you just learned and then come on back because we got stuff to learn.

**译文**

导致皮肤干燥的首要原因是什么？毛巾！好吧，也许你现在真的应该赶紧去游个泳。现在正是休息一下的好时机，让你的大脑思考一下你刚刚学到的内容，然后再回来，因为我们还有东西要学呢。

## 21. 20. Intro to User Sessions

**原文**

You see this right here that means we're logged in that's what we're gonna do in this exercise We're finally doing some off stuff, but it actually is gonna look a lot like what we've been doing already in fact Very very much like what we've been doing already, but we're actually gonna be doing auth related things So we've got a login screen I want you to go to and in that we're gonna be finding the user verifying the password That'll actually be the next exercise so we're gonna ignore the password for right now and then you're gonna set the user ID

**译文**

你看这里，这说明我们已经登录了，这就是我们要在本练习中完成的内容。我们终于要处理一些外部相关的内容了，但实际上它会和我们之前做的非常相似——事实上，和我们之前做的几乎一模一样，只是这次我们真正要处理的是与认证相关的事情。所以我们有一个登录界面，我希望你前往该界面，并在其中找到用户、验证密码。这将是下一个练习的内容，所以我们现在先忽略密码，然后你将设置用户 ID。

## 22. 21. Managing User Sessions with Separate Cookies

**原文**

For this step of the exercise, it's actually going to be really similar to the session storage we created for our toast messages. We're keeping these separate because it just kind of makes sense to me that these would be separate cookies for each one of these. So we're going to have an EN underscore session that is going to be a cookie for managing our user's session. So they're logged in information. So that's what you're going to do in this exercise. Have a good time.

**译文**

对于本练习的这一步，实际上会与我们为“提示消息”创建的会话存储非常相似。我们将它们分开处理，是因为在我看来，为每个功能分别设置独立的 Cookie 会更合理。因此，我们将创建一个名为 EN_session 的 Cookie，用于管理用户的会话信息，也就是用户的登录状态。这就是你在这项练习中需要完成的内容。祝你顺利！

## 23. 22. Secure Cookie Session Storage

**原文**

So this is going to be a util and that's going to be session dot server dot yes, and it's pretty similar to our toast session storage. So I'm going to copy this and paste it right here. We're going to export this. We're going to call it simply session storage. It'll be create cookie session storage from remix run node. And then the name of this one, it's got to be different. We can't have two session storages competing for the same name. So we're going to call this EN underscore session. That's EN for epic.

**译文**

所以这将是一个工具函数，也就是 session.server.js，它和我们的 toast 会话存储非常相似。所以我将复制这段代码并粘贴到这里。我们将导出它，并简单地将其命名为 session storage。它将从 remix run node 中创建 cookie 会话存储。然后，这个的名称必须不同。我们不能有两个会话存储竞争相同的名称。所以我们将它命名为 EN_session。这里的 EN 代表 epic。

## 24. 23. User Authentication and Session Management

**原文**

So we're just getting started with all this stuff. We've got a login page that Kelly built for us with a username and password. We don't have passwords in our database yet. We'll get to that soon. So as long as the username is filled in properly and we can find a user by that username, then we'll assume that the password is correct and we'll just let them in. But in the process of letting them in, that means we're going to be setting a cookie, so setting the session storage value for the user ID, and then doing the commit session, the stuff that we're

**译文**

所以我们现在才刚刚开始接触所有这些内容。我们有一个 Kelly 为我们构建的登录页面，里面有用户名和密码。我们的数据库中目前还没有密码，我们很快会处理这部分。所以只要用户名被正确填写，并且我们可以通过该用户名找到对应的用户，我们就会假设密码是正确的，然后直接让用户登录。但在让用户登录的过程中，这意味着我们将设置一个 Cookie，也就是为用户 ID 设置会话存储的值，然后执行提交会话的操作，也就是我们所说的……

## 25. 24. User Authentication and Session Management with Login Forms

**原文**

Let's head on over to the login route here and right up here we've got all this regular comform stuff that we've done before. We have parts of the form data and here's our login form schema and we are transforming the data that has been provided. So the data that's provided is the username and password. So assuming that those things are correct, they pass their schema, then we get into this transform. Now we've got this section for if the intent is to not submit, then we're going to exit early.

**译文**

我们现在转到登录路由这里，就在上方，我们有之前做过的所有常规表单相关的内容。我们有一部分表单数据，这里是我们的登录表单模式，我们正在转换所提供的数据。因此，所提供的数据是用户名和密码。假设这些内容是正确的，它们通过了模式验证，然后我们就进入这个转换环节。现在我们有一个部分，用于处理意图不是提交的情况，这时我们会提前退出。

## 26. 25. Load User Avatars

**原文**

We may have our enSession in here and somewhere in there, our user ID exists, but we need to resolve that to an actual user so that we can load the user's avatar or whatever in this position so that we can be logged in as that user. So if I refresh once you're all done, this should show the user's avatar.

**译文**

我们可能在这里有一个 enSession，在某个地方也存在我们的用户 ID，但我们需要将其解析为一个实际用户，以便能够在此处加载该用户的头像或其他内容，从而以该用户的身份登录。因此，当你们全部完成后，如果我刷新一次，这里就应该能显示用户的头像。

## 27. 26. Handling User Authentication and Session Management with Prisma

**原文**

All right, let's go to the root. And right in here, we need to load the user. So we're going to get our cookie session from await session storage from our util dot get session from the request dot headers dot get cookie, the cookie header from the request. And then we can get the user ID from the cookie session dot get user ID. And with that, if there is a user ID, then we can grab

**译文**

好的，现在我们进入根目录。就在这里，我们需要加载用户。因此，我们要从 `await sessionStorage` 中获取我们的 Cookie 会话，具体是通过 `util.getsession` 从 `request.headers.getcookie` 获取请求中的 Cookie 标头。然后，我们可以通过 `cookiesession.getuserid` 从 Cookie 会话中获取用户 ID。这样，如果存在用户 ID，我们就可以获取到。

## 28. 27. Dad Joke Break User Sessions

**原文**

Why are skeletons so calm? Because nothing gets under their skin. Actually, you know what? Maybe it would be a better thing if we just kind of let things slide. Now, that's a complex topic, too nuanced for us to get into right now. But hopefully the joke gave you a little bit of a chuckle. And now you have an opportunity to get up, move around, get some exercise, whatever you need to do before you get back to these exercises. So have a good time. We'll see you when you come back.

**译文**

为什么骷髅总是那么淡定？因为没什么事能钻进它们的皮肤里。不过说真的，也许我们干脆就让事情顺其自然会更好。当然，这也是一个很复杂的话题，太过微妙，我们现在就不深入探讨了。希望这个笑话能让你会心一笑。现在，你可以站起来活动一下，做些锻炼，或者在做这些练习前，做任何你需要做的事情。祝你过得愉快，等你回来我们再见面。

## 29. 28. Intro to Password

**原文**

Time to talk about passwords. Hooray! All right, I got a couple things I want to talk with you about passwords. I go into more detail in the instructions, but let's talk about a couple high-level things. First off, don't store plain text passwords. Such a bad idea. If a bad actor gets a hold of your database, then sure, they have access to all your data. So what's big whoop? But the fact is they have access to all the plain text passwords of your users, some of whom may actually reuse those passwords on other services. And as much as you can say, well, they shouldn't do that.

**译文**

是时候聊聊密码了。太棒了！好的，我有几件关于密码的事情想和大家聊聊。我会在说明中更详细地展开，但咱们先来聊几个宏观层面的问题。首先，不要存储明文密码。这绝对是个馊主意。如果不法分子拿到了你的数据库，那他们当然就能访问你的所有数据。这有什么大不了的？但问题在于，他们还掌握了你所有用户的明文密码，而其中一些用户可能真的会在其他服务上重复使用这些密码。尽管你可以说，嗯，他们本不该这么做。

## 30. 29. Creating an Optional Password Model in Prisma Schema

**原文**

Let's set up some password model data. So you're going to go to your Prisma schema and you're going to add a password model, but not a field in the user. No, it's got to be a model. And so one one model. And yeah, that's kind of interesting actually, because you cannot make it a required field. It has to be optional just because database constraints don't allow you to make it not optional. And at first glance, that might feel like that's not a good idea or that there's something missing there. But later on,

**译文**

我们来设置一些密码模型数据。你需要进入 Prisma 模式文件，添加一个密码模型，但不是用户模型中的一个字段。不，它必须是一个独立的模型。没错，就是这个样子的模型。说实话，这一点其实挺有意思的，因为你不能将其设为必填字段。它必须是可选的，仅仅是因为数据库约束不允许你将其设为非可选。乍一看，这似乎不是一个好主意，或者让人觉得有些不对劲。但稍后你会发现，

## 31. 30. Model Relationships and Handling Passwords in Database Schema

**原文**

So let's go to our schema and right down here, we're going to create our model, model, password. And this one's going to be a little simpler than most of them. We don't need to create it out. I don't think that really makes too much sense to have a created at or updated at like, I mean, maybe you might care about that. But yeah, it doesn't really feel that important to me. In fact, even an ID doesn't seem to be necessary here. So we're just going to have the hash, and we're going to have the user and the user

**译文**

那么，我们转到模式部分，就在这里创建我们的模型——password 模型。这个模型会比大多数模型简单一些。我们不需要创建它的创建时间或更新时间字段。我不觉得添加 created_at 或 updated_at 有什么太大意义——当然，也许你确实关心这些。但对我来说，这些并不那么重要。事实上，就连 ID 在这里似乎也没有必要。所以，我们只需要哈希值、用户以及用户。

## 32. 31. Generating Passwords for Secure User Creation

**原文**

Even though our password isn't required, it actually would be really nice if we made sure that the users we create do have passwords. And so your job is to update our seed script so that our users have passwords generated. For the Codi user, we can generate a password that we'll just remember. So I call it Codi loves you. You can call it what you like, but Codi does. Yeah, I love you. Codi does care about you. So that's what the password for Codi is.

**译文**

虽然我们的密码并不是强制要求，但如果能确保我们创建的用户确实设置了密码，那其实会非常好。因此，你的任务是更新我们的种子脚本，为我们的用户生成密码。对于 Codi 用户，我们可以生成一个我们会记住的密码。我把它叫做“Codi loves you”。你可以随便起个名字，但 Codi 确实是这样想的。是的，我爱你。Codi 确实关心你。所以，这就是 Codi 的密码。

## 33. 32. Secure Password Creation with Prisma

**原文**

We're going to use Bcrypt to create our password. So let's go to our seed right here and let's go down to Codi first. I like to update Codi's password first right here. So we're going to add a password field right here and this is again another model. So we're going to have a create and then that's going to have a hash and we're going to generate this hash the same way we want to generate it in our application that's using Bcrypt and Bcrypt. Yeah, sure. Hash sync. Codi loves you. That's perfect.

**译文**

我们将使用 Bcrypt 来创建密码。那么，让我们来到这里的 seed，然后先向下找到 Codi。我喜欢先在这里更新 Codi 的密码。所以我们要在这里添加一个密码字段，这同样是一个模型。因此我们将有一个 create，然后它将包含一个 hash，我们将以与应用程序中相同的方式来生成这个 hash，也就是使用 Bcrypt。Bcrypt。是的，没错。Hash sync。Codi 爱你。这太完美了。

## 34. 33. Enhancing User Creation by Adding Passwords

**原文**

So Kelly's put together a sweet create account page for us that does all this onboarding. And so your job is to take the password that they provide and create that password when we create the user. So we already have the user creation stuff happening. Your job is just to make it so that we can create the password along with that. So have a good time.

**译文**

所以 Kelly 为我们准备了一个很棒的创建账户页面，可以完成所有这些引导流程。你的任务是使用他们提供的密码，在创建用户时一并创建该密码。我们已经实现了用户创建的功能，你的工作就是让密码也能在创建用户的同时被创建出来。祝你玩得开心。

## 35. 34. Creating and Hashing Passwords for User Sign-Up

**原文**

So Kelly put this together for us. Let's go to the signup route. And this should all be familiar to you since we've gone through all the conform and Zod stuff so far. So what Kelly did was put together this transform for us so we can retrieve the password from submitted form. And then we're going to create the password right here. This will be kind of familiar as well. Password. And that's going to be hash or it was sorry, create. There we go. And then hash. And this is going to come from B crypt. And we're going to

**译文**

所以 Kelly 为我们整理了这些内容。我们来看看注册路由。由于我们之前已经学习过所有关于 conform 和 Zod 的知识，所以这些内容对你来说应该都很熟悉。Kelly 为我们准备了这个转换函数，以便我们可以从提交的表单中获取密码。然后我们将在这里创建密码。这部分内容对你来说应该也比较熟悉。密码。然后应该是哈希，哦抱歉，是创建。好了。接着是哈希。这部分将来自 Bcrypt。然后我们将

## 36. 35. Dad Joke Break Password

**原文**

Breaking news! Energizer Bunny arrested! Charged with battery! Haha! It just keeps going! Alright, but you need to take a break. You can't just keep going. You don't run by batteries. You run by food and stuff. So go get yourself some food, get yourself something to drink, and then come on back because we got some more stuff to learn. Let's go!

**译文**

突发新闻！劲量兔被捕！罪名是“电池”相关！哈哈！它真是永不停歇！好吧，但你得休息一下。你不能就这么一直继续下去。你不是靠电池驱动的，你是靠食物之类的东西来运转的。所以去弄点吃的、喝点东西，然后再回来，因为我们还有更多内容要学。出发！

## 37. 36. Intro to Login

**原文**

All right, I think it's about time that we make it so that you can't log in as any user just by knowing their username. And so we are actually going to verify that the password is correct. We're going to use Bcrypt for this because it has this nice compare method. So you pass in the password that the user supplied, and then the hash that we stored in the database, and that will tell you whether or not it's valid. So you're going to be doing that. And then we're going to start adding some utilities for our UI to know whether the user is currently logged in.

**译文**

好的，我认为现在是时候实现一个功能，让用户仅凭知道用户名就无法登录。因此，我们将验证密码是否正确。为此，我们将使用 Bcrypt，因为它有一个方便的比较方法。你只需传入用户提供的密码，以及我们存储在数据库中的哈希值，它就会告诉你密码是否有效。接下来你将实现这个功能。然后，我们将开始为 UI 添加一些工具，以便判断用户当前是否已登录。

## 38. 37. Secure Password Authentication with bcrypt Compare in Node.js

**原文**

Right now I can log in as any user with any password and it lets me in. Your job is to actually compare the hash of the password that the user has entered with the hash of the password that we have saved in the database. You're going to use bcrypt compared to do this. So let's get going.

**译文**

目前，我可以使用任意用户的任意密码登录，系统都会允许我进入。你的任务是实际比较用户输入的密码哈希值与我们数据库中保存的密码哈希值。你将使用 bcrypt 来完成这项工作。那么，我们开始吧。

## 39. 38. Implementing Secure Password Verification in User Login

**原文**

We don't have logout implemented yet. And so we do have to go to application and clear out the cookies to be able to log out. We'll make that logout functionality soon. So let's go to our login. And we'll come down here to include the password hash. So we want to, like I said, we made the password separate from the user model so that people wouldn't accidentally include it. Well, in this case, we actually do want to include it. So we're going to select the password.

**译文**

我们还没有实现退出登录功能。因此，我们必须进入应用程序并清除 Cookie 才能退出登录。我们很快会添加这个退出登录功能。现在让我们转到登录部分。然后我们向下找到这里，包含密码哈希。正如我之前所说，我们把密码从用户模型中分离出来，是为了防止人们意外地将其包含进来。不过在这种情况下，我们确实希望包含它。因此，我们将选择密码。

## 40. 39. Securing UI Elements

**原文**

Now that we can be logged in as somebody and like legit logged in as somebody, it makes a lot of sense for us to have this new note button and the delete and edit buttons on our own stuff, but not on other people's stuff. That wouldn't make any sense to see that at all. The new note, that doesn't make sense. I shouldn't be able to make a new note on somebody else's profile. So you're going to be making some utilities to make it easy to hide these different UI elements so that we only see it on our own profile and we don't see it

**译文**

既然我们现在可以登录为某个用户，并且是真正意义上地登录为某个用户，那么在我们的内容上显示“新建笔记”按钮以及“删除”和“编辑”按钮，而在他人内容上不显示这些按钮，就变得非常合理。否则看到这些按钮就毫无意义了。“新建笔记”按钮也是如此，我不应该能在别人的个人资料上创建新笔记。因此，你将需要制作一些工具，以便轻松地隐藏这些不同的 UI 元素，从而确保我们只能在个人资料上看到它们，而不会在别处看到。

## 41. 40. Dad Joke Break Login

**原文**

A quick shout out to all the sidewalks out there. Thank you for keeping me off the streets. Haha. Alright, this is a good time for you to take a break, get up, get some water. I need to refill my water bottle. So go, you know, that's a good sign. It means that I've actually been drinking water. So water is like a really big part of your body and it needs replenishing. So go get yourself a drink of water and then go on a quick walk or whatever. Come on back because we got some more learning to do. I'm excited to see you again.

**译文**

在此向所有的 sidewalk 快速致敬。感谢你们让我远离街道。哈哈。好了，现在正是你休息一下、站起来、喝点水的好时机。我需要给我的水瓶加水。所以去吧，你知道的，这是一个好迹象。这意味着我确实一直在喝水。水是你身体中非常重要的一部分，需要及时补充。所以去给自己倒杯水，然后去散个步或做点别的什么。再回来吧，因为我们还有更多要学习的内容。我很期待再次见到你。

## 42. 41. Leveraging Utility Functions for User Data Handling and UI Customization

**原文**

The utility we're going to build is in apputils and user.ts. So this is going to be responsible for the hooks we're going to use to make the user data available everywhere. And we're going to use a couple of utilities for this. So we're going to import user outloader data from remix.runreact. And we're also going to import the loader that has the data we're looking for. So we look at the root, then here we're loading the user right here and we're sending it back as part of our JSON. And there are a couple of things we need to keep in mind.

**译文**

我们要构建的工具位于 apputils 和 user.ts 中。它将负责提供我们用来在全局范围内共享用户数据的钩子。为此，我们将使用几个工具。因此，我们将从 remix.runreact 导入 user outloader data。同时，我们还将导入包含所需数据的 loader。我们查看根目录，然后在这里加载用户数据，并将其作为 JSON 的一部分返回。此外，我们还需要注意几个事项。

## 43. 42. Intro to Logout

**原文**

All right, it's time to make the logout actually work. So when we log in, we have, what Cody loves you? We have this logout button you're going to be making that work. We're also going to be doing automatic logout so that the user is automatically logged out after a certain amount of time. Of course, longer than that. But yeah, so there are a couple of things that we need to consider with all of this. There's expires and max age, which are properties that you can set on a cookie that will tell the browser when to eject

**译文**

好的，现在是时候让注销功能真正生效了。当我们登录时，有“Cody 爱你吗？”这样的内容，还有一个注销按钮，你将让它正常工作。我们还将实现自动注销功能，这样用户在经过一段时间后会自动被注销。当然，这个时间会比那个更长。不过，总之，在处理这些功能时，我们需要考虑几个问题。其中包括 expires 和 max age，这两个属性可以设置在 Cookie 上，用来告诉浏览器何时清除 Cookie。

## 44. 43. Transforming a Logout Link into a Secure Logout Form

**原文**

Your job in this exercise is to make this logout button work. So right now it's just a form that doesn't do anything. You need to change it to a form that posts to slash logout because we want to do a post for this type of a mutation, not a get. So it's very common for applications to just have like a route that you have a link and it links them to the logout route and that will log them out. No, you want to do a post because that it's better for security for various reasons. So that is your job.

**译文**

你的任务是让这个退出登录按钮能够正常工作。目前它只是一个没有任何功能的表单。你需要将其改为一个向 `/logout` 发送 POST 请求的表单，因为对于这类“变更操作”，我们希望使用 POST 而非 GET。许多应用程序通常会提供一个链接，通过链接跳转到退出登录路由来实现退出功能。但你不应该这样做，而应使用 POST 请求，因为出于多种安全考虑，这样做更为稳妥。这就是你的任务。

## 45. 44. Logout Functionality with Session Storage and CSRF Protection

**原文**

So the first thing we want to go to is our username route. And in here, we've got our form for that logout. So that logout button right there, we're going to want to post. So method post, and because cross site request forgery, all that good stuff. Speaking of that, let's add our authenticity token input from remix utils. And then we're going to post to the action slash logout. Now, if we don't have the action, it's going to post to this route. And so we could put the action

**译文**

首先，我们要进入的是用户名为路由的路径。在这里，我们有用于登出的表单。因此，我们需要对该登出按钮执行 POST 请求。所以方法设为 POST，并且由于跨站请求伪造（CSRF）等相关安全问题，我们需要添加来自 Remix 实用程序的真实性令牌输入。然后，我们将向 `/logout` 动作发起 POST 请求。如果我们没有指定动作，请求将提交到当前路由。因此，我们可以将动作设置为...

## 46. 45. Implementing Remember Me Functionality for Login Sessions

**原文**

So when we log in, if I go codey and codey loves you before we do that, let's open up our network tab here. And when I hit log in, then we're going to get this post request and our cookie is going to be set as part of that post request. And in here we have our path slash HTTP only same site lacks all that is exactly what we'd expect. If we come over to the application, and we see that in session, this says it expires or slash max age.

**译文**

所以当我们登录时，如果我在执行之前先输入 codey 并且 codey 爱你，那么我们先在这里打开网络选项卡。当我点击登录时，我们会收到一个 POST 请求，而我们的 Cookie 就会作为该 POST 请求的一部分被设置。在这里，我们有路径、斜杠、HTTP 仅、同源、无等属性，这完全符合我们的预期。如果我们切换到“应用”选项卡，就会看到在会话存储中，这里显示其过期时间为斜杠或最大年龄。

## 47. 46. Implementing Remember Me Functionality

**原文**

So we have this new Remember Me checkbox on both the Create and Account page as well as the login page. And so what we're going to do is go to login page first and come on down here. Here's the updates to our Zod schema for that Remember Me checkbox. We'll come down here and we're going to add an expires option so that we can configure when this session or this cookie will expire. So as a second argument to commit session, we'll say expires.

**译文**

因此，我们在“创建”页面、“账户”页面以及登录页面都新增了一个“记住我”复选框。接下来，我们先前往登录页面，然后向下滚动到这里。这里是对 Zod 模式进行的更新，用于处理这个“记住我”复选框。我们向下滚动到这里，添加一个 `expires` 选项，以便配置该会话或 Cookie 的过期时间。因此，作为 `commit session` 的第二个参数，我们将传入 `expires`。

## 48. 47. Managing Inactive User Sessions

**原文**

So I'm going to log in as one of these other users so we can take a look at an interesting use case that doesn't really happen a lot, but definitely could happen. So we'll log in as this user and now we'll go find that user in our database. We will delete this record. Let's say that maybe some admin deleted it or they deleted it in a different tab or something like that. And so now if I refresh the page, I'm no longer logged in. That's exactly what we want. But the problem is that my session is still active. So there's still a user ID in here.

**译文**

那么，我将以其中一个其他用户的身份登录，这样我们就能查看一个不太常见但确实可能发生的情况。我们将以该用户身份登录，然后在数据库中查找该用户。我们会删除这条记录。假设可能是某个管理员删除了它，或者他们在另一个标签页中删除了它，诸如此类。现在，如果我刷新页面，我就已经不再处于登录状态了。这正是我们想要的结果。但问题在于，我的会话仍然处于活动状态。因此，这里仍然包含一个用户 ID。

## 49. 48. Destroying Sessions and Handling Weird States

**原文**

I'm going to leave everything up as it was where we have this session that doesn't have a user ID in it anymore. And when I'm done, we should see this session getting destroyed. So let's go to our route. And we'll come right here and we'll say, if there's a user ID, but there's, whoops, there's not a user, then that's where we're in that weird spot. So we're going to return a redirect to, and actually let's throw so we don't have issues with TypeScript or whatever, we'll just throw a redirect to

**译文**

我会把所有内容都保持原样，现在我们有一个不再包含用户 ID 的会话。当我完成之后，我们应该会看到这个会话被销毁。那么，让我们转到我们的路由。我们就在这里，然后说：如果存在用户 ID，但是——哎呀——没有用户，那我们就处于那种奇怪的情况。所以我们要返回一个重定向，而且实际上，为了避免 TypeScript 或其他问题，我们直接抛出（throw）一个重定向到

## 50. 49. Implementing Automatic Logout with Modals

**原文**

In this exercise, we're actually going to do something that we don't need for this app, but it's common enough that we're going to just do the exercise and then Kelly will remove all the code later. So Kelly actually added a bit of code for a modal that'll pop up when the user's been logged in for a little bit. So I'm going to log in as Cody and then we'll just wait for a little bit. No activity. I'm going to say remain logged in so we can see that. So that modal pops up after a certain amount of time for this exercise. We've made it obviously quite short.

**译文**

在本练习中，我们实际上要做一些对这个应用来说并不需要的东西，但因为这种情况相当常见，所以我们还是先完成这个练习，之后 Kelly 会删除所有相关代码。Kelly 实际上添加了一小段用于模态框的代码，当用户登录一段时间后，该模态框就会弹出。因此，我将以 Cody 的身份登录，然后稍等片刻，期间不进行任何操作。我会选择“保持登录”状态，以便能看到效果。这样，在本次练习中，模态框就会在特定时间后弹出。显然，我们把这个时间设置得非常短。

## 51. 50. Auto-Logout Functionality

**原文**

Let's go to our route. And let's get this thing rendered first, we're going to have an is logged in option to our document. And we'll grab the type for that. That's a Boolean. And then when we go to document right here, we're going to say is logged in will be true if the user is a so Boolean user. There we go. And let's actually we'll make this optional as well. And then

**译文**

让我们转到我们的路由。首先我们来渲染这个东西，我们将在文档中添加一个 is logged in 选项。然后我们获取它的类型。这是一个布尔值。接着当我们来到这里处理文档时，我们会说：如果用户是一个布尔类型的用户，那么 is logged in 就为 true。好了。然后我们实际上也让这个成为可选的。然后

## 52. 51. Dad Joke Break Logout

**原文**

I was going to get a brain transplant, but I changed my mind. Maybe it feels like you're getting a brain transplant right now with all the stuff that you're learning. So this is a good time for you to take a break. Get up, walk away, come back, and let's keep going. Yeah, don't skip the walk away part. You got to move your body in some way. If you're physically able, then walk. If you're not, then there's other motions would be a good thing to just get the blood flowing in your body because

**译文**

我本来打算去做个大脑移植手术，但后来改变主意了。也许你现在正在学的东西，让你感觉就像在做大脑移植一样。所以现在正是你该休息一下的好时机。站起来，走开一会儿，然后再回来，我们继续。是的，别忘了“走开”这一步。你得以某种方式活动一下身体。如果你身体条件允许，那就去散步。如果不行，做一些其他的运动也很好，目的只是让血液在身体里流动起来，因为

## 53. 52. Intro to Protecting Routes

**原文**

We're going to start protecting routes and it's actually pretty simple. Can the user be here? Then if not, send them away. That's it. So the idea is we're going to have a couple of different routes that we're going to take. We have the loader, so getting data. The loader is where you're going to say whether or not the user can be here. So you're going to look for the user in the request and you'll get the user ID. We already do that in the root. In fact, Kelly made a couple of utilities

**译文**

我们将开始保护路由，其实非常简单。用户能在这里吗？如果不能，就把他们送走。就是这样。所以，我们的思路是会有几个不同的路由来处理。我们有加载器，用来获取数据。在加载器中，你将判断用户是否可以在此处。因此，你需要在请求中查找用户，并获取用户 ID。我们在根目录中已经这样做了。实际上，Kelly 还创建了一些工具。

## 54. 53. Creating Protected Routes

**原文**

So I'm logged in. It wouldn't make a lot of sense for me to go to login. Even though we don't have any links there, it just, it'd be confusing. I've used apps that will allow you to go to the login screen even when you're logged in. And sometimes they accidentally like navigate you there in some ways. And it's really annoying. I don't like that. It's very confusing. So the login page probably not somewhere I should be able to go as well as the onboarding page, the signup page. I shouldn't be able to go there either when I'm logged in.

**译文**

我现在已经登录了。如果我去登录页面，其实没什么意义。尽管那里没有任何链接，但那样做只会让人感到困惑。我用过一些应用，它们允许你在已登录的状态下跳转到登录界面，有时还会不小心以某种方式把你导航到那里，这真的很烦人。我不喜欢这样，因为它非常令人困惑。所以，登录页面大概也不应该是我能访问的地方，同样地，引导页面和注册页面也不应该在我登录时还能访问。

## 55. 54. Creating an Auth Utility

**原文**

Because we're going to need this on multiple routes, I want to make a utility for it. So we're going to make auth.server be our utility. Kelly moved a bunch of stuff into here. So there's a couple of things that we were doing in other routes that we've just put into here, like the login and sign up functions, all that stuff. So we have all of our auth stuff in one place. And we're going to make another utility called require anonymous. So it's export a function called require anonymous. And here we're going to take a request. And that is going to be our request. There we go.

**译文**

由于我们将在多个路由中使用这个功能，我想为它创建一个工具。因此，我们将把 auth.server 作为我们的工具。Kelly 把很多东西都移到了这里。所以，我们之前在其他路由中执行的几项操作现在都已放在这里了，比如登录和注册函数，以及所有相关的内容。这样，我们所有的认证相关功能都集中在一个地方。接下来，我们还将创建另一个名为 require anonymous 的工具。它会导出一个名为 require anonymous 的函数。在这里，我们将接收一个请求。这个请求就是我们的请求。就是这样。

## 56. 55. Building a Profile Page

**原文**

We've got this edit profile page that allows us to make changes to our profile. We can change our profile picture. We can change our name and save that. And we can change our password and we can even download our data. So there we go. I already did it. We can download our user data. So all sorts of cool things. And then of course, delete all your data. Now we can delete ourselves, which I'm not going to do right now. So all of this is

**译文**

我们有一个编辑个人资料页面，可以在此对个人资料进行修改。我们可以更改头像，也可以更改姓名并保存。此外，我们还能修改密码，甚至可以下载自己的数据。就是这样。我已经操作过了。我们可以下载用户数据。总之，有很多很酷的功能。当然，还有删除所有数据的选项。现在我们可以删除自己的账户，不过我现在不会这么做。所以所有这些功能都……

## 57. 56. User Authentication and Authorization

**原文**

So let's get started by exporting a function called requireUserId. And Copilot can actually do most of this stuff for us because it's pretty simple. It's just the opposite of this requireAnonymous that we did already. So we get the userId with that util. If there's not one, then we're going to throw a redirect to the login. And then we'll return the userId as what we give back. So if we apply this to all of these pages, then we need to get the userId with the

**译文**

那么，我们先从导出一个名为 requireUserId 的函数开始。实际上，Copilot 可以为我们完成大部分工作，因为这个功能相当简单。它与我们之前实现的 requireAnonymous 功能正好相反。我们会通过那个 util 获取 userId。如果不存在 userId，我们就会抛出重定向到登录页面的操作。然后，我们将返回的 userId 作为结果返回。因此，如果我们将这个逻辑应用到所有这些页面中，我们就需要通过 util 来获取 userId。

## 58. 57. Securing User Access

**原文**

You want to see something really cool? I can go to my notes here and I can create a new note. Well, what's a little less cool is I can actually do that from an unauthenticated user as well. So, LOL, I pick my nose, of course, the thing that you would say if you wanted to troll somebody. So, yeah, definitely not something that we want people to be able to do. And so your job is to make it so they can't. Not only can they not get to the new page, but you also want to make it so they can't get to the edit page.

**译文**

你想看点真正酷的东西吗？我可以到这里面的笔记中，创建一条新笔记。不过，没那么酷的是，未认证用户实际上也能做到这一点。所以，LOL，我“挖鼻孔”——这当然是你想恶搞别人时会说的话。没错，这绝对是我们不希望用户能做的事情。因此，你的任务就是让他们做不到这一点。他们不仅无法访问新页面，你还得让他们也无法访问编辑页面。

## 59. 58. Authorization and User Authentication

**原文**

To start, we're going to go to AuthServer. And in here, we're going to see what Copilot can do for us. So export a sync function called requireUser. And we're going to get the user ID. Nah, that's not quite right, Copilot. We're going to get the user ID from await requireUserID. Because we're requiring the user, we're going to definitely require that they have an ID as well. And so all of the logic that we have behind requireUserID makes perfect sense in the context of requireUser. So here now, we're going to

**译文**

首先，我们要进入 AuthServer。在这里，我们将看看 Copilot 能为我们做些什么。因此，导出一个名为 requireUser 的同步函数。然后我们要获取用户 ID。不，Copilot，这样不太对。我们应该通过 await requireUserID 来获取用户 ID。因为我们正在验证用户，所以肯定也需要确保用户拥有 ID。因此，我们所有关于 requireUserID 的逻辑在 requireUser 的上下文中都非常合理。所以现在，我们要

## 60. 59. Redirect Functionality

**原文**

Let's say that I'm over here and I'm like, I want to change my picture and I click change and I decide, okay, yeah, this is the picture I want. I'm going to go with the Koala cuddle. And then I like forget about it or something. I've got another tab open and I'm like, yeah, okay, I've got to be done. We're going to log out. So then I come over here and I hit save photo and I go to login. That's not fun. Okay, we'll say Cody, Cody loves you. And now I forgot, what was I doing?

**译文**

假设我现在在这里，心想，我想换一张照片，于是我点击“更改”，然后决定，好的，没错，就是这张照片了。我选择“考拉抱抱”。然后我可能就把这事儿给忘了。我又打开了另一个标签页，心想，好吧，我得赶紧弄完。我们要退出登录了。接着我回到这里，点击“保存照片”，然后去登录。这可不太妙。好吧，我们就说Cody，Cody爱你。现在我忘了，我刚才在做什么来着？

## 61. 60. Handling Redirects Safely in User Authentication

**原文**

Let's go to our util right here where we're saying require user ID. We're going to take an optional second argument called or that's just an object that has a redirect to and we'll default that to an empty object that way you don't have to provide it. And we will default this to actually nothing we're going to allow people to specify a string or if they don't want to specify any redirect so like we're going to go to login. If we don't want them to have a

**译文**

让我们来到这里的工具函数，我们正在这里写 `require user ID`。我们将添加一个可选的第二个参数，叫做 `options`，它只是一个包含 `redirect` 字段的对象。我们会将其默认值设为一个空对象，这样你就不需要提供它了。而这个参数我们实际上默认设为 `null`——我们将允许用户传入一个字符串，或者如果他们不想指定任何重定向，比如我们想要跳转到登录页，就可以不传。

## 62. 61. Dad Joke Break Protecting Routes

**原文**

What's red and smells like blue paint? Red paint! As a yeah, definitely a dad joke there. All right. Well, now is a good time to paint the town red. No, just kidding. I mean, it depends on what time it is and I don't even know what that phrase means. I have some ideas. Anyway, let's let's move on. Go ahead and go to the bathroom, go get a drink, go whatever, go give somebody a high five, tell them how awesome you're doing at all these exercises and then come back because

**译文**

什么东西是红色的，闻起来像蓝色油漆？红色油漆！是啊，这绝对是个老爸式冷笑话。好吧。现在正是把整座城市染成红色的好时机。不，我只是开玩笑。我的意思是，这取决于现在是什么时候，而且我甚至都不知道这句话是什么意思。我倒是有一些想法。总之，我们继续吧。去吧，上个洗手间，去拿杯喝的，做点什么都行，去跟别人击掌，告诉他们你在做这些练习时表现得有多棒，然后再回来，因为

## 63. 62. Intro to Permissions

**原文**

In this exercise, we're going to talk about role-based access control or RBAC. I'm not sure if that's how you say it, but that's how I say it, RBAC. And so it's easiest to kind of visualize this from the data perspective, and then we can talk about other things. So we've got our users, and users can have, in an RBAC situation, users can have multiple roles. So this could be like admin role, user role, a marketing team role, like there are all kinds of different kind of personas that you think about.

**译文**

在本练习中，我们将讨论基于角色的访问控制，即 RBAC。我不确定是不是这么说的，但我就是这么说的：RBAC。最简单的方式是从数据角度来理解它，然后我们再讨论其他内容。我们有用户，在 RBAC 模型中，用户可以拥有多个角色。比如管理员角色、用户角色、市场团队角色等等——你可以想象出各种各样的不同身份。

## 64. 63. Role-Based Access Control with Prisma

**原文**

Let's get started by updating our Prisma schema. So we need to add a permissions table and a roles table or model so that we can create this role-based access control. And this is going to be a many to many. A user can have many roles and roles can be assigned to many users. And then we're going to have a many to many on the roles and permissions as well. So a role can have many permissions and a permission can be assigned to many roles.

**译文**

让我们通过更新 Prisma 模式来开始。我们需要添加一个权限表和一个角色表（或模型），以便实现基于角色的访问控制。这将是一个多对多关系：一个用户可以拥有多个角色，而一个角色也可以分配给多个用户。此外，角色和权限之间也将是多对多关系：一个角色可以包含多个权限，而一个权限也可以被分配给多个角色。

## 65. 64. Modeling Permissions and Roles in Prisma Database

**原文**

Let's go over to our schema.prisma file and we'll come down here and we'll create these models. So model permission and we'll let co-pilot fill in some of this stuff for us. So we're going to have an ID that's like everything else we've done. We'll have an action entity and access. So this would be our create read update delete. I'm going to add that as a comment. We can't do enums as part of SQLite. You could do an enum with other databases. I've done that before.

**译文**

让我们转到 schema.prisma 文件，然后向下滚动并创建这些模型。所以，模型 permission，然后让 co-pilot 帮我们填充部分内容。我们将有一个 ID，这和我们之前做的所有事情都一样。我们会有一个 action、entity 和 access。这将是我们的创建、读取、更新、删除操作。我会将其添加为注释。SQLite 不支持将枚举作为其一部分。你可以使用其他数据库来创建枚举，我以前这样做过。

## 66. 65. Managing Roles and Permissions

**原文**

Now that we've got our database up to date, we need to make sure that we create new users with the user role. Otherwise, when we add our permission stuff throughout the app, they won't be able to do stuff with their own stuff. Oh, and speaking of the user role, we got to create that too, as well as an admin role. We're going to be creating these as part of the seed script. And then you would want to apply this same sort of seed script or push a seeded database up to your production database. So you have access or pre seeded the things that are

**译文**

既然我们已经将数据库更新至最新版本，接下来需要确保新用户是以“用户角色”创建的。否则，当我们在整个应用中添加权限相关功能时，用户将无法对自己拥有的内容执行操作。哦，说到用户角色，我们还需要创建它，同时还要创建一个管理员角色。我们将把这些角色的创建作为种子脚本的一部分来完成。然后，你应当将这种种子脚本应用到生产数据库中，或者将已包含种子数据的数据库推送到生产环境，以便你能够访问或预先填充所需的初始数据。

## 67. 66. Seed Data

**原文**

Let's go to our seed script and we'll come right here and we're deleting all the users. But remember, we by deleting all the users, we're able to delete pretty much everything because the users notes will get deleted. There are no images, their user images, their passwords, all of those things will get deleted when the user is deleted. However, roles and permissions are not tied to any particular user. And so deleting the users will still have the roles and permissions. And if we're about to create new roles and permissions, then we're going to have a conflict.

**译文**

让我们转到种子脚本，然后来到这里，删除所有用户。但请记住，通过删除所有用户，我们实际上可以删除几乎所有的内容，因为用户的笔记也会被删除。用户的图片、用户图片、密码等所有内容，都会在用户被删除时被清除。然而，角色和权限并不与任何特定用户绑定。因此，删除用户后，角色和权限仍然存在。如果我们接下来要创建新的角色和权限，就会出现冲突。

## 68. 67. Implementing User Permissions and Authorization Logic

**原文**

So as Cody is an admin user, Cody should be able to delete other people's notes. So I should be able to hit this and get it deleted right now. That's not possible because we need to add some logic in our application to check the user's permissions and then check whether they're authorized to do this. And Cody should be authorized to do this. Kelly added a little bit of logic to make it so that it's easier to display this bar when we have those permissions. So you're going to be adding a little bit of logic to the loader for this page to determine whether the user

**译文**

由于 Cody 是一名管理员用户，因此他应该能够删除其他人的笔记。所以我现在应该可以点击这个按钮并将其删除。但目前还无法实现这一点，因为我们需要在应用程序中添加一些逻辑，用于检查用户的权限，然后判断他们是否有权限执行此操作。而 Cody 应该是有权限的。Kelly 添加了一小部分逻辑，以便在用户具备这些权限时更容易地显示这个栏。因此，你将需要为该页面的加载器添加一小部分逻辑，以确定用户是否...

## 69. 68. Implementing Role-Based Permissions

**原文**

This is our note ID route. So let's go in there. We're going to start in our loader to determine whether or not we should display these right now. Coe's got us displaying these all the time saying that we can delete is true. But that is not the case. So let's come up here and let's first get the user ID. So user ID is await get user ID from our server utils request here request there. There we go.

**译文**

这是我们的笔记 ID 路由。那我们先进入这里。我们将从加载器开始，确定现在是否应该显示这些内容。目前的代码让我们一直显示这些内容，并提示“可以删除”为 true。但事实并非如此。所以我们来到这里，首先获取用户 ID。用户 ID 是通过 `await getUserID` 从我们的 `server/utils/request` 中获取的。就是这样。

## 70. 69. Securing Admin Pages with User Permissions

**原文**

We have now created a bunch of utilities that we'll be able to use for making much easier queries to determine whether a user has permission to do a particular thing, which is quite nice. And so in addition to that, Kelly has also made us an admin page, which doesn't really do a whole lot yet. But we want to lock this down to only admin users. And so you've got a couple of things that you need to do in this exercise. First, you need to update the root loader so that

**译文**

我们现在已经创建了一堆工具，这些工具将能帮助我们更轻松地执行查询，以确定用户是否有权限执行特定操作，这相当不错。此外，Kelly 还为我们创建了一个管理页面，虽然目前它还没有太多功能。但我们希望将其限制为仅管理员用户可见。因此，在本次练习中，你需要完成几项任务。首先，你需要更新根加载器，以便

## 71. 70. Implementing Role-based Access Control and Permissions

**原文**

The first thing we're going to need to do is in our permissions utilities, we've got a couple TS ignores right here. And that's because we're trying to infer the user type from what the use user returns use user returns, maybe user, which is coming from use optional user, which comes from ultimately, our root loader. So if we dive into the root loader, we're not loading enough of the information that our permissions utilities need to be able to determine the permissions.

**译文**

首先，我们需要在权限工具中处理这里存在的几个 TS 忽略项。这是因为我们试图从 `useUser` 的返回值推断用户类型——`useUser` 返回的可能是一个用户对象，而这个对象来自 `useOptionalUser`，最终又源自我们的根加载器。因此，如果我们深入查看根加载器，会发现它加载的信息不足以让权限工具判断出所需的权限。

## 72. 71. Dad Joke Break Permissions

**原文**

Where'd you learn to make ice cream? Sunday school! Haha! I actually just had a Sunday with my kids the other day. Sundays are delicious. So, well done on that exercise. That is a lot of work to get through all this stuff. You're doing excellent. I want you to keep going, but you need to take breaks because if you don't take breaks, then your brain will explode and you won't remember anything. So taking breaks is actually very much an important part of the learning process. And so that's why I have these videos so that I can kind of

**译文**

你是在哪儿学会做冰淇淋的？主日学！哈哈！其实前几天我才刚和孩子们过了一个周日。周日真是美好时光。所以，那个练习你做得很好。要完成所有这些内容可真是下了不少功夫。你表现得非常出色。我希望你能继续坚持下去，但你需要适当休息，因为如果你不休息，你的大脑就会爆炸，到时候什么都记不住了。所以，休息其实是学习过程中非常重要的一部分。这也是我制作这些视频的原因，这样我就可以……

## 73. 72. Intro to Man Sessions

**原文**

In this exercise, we're going to be adding a sweet new feature that allows users to sign out of other sessions. So they'll be logged into multiple computers or multiple devices on their phone and everything. And then they find out, oh yeah, like that was a public library. I need to be signed out, but I can't get back to the library for some reason. So this would allow them to sign out of that session proactively so that the library is no longer signed in. And yeah, so I've got signed in into this incognito window. And I've got signed in over here.

**译文**

在本练习中，我们将添加一个非常实用的新功能，允许用户退出其他会话。这样，用户可以在多台电脑或手机设备上都保持登录状态。之后他们可能会发现，哦对了，那台设备是在公共图书馆使用的，我需要退出登录，但因为某些原因无法再回到图书馆。这个新功能将允许他们主动退出该会话，从而确保图书馆的设备不再处于登录状态。比如，我现在在这个无痕窗口中登录了，同时在这里也登录了。

## 74. 73. Managing User Sessions and Allowing Data Downloads

**原文**

So let's get started with sessions. The first thing we're going to need to do is update the database because now instead of storing the user ID in a cookie, we're going to store it in a session object in the database and that way we can manage those sessions ourselves. We're also going to update the download user data so that the user can download their sessions because why not? Like we let the user download all of their data, including their sessions. There's not a lot of data in there, but you know, maybe they want it. So with that, I think

**译文**

那么，让我们开始学习会话（sessions）吧。首先，我们需要更新数据库，因为现在不再将用户 ID 存储在 Cookie 中，而是将其存储在数据库的会话对象中，这样我们就可以自行管理这些会话。我们还将更新下载用户数据的功能，以便用户能够下载自己的会话——为什么不呢？既然我们允许用户下载自己的所有数据，当然也包括会话。虽然其中包含的数据并不多，但谁知道呢，也许用户就是想要。所以，说到这里，我想

## 75. 74. Integrating User Sessions into the Login Process

**原文**

So let's get into our schema. We'll come down here. Yeah, right around here with the sessions. So it's going to be pretty typical model, we'll say model session. And this is going to have all the typical stuff so Copilot can do it. Now we've got the ID, the expiration date. So that is a date time that's when this thing expires. In the future, we can add a cron job that will just delete old sessions from the database automatically. These will get deleted when we log out and other things too, but they could

**译文**

那么，我们开始进入模式设计部分。我们往下走，就在这里，关于会话的部分。这将是一个非常典型的模型，我们就叫它 model session。它会包含所有常规字段，这样 Copilot 就能处理了。现在我们有 ID 和过期日期。这是一个日期时间字段，表示该会话何时过期。将来，我们可以添加一个定时任务（cron job），自动从数据库中删除旧的会话。当我们注销时以及其他一些操作也会删除这些会话，但它们可能……

## 76. 75. Implementing Session-Based Authentication

**原文**

Getting things updated with the new sessions is actually quite a bit of work. So we're going to split this up into two steps. First, we're going to update the auth utils. And then in the next step, we'll update the login and sign up flows. So in this step, you're just going to go to the auth server utility and change everything from being user ID centric over to sessions and session IDs. We've got a couple of utilities that actually kind of require, like we have literally require user ID.

**译文**

要让一切与新的会话同步，实际上需要相当多的工作。因此，我们将把它分成两个步骤。首先，我们会更新身份验证工具。然后在下一步中，我们会更新登录和注册流程。因此，在这一步中，你只需要前往身份验证服务器工具，将所有基于用户 ID 的内容更改为基于会话和会话 ID。我们有几个工具实际上需要用户 ID，比如我们确实需要用户 ID。

## 77. 76. Authentication Logic with Session IDs and User Creation

**原文**

Let's open up the AuthServerUtils and we're going to keep this user ID key variable name because other files are using it. We'll fix that in the next step of the exercise. But we are going to change this, the actual value to session ID to communicate what it actually is. And we're going to then rename this to session ID because that's now actually a session ID. And then instead of querying the user table that we're now storing session IDs. And so we're going to look for this in the session table that we just made. And so this is

**译文**

让我们打开 AuthServerUtils，我们会保留这个用户 ID 键的变量名，因为其他文件正在使用它。我们将在练习的下一步中修复这个问题。但我们将更改这个实际的值，将其改为会话 ID，以明确它实际代表的含义。然后我们会将其重命名为会话 ID，因为它现在确实是一个会话 ID。接着，我们不再查询用户表，因为我们现在存储的是会话 ID。因此，我们将在刚刚创建的会话表中查找这个值。所以这就是

## 78. 77. Improving Login and Signup Flows with Session Management

**原文**

All right. In this step, we're going to be able to log in. Right now, that's not exactly working quite right. We need to actually update the login and the sign up flows so that you can properly log in with a session instead of relying on user IDs. That is your task in this one. You're going to be updating both of these routes as well as the Auth server to finally rename that variable from user ID key to session ID key. Have a good time with that. We'll see you when you're done.

**译文**

好的。在这一步中，我们将实现登录功能。目前，登录功能还不能完全正常工作。我们需要实际更新登录和注册流程，以便用户能够通过会话（session）正确登录，而不是依赖用户 ID。这就是你这一步的任务。你将同时更新这两个路由以及 Auth 服务器，并最终将该变量从“user ID key”重命名为“session ID key”。祝你顺利！完成后我们再见。

## 79. 78. Updating Login and Signup Routes to Use Sessions instead of User IDs

**原文**

Let's go to the Auth server first and we're going to rename this variable from user ID key to session key. And there that should update everything in this file. And actually, thanks to TypeScript being amazing, we're also going to get that update here. So session key is right there. So that's awesome. So now instead of worrying about the session or the user ID key variable being a funny name, now it's session key. But we

**译文**

我们先去 Auth 服务器，把这个变量从 user ID key 重命名为 session key。这样应该就能更新这个文件里的所有内容了。而且多亏了 TypeScript 的强大，我们这里也会自动更新。看，session key 就在这里，太棒了。现在就不必再担心 session 或 user ID key 这个变量名听起来奇怪了，现在它叫 session key。不过我们

## 80. 79. Proactive Session Management

**原文**

So the entire purpose of doing managed sessions is so that we can delete them pro like programmatically or proactively. And so if we go to our profile page right down here, we've got this new section that Kelly put together for us. This is your only session is what it says now. But if we have multiple sessions, then that will show how many sessions we have and give us an option to delete all of the other sessions. So that way we can log out of the library that

**译文**

因此，使用托管会话的主要目的，就是让我们能够以编程式或主动的方式将其删除。如果我们前往这里的个人资料页面，就会看到 Kelly 为我们创建的这个新部分。目前显示的是“您只有一个会话”。但如果我们拥有多个会话，这里就会显示会话数量，并提供一个选项来删除所有其他会话。这样一来，我们就可以退出该库。

## 81. 80. Managing Sessions and Sign Out in Web Applications

**原文**

So let's go to our profile index file here and we'll start in the loader. We need to count how many sessions there are so we can display how many sessions there are and let the user delete the other ones. So we'll add a count here of the sessions or yeah we'll select sessions where the expires expiration date is greater than the current date. So all the active sessions we don't want to display the expired sessions that would just confuse the user and be

**译文**

那么，我们转到这里的个人资料索引文件，从加载器开始。我们需要计算有多少个会话，这样我们才能显示会话数量，并让用户删除其他会话。因此，我们在这里添加一个会话计数，或者，是的，我们会选择那些过期日期大于当前日期的会话。也就是说，我们只保留活动会话，不想显示已过期的会话，那只会让用户感到困惑，并且

## 82. 81. Dad Joke Break Man Sessions

**原文**

What do you call a boy who stopped digging holes? Douglas! Ha ha ha! Alright, that's pretty good. Actually, if you've never read the book, Holes, it's kind of an interesting one that my kids just finished recently. But, uh, and now might be a good time because it's time for your break. So, good for your brain to move on, like, go do something else for a little bit. I just finished Breath of the Wild, which was pretty cool. So, like, go play a video game if that's your thing. And, yeah, then stop doing that and come back because we still got stuff to do.

**译文**

你管一个不再挖洞的男孩叫什么？道格拉斯！哈哈哈！好吧，这个笑话还不错。其实，如果你还没读过《洞》这本书，那它还挺有意思的，我的孩子们最近刚读完。不过，呃，现在可能正是个好时机，因为该休息了。所以，让你的大脑换换思路，去做点别的事情吧。我刚通关了《旷野之息》，那游戏真的很棒。所以，如果那是你的菜，就去玩会儿电子游戏吧。然后，嗯，就停下手头的事回来，因为我们还有事情要做呢。

## 83. 82. Intro to Email

**原文**

To verify our users, we're going to need to send an email address. There's all this conversation about validating email addresses, but the only real way to validate an email address is to send an email and have the user prove to you that they have access to that email by verifying that. We're not going to get into verification in this exercise. This exercise is all about sending the email. But we don't want to send a real email during development because then we have the whole email flow that just like disrupts our development. In addition, it will cost us money to run

**译文**

为了验证用户身份，我们需要发送一个电子邮件地址。关于电子邮件地址验证有很多讨论，但唯一真正能验证电子邮件地址的方法就是发送一封邮件，并通过验证让用户证明他们拥有该邮箱的访问权限。在本练习中，我们暂不涉及验证部分。本练习的重点是发送邮件。但在开发阶段，我们不想发送真正的邮件，因为这会引入完整的邮件流程，从而干扰我们的开发工作。此外，发送邮件还会产生费用。

## 84. 83. Integrating Email Services

**原文**

We're going to start sending emails. So you're going to need to add API key for the resend service. We're definitely using a service for this. And we're going to add some integration code for actually sending emails. We'll just have a simple send email function. So you're going to be implementing the guts of that. And we're also going to need to make sure that our environment variables available everywhere. So yeah, with that, we'll also want to actually start sending

**译文**

我们将开始发送电子邮件。因此，你需要为 Resend 服务添加 API 密钥。我们肯定会使用一个服务来完成这项工作。我们还将添加一些集成代码来实际发送电子邮件。我们将只编写一个简单的发送电子邮件函数。因此，你将需要实现该函数的核心逻辑。此外，我们还需要确保环境变量在所有地方都可用。所以，接下来我们还将真正开始发送电子邮件。

## 85. 84. Sending Emails with the Resend API using Fetch

**原文**

Let's get the environment variable set up first. We're going to go to our .env. We'll add a resend API key. This is what you would get from logging into resend and setting up your account. Then you'll find the API key in there. So it's going to be some super secret value of some kind. And then we'll go to our env server and we'll add that to our configuration here. So we get that runtime validation. Make sure that at the start of our app we have the resend API key.

**译文**

我们先来设置环境变量。我们要进入 .env 文件，添加一个 Resend API 密钥。这是你登录 Resend 并设置账户后获取的内容。然后你就能在那里找到 API 密钥。它会是一个超级机密的值。接着，我们要进入 env server，将其添加到这里的配置中。这样我们就能获得运行时验证。确保在应用启动时我们已设置好 Resend API 密钥。

## 86. 85. Mocking APIs with MSW and Testing

**原文**

We don't want to hit the real resend API during development or testing because that could potentially cost us money and it makes things a little slower and it requires an internet connection. So for all those reasons, we're going to make a mock, but we don't want to touch any of our source code. We want to try and do as many of the mocks as like a sidecar thing as possible. So we're going to use a service or a library called MSW that stands for mock service worker. Now it actually has nothing to do with server service workers the way that we're using it.

**译文**

在开发或测试期间，我们不想调用真实的重新发送 API，因为这可能会产生费用，还会让流程变慢，并且需要网络连接。因此，出于所有这些原因，我们将创建一个模拟环境，但我们不想改动任何源代码。我们希望尽可能以“旁路”（sidecar）的方式完成这些模拟。为此，我们将使用一个名为 MSW 的服务或库，它的全称是 Mock Service Worker（模拟服务工作者）。不过，就我们目前的使用方式而言，它与真正的服务工作者（Service Worker）其实毫无关系。

## 87. 86. Setting Up a Mock Server with MSW Node

**原文**

Let's get started by getting the mock server itself up and running. So we'll go to our mock index right here. And this is where we've got our file that's going to be setting up our mock service worker. We're going to bring in setup server from MSW node. And we'll take care of resend here in a little bit. We just want to get this server up and going to get it started. So we're going to call setup server. And we're going to pass in these miscellaneous handlers. This is for remixes.

**译文**

让我们先启动并运行模拟服务器本身。因此，我们将进入这里的模拟入口文件。这里是我们用来设置模拟服务工作者的文件。我们将从 `MSW` 模块中引入 `setupServer`。稍后我们再处理 `resend` 的问题。现在我们只想让这个服务器启动起来。因此，我们将调用 `setupServer`，并传入这些零散的处理器。这是用于 Remix 的。

## 88. 87. Email Verification Flow

**原文**

Now that we don't actually send emails when emails are sent, we just log the email contents to the terminal output. We can actually start building our sign up page to follow the auth flow that we want. So before you would just go to sign up and you would enter in your email and your username and all that stuff. But we want to verify the user's email before we let them finish setting up an account. Your product manager may have a different opinion about how to do this. Maybe they want to get people on

**译文**

既然我们现在发送邮件时并不会真正发送电子邮件，而只是将邮件内容记录到终端输出中，我们其实就可以开始构建注册页面，以实现我们想要的认证流程了。以前，用户只需前往注册页面，输入自己的电子邮件地址、用户名等信息即可。但我们希望在用户完成账户设置之前，先验证其电子邮件地址。你的产品经理对此可能有不同的看法，也许他们希望先让用户注册下来……

## 89. 88. User Verification Emails

**原文**

Let's go over to sign up and we'll come right here and instead of this nonsense response that we're just hard coding, we're going to await send email from our utility there. And two will be the email address that the user entered. We've got a honeypot on here. So we feel pretty confident that this will be an actual user trying to send an email. Our subject can be whatever our text can be whatever it's really not a huge deal right now what the actual email contents say. So with that, we should be good to go.

**译文**

我们过去注册一下，然后直接来到这里。不再使用硬编码的无意义响应，而是从我们的工具中调用 `await send_email`。第二个参数将是用户输入的电子邮件地址。我们在这里设置了一个蜜罐，因此我们很有信心这会是一个真正想要发送邮件的用户。主题和内容可以随意设置，目前邮件的具体内容并不重要。这样一来，我们应该就可以开始运行了。

## 90. 89. Secure Email Transfer and Storage with Cookies for Onboarding

**原文**

So we've got a little bit of a challenge here when I say bobby at example.com right now we're just sending people over to the onboarding but we need to have some mechanism to send the email address that they entered over to onboarding but there are two problems with this. Problem number one is we want to be able to verify the user's email address and like anybody could just say oh I'm just going to set it to any email address and then fill out the onboarding form and now I'm good so we have to have like some sort of process here to say hey

**译文**

所以我们现在面临一个小小的挑战。当我输入“bobby@example.com”时，目前我们只是将用户引导至“onboarding”页面，但我们需要一种机制，将他们输入的电子邮件地址发送到“onboarding”页面。不过，这里存在两个问题。第一个问题是，我们希望验证用户的电子邮件地址——因为任何人都可能随便输入一个电子邮件地址，然后填写“onboarding”表单，然后就万事大吉了。因此，我们必须建立某种流程来确认这一点。

## 91. 90. Passing Data Between Routes

**原文**

We've got a new utility right down here called the verification that server and it's actually gonna look a lot like our session server So I'm gonna copy that and paste it right here We're gonna use Ian verification as the name of our cookie these do need to be unique Otherwise, they'll override each other and also we want to set the max age for this because we want it to naturally expire after About 10 minutes. So let's set that max age right there and that is in seconds not millisecond at

**译文**

我们这儿有一个新的实用工具，叫做 verification that server，它看起来会和我们的 session server 非常相似。所以我要把它复制过来，然后粘贴到这里。我们将使用 Ian verification 作为我们 cookie 的名称，这些名称必须是唯一的，否则它们会相互覆盖。此外，我们还想为这个 cookie 设置最大存活时间，因为我们希望它在大约 10 分钟后自然过期。所以我们就在那里设置这个最大存活时间，注意这个时间是以秒为单位，而不是毫秒。

## 92. 91. Dad Joke Break Email

**原文**

How do you make a one disappear? You add G and it's gone. Some of these dad jokes actually are pretty, pretty clever. Well done. All right, this is a good time for you to take a break. So stand up, do some stretches, walk around, do something, you know, exercise in some way to get your body moving, get the blood flowing because brain needs blood flow. So take care of your brain, take care of yourself, and then come on back because we've got more to do. I'm excited to have you back.

**译文**

要怎么让一个“1”消失呢？加上一个“G”，它就消失了（gone）。这些冷笑话其实真的挺挺巧妙的。做得好。好了，现在正是你休息的好时机。所以站起来，做做拉伸，走动一下，随便做点什么，你知道的，用某种方式锻炼一下，让你的身体活动起来，让血液流动起来，因为大脑需要血液流动。所以照顾好你的大脑，照顾好你自己，然后再回来吧，因为我们还有更多事情要做。我很期待你回来。

## 93. 92. Intro to Verification

**原文**

So now we want to actually verify that a user owns the email address before we allow them to sign up. The easiest way for us to walk through this is to walk through a flow diagram. So here we have the user, server, and verification in email client. The user is going to come to our sign up form. They're going to submit their email address. And then the server is going to say, oh, OK, you want to sign up for an account with this email address. So I'm going to create a verification that's going to have some special and secret information.

**译文**

现在，我们希望在允许用户注册之前，先验证该用户是否拥有这个电子邮件地址。要理解这个过程，最简单的方式就是走一遍流程图。这里我们有用户、服务器和电子邮件客户端中的验证环节。用户会访问我们的注册表单，并提交他们的电子邮件地址。然后服务器会说：“哦，好的，你想用这个电子邮件地址注册一个账户。那么我将创建一个验证，其中包含一些特殊的保密信息。”

## 94. 93. Implementing One-Time Password Verification with Database Storage

**原文**

To get things started, we need to create a model for this in our database. We need a table for verifications that we can look up when the user says, hey, here's my code. We need to be able to verify that code. Now, we're not actually storing the code itself in the database. Again, this is a one-time password. And so we're going to store the information necessary for verifying that one-time password. So things like the digits and the period and the algorithm, the secret,

**译文**

首先，我们需要在数据库中为此创建一个模型。我们需要一个用于验证的表，以便在用户说“嘿，这是我的代码”时可以进行查找。我们需要能够验证该代码。现在，我们实际上并没有将代码本身存储在数据库中。同样，这是一个一次性密码。因此，我们将存储验证该一次性密码所需的信息，例如数字、小数点、算法以及密钥等。

## 95. 94. Creating a Verification Model in Prisma for User Verification

**原文**

So let's create this model in our schema. We've got this verification model down here. So model verification. And I'm going to let Copilot fill that in for us because there's a bit and it's pretty straightforward. I'll just explain it to you. So we've got our ID. That's just like the other models that we've got. We've got a created app to keep track of when this was created. I don't really see a whole lot of sense in an updated app because these won't typically be updated anyway. So then we also have the type. This is the type of thing that they're trying to verify. So this would be like two

**译文**

那么，让我们在模式中创建这个模型。我们这里有一个验证模型，也就是模型验证。我将让 Copilot 为我们补全这部分代码，因为这部分内容不多，而且相当直接。我来简单向你解释一下。我们有 ID，这和我们已有的其他模型一样。我们还有一个 created_at 字段，用于跟踪该记录的创建时间。我其实不太理解为什么需要一个 updated_at 字段，因为这些记录通常本来就不会被更新。接下来我们还有一个 type 字段，表示用户试图验证的内容类型。比如，这可能对应两种情况……

## 96. 95. User Verification Workflow

**原文**

Right now when the user wants to sign up, they can go to marty at example.com and it will send them right over to onboarding, but they haven't actually verified their email at this point. So we don't want to put the verified email in the verification storage until it's actually been verified. So we've actually created a slash verify route that we're going to be using. So if we go to verify, then we've got this route already set up for you by Kelly, the co-worker. Thank you, Kelly. And your job is to make it so that we

**译文**

目前，当用户想要注册时，他们可以访问 marty@example.com，然后系统会将他们直接引导至引导流程，但此时他们的电子邮件尚未真正验证。因此，我们希望在邮件真正验证之前，不要将已验证的电子邮件信息存入验证存储中。为此，我们创建了一个 `/verify` 路由，并将要使用它。如果我们访问 `/verify`，那么同事 Kelly 已经为你设置好了这个路由。谢谢你，Kelly。而你的任务是让它能够实现以下功能：

## 97. 96. Generating One-Time Passwords and Verification URLs in a Signup Flow

**原文**

So let's go to our signup route. And right here, we're going to generate our one-time password. So here we'll say generate tootp. That's come from Epic Web tootp. And we want to specify the algorithm as SHA-256. It's more secure than the default of SHA-1. SHA-1 is the default because one-time password generators like Google Authenticator and one password, they default to SHA-1. And in some cases, don't even work with any other algorithm.

**译文**

那我们来到注册路由。就在这里，我们将生成一次性密码。这里我们调用 `generateTOTP`，它来自 `EpicWebTOTP`。我们需要将算法指定为 SHA-256。它比默认的 SHA-1 更安全。之所以默认使用 SHA-1，是因为像 Google Authenticator 和 OnePassword 这样的一次性密码生成器默认都使用 SHA-1，而且在某些情况下，它们甚至无法使用其他算法。

## 98. 97. Implementing User Code Verification with TOTP

**原文**

All right, it's time to actually implement this thing. So what we're going to be doing in this step of the exercise is we need to grab the code that the user has submitted in addition to all of the other data that we have in the URL search prams to actually verify that the user is submitting the proper code. So we're going to have to look in the database for the target and type combo and then verify the one time password that

**译文**

好的，现在是时候真正实现这个功能了。在本练习的这一步骤中，我们需要获取用户提交的代码，并结合 URL 搜索参数中的其他所有数据，来验证用户是否提交了正确的代码。因此，我们将在数据库中查找目标与类型的组合，然后验证一次性密码。

## 99. 98. Verification Flow and Dynamic Query Parameters

**原文**

Let's go over to the verify route and right up here we're going to add the type because we do set the type in our query params up here, but we don't actually render the type and we could just hard code it as onboarding, but we know that we're going to be having other verification types. We're going to add two factor authentication and stuff like that. So we're going to add a type query param here. Export const type query param. This is going to be the type and then we're going to need a schema.

**译文**

我们转到 verify 路由，就在上方这里添加 type，因为我们在上方的查询参数中确实设置了 type，但我们并没有实际渲染它。我们可以直接将其硬编码为 onboarding，但我们知道将来还会有其他验证类型，比如双因素认证等。因此，我们要在这里添加一个 type 查询参数。导出 const typeQueryParam。这将是 type，然后我们还需要一个模式。

## 100. 99. Dad Joke Break Verification

**原文**

New atoms frequently lose electrons when they fail to keep an eye on them.

**译文**

新原子在疏于看管时，常常会失去电子。
