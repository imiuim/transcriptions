# Kent C. Dodds - Epic Web. Ship Modern Full-Stack Web Applications part5

- 来源：[B站 BV1RZVtzWEJ6](https://www.bilibili.com/video/BV1RZVtzWEJ6)（up 主：lmt831，共 78 P）
- 说明：英文转录 + 中文翻译（机器翻译，仅供学习参考）

---

## 01. 28. Effective Error Handling and Console Capture Testing

**原文**

So the first thing I'm going to do is I'm going to go to the test config and I'm going to say restore mocks true. So by default at the end of every test or before the test start at some point between tests, the all the mocks that were created will be restored. I think this is a great default. And so we're going to enable it by default. We restart due to config changes. And now we are in a solid position. So we can come in here and delete this. We no longer need to do that cleanup, which is nice. That doesn't necessarily mean that you can

**译文**

所以我要做的第一件事就是进入测试配置，然后设置 `restoreMocks` 为 `true`。默认情况下，在每次测试结束时或测试开始前（即在两次测试之间的某个时间点），所有创建的模拟对象都会被恢复。我认为这是一个很棒的默认设置。因此，我们将默认启用它。由于配置更改，我们重启了测试环境。现在我们已经处于一个稳定的状态了。因此，我们可以到这里把这个删掉。我们不再需要执行那样的清理操作了，这很好。但这并不一定意味着你就可以

## 02. 29. Creating a Setup File for Test Environment Setup

**原文**

I want this everywhere. I want to put this stuff in a place that is automatically included for all of the files in my test, or all my test files in my application. So we need to move this to a setup file and then update our vTest config to automatically require or import that file for all of our tests. So that is your task in this exercise is to create that setup file and then we've got a couple other things that we want to think about for that setup file.

**译文**

我希望这段代码能在全局生效。我想把这些内容放在一个位置，让它能够自动包含到我测试中的所有文件，或者应用程序中的所有测试文件里。因此，我们需要将这些内容移动到一个设置文件中，然后更新我们的 vTest 配置，以便自动要求或导入该文件以供所有测试使用。所以，本次练习中你的任务就是创建这个设置文件，此外我们还需要考虑该设置文件的另外几个问题。

## 03. 30. Setting Up Test Environment and Utilizing Setup Files with VTest

**原文**

A good place to put this would be in our test directory right here. And inside of this test directory, we've got a couple things already. We're going to make a new directory called setup. And inside of that, we'll have a setup test ENV. So this is our test environment. And inside of this, we're going to take a couple of the things that we've got that are like part of our setup for our server. So the environment that we're setting up. So we've got our dot ENV config. So this will import all of our environment very well.

**译文**

一个合适的位置就是放在我们这里的测试目录中。在这个测试目录里，我们已经有一些东西了。我们将创建一个新的目录，命名为 setup。然后在这个目录中，我们会创建一个 setup 测试环境。这就是我们的测试环境。接下来，我们会把一些属于服务器设置的部分内容移到这里。也就是我们正在设置的环境。我们有我们的 .ENV 配置文件，它会很好地导入我们所有的环境配置。

## 04. 31. Dad Joke Break Unit Test

**原文**

Why do crabs never give to charity? Because they're shellfish. Ha ha ha. You should give to charity. It's a good thing. We're very blessed. Wherever you're at in your life, there are always people who are worse off. And that is just kind of a sad situation. But, yeah, doing good things for other people is just a really nice thing to do. It makes the world a better place. And so I hope that you are making the world a better place. I'm trying to. And together we can make the world better. And it'll be awesome. But right now it's time to take a break.

**译文**

为什么螃蟹从不捐款？因为它们太“壳”善（shèlì）了。哈哈哈。你应该去捐款。这是一件好事。我们真的很幸运。无论你处于人生的哪个阶段，总有人过得比你好。这实在有点令人难过。不过，为别人做些好事，真的是一件很棒的事。它能让世界变得更美好。所以我希望你也正在让世界变得更美好。我正在努力。只要我们齐心协力，就能让世界变得更好。那一定会很棒。不过现在，该休息一下了。

## 05. 32. Intro to Component Testing

**原文**

Okay, who's ready to learn about component testing? We're gonna be testing components. It's gonna be awesome. So as part of this exercise, I want you to think about two users in particular. The end user who's gonna be clicking the buttons of the components that you're rendering and or just visually seeing or through a screen reader seeing the different elements that you're rendering. And then the developer user that's going to be rendering your component. They're using the JSX syntax with your component.

**译文**

好的，谁准备好学习组件测试了？我们将要对组件进行测试。这一定会很棒。因此，作为本次练习的一部分，我希望你们考虑两类特定的用户。一类是最终用户，他们将点击你们所渲染的组件中的按钮，或者只是通过视觉方式，亦或是通过屏幕阅读器来查看你们所渲染的各种元素。另一类是开发者用户，他们将渲染你们的组件。他们会使用 JSX 语法来使用你们的组件。

## 06. 33. Error List Component with React Testing Library

**原文**

In this exercise, we're going to be testing the error list component. So it's rendering JSX. We need to be able to render that JSX in the same way that it's going to be rendered in our application. That is to the DOM. Now, we're going to be using a library called testing library or React testing library for this. I wrote this a few years ago to make testing react a lot easier and it is. It's great. So you're going to be able to use React testing library to test this component. We've got a couple of cases here.

**译文**

在本练习中，我们将测试错误列表组件。该组件会渲染 JSX。我们需要以与应用程序中相同的方式渲染这些 JSX，也就是将其渲染到 DOM 中。为此，我们将使用一个名为 testing library 或 React testing library 的库。我几年前编写了这个库，它让 React 测试变得简单得多，事实也的确如此。它非常棒。因此，你将能够使用 React testing library 来测试这个组件。这里有几个测试用例。

## 07. 34. Testing React Components with JSDOM

**原文**

So let's pop open this file and we need to add a JS DOM comment pragma at the top. So by default, our tests are all running in Node, but for this particular test, even though we can server render React components and stuff, we're typically concerned about the client-side render of our components. And more often than not, you're going to want to test user events and stuff like that. So we're going to add the JS DOM or the VTest environment to GDM.

**译文**

那么，我们先打开这个文件，需要在顶部添加一个 JS DOM 注释声明。默认情况下，我们的所有测试都是在 Node 中运行的，但对于这个特定的测试来说，尽管我们可以对 React 组件等进行服务器端渲染，但我们通常更关心的是组件的客户端渲染。而且大多数时候，你都会希望测试用户事件之类的操作。因此，我们将 JS DOM 或 VTest 环境添加到 GDM 中。

## 08. 35. Proper DOM Cleanup for Reliable Testing

**原文**

So Kelly finished the test for us and feel free to delete these tests and write them yourself if you want to practice. But they're not working. There's a problem with them and it has to do with the fact that we're mucking with the DOM and not cleaning up after ourselves. So your task is to handle the cleanup. This will be pretty quick. We'll see you when you're done.

**译文**

所以 Kelly 已经帮我们完成了测试，如果你想要练习，随时可以删除这些测试并自己编写。但它们目前无法正常运行。测试中存在一个问题，这与我们操作 DOM 后没有进行清理有关。因此，你的任务是处理清理工作。这部分会很快完成。等你完成后我们再见。

## 09. 36. Ensuring Isolation and Proper Test Execution

**原文**

So we've got a failing test. Let's take a look at what that failing test looks like. So it shows nothing. We've given an empty list. That works. It shows a single error. And then once we say shows multiple errors, and that's a problem. Now you might think at first glance that, okay, so this test is the one that has the problem. But check this out. If I say, all right, I want to do this one only dot only that. And now it's suddenly passing. That is a great sign that you are not cleaning up after yourself in another test. If it fails when it's run with other tests, but then six

**译文**

所以我们遇到了一个失败的测试。让我们来看看这个失败的测试是什么样子。它显示什么都没有。我们提供了一个空列表，这没问题。它显示了一个错误。然后当我们说“显示多个错误”时，问题就出现了。现在你可能乍一看会认为，好吧，就是这个测试有问题。但请看这个。如果我说，好的，我只想单独运行这个测试。现在它突然通过了。这是一个非常好的迹象，表明你在另一个测试中没有清理好自己的状态。如果它在与其他测试一起运行时失败，但随后又……

## 10. 37. Dad Joke Break Component Test

**原文**

Why did the cookie cry? It was feeling crummy. Okay, that yeah, that one's pretty bad. But yeah, maybe now's a good time to go grab a cookie because it's break time. Go take a break and come back because we're not done.

**译文**

为什么饼干哭了？因为它感觉很糟糕。好吧，是的，这个笑话确实挺冷的。不过，现在或许正是去拿块饼干的好时机，因为已经到了休息时间。去休息一下再回来吧，因为我们还没结束呢。

## 11. 38. Intro to Hooks

**原文**

Sometimes you've got low level hooks that you want to test because they're pretty complicated or they're just really critical to the business or something. And so you want to have like a couple of tests that are specific for this hook. And so there are actually two approaches that we can take and they both make sense in some scenarios. So we're going to go through both of them. The first is just here is an example using useCounter, pretty simple thing. But the first is to use the render hook utility from testing library react.

**译文**

有时，你有一些底层钩子需要测试，因为它们相当复杂，或者对业务至关重要。因此，你可能希望编写一些专门针对这个钩子的测试。实际上，我们有两种方法可以采用，这两种方法在特定场景下都很有道理。接下来，我们将逐一介绍这两种方法。第一种方法如下：这里有一个使用 `useCounter` 的简单示例。第一种方法是使用 React Testing Library 提供的 `renderHook` 工具。

## 12. 39. Double Confirmation Feature

**原文**

We have this feature where users can upload and change and delete their profile photo. And we want to make sure that they don't accidentally delete their photo, like just by accidentally clicking on the button. So we're going to kind of double check and make sure that they know what they're about to do. And because it's a destructive operation and be a pain for them to have to go find their profile photo again and upload it. And often what people will do is they'll have this big modal that pops up and that works especially to vary if it's a

**译文**

我们有一个功能，允许用户上传、更改和删除自己的头像。我们希望确保用户不会意外删除头像，比如不小心点击了按钮。因此，我们将进行二次确认，确保用户清楚自己即将执行的操作。由于这是一个破坏性操作，如果用户需要重新寻找并上传头像会很麻烦。通常，人们会采用一个弹出式的大模态框来实现这一点，这种方式尤其有效，特别是当它……

## 13. 40. Testing Custom React Hooks with RenderHook and Act

**原文**

All right, let's open up our use double check test. And here we're going to get our result from awaiting, wait render hook from testing library react, and we're going to call use double check from our utilities. So this result is going to have a current property on it. And you might say, well, Kent, why doesn't it just return exactly what this use double check returns? Why do we have to have this current intermediate intermediary? And the reason

**译文**

好的，让我们打开我们的 useDoubleCheck 测试。在这里，我们将从 `@testing-library/react` 的 `wait` 钩子中等待并获取结果，然后调用我们工具库中的 `useDoubleCheck`。因此，这个结果会有一个 `current` 属性。你可能会问，Kent，为什么它不直接返回 `useDoubleCheck` 的实际返回值呢？为什么我们需要这个中间的 `current` 属性？原因如下：

## 14. 41. Custom Test Components vs Render Hook Utility

**原文**

There are a couple things that I'm not super jazzed about this hook test. And so I want to show you how to test the hook using a test component. A test component is actually sort of what the render hook utility is doing under the hood, but in a way that isn't at all specific to your hook. And so everything is communicated through this result.current object here. And so what you can do with a custom

**译文**

对于这个钩子测试，有几点我并不太满意。因此，我想向你展示如何使用一个测试组件来测试这个钩子。测试组件实际上就是 `renderHook` 工具在底层所做的工作，但它的方式完全不依赖于你具体的钩子。所有信息都是通过这里的 `result.current` 对象来传递的。因此，你可以对自定义钩子做如下操作：

## 15. 42. Testing React Hooks

**原文**

The first step here is we need to make a test component. So let's make this function called test component. And then we're going to need to manage some state to communicate to the outside world what the current state of our internal state is. So we are going to get our double check from use double check. But then we need to maintain some state to determine like this stuff that we need to assert on. And so if we look at our hook test,

**译文**

第一步是创建一个测试组件。因此，我们先创建一个名为 test component 的函数。然后，我们需要管理一些状态，以便向外部世界传达我们内部状态的当前情况。因此，我们将从 use double check 中获取双重检查功能。但随后，我们还需要维护一些状态，以确定需要断言的这些内容。因此，如果我们查看我们的 hook 测试，

## 16. 43. Dad Joke Break Hooks

**原文**

I think circles are pointless. Haha. All right, this is a good time to take a break. Do some stretches, get some water, and go to the bathroom. Go give somebody a high five and tell them that they're awesome. And whatever it is that you do to fill somebody else's day with joy, which, you know, is a little selfish because it actually fills your day with joy too. So go do something like that and then come back because we're still learning here.

**译文**

我觉得圆圈毫无意义。哈哈。好了，现在正是休息的好时机。做一些拉伸运动，喝点水，去趟洗手间。去和别人击掌，告诉他们他们真的很棒。无论你想做什么来点亮他人的这一天——你知道的，这其实也有点自私，因为它同样也会点亮你的一天。所以，去做点类似的事情吧，然后再回来，因为我们还在继续学习呢。

## 17. 44. Intro to Testing Remix

**原文**

So you've got a remix route or you've got a component that uses the link element or a form or use submit or any of these remix C things. You need to be able to provide the same sort of things that remix provides to those components and those hooks so that they can operate efficiently. So in this example, we've got this use loader data. Where does that loader data come from? Well, it comes from remix. The remix is keeping track of all the data that you're loading into your application. And you need to have that provide

**译文**

所以你有一个 remix 路由，或者你有一个使用了 link 元素、表单、submit 或任何其他 remix C 相关功能的组件。你需要能够为这些组件和钩子提供与 remix 所提供的相同类型的内容，以便它们能够高效地运行。因此，在这个例子中，我们有这个 use loader data。这个 loader data 来自哪里呢？它来自 remix。remix 正在跟踪你加载到应用程序中的所有数据。而你也需要提供这些数据。

## 18. 45. Creating a Stub for Testing Component Logic in Remix

**原文**

So here we've got our username route and if we are not logged in then it's just going to say when the user joined it'll say their name it'll have their avatar and it will have a link to their notes but if we log in as this user and then go to there then we're also going to get a logout button and an edit profile button. So there's right there we've got some logic and having some logic for this sometimes it makes sense to do at a lower level than an end-to-end test especially when you get into

**译文**

这里我们有一个用户名路由。如果用户未登录，页面会显示用户加入时的名称、头像，并提供一个指向其笔记的链接。但如果我们以该用户身份登录后再访问此页面，还会看到一个退出登录按钮和一个编辑个人资料按钮。因此，这里我们实现了一些逻辑。对于这类逻辑，有时在比端到端测试更低的层级进行测试会更合理，尤其是当你开始涉及……

## 19. 46. Rendering Components with Mock Data

**原文**

Right from the get go, we're getting an error. Uncaught error, use loader data must be used within a data router. So if we go into here and take a look at the component that we're rendering, right there, that's the use loader data that needs to be rendered within a data router. So to be able to do that, we need to bring in createRemixStab, which is going to be able to create a fake version of the remix app for us. So we create the step right here. We're going to say our app.

**译文**

从一开始，我们就遇到了一个错误。未捕获的错误提示：`useLoaderData` 必须在数据路由器（data router）内部使用。因此，如果我们进入这里并查看正在渲染的组件，就在我们刚才看到的位置，那个 `useLoaderData` 必须在数据路由器中才能渲染。为了实现这一点，我们需要引入 `createRemixStub`，它能为我们创建一个模拟版的 Remix 应用。所以我们在这里创建这个步骤，并指定我们的应用。

## 20. 47. Creating a Parent Route for Accessing Root Data

**原文**

We've got another test that Kelly put together for us for the authenticated side of this and the it's not working right now. It's failing for us. And the reason that it's failing is because to determine whether the user that is viewing this profile is the logged in user that they're looking at their own profile is based on this use optional user hook. If we dive into that, that use optional user hook is calling use route loader data for the route. And yeah, that ID

**译文**

我们又收到了一个由 Kelly 为我们准备的测试用例，用于测试认证相关的部分，但目前它无法正常工作。该测试正在失败。失败的原因是：要判断当前查看该配置文件的用户是否就是正在查看自己配置文件的已登录用户，其依据是这个 `useOptionalUser` 钩子。如果我们深入查看，会发现这个 `useOptionalUser` 钩子调用了 `useRouteLoaderData` 来获取路由数据。是的，就是这个 ID。

## 21. 48. Creating Routes and Context in Remix

**原文**

So what we need to do is create another route and this is going to be our route route and it actually does need an ID because that's how we identify it. So we'll call it route, not root, route. And remix actually gives an ID to our routes. We don't normally have to do that, but in this case, because we rely on that ID, we need to specify that here. So then we're going to have a path be slash and our loader is going to have to be the awaited version of the return.

**译文**

所以我们需要做的是创建另一个路由，这将是我们的 route 路由，而且它确实需要一个 ID，因为这是用来识别它的方式。所以我们把它命名为 route，而不是 root，是 route。Remix 实际上会为我们的路由分配一个 ID。我们通常不需要这样做，但在这种情况下，因为我们依赖这个 ID，所以需要在这里进行指定。然后，我们将有一个路径为斜杠，而我们的 loader 则必须是 await 版本的返回值。

## 22. 49. Dad Joke Break Testing Remix

**原文**

Why are fish so smart? Because they live in schools. All right. My kids are in school right now. In fact, I think one of my kids just got home from kindergarten. And so I'm going to go up and say hi to them because it's break time. So go take a break. Go say hi to your family, your loved ones. Send somebody a text and tell them that you were thinking of them and you think that they're just a great person. Brighten somebody's day and feel awesome about yourself because you're doing great. Keep it up. We'll see you when you get back.

**译文**

鱼为什么这么聪明？因为它们成群结队地生活。好吧，我的孩子们现在正在上学。事实上，我觉得其中一个孩子刚从幼儿园回来。所以我现在要上去跟他们打个招呼，因为现在是休息时间。所以，去休息一下吧。去跟你的家人、你所爱的人问好吧。给某人发条短信，告诉他们你正在想着他们，你觉得他们是个很棒的人。让某个人的心情变得晴朗起来，同时也会让你自己感觉很棒，因为你做得很好。继续加油。等你回来时我们再见。

## 23. 50. Intro to Http Mocking

**原文**

All right, it's time to mock things again. We're going to be mocking HTTP and you've already done this a couple of times with MSW and we're going to continue to use MSW for this. But there are a couple of considerations that we need to address in this test. So, again, the more your tests resemble the way your software is used, the more confidence they can give you. That is 100% true. However, for being reasonable, like we do have to fake things out in some situations. And so like if their system goes down,

**译文**

好的，又到了模拟测试的时间。这次我们要模拟 HTTP 请求，你之前已经用 MSW 做过几次了，这次我们仍将继续使用 MSW。不过，在本次测试中，我们还需要考虑几个问题。再次强调，你的测试越接近软件的实际使用方式，就越能给你带来信心——这一点是绝对正确的。然而，为了保持测试的合理性，在某些情况下我们确实需要模拟一些场景。比如，如果他们的系统宕机了，

## 24. 51. GitHub Sign-In Callback

**原文**

With the way that we have our mock set up already, when you go to sign in with GitHub, that will actually sign you in as Kodi. Because Kodi already has an association in the database, a connection with a GitHub user that we have mocked as like our mock login for this GitHub. So if you want to test the thing manually that we're going to test here in a moment, then you'll have to come over here to the sign up page. Let's pop open our network tab. We'll change this to someone else.

**译文**

按照我们目前的模拟设置，当您使用 GitHub 登录时，系统实际上会以 Kodi 的身份登录。因为 Kodi 在数据库中已经存在一个关联，即与我们为 GitHub 模拟登录所创建的 GitHub 用户的连接。因此，如果您想手动测试我们稍后将在此处测试的功能，就需要前往注册页面。现在，我们打开网络选项卡，然后将这个用户更改为其他人。

## 25. 52. Testing OAuth2 Flow and Mocking GitHub API Responses

**原文**

So let's go to our Auth provider callback test. And there are a couple of things that we need to make sure that we're doing. So first of all, when we go through this Auth process, we're going to be talking to the GitHub API. Now for development, we already put together a GitHub mock. So if we go to GitHub under our mocks, we've got a mock here already for dealing with that API during development. We developed this already. But we need to make sure that we have the mocks running in our tests. So if we go to our index and TS,

**译文**

那么，我们来看看 Auth 提供程序回调测试。有几个地方需要确保我们做对了。首先，当我们执行这个 Auth 流程时，会与 GitHub API 进行交互。在开发阶段，我们已经创建了一个 GitHub 模拟模块。因此，如果我们进入 mocks 文件夹下的 GitHub 部分，会发现这里已经有一个用于在开发期间处理该 API 的模拟模块。我们已经完成了这个模块的开发。但我们需要确保在测试时这些模拟模块能够运行。所以，如果我们转到 index.ts 文件，

## 26. 53. Testing Error Handling in GitHub API Interceptor

**原文**

The way we've gotten this written is that anytime anybody asks us for any access token, we will gladly create a new GitHub user for them and return a access token. So it's not exactly the way that the GitHub API actually works, but it works really well for our local development. So the trick is we want to, like we do have logic for what happens if we can't get an access token, if there's some sort of problem there, like maybe GitHub is down or the code that was provided is invalid.

**译文**

我们实现这一功能的方式是：每当有人向我们请求访问令牌时，我们都会很乐意为其创建一个新的 GitHub 用户，并返回一个访问令牌。虽然这并非 GitHub API 的实际工作方式，但对于我们的本地开发来说效果非常好。因此，关键在于我们需要处理无法获取访问令牌的情况——例如，当出现某些问题（比如 GitHub 宕机或所提供的代码无效）时，我们也需要有相应的逻辑来应对。

## 27. 54. Testing Error Handling and Assertions with Mock API Calls

**原文**

We borrowed a lot of stuff from the previous test. This should look kind of familiar. We're going to make a utility out of this a little bit later. But we want things to behave a little differently now. So instead of sending users off to onboarding, we want them to go to login. So let's add that assertion here so we get our test failing first. So assert redirect, the response should go to login. Now that response is going to come from this. And I happen to know also that when there's an error, we throw a response object.

**译文**

我们从之前的测试中借用了很多东西。这段代码看起来应该有点眼熟。我们稍后会把它做成一个工具。但现在我们希望行为稍有不同。因此，我们不希望将用户引导至引导流程，而是希望他们前往登录页面。所以，我们在这里添加这个断言，让我们的测试先失败。因此，断言重定向，响应应该跳转到登录页面。现在，这个响应将来自这里。而且我恰好知道，当出现错误时，我们会抛出一个响应对象。

## 28. 55. Streamlining Repetitive Test Setup for Optimal Efficiency

**原文**

Another important testing principle is avoiding repeating yourself, but not going so far into like dry. Don't repeat yourself. You want to avoid hasty abstractions. But that said, there are definitely some abstractions that we can very clearly see in here. There's some setup for having an authenticated request, like a request that's all set up with the GitHub auth flow being ready. And so that would be really nice to have as a separate function. And the reason

**译文**

另一个重要的测试原则是避免重复自己，但也不要过度追求所谓的“干燥原则”。不要重复自己。你希望避免草率的抽象。话虽如此，我们确实可以在这里清楚地看到一些抽象。例如，有一些用于发起经过身份验证的请求的准备工作，比如一个已经通过 GitHub 身份验证流程设置完毕的请求。因此，如果能将这些工作作为一个独立的函数来提供，那就非常好了。而原因就在于

## 29. 56. Efficient Code Organization with Setup Functions

**原文**

So I normally put these types of setup file or functions toward the bottom of the file. That's like, it reads like a newspaper article where the most important stuff is at the top. And then as things get more implementation detail specific or just more explicit, that comes down toward the bottom. And the reason they used to do that, or maybe some newspaper organizations or article organizations still do this, the reason they would do that is so that the editor could just come in and snip out the whatever part of the article

**译文**

所以我通常会把这类配置文件或函数放在文件的底部。这就像阅读一篇新闻报道，最重要的内容放在顶部。而随着内容变得越来越具体、偏向实现细节或更加明确，这些内容就会逐渐向下排列。他们过去之所以这样做，或者也许某些报社或文章组织至今仍沿用这种做法，原因就在于编辑可以直接进来，把文章的某个部分剪切掉。

## 30. 57. Dad Joke Break Http Mocking

**原文**

Did you hear about the runner who was criticized? He just took it in stride. Haha. Actually, you know, stop criticizing people. You know, if they invite your criticism or your feedback, then that's great. But if this is a person that you have no really established relationship with, and they certainly, if they didn't ask for any of your feedback, then like just let it slide. Let people be the people that they are. If they ask for your feedback,

**译文**

你听说过那个被批评的跑步者吗？他只是泰然处之。哈哈。其实，你知道吗，别再批评别人了。你知道的，如果他们邀请你提出批评或反馈，那当然很好。但如果你和这个人并没有真正建立关系，而他们显然也没有征求你的任何意见，那就随它去吧。让人们做他们自己就好。如果他们征求你的意见，

## 31. 58. Intro to Auth Integration

**原文**

Okay, we're at the integration level and we want to do authenticated requests. And so there are a couple of things you have to do to make this work. All of our loaders and actions are talking directly to a database and you could mock out that database if you want to. There's definitely some situations where that makes sense, but not very many. It's awful, awful, awful to mock out a database. And so what you can do instead is just set up the database and use the actual database and just make sure you're cleaning up after yourself. Now, at this level of tests where you're

**译文**

好的，我们现在处于集成测试层面，并希望执行经过身份验证的请求。为此，你需要完成几项工作。我们所有的加载器和操作都直接连接数据库，如果你愿意，也可以对这个数据库进行模拟。在某些情况下这样做确实有道理，但这种情况并不多见。模拟数据库是一件非常非常糟糕的事情。因此，你可以选择直接配置数据库并使用真实的数据库，同时确保测试结束后清理相关数据。现在，在你进行这种级别的测试时，

## 32. 59. Testing Authenticated Requests and Connection Creation

**原文**

So far we've tested the situation where things fail to authenticate and we've also tested the situation down here where we send the user to onboarding. But now we're going to test when a user is logged in, it creates a connection. So we need to create a authenticated request. So this request needs to have all of the cookies necessary or the cookie for the session to identify a living and existing session. So you're going to be creating a real session

**译文**

到目前为止，我们已经测试了验证失败的情况，也测试了下面这里将用户引导至引导流程的情况。但现在，我们要测试用户登录时会创建连接的情形。因此，我们需要创建一个经过身份验证的请求。这个请求必须包含所有必要的 Cookie，或者包含用于识别有效且存在的会话的会话 Cookie。所以，你将需要创建一个真实的会话。

## 33. 60. Creating and Authenticating Users for Connection Setup

**原文**

All right, so for us to be able to be logged in and create a connection, we're going to be creating users. We need to have a user to be logged in as. And for us to be able to create a connection, we need to create a connection with a GitHub user that does exist and that our mock will respond to. So there are a couple of things we're going to need to do as part of our setup. First of all, let's get a GitHub user with await insert GitHub user from our mock. Now we'll add it to the list of users that

**译文**

好的，为了能够登录并建立连接，我们需要创建用户。必须有一个用户用于登录。而为了能够建立连接，我们需要与一个真实存在的 GitHub 用户建立连接，并且我们的模拟程序能够响应该用户。因此，在设置过程中，我们需要完成几件事情。首先，让我们通过 `await insertGitHubUser` 从模拟程序中获取一个 GitHub 用户。现在，我们将它添加到用户列表中。

## 34. 61. Assertions for GitHub Login Session Creation

**原文**

We've got a couple situations where the user uses the GitHub login to actually create a session and we want to make an assertion on that. So we've got a couple assert session made for our tests like when a user exists with the same email, connect the account, make a session, another one for right here. If the user is not logged in, but the connection is this, make a session so they're logging in with GitHub. So I want you to write this assert session

**译文**

我们有几种情况，用户通过 GitHub 登录来实际创建一个会话，而我们希望对此进行断言。因此，我们为测试编写了几个 `assert session` 用例，例如：当用户已存在相同邮箱时，连接账户并创建一个会话；另一个用例则针对当前场景。如果用户未登录，但连接状态为这种情况，就创建一个会话，使其通过 GitHub 登录。因此，我希望你编写这个 `assert session`。

## 35. 62. Verifying Session Creation and User Authentication

**原文**

So the first thing we want to do is get the cookie out of the response. So our set cookie header from response dot headers dot get cookie or set cookie. So this is the response from the server to the client. They're going to send set cookie headers for setting the session cookie. Okay, so then let's make sure that that cookie exists because this could return null. So we'll just make sure that the set cookie header has been set.

**译文**

首先，我们要从响应中获取 Cookie。因此，我们需要从 `response.headers.get("cookie")` 或 `response.headers.get("set-cookie")` 中获取设置 Cookie 的标头。这是服务器返回给客户端的响应。服务器会发送 `set-cookie` 标头来设置会话 Cookie。好的，接下来我们要确保这个 Cookie 存在，因为它可能会返回 `null`。因此，我们只需确认 `set-cookie` 标头是否已经被设置。

## 36. 63. Integrating Real Database with User Routes

**原文**

Now let's bring some of this database goodness to our route that we were testing earlier. This is our username route. We already have the test in here for the user profile when not logged in and the user profile when you are logged in. And so instead of doing this, create fake user, I want you to delete that and create an actual user. We're going to use a couple of utilities to insert that. And we already have the setup stuff to handle cleanup for everything now. So you can insert users as you please and

**译文**

现在，让我们把一些数据库的强大功能应用到我们之前测试的路线中。这就是我们的用户名字路线。我们已经在这里测试了未登录状态下的用户配置文件以及登录后的用户配置文件。因此，不要执行“创建虚拟用户”这一步，我希望你将其删除并创建一个真实的用户。我们将使用几个工具来插入该用户。而且我们现在已经有处理所有清理工作的设置。因此，你可以根据自己的需要插入用户，并且

## 37. 64. Authentication in Database Integration Tests

**原文**

So now we're going to delete this fake user, create fake user stuff. And instead, we're going to create a new user using that insert user. So here's our user equals await insert new user from the DB utils. And our setup function is already handling deleting that user. So that works out nicely for us. And then we need to get a image so that we can add an image to this user, because that's part of what we're testing is that they have an image.

**译文**

现在我们要删除这个假用户，创建一些假用户相关的东西。取而代之的是，我们将使用那个插入用户的函数来创建一个新用户。所以这里我们写：`user = await insert_new_user()`，它来自 `DB utils`。我们的 `setup` 函数已经处理了删除该用户的事情，所以这对我们来说非常方便。然后我们需要获取一张图片，以便为这个用户添加图片，因为我们要测试的内容之一就是用户是否拥有图片。

## 38. 65. Dad Joke Break Auth Integration

**原文**

What musical instrument is found in the bathroom? A tuba toothpaste. Haha. All right, so actually you got a comment on that. You know, it's kind of like a trope or a meme to say that, you know, spouses who disagree on how you squeeze the toothpaste are going to have like a really hard time they always argue about, no, squeeze it from the middle, no, squeeze it from the back. And it's this big thing, my wife and I disagree on this. And we have two tubes of toothpaste in there. It's not like we're going to, the toothpaste is going to expire before we finish it all by ourselves.

**译文**

浴室里有什么乐器？答案是“ tuba 牙膏”（Tuba 与“ tube”谐音）。哈哈。好吧，其实你对此还有评论。你知道的，这有点像一种老生常谈或网络迷因：夫妻之间如果对于如何挤牙膏意见不合，就会遇到大麻烦——他们总是争论不休：“不，要从中间挤！”“不，要从后面挤！”这竟然成了件大事。我妻子和我在这方面就有分歧，所以我们那里放着两支牙膏。我们又不是非得在牙膏过期前把它全部用完。

## 39. 66. Intro to Custom Assertions

**原文**

So we've got a bunch of assert functions in our test and I'm not a super fan of those. I like the actual assertions that are built in. Well, it turns out that we can turn these things into our own assert function. So if we had this example of assert logged in where we're looking for a link that says the user's name and a link or a button that says log out and that's how we determine that the user's logged in, then this is how you might implement that.

**译文**

在我们的测试中，我们使用了一大堆 `assert` 函数，而我并不是特别喜欢这些。我更喜欢那些内置的断言功能。不过，事实证明，我们可以将这些功能封装成我们自己的 `assert` 函数。例如，在“已登录”这个示例中，我们期望看到一个显示用户名称的链接，以及一个显示“退出登录”的链接或按钮，并以此来判断用户是否已登录。那么，这就是实现这一功能的一种方法。

## 40. 67. Custom Matchers for Assertions

**原文**

So you know these assertions that we've got down here where we have assert to sent and session made and assert redirect, they don't really match the style of the expect assertion library. And you can actually make your own mattress. In fact, we're using some of those in our, let's see, double check test right here. So we've got some custom mattress right here to have text content. That's a custom matcher that comes from just DOM. And so we can make our own custom mattress for our own application that

**译文**

你知道，我们下面这些断言——比如 `assert to sent`、`session made` 和 `assert redirect`——它们其实并不太符合 `expect` 断言库的风格。实际上，你可以自己编写自定义的匹配器。事实上，我们在当前的“双重检查测试”中就使用了一些这样的匹配器。这里有一些自定义的匹配器，用于检查文本内容。这是一个源自 DOM 的自定义匹配器。因此，我们也可以为自己的应用程序编写自定义的匹配器。

## 41. 68. Custom Assertions with Jest's Expect Library

**原文**

All right, let's extend expect with a customer search in call to have redirects. And this is going to take a response and a redirect to let's also get our types going in here. Here's our template that we're going to have this called to have redirect. And it's going to accept a response and a redirect to but the first argument in your matcher is not represented in this type. We don't actually

**译文**

好的，让我们通过添加客户搜索功能来扩展 expect，以支持重定向。这将需要一个响应和一个重定向。同时，我们也需要在这里处理类型。这是我们将要使用的模板，用于处理重定向。它将接受一个响应和一个重定向，但你的匹配器中的第一个参数并未在此类型中表示。我们实际上并没有……

## 42. 69. Dad Joke Break Custom Assertions

**原文**

Toasters were the first form of pop-up notifications. There it is again. Toasters, you have toasts in a web application. We are misappropriating a bunch of terms that regular human beings like cookies and toasters and like toasts and all like so many things that we just decide, oh, we're gonna call that in computer science and now there's confusion. Anyway, there you go. You have toasters. Maybe this is a good time to go grab yourself

**译文**

“Toast”（弹出提示）是最早的弹出通知形式。它又来了。在 Web 应用中，你有“toast”。我们正在挪用一堆普通人类熟悉的术语，比如 Cookie、Toast 和 toast（烤面包片）等等。我们决定，哦，我们就在计算机科学里这么叫吧，结果现在造成了混淆。不管怎样，就是这样。你有“toast”了。也许现在正是去给自己拿一个的好时机。

## 43. 70. Intro to Test Database

**原文**

Now it's time to improve our database setup. So right now all of our integration tests that talk to the database are talking to our development database and That is just not my favorite thing. I already talked about how I like my end-to-end test to use the real database and that's because I like Running the end-to-end tests alongside the actual development and I kind of use the end-to-end test I kind of help me with development So it just makes sense for those to use the same database and as long as I'm keeping track of everything and cleaning up after myself then that normally isn't too much

**译文**

现在是时候改进我们的数据库设置了。目前，所有与数据库交互的集成测试都连接的是我们的开发数据库，而这并不是我喜欢的做法。我之前已经提到过，我希望端到端测试使用真实的数据库，因为我喜欢将端到端测试与实际开发并行进行，并且我会在一定程度上利用这些端到端测试来辅助开发。因此，让它们使用同一个数据库是合理的。只要我能跟踪好一切并及时清理，通常这并不会造成太大问题。

## 44. 71. Setting Up a Test Database for Prisma Integration Tests

**原文**

A lot of our tests are calling this insert new user and that's sticking that into our development database. We want to have a separate test database. Now the trick here is that this insert new user, of course, that uses Prisma and the Prisma client comes from this Prisma client that we're creating right here and that determines where to connect to based on the environment variable database URL. Now, of course, we could set that database URL when we run our tests, but that would be kind of annoying. I'd rather just have that kind of hard coded

**译文**

我们有很多测试都在调用这个“插入新用户”的功能，而这些数据会写入我们的开发数据库。我们希望使用一个独立的测试数据库。现在的关键问题是，“插入新用户”这个功能当然使用了 Prisma，而 Prisma 客户端正是由我们在这里创建的 Prisma 客户端提供的。该客户端会根据环境变量 `databaseURL` 来决定连接到哪个数据库。当然，我们可以在运行测试时设置这个 `databaseURL`，但那样会有点麻烦。我宁愿直接将其硬编码。

## 45. 72. Setting Up an Isolated Database for Tests

**原文**

All right, let's make sure that we set our environment variables before Prisma gets imported by importing the DB setup right up here at the top, just as Cody instructs. And so then within this, we can set the database environment variable. So let's get the database file setup and the database path set to the current working directory plus the database file. And then we can say path from node. And then let's set the database

**译文**

好的，让我们确保在 Prisma 被导入之前设置好环境变量，就像 Cody 所指导的那样，把数据库设置直接放在最顶部导入。然后，我们就可以在这里设置数据库环境变量了。我们先来设置数据库文件，并将数据库路径设置为当前工作目录加上数据库文件。接着，我们可以使用 node 的 path 模块。然后我们来设置数据库。

## 46. 73. Optimizing Database Seeding for Faster Execution

**原文**

Okay, so I'm not a super fan of how long this takes. This is not cool. And honestly, most of the time that it's taking is in the seed script. That is just, we're seeding our database with way too much stuff. We don't need all that stuff. However, some of it we actually do need. So we can't just say, don't run the seed. Like we need the roles and we need the permissions. We're gonna rely on some of that stuff for creating new users as part of the login process and stuff like that. So we kind of need like a minimal seed.

**译文**

我不太喜欢这个过程耗时这么长。这真不酷。老实说，大部分时间都花在了种子脚本上。这是因为我们用太多数据来填充数据库了。我们根本不需要那么多数据。不过，其中有些数据我们确实需要。所以我们不能直接说“不要运行种子脚本”。比如，我们需要角色和权限。在登录流程中创建新用户等操作时，我们都需要依赖这些数据。因此，我们其实需要一个最小化的种子数据。

## 47. 74. Optimizing Database Seeding for Faster Execution_2

**原文**

So first we're going to go to our seed script and we need to, yeah, I'm fine like deleting all that stuff is not a big deal. But we need to create all these permissions and then we need to create all of the roles. And then once we've done that, we don't need any users in the database. And so we can add an if the process minimal seed, then we'll return early. And that's it. We can add a console log to make it helpful log and like thumbs up, minimal seed complete.

**译文**

首先，我们要进入种子脚本。嗯，我觉得直接删除所有那些内容也没关系。但我们需要创建所有这些权限，然后创建所有的角色。完成这些之后，数据库里就不需要任何用户了。因此，我们可以添加一个判断：如果进程是“最小化种子”模式，就直接提前返回。就这样。我们还可以添加一个控制台日志来提供帮助信息，比如“竖起大拇指：最小化种子完成”。

## 48. 75. Managing Test Databases for Parallel Testing

**原文**

If you've actually tried to run all of the tests here, so let's go NPM test without a qualifier for which test we want to run, you might have run into a problem running the user profile tests and our other tests at the same time. And the problem is that because they're running at the same time, they're pointing at the exact same database, when they each run there after each to delete many users, that's going to muck up with that global state that is kind of shared between them. So we need to make it so that we're

**译文**

如果你真的尝试过运行这里所有的测试，比如直接运行 `NPM test`，而没有指定要运行哪一个测试，那么你可能会在同时运行用户资料测试和其他测试时遇到问题。问题在于，由于这些测试是同时运行的，它们都指向了同一个数据库。当每个测试运行结束后删除大量用户时，就会破坏它们之间共享的全局状态。因此，我们需要确保……

## 49. 76. Isolating Test Databases for Efficient Testing

**原文**

So let's see if we can manage this. This is actually really not going to be a huge challenge. So all that we're going to do is add another part to this database file string that is going to be unique per test or test process. And vTest actually creates a unique environment variable for each of our test processes. That can be used kind of as a unique identifier. So we'll add a dot to separate this and we'll say process.

**译文**

那我们来看看能不能搞定这件事。其实这并不会是一个太大的挑战。我们要做的，就是在这个数据库文件字符串中添加另一部分，这部分对于每个测试或测试进程都是唯一的。而 vTest 实际上会为每个测试进程创建一个唯一的环境变量，这个变量可以用作某种唯一标识符。因此，我们会添加一个点号作为分隔符，然后写上 process。

## 50. 77. Optimizing Test Setup

**原文**

So I'm not super jazzed about how long this is taking and we can make it faster. And so what we're going to do in this step is going to be a little bit more complicated than what we've done so far. And that is we're going to have a global setup module that's going to be responsible for setting up all the global stuff that we need for our application to work. So, and that's actually a part of the VTest config. So we're going to set a global setup that will run before anything else.

**译文**

我对当前耗时这么长不太满意，我们可以让它更快一些。因此，这一步要做的内容会比之前稍微复杂一些。我们将创建一个全局初始化模块，负责为我们的应用正常运行设置所有必要的全局内容。而这实际上是 VTest 配置的一部分。因此，我们将设置一个全局初始化模块，它会在任何其他操作之前运行。

## 51. 78. Optimizing Test Setup with Global Database Configuration

**原文**

All right, so step one, we're going to go to this global setup file. This is the file that we're going to be using for the setting up our base database. So the idea is we have this base database, and then all of the other processes will just copy that one and then run their tests. So it will be way, way faster. So let's go to our vTest config, and we'll add a global setup that is specified to this file right here.

**译文**

好的，那么第一步，我们要进入这个全局配置文件。我们将使用这个文件来设置我们的基础数据库。其思路是，我们有一个基础数据库，然后所有其他进程只需复制该数据库并运行各自的测试。这样速度会快得多。现在让我们进入 vTest 配置，并添加一个指定到此处的全局配置。

## 52. 79. Dad Joke Break Test Database

**原文**

Did you hear about the new restaurant on the moon? The food is great, but there's no atmosphere. All right, now's the time to get up and go to a restaurant or something because you finished this awesome exercise. Bravo to you. Great job. Now is a good time for a break and let your brain just relax and chill. And then you can move on with your life and take all this wonderful knowledge and apply it to whatever awesome projects that you're working on. So awesome job.

**译文**

你听说月球上那家新餐厅了吗？食物很棒，但就是没什么“氛围”（气氛）。好了，现在该起床去餐厅什么的了，因为你已经完成了这项超棒的练习。为你喝彩！干得漂亮！现在正是休息的好时机，让你的大脑放松一下、 chill 一会儿。然后你就可以继续你的生活，把这些宝贵的知识应用到正在进行的任何超棒项目中。所以，干得漂亮！

## 53. 80. Outro to Web Application Testing Workshop

**原文**

Hey, you remember all this stuff? You just did all that. Awesome job. Look at this amazing set of tests that you put together, both in our UI for the Playwright stuff, as well as like lower level tests that we put together. You've learned a ton of stuff and you need to put this to practice, like Pronto. So go to your work app and start adding all these tools and get testing set up. Make it easier for people to add tests themselves. And you'll be way happier, way more confident.

**译文**

嘿，你还记得所有这些内容吗？你刚刚才完成所有那些工作。干得真棒。看看你整理的这套超赞的测试，既有我们为 Playwright 编写的 UI 测试，也有我们搭建的一些底层测试。你已经学到了很多知识，现在需要把它们付诸实践，就像 Pronto 那样。所以，快打开你的工作应用，开始添加所有这些工具，把测试环境搭建起来吧。让别人也能更轻松地自行添加测试。这样一来，你会开心得多，也自信得多。

## 54. 001 Content Management Systems with Alexandra Spalato - Epic Web Dev by Kent C.

**原文**

Hello everybody, I'm joined by my friend, Alexandra's Palato. How are you doing? Fine, and you? Doing great. I am joining you from Utah and Alexandra is coming from Spain, right? Yes, I'm in Madrid. Yeah, awesome. Madrid, I have only been to the airport, so maybe one day I can get out of the airport. Yes, you should come for tapas. I will be there. Yeah. So Alexandra and I met online.

**译文**

大家好，我邀请到了我的朋友 Alexandra's Palato。你好吗？我很好，你呢？我这边一切顺利。我现在从犹他州加入，而 Alexandra 是从西班牙来的，对吧？是的，我现在在马德里。太棒了。马德里，我只去过机场，所以也许有一天我能走出机场。是的，你应该来尝尝西班牙小吃。我一定会去。没错。那么，我和 Alexandra 是在网上认识的。

## 55. 002 Leadership in Tech with Ankita Kulkarni - Epic Web Dev by Kent C. Dodds - 19

**原文**

Hello everybody. I'm so excited to be joined today by my friend Ankita. Oh shoot, I didn't practice your last name. I'm going to try it. Kukarni? Yes, he got it right. Sweet. So Ankita and I, I always like to say where we met. I think the first time we met in person, was it at remix comp this year? Or at React? Yeah, I guess both were in Uda, right? Yes.

**译文**

大家好。今天我的朋友 Ankita 能来参加，我真的非常激动。哎呀，我刚才没有练习你的姓氏。我来试试看。Kukarni？是的，他说对了。太棒了。所以，Ankita 和我总是喜欢说说我们是在哪里认识的。我想我们第一次当面见面，是在今年的 remix comp 吗？还是在 React 活动上？嗯，我猜两次活动都是在 Uda 吧？是的。

## 56. 003 API Mocking with Artem Zakharchenko - Epic Web Dev by Kent C. Dodds - 1280x7

**原文**

Hey, Ardham, how's it going? Hey, hey, Kanta. It's great. What about you? I'm doing great. And everybody watching right now, hopefully you've been enjoying the exercises and stuff. Ardham is the creator of MSW, which we're using in the workshops. And it's awesome. I've been working on that for years now. I'm going to try and pronounce your last name. You gave me a guide. Let's try. Zach Archiko?

**译文**

嘿，Ardham，最近怎么样？嘿，嘿，Kanta。挺好的。你呢？我很好。还有现在正在观看的各位，希望你们一直在享受这些练习之类的东西。Ardham是MSW的创建者，我们正在工作坊中使用它。这真是太棒了。我已经为此努力了好几年了。我来试着念一下你的姓氏。你给了我一个发音指南。我们来试试。Zach Archiko？

## 57. 004 Enhancing SQLite with Ben Johnson - Epic Web Dev by Kent C. Dodds - 1920x108

**原文**

What is up everybody? I am so excited to be joined by my friend Ben Johnson and Ben and I met through his work on Lightstream and light FS at over at fly and Yeah, it's been a just a pleasure to work with Ben and and the test the limits of light FS a little bit and Yeah, Ben has just been a really awesome help in me getting my way

**译文**

大家好！我非常高兴能与我的朋友 Ben Johnson 一起录制节目。我和 Ben 是通过他在 Lightstream 和 Light FS 方面的工作认识的，他当时在 Fly 工作。是的，能和 Ben 一起合作，共同探索 Light FS 的极限，真的非常愉快。Ben 在帮助我推进项目方面，确实提供了非常棒的协助。

## 58. 005 The Evolution of Type Safety with Colin McDonnell - Epic Web Dev by Kent C.

**原文**

Hey everybody, how's it going? Colin? Not too bad. How you doing? Doing great. Everybody, this is my friend Colin and Colin is the creator of Zod and you've probably by this point in the Epic Web Workshop, you've probably used Zod a bit. We use Zod a lot in this workshop series. So I think I definitely appreciate everything that Colin has done. One thing before I let Colin introduce himself, one thing I want to mention

**译文**

大家好，最近怎么样？Colin？还不错。你呢？我状态很好。各位，这是我的朋友 Colin，他是 Zod 的创建者。在 Epic Web Workshop 进行到目前阶段时，大家可能已经用过一些 Zod 了。在本系列工作坊中，我们大量使用了 Zod。所以，我非常感谢 Colin 所做的一切。在让 Colin 自我介绍之前，还有一点我想提一下。

## 59. 006 Simplifying Web Form Management with Edmund Hung - Epic Web Dev by Kent C. D

**原文**

Hey everybody. I'm excited to be joined by Edmund Hung. Say hi Edmund. Hello. Edmund is the creator of Conform, the library that we're using in the Epic Stack and through all the workshop exercises and everything. Conform touches pretty much everything that we do as part of the Epic Stack, whether you're doing the login form or file upload or like just there's the

**译文**

大家好。我很高兴能与 Edmund Hung 一同亮相。来，Edmund，跟大家打个招呼吧。你好。Edmund 是 Conform 的创建者，我们目前在 Epic Stack 以及所有工作坊练习中使用的就是这个库。Conform 几乎涉及我们使用 Epic Stack 所做的每一件事，无论是登录表单、文件上传，还是其他功能。

## 60. 007 Scalable Databases and Authentication with Iheanyi Ekechukwu - Epic Web Dev

**原文**

What's up everybody? This is your friend can't see dots and I'm joined by my friend a honey a kitchen coup. How are you doing honey? They're right doing alright. Yeah, it's good to be here Did I get your name right? No, but it's okay. I know it's the high you got the first name pretty good last names a kichu koo It's hard man. It's a lot of letters intimidating. I get it. I know it's all good You spend your entire life correcting people on the pronunciation of your last name

**译文**

大家好！我是你们的朋友“看不见点”，今天和我一起的是我的朋友“一个蜂蜜一个厨房 coup”。你最近怎么样，亲爱的？他们一切都好。是啊，能来这里真好。我说对你的名字了吗？没有，不过没关系。我知道你第一个名字取得挺好的，姓氏是“kichu koo”。这可真难啊，字母太多了，有点吓人。我明白。我知道，没关系。你这一生都在纠正别人对你姓氏的发音。

## 61. 008 Understanding Web Development with Jacob Paris - Epic Web Dev by Kent C. Dod

**原文**

Hello, everybody. Hi, Jacob. Thank you so much for coming. Yeah, thanks for having me. So, Jacob, if you haven't run into Jacob yet, then this is a treat for you. Jacob has been posting a nonstop on his blog all about remakes and the stuff that he's working on. Jacob's currently working on a course of his own that is going to be awesome that dives into building a linear clone. I'll let him talk about that a little bit more too.

**译文**

大家好。嗨，Jacob。非常感谢你的到来。是啊，感谢邀请我。那么，Jacob，如果你还没有认识 Jacob，那你可真是有福了。Jacob 一直在他的博客上不间断地发布关于重制项目以及他正在开发的内容。Jacob 目前正在开发一门属于自己的课程，内容非常棒，将深入探讨如何构建一个线性克隆。我也会让他再多讲一些相关内容。

## 62. 009 The Depth of Software Testing with Jessica Sachs - Epic Web Dev by Kent C. D

**原文**

Hey everybody, I'm super excited to be joined by my friend Jess. Say hi Jess. Hello. So Jess and I go way back. My goodness, we have known each other for a while. I'm trying to, I always try to think of like, where did we meet and how did that relationship start? I think we probably go back to like 2015, 16 timeframe. Yeah, that's been a minute. Yeah, it's been great. And it's just been a pleasure to know you and keep up with all the

**译文**

大家好，我非常高兴能有我的朋友 Jess 加入。来，Jess，跟大家打个招呼。你好。我和 Jess 认识很久了。天哪，我们已经认识有一段时间了。我总是会去想，我们到底是在哪里认识的，这段关系又是如何开始的？我想我们大概可以追溯到 2015、16 年左右。是啊，已经过去好一阵子了。是的，这一直都很棒。能认识你，并且一直关注着你的一切，真的是一种荣幸。

## 63. 010 Platform Engineering with Jocelyn Harper - Epic Web Dev by Kent C. Dodds - 1

**原文**

What is up everybody? So I'm excited to be joined by Jocelyn Harper Jocelyn you go by Josie, right? I do yeah, I do okay. Does does anybody call you Jocelyn? Close friends. It's very funny because I feel like Josie has become like my online tech Persona like name people in real life call me Jocelyn. Yeah. Yeah, I actually can relate to that so Years and years ago. I bought the domain kentasy.com

**译文**

大家好！我很高兴能邀请到 Jocelyn Harper。Jocelyn，你通常叫自己 Josie，对吧？是的，没错。那有人叫你 Jocelyn 吗？只有关系很近的朋友。这很有趣，因为我觉得 Josie 已经成了我在网上的技术形象——现实生活中的人还是叫我 Jocelyn。是的，我其实也能理解这种感觉。很多很多年前，我买下了 kentasy.com 这个域名。

## 64. 011 Navigating the Testing Terrain with Debbie O'Brien - Epic Web Dev by Kent C.

**原文**

Hey everybody, welcome. This is my friend Debbie. Say hi Debbie. Hi everyone. So Debbie O'Brien is you live in Spain, right? In Mallorca, yes. Mallorca, yes. So Debbie lives in Spain. I met Debbie in person. I think the first time we met in person was in Croatia last year where we went swimming together in the Mediterranean, which was fun. And actually, like you pushed me, not like physically pushed me, but like you pushed me.

**译文**

大家好，欢迎。这是我的朋友 Debbie。跟 Debbie 打个招呼吧。大家好。那么，Debbie O'Brien，你住在西班牙，对吧？在马略卡岛，是的。马略卡岛，没错。所以 Debbie 住在西班牙。我跟 Debbie 是线下见面的。我想我们第一次线下见面应该是在去年的克罗地亚，当时我们一起在地中海游泳，非常有趣。而且，其实是你推动了我——不是那种身体上的推，而是你激励了我。

## 65. 012 Exploring the Front-End Ecosystem with Mark Dalgleish - Epic Web Dev by Kent

**原文**

Hello everybody, this is my friend Mark. Oh, I do this every time I practice your last name and then I'm like saying it and You're not the only one so don't don't feel I guess don't feel special. No, but you are special. Don't don't feel singled out. Okay, Del Gleesh, you nailed it. Yes So this is Mark Mark and I You know, I don't think we've ever met have we met in person we have in Amsterdam. Oh, oh, that's right

**译文**

大家好，这位是我的朋友马克。哦，我每次练习你的姓氏时都会这样，然后就像在说它一样。你不是唯一一个，所以别……我猜别觉得自己很特别。不，但你确实很特别。别……别觉得自己被单独拎出来了。好的，Del Gleesh，你说得太准了。是的，所以这位是马克。马克和我……你知道的，我想我们以前从未见过面，是吗？我们在阿姆斯特丹见过面。哦，哦，对，没错。

## 66. 013 Navigating Changing Web Technologies with Mark Thompson - Epic Web Dev by Ke

**原文**

What is up everybody? I'm so excited to be joined by Mark Thompson. This is Texan. You'll have to tell us what that nickname is all about, Mark. But yeah, so Mark and I met, I think on Twitter. I don't think we met in person before we met on Twitter, which is actually describes most of my relationships these days. But yeah, I think the first time we met in person was at NGConf this year, where I just like... Well, second time.

**译文**

大家好！我非常高兴 Mark Thompson 能加入进来。这位是 Texan。Mark，你得给我们讲讲这个外号的由来。不过呢，我和 Mark 是在 Twitter 上认识的，我想我们在 Twitter 上认识之前应该没见过面——这其实也形容了我现在的大多数人际关系。不过呢，我想我们第一次见面是在今年的 NGConf 上，我当时就……好吧，是第二次见面。

## 67. 014 The Magic of TypeScript with Matt Pocock - Epic Web Dev by Kent C. Dodds - 1

**原文**

Hello everybody. This is an exciting day. We get to talk with Matt Pocock about TypeScript and other things. So if you haven't heard Matt yet, then you're in for a treat. Matt is just a lovely person to chat with. He has a very nice voice. If you take any of his courses, you will hear a lot, which is great. And yeah, we're excited to chat about the thing that Matt is really

**译文**

大家好。今天是个令人兴奋的日子。我们将与 Matt Pocock 一起探讨 TypeScript 及其他相关话题。所以，如果你还没有听过 Matt 的分享，那你可真是有福了。Matt 是一个非常可爱的聊天对象，他的声音也非常好听。如果你上过他的任何一门课程，就会听到他讲很多内容，这非常棒。是的，我们很兴奋地能与 Matt 聊聊他真正擅长的领域。

## 68. 015 Building Deep Skills with Michael Chan - Epic Web Dev by Kent C. Dodds - 192

**原文**

What is up everybody? I'm joined by my friend Chan Tastic Michael Chan Michael say hi. Hey, hello everyone. I am so thrilled to be joined by Michael We just finished having an hour long conversation before recording. We just enjoy each other's company We enjoy each other's company a lot actually. It's so good So yeah, Michael. I'm so happy that you're here with us I'm trying to remember

**译文**

大家好！我邀请了我的朋友 Chan Tastic Michael Chan，Michael，跟大家打个招呼吧。嗨，大家好。能和 Michael 一起录制节目，我真的非常激动。在录制前，我们刚聊了整整一个小时。我们真的很喜欢彼此陪伴，其实我们非常享受在一起的时光。真是太棒了。所以，Michael，你能为我们节目感到特别高兴。我正努力回想……

## 69. 016 Examining MDX with Monica Powell - Epic Web Dev by Kent C. Dodds - 1920x1080

**原文**

Hey everybody, I am excited to be joined by Monica Powell. Say hi Monica. Hello everyone. All right, so if you haven't met Monica yet, she's just a delight. I have, we've crossed paths a number of times. I think every time has been at conferences, at least in person, that conferences bring people together, I guess. But yeah, Monica, I think, I'm pretty sure that I met you on Twitter first, but this is

**译文**

大家好，我很高兴能邀请到 Monica Powell。Monica，跟大家打个招呼吧。大家好。好的，如果你们还不太认识 Monica，那她真的是一位非常可爱的人。我们之前已经见过好几次了。我想每次都是在会议上，至少是在线下的场合——毕竟会议能把大家聚集在一起嘛。不过，Monica，我记得我好像最早是在 Twitter 上认识你的，但这次是……

## 70. 017 Efficient Form Management with Sandrina Pereira - Epic Web Dev by Kent C. Do

**原文**

Hello everybody. I'm super excited to be joined today by my friend, Sandrina. And I'm going to try your last name and you can correct me. It's Pereria. Perera. Well, thank you. That's not the first time that I've tried to pronounce your name on a podcast before. So, yeah, I don't really have a good idea. It's not, though, like for your

**译文**

大家好。我今天非常激动地邀请到了我的朋友 Sandrina。我来试试你的姓氏，你可以纠正我。是 Pereria。Perera。嗯，谢谢你。这已经不是我第一次在播客里尝试念你的名字了。所以，是的，我其实也不太确定该怎么念。不过，这倒不像……

## 71. 018 Transitioning from Rails to Remix with Sergio Xalambri - Epic Web Dev by Ken

**原文**

Hello everybody, this is Sergio Zalambri. Say hi Sergio. Hi Sergio. There you go, nice. Good. So Sergio, you've definitely, as you've been going through these workshops, Sergio is the author of a number of the packages and even patterns of different things that we've been doing in the workshops. So super thrilled to have Sergio in here. Sergio and I met as part of Remix. So like, I think Sergio

**译文**

大家好，我是 Sergio Zalambri。跟 Sergio 打个招呼吧。你好，Sergio。就是这样，很好。好的。那么 Sergio，在你参加这些工作坊的过程中，你肯定已经……Sergio 是我们在工作坊中所涉及的多个软件包甚至各种模式的设计者。所以，我们非常高兴 Sergio 能来到这里。Sergio 和我是在 Remix 项目中认识的。所以，我想 Sergio……

## 72. 019 The Capabilities and Ecosystem of Tailwind CSS with Simon Vrachliotis - Epic

**原文**

Hey everybody, this is my friend Simon Vrishulotis. Oh man, I practiced it. I knew I was gonna get it. And then it's Simon Vrishuliotis. Vrishuliotis. Yeah. Oh man, I'm, okay. Simon Vrishuliotis. And so Simon and I, I actually, I'm trying to remember, I don't think we've ever met in person before. We haven't. Yeah, that's a shame. We gotta like fix that at some point. But yeah,

**译文**

大家好，这位是我的朋友 Simon Vrishulotis。天哪，我练习过。我就知道我能说对。结果呢，是 Simon Vrishuliotis。Vrishuliotis。没错。天哪，我……好吧。Simon Vrishuliotis。所以，Simon 和我，其实……我得想想，我们以前好像从未见过面。确实没见过。是啊，真可惜。我们总得找个时间把这事补上。不过，是的……

## 73. 020 The Crucial Role of Database Optimization with Tyler Benfield - Epic Web Dev

**原文**

Hello everybody. This is a great day. I'm going to be talking with my friend Tyler Benfield. Say hi, Tyler. Hey, everyone. Yeah, Tyler and I, I think I kind of feel like we've met before this last remix conf, but I can't remember it was, was this remix conf the first time we met? No, so funny fact. This is the last react conf back in Hendersonville. We briefly met.

**译文**

大家好。今天是个好日子。我将和我的朋友 Tyler Benfield 聊一聊。来打个招呼吧，Tyler。嘿，大家好。是的，Tyler 和我，我觉得我们好像在上次 Remix 大会之前就见过面了，但我记不清了，这次 Remix 大会是我们第一次见面吗？不是，有个有趣的事实。这是在 Hendersonville 举办的最后一次 React 大会。我们当时短暂地见过面。

## 74. 021 Product Management with Nevi Shah - Epic Web Dev by Kent C. Dodds - 1920x108

**原文**

Hello, everybody. I'm super excited to be joined by Nevi. Actually, I didn't ask how to pronounce your last name. Is it Shah? It's Shah. Okay. Great. Nevi Shah. Nevi and I met at RemixConf this last year. She proposed to speak alongside Igor Minar of the AngularJS team fame. He's now over with Nevi at Cloudflare. They spoke together at RemixConf this year. It was awesome to have them speak.

**译文**

大家好。我非常高兴能与 Nevi 一同登台。其实，我之前还没问过您姓氏的发音。是 Shah 吗？没错，就是 Shah。好的，太棒了。Nevi Shah。Nevi 和我是在去年的 RemixConf 上认识的。她提议与大名鼎鼎的 AngularJS 团队成员 Igor Minar 一同演讲。他现在已经和 Nevi 一起在 Cloudflare 工作了。他们今年又在 RemixConf 上一起进行了演讲。能邀请到他们演讲真是太棒了。

## 75. 022 From Tech Sales to Engineering with Shaundai Person - Epic Web Dev by Kent C

**原文**

What is up everybody? I am joined by one of my very dear friends Shonda. Oh my goodness. I almost said your name wrong and like I was getting partway through it and like I'm gonna say this wrong and I feel so bad. So this is Shonda person. Say hi Shonda. Hi. Oh my goodness. How embarrassing. So because like the thing is that you get like people say your name wrong all the time and I am not one of those people. I say your name wrong. I know. We've known each other for a while.

**译文**

大家好！我今天请到了一位我非常要好的朋友——Shonda。天哪，我差点把你的名字说错了。我当时说到一半，突然意识到自己可能要念错，心里特别不好意思。所以这位就是Shonda本人。Shonda，打个招呼吧。你好。天哪，太尴尬了。因为通常来说，总是会有人把你的名字念错，而我偏偏不是那种人——我也会把你的名字念错。我知道，我们都认识这么久了。

## 76. 023 Remix Behind the Scenes with Ryan Florence - Epic Web Dev by Kent C. Dodds -

**原文**

What is up everybody? I'm super excited to be joined by my friend Ryan Florence say hi Ryan Every time you say that to me I almost say hi Ryan like it's some funny joke. I mean like it kind of is you can I know but I've done it every single time we've done one of these things. Yeah, it's true. So anyway, hello, I'm right Yeah, actually I had Ryan on the Chatsworth Kent podcast I think season four and that season

**译文**

大家好！我超级兴奋能和我的朋友 Ryan Florence 一起出现，来打个招呼吧，Ryan。每次你对我这么说的时候，我几乎都会回应“hi Ryan”，就像是个搞笑的梗一样。我的意思是，这确实有点像，虽然我知道，但每次我们做这种节目的时候我都会这么做。是的，没错。总之，大家好，我是 Ryan。是的，其实我之前在 Chatsworth Kent 播客第四季的时候请过 Ryan 来做客，就是那一季。

## 77. 024 Art, Code, and Data Visualization with Shirley Wu - Epic Web Dev by Kent C.

**原文**

Hey everybody, I am so excited to be joined by my friend Shirley Wu. Say hi Shirley. Hi everyone, hi Kent. Hi, all right, so Shirley and I go back pretty far actually. I think when we first met on Twitter, as where I meet most of my friends these days, or ex as it is now called, but it was Twitter back then and then we met in person. I want to say I'm pretty sure I've got a picture of us at Fluid

**译文**

大家好，我非常高兴能有我的朋友 Shirley Wu 加入。来，Shirley，跟大家打个招呼吧。大家好，Kent 你好。好的，其实 Shirley 和我认识已经很久了。我想我们第一次见面应该是在 Twitter 上——我最近的大部分朋友（或者像现在说的那样，“前朋友”）都是在那里认识的，不过那时候它还叫 Twitter。后来我们又见了面。我记得，我好像还有一张我们当时在 Fluid 的合照。

## 78. 025 The Future of Authentication with Will Johnson - Epic Web Dev by Kent C. Dod

**原文**

Hey everybody, I'm joined by my friend Will Johnson say hi Will. Hey, what's up everybody? Super happy to have you here. Thank you so much for giving us some your time today. So Will and I we met I in person This is another one of those that we met online first and then met in person in a conference Yeah, and I think I'm pretty sure where we met online first was through egghead in the egghead slack Is that right or did we get we meet first on Twitter? I think it was an egghead

**译文**

大家好，今天我请来了我的朋友 Will Johnson，来跟大伙儿打个招呼吧，Will。  
嗨，大家好！  
非常高兴你能来到这里。  
真的非常感谢你今天能抽出时间参加我们的节目。  
那么，Will 和我呢，我们是线下认识的。这又是我们那种先在网上认识、后来在一次会议上才线下见面的例子之一。  
是啊，我记得我们第一次应该是在 egghead 的 Slack 群里认识的，对吧？还是说我们先在 Twitter 上认识的？  
我记得应该是在 egghead。
