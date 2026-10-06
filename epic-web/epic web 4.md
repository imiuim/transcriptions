# Kent C. Dodds - Epic Web. Ship Modern Full-Stack Web Applications part4

- 来源：[B站 BV18HVxz3EWc](https://www.bilibili.com/video/BV18HVxz3EWc)（up 主：lmt831，共 100 P）
- 说明：英文转录 + 中文翻译（机器翻译，仅供学习参考）

---

## 01. 100. Intro to Reset Password

**原文**

We're going to reset the password. This is going to be a little bit anticlimactic. The biggest part of this is actually just reusing the verification flow that we already did, or using some improved utilities that have been put together for us by Kelly, the coworker. So you've already done all of the stuff with the onboarding verification and all of that stuff. We're just going to be reusing some of that. And Kelly moved some things around to make it easier for you to

**译文**

我们将要重置密码。这个过程可能会有点平淡无奇。其中最大的部分其实就是复用我们已经完成的验证流程，或者使用由我们的同事 Kelly 为我们准备的一些改进后的工具。因此，你已经完成了所有与入职验证相关的工作。我们现在只是要复用其中的一些内容。此外，Kelly 还对一些内容进行了调整，以便你更轻松地使用它们。

## 02. 101. Implementing Forgot Password and Reset Password Flows

**原文**

Ever since I started using a password manager, I haven't really had too much trouble with remembering my password problem, but a lot of people do still have this problem. And sometimes I try to log into something that I haven't logged into a long time ago, and yeah, I need to reset my password. So having the forgot password or reset password flow is very, very important, and that's what you're going to be implementing here. Now, this is going to require that we send an email to the user to verify that they are the one

**译文**

自从我开始使用密码管理器以来，我在记住密码方面几乎没怎么遇到过问题，但很多人仍然有这个问题。有时，当我尝试登录一个很久没有登录过的服务时，我确实需要重置密码。因此，设计“忘记密码”或“重置密码”的流程非常重要，而这正是你将在这里实现的功能。现在，这将需要我们向用户发送一封电子邮件，以验证用户身份。

## 03. 102. Resetting Passwords and Handling Verification

**原文**

Let's start by going to our forgot password route. And in here, we're inside of our action. Once we've verified that the user submitted their username or email properly, and that the user does in fact exist and all of that stuff, then we can create our verification. Now, we already did something like this. So we have this new prepare verification utility. So this is where we're going to get our redirect to and our verify URL and our OTP is going to come from a awaited call to prepare

**译文**

让我们先转到“忘记密码”路由。在这里，我们位于其 action 内部。一旦我们验证了用户正确提交了用户名或电子邮件，并且该用户确实存在等等，我们就可以创建验证逻辑。现在，我们之前已经做过类似的事情了。因此，我们有一个新的“prepare verification”工具。我们将在这里获取重定向地址和验证 URL，而 OTP 将通过 await 调用 prepare 来获取。

## 04. 103. User Authentication and Password Reset Flow

**原文**

So we've got a little bit more work to do. Right now we're saying hi, get this from the session, but that's supposed to be our username. So we've got to retrieve the username out of the cookie. So that first of all, we want to make sure that there is a username in there. If there's not, then we haven't actually properly verified and we shouldn't even be here in the first place. So we'll kick people out if they're logged in, they shouldn't be logged in and be here either. So if you're anonymous, we're going to kick you or if you're not anonymous, we're going to kick you out. If you don't have a username in your cookie, you haven't verified it.

**译文**

所以我们还有更多工作要做。目前我们只是说“hi”，并从会话中获取这个值，但这本应是我们的用户名。因此，我们必须从 Cookie 中获取用户名。首先，我们要确保其中确实包含用户名。如果没有，那就说明我们尚未正确验证身份，根本不应该出现在这里。所以，如果用户已经登录了，我们就会将他们踢出——他们本不该登录并出现在这里。也就是说，如果你是匿名用户，我们会将你踢出；如果你不是匿名用户，我们也会将你踢出。如果你的 Cookie 中没有用户名，那就说明你尚未完成验证。

## 05. 104. Secure Password Reset Flow Implementation

**原文**

The first thing I think we should do is go to the reset password right here and we're going to make a little utility for our loader in action to make sure that only people who are allowed to be here can be here. So we're going to export a function called require reset password username. Remember we're setting that right up here where we're handling the verification and so that's a password username session key that's something that's in the session.

**译文**

首先，我认为我们应该做的是前往这里的“重置密码”部分，然后为我们的加载器创建一个小型实用程序，以确保只有被授权的人员才能在此处访问。因此，我们将导出一个名为 `require reset password username` 的函数。请记住，我们是在这里处理验证时设置它的，所以这是一个包含密码、用户名和会话密钥的内容，而这些信息都存储在会话中。

## 06. 105. Dad Joke Break Reset Pass

**原文**

I made a belt out of watches once. It was a waste of time. Ha ha. All right. So now's a good time for you to get up and stretch and walk around or whatever you're going to do to get some blood flowing in your body because that's important for these brains. One day maybe we will all be a part of the Borg and you won't need to relax or rest or anything like that. But right now, actually they did. They were constantly charging or whatever. But for right now, before we end up in the multiverse,

**译文**

我曾经用钟表做过一条腰带。那纯属浪费时间。哈哈。好了。现在正是你起身伸展、四处走动的好时机，或者做点别的什么来促进身体的血液循环，因为这对你这些大脑来说很重要。也许有一天我们都会成为“博格”（Borg）的一员，到那时你就不需要放松、休息或做任何类似的事情了。不过眼下，实际上他们确实需要。他们不停地充电或类似的事情。但就目前而言，在我们最终进入多重宇宙之前，

## 07. 106. Intro to Change Email

**原文**

It's time to change people's emails. People want to be able to change their emails. I think that's a sensible, reasonable thing to do, and we need to verify the user's ownership of their own account and the new email address. So that's what we're going to be doing in this exercise. The idea is you have this change email. We want to change it to codeyatexample.com, and we go to our inbox and we copy this and paste it, and then we get a little notification that we changed it to codeyatexample.

**译文**

是时候让用户更改他们的电子邮件地址了。用户希望能够更改自己的电子邮件地址。我认为这是一个合理且明智的做法，我们需要验证用户对其本人账户以及新电子邮件地址的所有权。因此，这就是我们将在本次练习中要做的事情。其思路是：你有一个“更改电子邮件”的功能。我们想将其更改为 codeyatexample.com，然后我们前往收件箱，复制并粘贴该代码，接着会收到一条小通知，提示我们已成功将其更改为 codeyatexample。

## 08. 107. Implementing Email Verification for Changing Email Addresses

**原文**

Our profile has this change email, and so we can change our email to codie at example.com. Send confirmation and kablooey. We can't find this page because you need to implement this. We need to implement the prepare verification, all this other stuff. So you need to prepare a verification, send the email, and when they confirm the email, then we're going to handle that verification to allow the user to make this change to their email address.

**译文**

我们的个人资料中有这个“更改电子邮件”功能，因此我们可以将电子邮件地址更改为 codie@example.com。发送确认邮件，然后“砰”的一声搞定。我们找不到这个页面，因为你需要实现它。我们需要实现“准备验证”以及所有其他相关功能。因此，你需要准备一次验证、发送电子邮件，当用户确认电子邮件后，我们就会处理该验证，允许用户更改其电子邮件地址。

## 09. 108. Implementing Email Change Verification

**原文**

So let's go to the profiles change email route here and right down here is where we need to get all this information from the prepare verification. So let's do that. const otp redirect uri verify URL equals prepare verification from our verify util. And for this one, it's going to be pretty similar to the ones we've done already. So the period is going to be 10 minutes, 10 times 60.

**译文**

那么我们转到这里的“修改邮箱”个人资料路由，就在下面这里，我们需要从 `prepareVerification` 中获取所有这些信息。那我们就开始吧。`const otpRedirectUriVerifyUrl = prepareVerification`，来自我们的 `verifyUtil`。对于这个，会和我们之前做的非常相似。所以有效期将是 10 分钟，也就是 10 乘以 60。

## 10. 109. Handling Email Verification and Updates

**原文**

So now we've got all the setup finished and your next step is to actually handle the verification. So once the user is actually verified that they own the new email address, we need to go ahead and let them change the email address and proceed from there. So your job is to handle the verification and allow the user to change their email address. Good luck.

**译文**

现在我们已经完成了所有设置，你的下一步就是实际处理验证。一旦用户成功验证了自己拥有这个新邮箱地址，我们就需要让他们更改邮箱地址，并继续后续操作。因此，你的任务是处理验证，并允许用户更改他们的邮箱地址。祝你好运。

## 11. 110. Implementing a Secure Email Change Flow

**原文**

So in our change email route, we've got this handle verification. This is going to be called when the user successfully verified their ownership of the new email address. We sent that email to the email that they said, hey, I want to change it to this new email. So we'll say, kodi at example.com. That will be this mission value email. And so we send one time password to that email address. When they end up in here, then we've verified that they do

**译文**

在我们的更改电子邮件路由中，我们有一个处理验证的逻辑。当用户成功验证其对新电子邮件地址的所有权时，该逻辑将被调用。我们已经将一封邮件发送到了用户指定的新电子邮件地址，例如 kodi@example.com。这个地址就是我们所说的目标电子邮件地址。然后，我们会向该电子邮件地址发送一次性密码。当用户最终进入此处时，我们就已经验证了他们确实拥有该邮箱。

## 12. 111. Dad Joke Break Change Email

**原文**

I asked my date to go to the gym the other day. They never showed up. That's when I knew we wouldn't work out. Ha ha. All right, this is a good time for you to take a break. So get up, get moving, take a break, and come back because I still want you here. I've been enjoying our time together. So like, why you gotta be like that? Let's go work out, I guess. Okay, see you in a bit.

**译文**

前几天我约我的约会对象一起去健身房。结果他们根本没来。那一刻我就知道，我们之间“不会有什么进展”了（不会“锻炼”成功）。哈哈。好了，现在正是你休息一下的好时机。所以快起来吧，动一动，休息一下，然后再回来，因为我 still want you here。我一直很享受我们在一起的时光。所以呢，你干嘛要那样啊？那咱们就去锻炼吧，我猜。好的，待会儿见。

## 13. 112. Intro to Enable Two-Factor Authentication

**原文**

we're going to enable two factor authentication for our users. And I think it's best to explain this using a diagram. So here we are. The user is going to say, Hey, I want to enable two factor authentication. The server says that sounds great. But I need to make sure that you're able to generate these codes. Because if if we enable this for you and then lock you out unless you give us code, then that's going to be a problem. You need to make sure to to demonstrate to me that you can generate these two factor auth codes. So we're going to

**译文**

我们将为用户启用双因素身份验证。我认为最好通过一张图来解释这个过程。现在我们来看这张图。用户会说：“嘿，我想启用双因素身份验证。”服务器会回应：“这听起来很棒。但我需要确认你能够生成这些代码。因为如果我们为你启用了这项功能，而你却无法提供代码，结果就会导致你被锁定，那可就麻烦了。你必须向我证明，你能够生成这些双因素身份验证代码。”所以，我们将要……

## 14. 113. Implementing Two-Factor Authentication Verification

**原文**

For this exercise, your job is to make it so that this enable 2FA button actually creates a two factor authentication verification. So this is a little bit kind of weird, but what we're going to do is make a verification that we'll be able to use on this page. And once we verify this, then that turns it into a actual two factor authentication verification. So we're going to have like a, a 2FA verify verification type, and then we'll have a 2FA verification type. So

**译文**

对于本次练习，你的任务是让这个“启用 2FA”按钮真正创建一个双因素身份验证。这听起来有点奇怪，但我们要做的是创建一个可以在这个页面上使用的验证。一旦我们验证了这个验证，它就会变成一个真正的双因素身份验证。因此，我们将有一个类似“2FA 验证”的验证类型，然后我们还将有一个 2FA 验证类型。所以

## 15. 114. Two-Factor Authentication with TOTP Codes

**原文**

So to make this button work, we're going to need to go to our profile to factor index route. Here we are. And there's the 2FA button right there that we'll submit to this action. So let's get the user ID, because that's the thing that we're going to be verifying. And then we want to generate the tootp config that we're going to save into the database. We don't need the one-time password that it gives back to us right from the get go. So what we're going to do is we're going to call generate tootp. We're actually good with all of this.

**译文**

为了让这个按钮能够正常工作，我们需要前往个人资料中的“两步验证索引”路由。现在我们在这里了，就能看到“2FA 按钮”，我们将提交该按钮以执行此操作。接下来，我们需要获取用户 ID，因为这是我们将要验证的关键信息。然后，我们需要生成两步验证配置，并将其保存到数据库中。我们一开始并不需要它返回的一次性密码。因此，我们要做的就是调用 `generate_totp` 方法。实际上，所有这些都准备就绪了。

## 16. 115. Generating Two-Factor Authentication Codes and QR Codes

**原文**

So we are generating the two-factor authentication verification code here, but we need to give the user an easy way to add this to their two-factor authentication app. So whatever tool they're using to generate one-time passwords. Lots of those tools will allow for taking a screenshot of a QR code or use the camera app and take the QR code so that it just inserts for them. But you always want to make sure that you include some text, the actual URI,

**译文**

因此，我们在这里生成双因素身份验证代码，但需要为用户提供一种便捷的方式，将此代码添加到他们的双因素身份验证应用中。无论他们使用哪种工具生成一次性密码，许多此类工具都支持通过截图二维码或使用相机应用扫描二维码，从而自动完成插入操作。不过，你始终需要确保包含一些文本，即实际的 URI。

## 17. 116. Generating QR Code and Auth URI for Two-Factor Authentication

**原文**

So let's go to the two factor verify route here and in our loader, that's where we're loading the data. We're going to load the user ID from require user ID. And then we're going to need to get the verification for the user if it exists at all. So we're going to not find first, but find unique. And because they should only have one of these where the target type matches the target of user ID, and then the type of two FA verify verify

**译文**

那么我们进入双因素验证的路径，在我们的加载器中，我们正是在这里加载数据。我们将从 `require user ID` 中加载用户 ID。然后，我们需要获取该用户的验证信息（如果存在的话）。因此，我们首先使用 `not find`，但随后使用 `find unique`。由于用户应该只有一条记录满足目标类型与用户 ID 的目标相匹配，并且类型为双因素验证（two FA verify verify）。

## 18. 117. Testing the Two-Factor Authentication Setup

**原文**

So now we're going to need to actually test this out and there are a couple of ways you can go about doing that. You can either like pull up your phone and scan the QR code and enter the code manually there. You could pull up one password and it can scan your screen and get the QR code or the one-time password there. Or you can just copy this. I will put this in the instructions and this will do the exact same thing. So what we're doing is we get the generate TOTP from EpicQuest.

**译文**

现在，我们实际上需要测试一下这个功能，有几种方法可以实现。你可以打开手机，扫描二维码并手动输入代码。你也可以打开 One Password，它会扫描你的屏幕，获取二维码或一次性密码。或者，你也可以直接复制这段代码。我会把它放在说明中，效果是完全一样的。我们现在做的就是从 EpicQuest 获取生成的 TOTP。

## 19. 118. Two-Factor Authentication Code Verification

**原文**

So let's enable 2FA and now we need to actually verify that the user can enter a valid code. We can totally do that ourselves. We can just grab this and stick it right here and then run this script and boom, we've got a code, but we've got to update the action here to actually perform that verification. So here we are in our action. And right here we have this code is valid. We're going to reuse a utility called is code valid for

**译文**

那么，我们来启用 2FA，现在需要实际验证用户是否能够输入有效的代码。我们完全可以自己完成这个操作。我们可以直接获取这段代码，把它粘贴到这里，然后运行这个脚本，砰的一声，我们就得到了一个代码。不过，我们必须更新这里的操作，以实际执行该验证。现在我们来到了操作部分。在这里，我们有“代码有效”这一项。我们将复用名为 is code valid 的工具来

## 20. 119. Dad Joke Break Enable Two-Factor Authentication

**原文**

I wanted to be a tailor, but I didn't suit the job. I actually am so relieved that I don't have to wear a suit to work. There was a time in my life that I did and there was a job that I had where I had to wear a full-on like shirt and tie full-on suit. I had a couple jobs like that actually. Not my favorite thing for sure. My dad was a CPA, so he wore a suit every day to work. That is not the life that I want to live. If that's what you enjoy, then

**译文**

我曾想成为一名裁缝，但这份工作并不适合我。实际上，我非常庆幸自己不必穿西装上班。人生中有一段时间我确实穿过西装，有一份工作需要我穿上衬衫、领带，再配上一整套西装。其实我有过几份这样的工作。那肯定不是我最喜欢的。我父亲是一名注册会计师（CPA），所以他每天都穿西装上班。那并不是我想要过的生活。如果你享受那样的生活，那么

## 21. 120. Intro to Verify Two-Factor Authentication (2FA)

**原文**

Okay, it's time to actually verify the two factor authentication code. So if I go to my profile here, we've got our two factor authentication is enabled. So if I log out and go to log in Cody, Cody loves Cody loves you. Then it should ask me for my two factor authentication code. If I generate that here, then we'll paste that here and submit and I should be able to log in. So let's talk about how the

**译文**

好的，现在是时候实际验证双因素认证代码了。如果我进入这里的个人资料，可以看到我们的双因素认证已启用。如果我退出登录并重新登录 Cody，Cody 爱你，Cody 爱你。然后系统应该会要求我输入双因素认证代码。如果我在这里生成该代码，然后将其粘贴到这里并提交，我就应该能够成功登录。那么，我们来谈谈它是如何实现的……

## 22. 121. Two-Factor Authentication and Session Verification

**原文**

For this step, you're going to handle what happens when I say, Cody loves you. When I say log in, when I hit this button, it's going to create a session. And your job is to put the session ID in the verification session storage in our verify session storage, instead of the regular session storage that manages the user authentication. And yeah, that's that's the part for this step. You all of course, you only want to do that if the user has two factor authentication enabled, which this user does. So that is your job.

**译文**

在这一步中，你将处理当我输入“Cody loves you”时会发生什么。当我输入“log in”或点击这个按钮时，系统将创建一个会话。你的任务是将会话 ID 放入“verify session storage”（验证会话存储）中，而不是放入用于管理用户身份验证的常规会话存储中。没错，这就是这一步要完成的部分。当然，你只应在用户启用了双重身份验证时才执行此操作，而当前用户确实已启用该功能。这就是你的任务。

## 23. 122. Implementing Two-Factor Authentication Flow

**原文**

Let's start out by going to login. And right here in our action function, we need to take a different path if the user has two factor authentication enabled. So let's determine that verification equals await prisma dot verification. And we're going to find find unique. And we're finding unique because they can only have one two factor off code at all. So we can find the target type. And the target

**译文**

让我们首先前往登录页面。就在我们的 action 函数中，如果用户启用了双重身份验证，我们需要走一条不同的路径。因此，我们来判断一下：verification 等于 await prisma.verification，然后调用 findUnique 方法。我们之所以使用 findUnique，是因为用户只能拥有一个双重身份验证代码。因此，我们可以找到目标类型，以及目标

## 24. 123. Switching to Verified Session ID After Code Verification

**原文**

For this next step, we need to actually handle the code once it's been submitted. So we already have the verification to verify that the code is correct. And we have our verify query programs and all that stuff that will say this is a two factor auth code and all that stuff. So what we need to do is actually handle after that verification has been done to switch from the unverified session ID to a verified session ID in our regular cookie session. And so that's your step here.

**译文**

在下一步中，我们实际上需要处理提交后的代码。我们已经有了验证代码是否正确的验证机制，也有用于验证的程序和相关逻辑，这些程序会判断这是一个双因素认证代码等。因此，我们需要在验证完成后，将普通 Cookie 会话中的未验证会话 ID 切换为已验证的会话 ID。这就是你接下来要完成的步骤。

## 25. 124. Two-Factor Authentication Login in Node.js

**原文**

Let's start in our login route and right up here we need to create a handle verification function. It's actually going to look a lot like our onboarding handle verification function. So I'm going to copy that to get us a little bit of a head start here. We're not going to do this bit though, so we'll get rid of that. And we're also not going to redirect onboarding either, but we'll get to that here in a bit. So let's bring in invariance. Let's bring in the verify function args. And then let's call this handle verification

**译文**

让我们从登录路由开始，就在上方这里，我们需要创建一个句柄验证函数。它实际上会和我们的入职流程句柄验证函数非常相似。因此，我将复制那个函数，以便能更快地开始。不过，我们不需要这部分内容，所以把它删掉。同时我们也不需要执行入职流程的重定向，不过稍后我们会处理这部分。现在，我们引入 invariance，再引入 verify 函数的参数。然后，我们把这个函数命名为 handle verification。

## 26. 125. Dad Joke Break Verify Two-Factor Authentication (2FA)

**原文**

My new thesaurus is terrible. In fact, it's so bad. I'd say it's terrible. Haha. I hope your thesaurus is better than that. How about awful? I don't know. Just abysmal. That's another good one. All right, but you're not abysmal. You're awesome. And you've done a really good job with this exercise. It's time to take a break. Get up and get yourself a drink. I'm going to go refill my water bottle because I'm out. It's always good to have an empty water bottle because it means you're drinking. So go get yourself some water.

**译文**

我的新同义词词典太糟糕了。事实上，它实在太差了。我会说它太糟糕了。哈哈。希望你的同义词词典比它好一些。那“糟糕透顶”怎么样？我不知道。总之就是“极差的”。这也是另一个不错的词。好吧，但你可不是极差的。你太棒了。而且你在这次练习中做得真的很好。是时候休息一下了。站起来去给自己倒点喝的吧。我要去给我的水瓶加水，因为已经空了。有一个空水瓶总是好的，因为这意味着你在喝水。所以快去给自己接点水吧。

## 27. 126. Intro to Two-Factor Authentication Check

**原文**

Sometimes your users want to do destructive operations that kind of require an extra sense of like, hey, let's make sure that you're totally positive that you want to do this. And so we're going to, and also not only that you want to do this, but that you are who you say you are, that the user didn't just get up and walk away. So that when they have two-factor authentication enabled, they probably are security minded and probably would appreciate us double checking when we want to do a destructive

**译文**

有时，用户希望执行一些破坏性操作，这就需要一种额外的确认机制，比如：“嘿，请确保你完全确定要执行此操作。”因此，我们不仅要确认用户确实想执行此操作，还要确认用户确实是其声称的身份，而不是用户刚起身离开。这样，当用户启用了双因素身份验证后，他们通常会有安全意识，并且可能希望我们在执行破坏性操作时进行双重确认。

## 28. 127. Two-Factor Authentication Deletion

**原文**

So sometimes users want to delete two-factor authentication for various reasons. And so we want to be able to support that. And right now, we actually do have a button for it, but it doesn't do anything. It says, JK, this has not been implemented. So that's your job is to remove that JK and actually delete this two-factor authentication verification code. This is actually pretty straightforward, but I'm having you do this for this step of the exercise,

**译文**

因此，有时用户出于各种原因希望删除双重身份验证。我们希望支持这一操作。目前我们确实为此提供了一个按钮，但它没有任何功能。上面写着“JK，这尚未实现”。因此，你的任务就是移除这个“JK”提示，并真正实现删除双重身份验证验证码的功能。这个任务其实相当直接，但在这个练习步骤中，我仍要你来完成它。

## 29. 128. Disabling Two-Factor Authentication

**原文**

So this is in our disable route of our two factor authentication stuff. And here we're going to await prisma dot verification dot delete. And where our type is to two factor verification type. And the target is actually we can put this in the target type. Can't we let's do that and type in there and the target is it

**译文**

所以这属于我们双因素认证流程中的禁用路由。在这里，我们将等待 `prisma.verification.delete` 的执行。其中我们的类型是 `twoFactorVerificationType`。而目标部分其实我们可以将其放入目标类型中，对吧？我们来这样做，在那里输入类型，目标就是这个。

## 30. 129. Adding User Re-Verification for Critical Operations

**原文**

So it's all well and good to let users create and delete and do all sorts of stuff to all their data. But sometimes there's a really destructive operation that you want to just like really make sure, are you sure you want to do this? Or am I sure that you're still the person that you say you are? All of that. And so even though they may have entered their two factor authentication code when they logged in, maybe it's been a while and we want to just double check and make sure that they really are the person that they say they are for situations where they're changing their email.

**译文**

让用户创建、删除以及对他们的所有数据进行各种操作，这当然是件好事。但有时会遇到一些极具破坏性的操作，这时你就需要再三确认：“你确定要执行此操作吗？”或者“我能确定你还是你所说的本人吗？”诸如此类的问题。因此，即使他们在登录时已经输入了双因素认证代码，但可能已经过去了一段时间，我们仍需要再次核实，确保他们确实是本人——尤其是在他们要更改电子邮件地址的情况下。

## 31. 130. Implementing Verification Age Check for Disable 2FA

**原文**

Now that we've got that utility, we're going to use that utility right here. So before even being able to get to the Disable 2FA page, we want to require that users verify or re-verify that their verification is no longer than two hours old. And then when they actually perform the action to disable, we'll want to double check that again. So we're going to make a utility called require recent verification that will use that utility should request 2FA. And if they

**译文**

既然我们已经有了这个工具，接下来我们就要在这里使用它。因此，在能够访问“禁用双重验证”页面之前，我们希望要求用户验证或重新验证其验证信息是否不超过两小时。然后，当他们实际执行禁用操作时，我们还需要再次进行双重检查。因此，我们将创建一个名为“require recent verification”的工具，该工具将使用“should request 2FA”工具。如果他们

## 32. 131. Managing User Verification and Two-Factor Authentication

**原文**

For the first part of this, we're going to be in the login route. And at first glance, you might think this is pretty easy. Oh, we just need to add a verified time in the cookie. Well, it's going to be a little bit more complicated than that. So let's take a look at this. We're going to have a verified time key right here for the value in the cookie. And really, all that we need is just cookie session.session.set. And the verified time key is date.now, right? That's all we need. Well, unfortunately,

**译文**

对于第一部分，我们将在登录路由中处理。乍一看，你可能会觉得这很简单。哦，我们只需要在 Cookie 中添加一个验证时间。嗯，实际上会比这个稍微复杂一些。那我们来看一下。我们将在这里为 Cookie 的值设置一个验证时间键。其实，我们真正需要的只是 `cookie session.session.set`。而验证时间键就是 `date.now`，对吧？这就是我们需要做的全部。然而，不幸的是，

## 33. 132. Redirecting Users to Re-verify for 2FA Disabling

**原文**

Let's make our utility in the disable route. So that's the route that we get to when we get here. We don't even want people to be able to be here if they haven't re-verified recently. And so we're going to require recent re-verification or verification in the loader as well as the action. So let's export a function called require recent re-verification. This is going to take a request and a user ID. And this is going to be

**译文**

让我们在 disable 路由中创建我们的工具函数。这就是我们到达这里时所进入的路由。如果用户最近没有重新验证，我们甚至不希望他们能够访问这里。因此，我们将在 loader 和 action 中都要求最近重新验证或验证。那么，让我们导出一个名为 require recent re-verification 的函数。它将接收一个请求和一个用户 ID。而这个函数将

## 34. 133. Session Expiry Issue During 2FA Disablement Flow

**原文**

This re-verification stuff actually has caused a little bit of a problem for us. So if I go to Kodi and Kodi loves you, and I'm going to say remember me, this is the key point here. And then we're going to get our two factor auth code right here and submit that. Okay, so I've got my session right here. It expires in 30 days or whatever. And so then I go over to my profile. And let's say that I want to disable two factor auth and I've already

**译文**

这种重新验证的机制实际上给我们带来了一点小问题。所以，如果我进入 Kodi，而 Kodi 又“喜欢你”，然后我选择“记住我”，这正是问题的关键点。接着，我们会在这里获取双因素认证码并提交。好的，现在我的会话就在这里，它会过期，比如 30 天后失效。然后我转到我的个人资料页面。假设我想禁用双因素认证，而我已经……

## 35. 134. Fixing Session Expiration Behavior in 2FA Disablement Flow

**原文**

So let's come into our session server right here and we're going to override the session storage dot commit session. So to be able to do that, we need to still call the underlying method. And so what we're going to do is have an original commit session so that we can still call that function when we need to. Okay, and then to override it, there are a couple of ways you can do this to monkey patch it, you could use the proxies and the reflect API and all sorts of interesting things. I think the most straightforward way to do this is with object

**译文**

那么，我们现在进入这里的会话服务器，然后覆盖 `sessionStorage.commitSession`。为了实现这一点，我们仍然需要调用底层的方法。因此，我们要做的就是保留一个原始的 `commitSession`，以便在需要时仍能调用该函数。好的，接下来要覆盖它的话，有几种方法可以实现，比如通过猴子补丁（monkey patch）的方式，你可以使用 Proxy 和 Reflect API 等各种有趣的技术。我认为最简单直接的方法是使用 `Object`。

## 36. 135. Dad Joke Break Two-Factor Authentication Check

**原文**

Did you hear about the campsite that got visited by Bigfoot? It got intense! Oh, these dad jokes, they never get old. Well, maybe they do get old for you and I apologize if that is your case. Feel free to skip these videos, but don't actually skip these break videos because it's important. You've got to take breaks. Your brain needs it. So take a break right now and yeah, we're still not done. We've got more stuff to learn. So come on back when you are rested and relaxed and feel ready to dive in and

**译文**

你听说过那个被大脚怪光顾过的露营地吗？那场面可太刺激了！哦，这些老爸笑话真是百看不厌。嗯，也许对你来说已经听腻了，如果是这样，我向你道歉。你可以随意跳过这些视频，但千万别跳过休息环节，因为这很重要。你一定要休息一下，你的大脑需要它。所以现在就来休息一下吧。是的，我们还没结束呢，还有更多内容要学。等你休息好了、放松了、准备好投入学习时，再回来吧。

## 37. 136. Intro to Oauth

**原文**

For many applications, authenticating with a third-party service of some kind is pretty much a requirement, whether it be social logins with like GitHub or x.com or Google or whatever, or in addition, single sign-on with an enterprise that has their own single sign-on implementation. Many of these are built with OpenIDC, and so OpenConnect or they have like their own implementation of something

**译文**

对于许多应用程序来说，通过某种第三方服务进行身份验证几乎是一项基本要求，无论是通过 GitHub、x.com 或 Google 等平台实现社交登录，还是额外采用企业级单点登录（其本身可能已有自定义的单点登录实现）。许多此类服务都基于 OpenIDC 构建，或者采用 OpenConnect，又或者是它们自己实现的某种方案。

## 38. 137. Integrating GitHub Authentication

**原文**

This is chopped up into a couple of different pieces. So for after this first step, you're not actually going to be able to go through the off flow because there are just a couple of things we need to do to get things set up before we do that. So first of all, we're going to be setting some GitHub environment variables so we can integrate with the GitHub API. If you want to, you can actually set like go to GitHub and get real credentials and everything, the client ID and secret. And so you can actually try this out. I'll do that in the video.

**译文**

这段内容被分成了几个不同的部分。因此，在完成这第一步之后，你实际上还无法继续执行后续流程，因为在那之前我们还需要做几件事来进行设置。首先，我们将设置一些 GitHub 环境变量，以便与 GitHub API 进行集成。如果你愿意，可以实际前往 GitHub 获取真实的凭据，包括客户端 ID 和密钥。这样你就可以亲自尝试一下了。我会在视频中演示这个过程。

## 39. 138. Setting up OAuth Authentication with GitHub

**原文**

To get started, let's create our OAuth application on github.com slash settings. That's application slash new. If you're using GitHub for your OAuth, then this is where you're going to go. If you're using Google or Twitter or wherever, they're all going to have their own different setup. But it's going to be something similar to this. So here I'm going to call this Epic Web demo. And the homepage URL will be your website. But we'll just say epicweb.dev.

**译文**

要开始，我们先在 github.com/settings 创建 OAuth 应用。也就是 application/new。如果你使用 GitHub 作为 OAuth 提供商，那么这就是你要去的地方。如果你使用的是 Google、Twitter 或其他平台，它们都会有各自不同的设置方式，但大致流程与此类似。这里我将其命名为 Epic Web demo。主页网址（homepage URL）可以是你的网站地址，我们暂时就填 epicweb.dev。

## 40. 139. Testing the OAuth Flow with GitHub Authentication

**原文**

So now we're going to test the actual auth flow. And so if you created a OAuth application in GitHub, you should actually be able to test the auth flow in this exercise once we're finished. So you're going to go to the auth GitHub callback route that Kelly put put together for us and fill in a couple of things in there to authenticate using the remix authenticator, the remix auth authenticator object that we just created. And then we're also going to go to the regular GitHub URL for

**译文**

现在，我们将测试实际的认证流程。如果你在 GitHub 上创建了一个 OAuth 应用，那么在本练习完成后，你就应该能够测试这个认证流程了。接下来，你需要访问 Kelly 为我们准备好的 GitHub 认证回调路由，并在其中填写几个信息，以使用 Remix 认证器（也就是我们刚刚创建的 Remix Auth 认证器对象）进行认证。然后，我们还将访问常规的 GitHub URL。

## 41. 140. Implementing OAuth2 Flow with GitHub for User Authentication

**原文**

Let's first go to our login where we're going to be rendering the provider connection form. If you dive into that, it's a pretty simple form. Just form here with the status button and shows an icon for the provider that we're connecting to. Not a whole lot of complex stuff going on here. Probably the most important part here is this form action that the action goes to slash auth slash provider name and we're going to provide GitHub. So this is going to the action is going to be auth GitHub.

**译文**

首先，我们前往登录页面，我们将在该页面渲染提供商连接表单。如果你深入查看，会发现这是一个非常简单的表单。这里只是一个包含状态按钮的表单，并显示我们正在连接的提供商图标。这里没有太多复杂的内容。其中最重要的部分可能是这个表单的 action，它会提交到 `/auth/provider-name`，而我们将提供 GitHub。因此，这个 action 将是 `auth GitHub`。

## 42. 141. Simulating Third-Party Dependencies

**原文**

I really don't like having third parties be tied into how I develop my software, both for development as well as testing. For a couple of reasons. If their servers go down, then we're stuck. We can't develop our software. If my network connection is slow or non-existent, then I'm stuck. Can't develop my software. If I have to pay for access to their APIs, then yeah, I'm paying out the no. So I really like to mock out all of my third parties

**译文**

我真的不喜欢在开发和测试软件时，让第三方服务与我的开发流程绑定在一起。原因有几个：如果他们的服务器宕机了，我们就会被卡住，无法开发软件；如果我的网络连接缓慢或完全中断，我也会陷入困境，同样无法开发软件；如果我必须为访问他们的 API 付费，那简直就是在无休止地花钱。因此，我非常喜欢将所有第三方服务都模拟（mock）出来。

## 43. 142. Simulating GitHub Authentication Flow with Mocks

**原文**

The first thing we're going to want to do is go to our ENV here and prefix both of these with mock underscore. Just to communicate, these are mocked and our server will behave a little bit differently. Our mocks will behave differently based on the fact that this is prefixed with mock. Okay, great. And then we can go to our auth GitHub route right here. And this is what handles or this is the action that handles me clicking on this. So right now if we let this go through, this is going to send us to GitHub.

**译文**

我们要做的第一件事，就是进入这里的 ENV，给这两个项都加上 `mock_` 前缀。这样做是为了表明它们是模拟的，我们的服务器行为也会因此略有不同。由于添加了 `mock_` 前缀，我们的模拟行为也会随之改变。好的，很好。接下来，我们可以来到这里的 `auth GitHub` 路由。这个路由负责处理我点击该选项时的操作。因此，如果现在让这个流程继续执行，它就会把我们重定向到 GitHub。

## 44. 143. Updating Prisma Schema for GitHub Login

**原文**

For us to be able to log in with GitHub, we need to have a user that has a connection already. And we also need to have some data or tables in the database for managing these connections. So your job in this exercise is to update the Prisma schema to add a connection model. The most important part of that is the provider name and the provider ID that would uniquely identify a connection or like an account on another service. And then it will be associated

**译文**

为了让我们能够通过 GitHub 登录，我们需要一个已经建立连接的用户。此外，我们还需要在数据库中准备一些数据或表来管理这些连接。因此，本次练习的任务是更新 Prisma 模式，添加一个连接模型。其中最重要的部分是提供商名称和提供商 ID，它们可以唯一标识一个连接，或者说另一个服务上的账户。然后，该连接将被关联起来。

## 45. 144. Establishing Connections and Seed Script in Prisma for GitHub Authenticatio

**原文**

Let's go over to our schema here and right down at the bottom. We're going to add a connection model. So model connection and It's going to have all the typical properties that we have. So we've got the ID just like all the others. We have a provider name. So this would be GitHub or Google or whatever other service that you're authenticating with. If you're authenticating with it a Enterprise and doing single sign-on or something like that, that would be

**译文**

现在我们转到模式部分，直接定位到底部。我们将添加一个连接模型。因此，我们创建一个 model connection，它将包含我们通常拥有的所有属性。比如，和其他模型一样，我们有一个 ID。还有一个 provider name，这可以是 GitHub、Google 或其他您用于身份验证的服务。如果您是通过企业系统使用单点登录等功能进行身份验证，那么这里就是相应的设置。

## 46. 145. Dad Joke Break Oauth

**原文**

How did Darth Vader know what Luke was getting for Christmas? He felt his presence. Haha. All right, so that was a bit of work, but you should pat yourself on the back, say good job to yourself, feel good about yourself. Like this is a lot of work, all this learning that you're doing. So keep on learning, but you know, it is good to take a break every now and then. So now is a good time to do that. Take a break and then come back and continue to learn and take notes and write things down that you're learning so you remember it. And then you can go use it in

**译文**

达斯·维达是怎么知道卢克圣诞节会收到什么礼物的？他感受到了卢克的存在。哈哈。好了，刚才这段内容确实有点难度，但你应该给自己点个赞，夸夸自己，感觉很棒吧。要知道，你现在学的这些东西可都是要花很多功夫的。所以，请继续学习下去，不过你知道吗，偶尔休息一下也是很好的。现在正是休息的好时机。先休息一下，然后再回来继续学习，做好笔记，把你学到的东西都写下来，这样你才能记住。然后你就可以把它们应用到……

## 47. 146. Intro to Provider Errors

**原文**

Sometimes things happen and we got to handle these connection errors. So occasionally the third party that you're authenticating with is going to be down. So you got to handle that edge case. That's going to be a pretty quick one. And also edge cases on connection. Sometimes they're like different situations. So let me demonstrate that one really quick. So here I am going to manage my connections. This is a new page that Kelly, the coworker made for us, which is nice. And we've got this connect with GitHub that's going through the exact same

**译文**

有时会发生一些事情，我们必须处理这些连接错误。因此，你正在验证身份的第三方服务偶尔会宕机。所以你必须处理这种边缘情况。这部分内容会讲得很快。另外，连接方面也存在一些边缘情况，有时它们属于不同的场景。让我快速演示一下。现在我要管理我的连接。这是同事 Kelly 为我们创建的新页面，挺不错的。我们这里有一个“与 GitHub 连接”的选项，它正在经过完全相同的流程

## 48. 147. Handling Errors in Third-Party API Calls

**原文**

Sometimes errors happen even in our third party APIs and we should probably handle those like reasonably well. And so if we go to our GitHub mock right here and uncomment this inside of the access token API call, for example, then right now, with what we have implemented, nothing happens. I click on this, nothing happens. I click on it a million times, nothing happens. Well, something actually is happening. If we check our logs, we're seeing this big failed defetch throw and all bad stuff.

**译文**

有时，即使是我们使用的第三方 API 也可能出现错误，我们应当以合理的方式处理这些错误。因此，如果我们来到这里的 GitHub 模拟示例，并取消注释访问令牌 API 调用中的这段代码，例如，那么以我们目前的实现来看，什么都不会发生。我点击它，没有反应。我点击一百万次，仍然没有反应。嗯，其实还是有事情在发生的。如果我们查看日志，就会看到这种“defetch”失败抛出的异常以及所有糟糕的信息。

## 49. 148. Handling Errors and Redirecting with GitHub Authentication

**原文**

So let's handle this error right here. We're going to go to our provider callback. And in here, we're going to just add a catch. That's going to be an error. This is going to be async, though. So let's take that error. And then we're going to throw await redirect with toast. We're going to redirect them back to the login. We're going to give them an error, let's say type error. And I don't typically like including the error message unless I really know what it's

**译文**

那么，我们来处理这里的错误。我们将前往 provider 回调函数，并在其中添加一个 catch 块。这个 catch 块将接收一个 error 参数。不过，由于这里是异步操作，我们需要处理这个 error。然后，我们将抛出 `await redirect with toast`，把用户重定向回登录页面，并向他们显示一个错误，比如类型为 `error` 的错误。通常，除非我非常清楚错误的具体内容，否则我不太喜欢直接包含错误信息。

## 50. 149. Handling Connection Errors and Duplication in Account Management

**原文**

Our users have this manage connections page that will show all of the connections that they have in their account. And if we try to connect with GitHub to an existing connection, then that's going to be a problem. Let's say we already have a connection for Cody right here. If we try to connect with GitHub again with that same thing, then that's just not going to work. So we want to display a connection error just say like, hey, that doesn't work. Or if we're signed in as a different user and try to connect with the same account as another user,

**译文**

我们的用户有一个“管理连接”页面，该页面会显示其账户中的所有连接。如果我们尝试将 GitHub 连接到一个已有的连接，就会出现问题。假设我们这里已经有一个 Cody 的连接。如果我们再次尝试用相同的凭据连接 GitHub，那么操作将无法成功。因此，我们希望显示一个连接错误，提示类似“嘿，这样行不通”的信息。或者，如果我们以另一个用户身份登录，并尝试连接另一个用户已使用的相同账户，也会出现类似情况。

## 51. 150. Handling Existing Connections in AuthProvider Callback

**原文**

Let's go to our auth provider callback. And right here, we know that the user's already gone through the GitHub auth flow. And so by the time they get here, we can look at that profile and know that whoever's making this request has access to this profile. Let's go see if there's an existing connection. So existing connection will come from await prisma.connection and it'll be actually a find unique where the provider name and provider ID

**译文**

让我们转到我们的身份验证提供商回调处。在这里，我们知道用户已经完成了 GitHub 身份验证流程。因此，当他们到达这里时，我们可以查看该配置文件，并知道发起此请求的用户有权访问此配置文件。让我们看看是否存在现有连接。现有连接将通过 `await prisma.connection` 获取，实际上是一个 `findUnique` 操作，其中会检查提供商名称和提供商 ID。

## 52. 151. Dad Joke Break Provider Errors

**原文**

Here about the new restaurant called Karma. There's no menu. You get what you deserve. Haha. That makes me think of the testing framework called Karma years ago, long before we had Playwright and Puppeteer and all those. Yeah, good times. You know, it was, it was all right. It was pretty good, but I'm really happy with the cool testing tools we have now. All right. So with that, it is break time. Time to take a quick little break, get a drink of water, go to the bathroom, whatever you need to do, and then come on back because we've got more stuff to learn.

**译文**

关于那家叫 Karma 的新餐厅。那里没有菜单。你能得到你所应得的。哈哈。这让我想起了多年前那个叫 Karma 的测试框架，远在我们拥有 Playwright 和 Puppeteer 以及所有那些工具之前。是啊，那段时光真不错。你知道的，它，它其实还行。相当不错，但我现在拥有的这些酷炫测试工具真的让我很满意。好了。那么，现在是休息时间。该短暂休息一下，喝杯水，去趟洗手间，做你需要做的任何事，然后再回来，因为我们还有更多内容要学习。

## 53. 152. Intro to Third Party Login

**原文**

I'm so excited because in this exercise, we're finally going to make this login with GitHub thing do what it says it's going to do, which is login with GitHub. We're also going to make support for create an account. So if we hit sign up with GitHub, that will allow users to sign up. But we've got a new onboarding flow specifically for that. Now, the trick here is that login already it involves more than just a couple of like setting a value in a cookie, right? Because now we've got two factor authentic

**译文**

我太激动了，因为在这次练习中，我们终于要让这个“使用 GitHub 登录”的功能真正实现其承诺的功能——也就是通过 GitHub 登录。我们还将支持创建账户。因此，如果我们点击“使用 GitHub 注册”，用户就可以完成注册。不过，我们会为这一流程引入全新的引导流程。现在，这里的关键在于，登录功能本身已经不仅仅涉及在 Cookie 中设置几个值那么简单了，对吧？因为现在我们引入了双重身份验证。

## 54. 153. Implementing GitHub Login with Two-Factor Authentication

**原文**

All right, it's finally time to make it so that when you click a login with GitHub, you actually log in with GitHub. And so in this exercise, there's actually not a whole lot for us to do. We just need to create a session. So first of all, you need to make sure that, all right, so that with this profile ID, here's the connection that they have. And so this is the user that's logging in. Once you determine that, then you can create the session. And then we just need to do the exact same thing that we're already doing in our login, which involves, you know,

**译文**

好的，现在终于到了实现点击 GitHub 登录时，真正通过 GitHub 登录的功能了。在这个练习中，我们其实要做的并不多，只需要创建一个会话即可。首先，你需要确保，好的，这样就能通过这里的个人资料 ID 找到用户已有的连接。这就是正在登录的用户。一旦确定了这一点，你就可以创建会话了。然后，我们只需要执行与现有登录流程中完全相同的操作，也就是涉及……

## 55. 154. Refactoring Login Logic and Implementing GitHub Login

**原文**

Let's head over to login first to do this refactor. So right down here in our action, we've got all of this logic that involves after we know that this user is who they say they are, and we've got a session ready for them. This involves the whole process of getting them logged in. And so we're going to take this, and we're going to cut it out. We're going to return handle new session, which will pass the request,

**译文**

我们先前往登录部分来完成这次重构。就在我们这里的 action 中，有所有这些逻辑——在我们确认用户身份无误并为其准备好会话之后，这些逻辑会处理整个登录流程。因此，我们将把这部分代码剪切出来，并返回 `handle new session`，它会传入请求。

## 56. 155. Sign Up with GitHub and Handling Mocked Data

**原文**

So now we're going to do the sign up with GitHub flow. And what's interesting about this sign up is that there's actually nothing different as far as the code path is concerned between clicking this button and clicking this button. It's just like aesthetics for the user. But whether you're going through the login with GitHub or the sign up with GitHub, it is the same. So if the only difference really is, is there already a user signed up or signed in with this particular GitHub account?

**译文**

现在我们要通过 GitHub 流程进行注册。这个注册流程的有趣之处在于，就代码路径而言，点击这个按钮和点击那个按钮实际上没有任何区别。这只是对用户而言的界面美观问题。但无论是通过 GitHub 登录还是通过 GitHub 注册，过程都是一样的。因此，唯一的真正区别可能在于：是否已经有用户使用了这个特定的 GitHub 账户进行了注册或登录？

## 57. 156. Onboarding and User Authentication with Third-Party Providers

**原文**

Let's get these users logged in. We'll go to our callback here and we've got this little Import of a couple of things that we're going to need here in a bit. So we'll just uncomment that and now we're handling a bunch of cases. So If there is an existing connection and user ID, then we're going to tell them they're already connected. If there is an existing connection, then we'll log them in and we also need to handle the case where there is not an existing connection, but the email from the provider matches an email we already have and we want to connect those and then log them in.

**译文**

让我们让用户登录。我们转到这里的回调函数，这里有一个小小的导入语句，导入了一些我们稍后需要用到的东西。我们只需取消注释即可，现在我们就处理多种情况了。如果存在现有的连接和用户 ID，那么我们会告知用户他们已经连接。如果存在现有的连接，我们会让用户登录。我们还需要处理这样一种情况：虽然不存在现有的连接，但来自提供程序的电子邮件地址与我们已有的某个电子邮件地址匹配，此时我们需要将两者关联起来，然后让用户登录。

## 58. 157. Dad Joke Break Third Party Login

**原文**

What's the tallest building in the world? The library. It's got the most stories. Ha ha. All right. Now it's a good time for you to take a break. All of this learning takes a lot of brain energy and you need blood flow and like sitting at the computer typing does not make your blood flow. Like you're moving fingers, but yeah, blood is not going through your body very efficiently. So it's a good time to get up, take a break, get a drink of water, go to the bathroom, whatever you need to do. Give somebody a high five. Give them a hug. Just make somebody feel awesome and then come back because we've got

**译文**

世界上最高的建筑是什么？是图书馆。它“故事”最多（楼层最多）。哈哈。好了。现在正是你休息的好时机。所有这些学习都需要消耗大量脑力，而你需要促进血液循环，但坐在电脑前打字并不能有效促进血液流动。虽然你的手指在动，但血液在体内的循环效率并不高。所以，现在正是起身休息、喝杯水、上个厕所、做点你需要做的事情的好时机。和别人击个掌，给他们一个拥抱，让别人感觉棒棒的，然后再回来，因为我们还有……

## 59. 158. Intro to Connection

**原文**

Connection management. So we're going to just do a couple of things here to make managing user connections a little bit better. So first we're going to manage what happens if a user logs in with GitHub and we see that the profile email matches the email address of a user we already have in our database. We should probably just make the connection and let the user in. And so that is one situation like because the whole point of this login process is we want to

**译文**

连接管理。因此，我们将在这里做几件事，以改善用户连接的管理。首先，我们将处理用户通过 GitHub 登录时，其个人资料的电子邮件地址与我们数据库中已有用户的电子邮件地址相匹配的情况。我们很可能应该直接建立连接并让用户登录。这就是其中一种情况，因为整个登录流程的核心目的就是我们希望

## 60. 159. Connecting Website and GitHub Accounts

**原文**

Let's say that we've got a user on our website and they want to connect their GitHub account. So the website account is kodi at kcd.dev and the GitHub user is also kodi at kcd.dev. Connecting those accounts could probably happen as part of the login process, right? That would make sense if they have ownership of both of those accounts. Then let's hit login with GitHub and oh, we've already got an email or a user with that email. Let's just connect their accounts and log them in. So for this exercise,

**译文**

假设我们的网站上有一个用户，他们想要连接自己的 GitHub 帐户。网站帐户是 kodi@kcd.dev，GitHub 用户也是 kodi@kcd.dev。连接这些帐户很可能可以作为登录流程的一部分来完成，对吧？如果他们拥有这两个帐户的所有权，这样做就很合理。那么，我们点击“使用 GitHub 登录”，哦，我们已经存在一个具有该电子邮件地址的电子邮件或用户了。那我们直接连接他们的帐户并登录即可。所以对于这个练习，

## 61. 160. Automatically Connecting User Profiles with Existing Accounts

**原文**

Let's go to our provider callback. And right here, after we've established that, oh, there's already an existing connection. Let's make that session. So all that stuff that we were doing before, we put into this handy little utility. And the reason is because we need that utility for what we're about to do. We're going to do exactly the same thing. So what we need to determine now is, OK, there's not an existing connection. But if there is a profile that already has

**译文**

让我们转到我们的提供者回调。就在这里，在我们确认“哦，已经存在一个连接”之后，我们来创建那个会话。因此，我们之前做的那些事情，都被我们放进了这个实用的小工具里。原因在于，我们即将要做的事情需要用到这个工具。我们将执行完全相同的操作。所以现在我们需要确定的是：好的，目前不存在连接。但如果已经存在一个拥有...的配置文件的话

## 62. 161. Adding Multiple GitHub Connections to User Accounts

**原文**

It's totally reasonable for you to have multiple accounts that they want to connect so they can log in with whichever account they're logged in at the time. And so we have our connections page that allows multiple GitHub connections. So what your job in this exercise is to support that in our connection callback. The one thing that I will call out specifically is in our provider's GitHub server where we have our handle mock action. To test this out, you can change this to whatever

**译文**

您拥有多个想要关联的账户是完全合理的，这样用户就可以使用当前登录的任意账户进行登录。因此，我们提供了一个支持关联多个 GitHub 账户的“连接”页面。在本练习中，您的任务就是在连接回调函数中实现对这一功能的支持。需要特别说明的一点是，在我们的 GitHub 服务器提供程序中，有一个用于处理模拟操作的句柄（handle mock action）。要测试这一功能，您可以将其更改为任意值。

## 63. 162. Connecting Existing Accounts with an Auth Provider

**原文**

Let's go over to our auth provider callback. And right here, if there is a user ID, that means that they're logged in. So once we get to this point, we know that it's not an existing connection and a user ID. So if we get here and we say if there's a user ID, then we know there's no existing connection. So we can make the connection. So if user ID, then we can await prisma connection dot create create

**译文**

让我们转到身份验证提供者的回调部分。就在这里，如果存在用户 ID，那就意味着他们已经登录。因此，一旦我们到达这一步，我们就知道这并非现有连接，并且存在用户 ID。所以，如果我们来到这里并判断存在用户 ID，那么我们就知道没有现有连接。因此，我们可以建立连接。所以，如果存在用户 ID，那么我们就可以等待 prisma connection.create 方法。

## 64. 163. Dad Joke Break Connection

**原文**

They're making a movie about clocks. It's about time. Ha ha. There you go. That one's a pretty good chuckle. So how are you doing? Are you doing okay? I hope you're doing awesome. I hope that you're having a really good time learning all this stuff. There's a lot to it and a lot to learn and it's that what I'm going for is really deep understanding. And so the cool thing about this is you can go through this material again later and give it a little bit of time to percolate and then come on back and and learn some more.

**译文**

他们正在拍一部关于时钟的电影。这部电影是关于时间的。哈哈。就是这样。这个笑话还挺好笑的。那么你最近怎么样？一切都好吗？我希望你一切都棒极了。我希望你在学这些东西的时候过得非常愉快。这里面有很多内容，也有很多需要学习的地方，而我追求的是真正深入的理解。所以，这件事很酷的一点是，你可以在稍后再重新学习这些材料，给它们一点时间慢慢消化，然后再回来继续学习更多东西。

## 65. 164. Intro to Redirect Cookie

**原文**

For this exercise, we're going to add the redirect cookie. Now you might be saying, Kent, we already did redirect. We have this support where you can say settings profile and then it says login redirect to all that stuff. Like that all works right now. But it doesn't work with the login with GitHub. And so the challenge here is that we can't just use the login URL query plan because we're going off site and then coming back. And so we lose that. So we need to have some persistent storage. And so there are a couple of things we need to do.

**译文**

在本练习中，我们将添加重定向 Cookie。现在你可能会说，Kent，我们已经实现过重定向了。我们已经有这样的功能：你可以设置“settings profile”，然后它会提示“login redirect”等相关内容。这些功能目前都能正常工作。但它们在与 GitHub 登录配合使用时却不起作用。因此，这里面临的挑战是：我们不能直接使用登录 URL 的查询参数（query plan），因为用户会跳转到外部网站然后再返回，这样一来这些信息就会丢失。所以我们需要一种持久化的存储方式。为此，我们需要完成几项工作。

## 66. 165. Managing Redirects in Forms and Handling Cookies for Persistent Navigation

**原文**

So right now we've got a redirect to in the URL. If I come over here and take a look at our form, let's get ourselves a little bit more room, then this form has a redirect to right here. It's hidden search or settings and slash profile. However, that is not the case for this form, which is completely different form. It just has the button and nothing else. So we need to add a redirect to so that the action that handles this form submission can put that redirect to

**译文**

现在我们看到 URL 中有一个重定向。如果我来到这里查看我们的表单，再给点空间，那么这个表单在这里有一个重定向，即 hidden_search 或 settings/profile。不过，这个表单的情况并非如此，它是一个完全不同的表单，只有一个按钮，没有其他内容。因此，我们需要添加一个重定向，以便处理该表单提交的操作能够执行该重定向。

## 67. 166. Adding Redirect Functionality to Login and Signup Forms

**原文**

Let's start out and log in and right down here in our UI, we've got the provider connection form and we want to add a redirect to prop to that. So redirect to is the redirect to that we're using for the login. Now it's not too jazzed about that. So we've got to go in here and get our redirect to prop defined. I think it's reasonable to say that this needs to be an optional string. So not required. And then we'll just render

**译文**

让我们开始，登录并直接来到我们的 UI 这里，我们有一个提供商连接表单，我们想为其添加一个重定向属性。因此，`redirect_to` 就是我们用于登录的重定向地址。目前它还没有被很好地处理。所以我们必须进入这里，定义我们的 `redirect_to` 属性。我认为可以合理地将其设为一个可选字符串，即非必需项。然后我们只需渲染即可。

## 68. 167. Handling Redirects and Cookies

**原文**

For this section, now that we've got this redirect to getting into the form, we got to go from the form into the cookie. And so that's your objective here. You've done cookies before. So Kelly, the coworker put together this redirect cookie utility for us. And so there are a couple of pieces or utilities here that one you're going to focus on is this get redirect cookie header. We also have another utility you're going to be using called getRipFurver that you'll be using to give a good default for what

**译文**

对于本节内容，既然我们已经完成了跳转到表单的这一步，接下来就需要从表单过渡到 Cookie。这就是你在这里的目标。你之前已经处理过 Cookie 了。所以，同事 Kelly 为我们编写了这个重定向 Cookie 工具。这里有一些组件或工具，其中你需要重点关注的就是这个 `get redirect cookie header`。此外，你还会用到另一个名为 `getRipFurver` 的工具，它会用于提供一个合理的默认值。

## 69. 168. Handling Authentication Redirects and Cookies

**原文**

So let's go to our auth provider route. That's the route that's going to handle this submission. And we'll grab these utilities. We're going to need those. And then we're going to wrap these two in a try catch so that we can augment the response that's thrown. So we're going to just re-throw the error, whatever it is. But if that error is an instance of a response object, then we're going to be able to do a couple of extra things. So let's get the form data from await.

**译文**

那么，我们转到认证提供程序路由。这个路由将处理提交操作。然后我们获取这些工具函数，因为我们需要用到它们。接着，我们将这两行代码包裹在 try-catch 中，以便能够增强抛出的响应。因此，我们会重新抛出错误，无论它是什么。但如果该错误是响应对象的一个实例，那么我们就可以执行一些额外操作。现在，让我们从 await 中获取表单数据。

## 70. 169. Handling Redirects

**原文**

Okay, now we're finally going to take that redirect value out of the cookie and then send that user to where they're supposed to go. And in addition, in this step of the exercise, we're going to add that destroy redirect to cookie header so that we can get the redirect to out of the user's cookie so they don't accidentally get redirected at some point later down the line. And so that is your objective in this exercise. There's actually, there are quite a few lines of code that are changed, but lots of it is pretty straight forward.

**译文**

好的，现在我们终于要从 Cookie 中取出那个重定向值，然后将用户发送到他们应该去的地方。此外，在本练习的这一步骤中，我们还将添加一个“销毁重定向”到 Cookie 标头，以便将重定向信息从用户的 Cookie 中清除掉，这样他们之后就不会在某个时间点被意外重定向了。这就是你在本次练习中的目标。实际上，有相当多代码行被修改了，但其中大部分内容都相当直接。

## 71. 170. Managing Redirects and Cookies

**原文**

So let's go to our callback. Woo, we're almost done. So we'll bring in these utilities and then we'll just go top to bottom and deal with every one of these cases piece by piece. So we're going to be using this object quite a bit, a set cookie header. So we'll just create an object for that. Then let's get the redirect value or the re-react to value from get redirect cookie value, which comes out of the request. And then right here where we're redirecting with toast to that is

**译文**

那么，让我们进入回调函数。哇，我们快完成了。接下来，我们会引入这些工具，然后从上到下逐一处理这些情况。我们将频繁使用这个对象，也就是“设置 Cookie 标头”（set cookie header）。因此，我们先为它创建一个对象。然后，通过 `get redirect cookie value` 获取重定向值或“重新响应”值，这个值来自请求（request）。接着，在我们使用 `toast` 进行重定向的位置，也就是

## 72. 171. Dad Joke Break Redirect Cookie

**原文**

What do birds give out on Halloween? Tweets! Haha! That actually is kind of sad. The death of Twitter and the rise of X. We'll see when you're watching this who knows what the world looks like. But birds do tweet. That is how we say what the sound that they make. So anyway, well done on everything. Pat yourself on the back. Give somebody a high five. This exercise stuff is a lot of work and you've got to take a break right down the stuff that you learned so that you don't forget because that's very

**译文**

万圣节期间鸟儿会发出什么声音？“推文”！哈哈！这其实有点令人难过。推特的消亡和X的崛起。当你观看这段视频时，谁知道世界会变成什么样子呢。但鸟儿确实会“tweet”（鸣叫）。我们就是这样形容它们发出的声音的。总之，为你所做的一切点个赞。给自己鼓鼓掌。跟别人击个掌吧。这些练习真的很耗费精力，你必须休息一下，回顾一下所学内容，以免忘记，因为这非常重要……

## 73. 172. Outro to Authentication Strategies & Implementation Workshop

**原文**

You, you should be so proud of yourself right now. You've done an amazing thing. We've done so much stuff as a part of this entire exercise and the series of exercises. So many things we've learned through the many, many exercise. I think there's over like 120 instances of the app in this workshop. So yeah, just a ridiculously huge workshop and you've done an amazing job. So well,

**译文**

你、你现在应该为自己感到非常自豪。你完成了一件了不起的事情。作为整个练习以及这一系列练习的一部分，我们已经做了很多很多的事情。通过这许多、许多的练习，我们学到了很多知识。我想在这个工作坊中，大约有超过120个应用实例。所以是的，这确实是一个规模大得离谱的工作坊，而你完成得非常出色。所以，很好，

## 74. 01. Intro to Web Application Testing Workshop

**原文**

It is time to do testing. Testing is great. Okay, maybe I'm overdoing it a little bit, but I really do enjoy testing. When you've got your tools set up in the right way and you have the utilities all ready for you, ready to go, it's actually quite nice to test. And so we're going to be covering a ton of stuff. We've got end-to-end tests with Playwright and this testing environment is pretty sick, I must say. And so you can like

**译文**

是时候进行测试了。测试很棒。好吧，也许我有点言过其实，但我确实很喜欢测试。当你以正确的方式配置好工具，并准备好所有实用程序、随时可以使用时，进行测试其实相当不错。因此，我们将涵盖大量内容。我们将使用 Playwright 进行端到端测试，而且这个测试环境真的很棒，我必须这么说。所以你可以……

## 75. 02. Intro to End-to-End

**原文**

Let's write some end-to-end tests. This exercise is going to introduce you to Playwright, this amazing tool that allows us to write awesome automated tests. So first, I want to talk about manual testing a little bit. No matter what you do, you cannot avoid testing. It is basically impossible. Nobody just writes code and then ships it without running some form of tests, whether that be an automated test that they wrote a script for, or manually running the code and executing the code.

**译文**

我们来编写一些端到端测试吧。本练习将向你介绍 Playwright——这款能帮助我们编写出色自动化测试的绝佳工具。首先，我想简单聊聊手动测试。无论你做什么，都无法避免测试。这基本上是不可能的。没有人会只编写代码就直接发布，而不运行任何形式的测试——无论是自己编写脚本进行的自动化测试，还是手动运行和执行代码。

## 76. 03. Writing Automated Tests with Playwright UI Mode

**原文**

Whenever you're writing an automated test, the way that I like to think about it is you put yourself in the shoes of the product manager, whoever's deciding how the product actually works. And that person, you just imagine yourself telling a manual tester what they should be doing to like every time there's a code change, I want you to go in here and do this. And so for the thing we're going to be testing, this is what I would say to that manual tester. Go to the homepage, type in Cody,

**译文**

每当编写自动化测试时，我喜欢这样思考：让自己站在产品经理的角度——也就是决定产品实际运作方式的人的角度。你可以想象自己正在告诉一个手动测试人员，每当有代码变更时，他们应该执行哪些操作。因此，对于我们要测试的这个功能，我会这样告诉那个手动测试人员：前往主页，输入“Cody”。

## 77. 04. Writing and Asserting Playwright Tests for Search Functionality

**原文**

So let's go ahead and go to our test e to e search dot test file. This is where our tests are going to be. And we're going to import expect and test from playwright test. And this is going to allow us to write a test, we can give it a title. So we can say, search from home page. And now we've got our steps. And this is going to be async for sure. And we're also going to need the page to be able to execute different commands and

**译文**

那么，我们现在就进入我们的 test-e-e-search.test 文件。我们的测试将写在这里。我们将从 playwright test 中导入 expect 和 test。这样我们就能编写一个测试，并为其指定一个标题。比如，我们可以写成：从主页进行搜索。现在我们就有了测试步骤。这个步骤肯定是 async 的。我们还需要 page 来执行不同的命令，并且

## 78. 05. Isolating Tests for Better Reliability and Flexibility

**原文**

Typically, it's a really bad idea to make your test rely on something outside of the test. And the reason for that is if somebody changes the setup for some reason and then pushes that, and then later you run your test and you're like, oh, this is broken now, and I have no idea why. And so there's that level of indirection that makes it a lot trickier to make your life happy. So what I recommend instead is you have your test be able to be completely isolated.

**译文**

通常，让测试依赖于测试外部的某些东西，是一个非常糟糕的主意。原因在于，如果有人出于某种原因更改了配置并提交更改，之后你运行测试时就会发现，哦，现在测试出错了，而你完全不知道为什么。这种间接性会让事情变得棘手得多。因此，我建议你让测试能够完全独立。

## 79. 06. Creating and Interacting with User Data

**原文**

Let's go to our search right here and we're going to create a new user. So let's get that new user from await prisma dot user dot create. And our data, we have a utility for this. This is create user from our DB utils. And I want to add a select all that we're going to need here is let's see the name true and the username true. And that should be enough actually. Okay, great. So now let's

**译文**

让我们来到这里的搜索处，然后创建一个新的用户。因此，我们通过 `await prisma.user.create` 来获取这个新用户。对于数据部分，我们有一个工具可以使用。这是来自我们 `DB utils` 的 `createUser` 工具。我需要添加一个全选操作，这里我们需要的是——让我看看——`name: true` 和 `username: true`。这样其实就足够了。好的，很好。那么现在让我们……

## 80. 07. Test Isolation in End-to-End Testing

**原文**

We've got ourselves a little bit of a problem. So every time we run this test, I seem to get another user on this user's page. So if I hit play again on this test, then refresh. Oh, there's another one. So this is a problem. And the solution is we need to clean up after ourselves. The test creates a new user, but we need to make sure we get rid of that user at the end of the test. So that way we don't just keep on filling up our database with tons of nonsense data, especially as you get lots of tests

**译文**

我们遇到了一个小问题。每次运行这个测试时，我似乎都会在这个用户的页面上添加另一个用户。所以，如果我再次点击这个测试的“播放”按钮，然后刷新页面，哦，又出现了一个新用户。这就是一个问题。解决方法是，我们需要在测试结束后清理自己创建的数据。测试会创建一个新的用户，但我们必须确保在测试结束时将该用户删除。这样，我们就不会让数据库中堆积大量无意义的数据，尤其是在测试数量增多时。

## 81. 08. Proper Setup and Teardown of Testing for Database Cleanup

**原文**

Yeah, yeah. Okay. This one was pretty quick, but it is important and that's why it deserves its own step in this exercise. It's literally just await prisma user delete where the user ID matches the ID of the user that we got. So let's add our ID right here. And we could also do their username because that's a unique field as well. But there we go. So we delete the user when we're all done. So we've got four users. If I run it again, or four extra users,

**译文**

嗯，嗯。好的。这一步完成得很快，但它很重要，因此值得在本练习中单独作为一个步骤。其实就是 `await prisma.user.delete({ where: { userId: 我们获取到的用户ID } })`。那我们在这里添加上我们的ID。我们也可以根据用户名来删除，因为用户名也是一个唯一字段。好了，就是这样。当我们完成所有操作后，就会删除用户。所以我们现在有四个用户。如果我再次运行，就会多出四个用户。

## 82. 09. Implementing Fixtures to Ensure User Deletion in Playwright Tests

**原文**

So we're not totally out of the woods yet. We still have a situation where we can end up with a user that was generated as part of the test and not actually deleted. And that situation is pretty simple, actually. If we've got an error that's thrown after we create the user, then that user is going to stick around because we never get around to the part of the code that is going to actually delete the user. So here we go. Got another one. And we play it again. It's going to break again after creating the user.

**译文**

所以我们还没能完全摆脱困境。我们仍然可能遇到这样的情况：某个用户作为测试的一部分被创建出来，但并未真正被删除。这种情况其实很简单：如果在创建用户之后抛出错误，那么这个用户就会一直存在，因为我们永远执行不到代码中真正负责删除用户的逻辑。现在我们开始。又出现了一个。我们再运行一次。它会在创建用户后再次出错。

## 83. 10. Playwright Fixtures for Testing

**原文**

So we're going to be making our own test object. So I'm going to use this as base. I said object, it actually is, it's a function with object properties like expect. So we're also going to remove expect here. And then we're going to say test dot extend or base base dot extend. And that is going to allow us to get our own test function. And test will also have the expect function as well. So we can get expect.

**译文**

所以我们要创建自己的测试对象。我将使用这个作为基础。我说是对象，但实际上它是一个具有 `expect` 等对象属性的函数。所以我们也要在这里移除 `expect`。然后我们执行 `test.extend` 或 `base.extend`。这样我们就能得到自己的测试函数。`test` 也将包含 `expect` 函数。因此我们可以获取到 `expect`。

## 84. 11. Dad Joke Break E2E

**原文**

What did one plate say to another plate? Dinner's on me! Haha! Alright, maybe it's dinner time for you and so this is a good time for you to take a break and go get dinner. And come on back because we've got more testing to do. So make sure to take a break, go fill up your water bottle if it's empty and because you got to stay hydrated, write down the stuff that you're learning, all that stuff is very important. But getting blood flow into your brain is also important. You're doing a great job, so let's keep up this good work.

**译文**

一个盘子对另一个盘子说了什么？晚餐我请客！哈哈！好吧，也许是时候该你去吃晚餐了，所以现在正是你休息一下、去吃晚餐的好时机。记得再回来，因为我们还有更多的测试要做。所以一定要休息一下，如果水瓶空了就装满水，因为你必须保持水分充足，把你学到的东西都记下来，所有这些都非常重要。不过，让血液流向你的大脑也很重要。你做得很好，让我们继续保持这种良好的势头吧。

## 85. 12. Intro to E2E Mocking

**原文**

Alright, I want to talk about mocking and I'm not just talking about like being nice to people and not mocking them. No, this is something else. So mocking is basically you take the real thing and you swap it out for something that's fake. Let's figure out why that would be. So we'll use an example. Let's say that I'm building a store where you can buy really cute plush koalas and I need to test to make sure that the checkout process works. That's probably the most important part of the whole thing is that the checkout process

**译文**

好的，我想谈谈“mocking”（模拟/Mocking），我说的不仅仅是待人友善、不取笑别人那种“mocking”。不，这是另一回事。所谓“mocking”，基本上就是你把真实的东西替换成一个虚假的替代品。那我们来想想为什么要这么做。我们用一个例子来说明。假设我正在开发一个商店，你可以在这里购买非常可爱的毛绒考拉，而我需要测试以确保结账流程能正常工作。这大概是整个系统最重要的一环，也就是结账流程。

## 86. 13. Writing Emails to the File System for Test Automation

**原文**

So we've got some new tests that Kelly put together for us, but they're not finished. We need to fix a couple of things. So if I run this onboarding test, this is going to go through the onboarding flow and it's going to get to this check your email piece. But we get stuck here because we actually don't have an email yet. This part is not yet implemented. So now what we need to do is somehow get this code, this verification code into our application. But there's not really a way for us to take a look at the terminal output and find

**译文**

所以我们现在有了一些 Kelly 为我们准备的新测试，但它们尚未完成。我们需要修复几个问题。如果我运行这个引导测试，它会执行整个引导流程，然后到达“检查你的电子邮件”这一步。但我们会在这里卡住，因为我们目前还没有电子邮件。这部分尚未实现。所以现在我们需要想办法将这个代码——也就是这个验证代码——引入到我们的应用程序中。但实际上并没有办法让我们查看终端输出并找到它。

## 87. 14. Handling Emails in Node.js using File System

**原文**

Like I said, this exercise is pretty darn simple. So if we go to our mock, Resend, then we're already getting the, like parsing the email and mocking out the email because we had to do that earlier for our development stuff. And you'll find that if you develop your software in such a way that you can run offline, then adding automated testing will be that much easier. And so what we have here is where, this is where we're logging things to the,

**译文**

正如我所说，这个练习简直再简单不过了。所以如果我们进入模拟部分，Resend，那么我们已经在解析邮件并模拟邮件了，因为我们在之前的开发工作中就必须完成这些。你会发现，如果你以能够离线运行的方式开发软件，那么添加自动化测试就会容易得多。所以我们现在这里，就是在这里将内容记录到……

## 88. 15. Reading Email from Disk in Test Environment

**原文**

So we've got the email on disk. Now we need to read that email. So we're going to add a little utility to require the email from disk. And then you're going to write or use that utility inside of the test to go and read that email. So this one's also pretty quick. There's not a lot to this one, but it is an important concept. So get to it. And when you're done, the test should pass.

**译文**

现在我们已经将邮件保存在磁盘上了。接下来我们需要读取这封邮件。因此，我们将添加一个小程序，用于从磁盘读取邮件。然后，你会在测试中编写或使用这个小程序来读取邮件。这部分内容也比较简单，涉及的东西不多，但它是一个重要的概念。开始动手吧。完成后，测试应该能够通过。

## 89. 16. Communicating Between Processes with File System in Node.js

**原文**

So first let's make the utility. We're going to go to our resend mock again and we're going to export a function called require email. It's going to take an email address. So yeah, email address that works. We'll call it a string. And then, oh, it looks like I called it recipient. We'll use that instead. And then we just need to grab that file from the file system in the same place. So here's our path join, the email to over here. So that's going to be our recipient.

**译文**

那么首先我们来创建这个工具函数。我们再次进入 resend mock，然后导出一个名为 require email 的函数。它将接收一个电子邮件地址。没错，就是一个有效的电子邮件地址。我们将其定义为字符串类型。然后，哦，看起来我之前把它命名为 recipient 了。我们就用这个名字吧。接着，我们只需要从文件系统中相同位置获取那个文件。这里就是我们的 path join，把电子邮件地址放在这里。这样，它就将成为我们的 recipient。

## 90. 17. Dad Joke Break E2E Mocking

**原文**

My friend keeps telling me, cheer up, you aren't stuck in a deep hole in the ground filled with water. I know he means well. When I read that first, it took me a second to figure out what that was saying, but it's funny. There you go, those puns there. Yeah, that's the core of the dad joke is a pun that like takes you a second to figure out. So there you go. That is that exercise. I think that was a lot of fun. So now it's a good time to take a break and just stand up and stretch

**译文**

我朋友总是跟我说：“振作点，你又没被困在一个灌满水的深坑里。”我知道他是一片好意。我第一次读到这句话时，还花了一小会儿才明白它到底在说什么，不过确实挺有趣的。喏，就是这种双关语。没错，老爸式笑话的核心就是一个需要你反应一下才能get到的双关梗。所以就是这样。这就是那个练习。我觉得那真的很有趣。那么现在正是休息一下、站起来伸展一下的好时机。

## 91. 18. Intro to Auth E2E

**原文**

So now we want to do the authenticated end-to-end test. This is actually easier than it used to be. So most of our apps, when you've got a login, a lot of the logic that really matters is, requires a logged in user. And so what your job is, is to make the browser that Playwright is running have the same sort of setup that an authenticated user would have. So in our application, we have cookies.

**译文**

现在，我们想执行经过身份验证的端到端测试。实际上，这比以前更容易了。对于大多数应用程序来说，当您拥有登录功能时，真正重要的逻辑通常需要用户已登录。因此，您的任务是让 Playwright 运行的浏览器具备与已验证用户相同的设置。在我们的应用程序中，我们使用 Cookie。

## 92. 19. End-to-End User Flow Testing and Authentication Utility

**原文**

So for this test, we're going to be doing a whole user flow. And this is actually a pretty typical end to end test. My end to end tests are typically pretty long. And it just follows the typical happy path for a user flow. Sometimes it'll do some sad path stuff, but most of the time we're doing happy path stuff and end to end test. OK, so here's the manual tester instructions. We're going to say log in with a user. We'll just use Kodi. Kodi loves you. And then we're going to go to that user, edit their

**译文**

那么在这个测试中，我们将执行一个完整的用户流程。这其实是一个非常典型的端到端测试。我的端到端测试通常都很长，它只是遵循用户流程中典型的“快乐路径”（happy path）。有时也会涉及一些“悲伤路径”（sad path）的情况，但大多数时候，端到端测试都是处理“快乐路径”的内容。好的，以下是手动测试人员的操作说明：我们将使用一个用户登录，就用 Kodi 吧，Kodi 很爱你。然后我们会进入该用户页面，编辑他们的……

## 93. 20. Login and Setting Cookies for Browser Testing

**原文**

So whatever you're doing, you just need to make sure that you're simulating in your test what it takes to be logged in. We already have a test for logging in as an existing user and onboarding with the link. So running those tests again before we run all the other tests that need to be authenticated would be an enormous waste of time. And so what we're going to do is have a utility that gets us logged in. So let's go to our 2FA test right here.

**译文**

所以，无论你正在做什么，只需确保在测试中模拟出登录所需的操作即可。我们已经有一个测试，用于以现有用户身份登录并通过链接完成引导流程。因此，在运行所有需要身份验证的其他测试之前，再次运行这些测试将极大地浪费时间。所以，我们要创建一个实用工具来实现登录。现在，让我们转到这里的 2FA 测试。

## 94. 21. Dad Joke Break Auth E2E

**原文**

Hold on, I have something in my shoe. I'm pretty sure that's a foot. That was pretty good. All right, so I know that one was actually pretty quick. Kind of, that may have been the only one step exercise that we've got. I think maybe had another one in this series of workshops, but it's actually, it's easier than it used to be. That used to be a lot harder to do. And depending on the setup that you've got, you may require a couple more steps, depending on

**译文**

等等，我鞋里有东西。我很确定那是一只脚。刚才那个做得还不错。好吧，我知道刚才那个其实挺快的。某种程度上，这可能是我们唯一的单步练习了。我想这个系列工作坊里可能还有另一个，但实际上，现在做起来比以前容易多了。以前要难很多。而且根据你现有的设置，你可能还需要多几步，具体取决于……

## 95. 22. Intro to Unit Test

**原文**

All right, we're gonna start unit testing. Woo, we're going from the top of the trophy to like the bottom part of the trophy. So the very bottom of the trophy is the static testing like ESLint, prettier and TypeScript. But right above that, this little section, unit testing. Unit testing is typically you use this for very dedicated functions that have like highly complex logic. You typically are gonna cover like your button components and stuff like that by just testing

**译文**

好的，我们现在要开始单元测试了。太棒了，我们要从奖杯的顶部一直做到底部。奖杯的最底层是静态测试，比如 ESLint、prettier 和 TypeScript。但就在它上面，这一小块区域就是单元测试。单元测试通常用于那些逻辑非常复杂的独立函数。你通常会通过测试来覆盖像按钮组件之类的东西。

## 96. 23. Unit Testing a Function for Error Messages

**原文**

Here's the function that we want to test, getErrorMessage. It takes an unknown argument. If that's a string, it returns an error. If it's an object and it has a message and the message is a string, then it returns that message. Otherwise, it's going to log to the console. That's going to be a bit of a challenge for us later and it will return unknown error. So your task is to write a test for this. It's a perfect use case for a unit test because it's got a little bit of logic in there and it is a pure function. Well, it's sort of pure. Actually, it's a little impure.

**译文**

以下是我们想要测试的函数 `getErrorMessage`。它接受一个未知参数。如果该参数是字符串，则返回一个错误。如果该参数是一个对象，并且包含 `message` 属性且 `message` 是字符串，则返回该消息。否则，它会向控制台输出日志。这将在稍后成为我们的一个挑战，并且函数将返回“未知错误”。因此，你的任务是为此编写一个测试。这是一个非常适合编写单元测试的用例，因为它包含了一些逻辑，并且是一个纯函数——好吧，它其实算是某种纯函数，但实际上它有一点点不纯。

## 97. 24. Writing Unit Tests for Utility Functions

**原文**

So I'm going to create this file right next to it. I like to co-locate my lower level tests like this. So we're going to say miss.test.tsx or ts. There we go. But we have a lot of utilities in here. And so I'm going to differentiate this one just a little bit by adding another dot in here and we'll say error message. And actually, this is totally legit. I will pretty often have multiple files that test different aspects of a utilities file.

**译文**

所以我要在它的旁边创建这个文件。我喜欢像这样把底层测试放在一起。所以我们把它命名为 miss.test.tsx 或 ts。好了。不过这里面有很多工具函数。所以我打算通过再加一个点来稍微区分一下这个文件，然后命名为 error message。实际上，这样做是完全没问题的。我经常会有多个文件来测试工具函数文件的不同方面。

## 98. 25. Managing Test Output and Error Logging with Console Mocking

**原文**

This console error is giving me heartburn. So it's very important to me that we keep our terminal output as clean as possible. When I showed up at a company that will remain unnamed and I ran the test, the log output was just outrageous. There was an enormous amount of logs. And as I was developing tests, it was very, very difficult for me to identify where my errors were and what was causing the errors. And like all it was just a nightmare.

**译文**

这个控制台错误让我非常头疼。因此，保持终端输出尽可能干净对我来说至关重要。当我去一家不便透露名称的公司并运行测试时，日志输出简直令人发指。日志数量极其庞大。在我开发测试的过程中，我很难确定错误出现在哪里，以及是什么导致了这些错误。总之，那真是一场噩梦。

## 99. 26. Testing Console Error with Spies

**原文**

All right, so to get rid of the console error, that's actually pretty easy. We just say console.error equals this function. Boom. Console error, gone. But the problem is that console error, like getting called is actually kind of part of our contract, part of our API. We're just saying, if you pass something that we can't determine the error, we're going to console error for you. And we're not getting any valuable information out of just overriding console.error. In addition, if we have another test after this one that

**译文**

好的，要消除控制台错误其实很简单。我们只需将 `console.error` 设置为这个函数即可。搞定，控制台错误就消失了。但问题是，`console.error` 被调用其实是我们契约的一部分，也是我们 API 的一部分。我们的意思是：如果你传入了我们无法确定错误的信息，我们就会帮你调用 `console.error`。而仅仅覆盖 `console.error` 并不会给我们带来任何有价值的信息。此外，如果我们在这条测试之后还有另一条测试，那么

## 100. 27. Implementing Test Hooks for Error Restoration in Playwright

**原文**

You may recall that we had a problem before with Playwright when we do some cleanup at the end of the test. And that is if we have some sort of error, throw a new error, blah, now, once we get to this console error step, this doesn't end up restoring. And that's going to be a problem for us because then future tests will not have the assertion or the error restored back to its original implementation. So that's going to be a problem for us.

**译文**

你可能还记得，之前我们在测试结束时执行清理操作时，Playwright 曾出现过一个问题。那就是，如果我们遇到某种错误并抛出一个新错误等等，一旦进入这个控制台错误步骤，错误就无法恢复。这会给我们带来问题，因为后续的测试将无法把断言或错误恢复到其原始实现状态。因此，这将是一个问题。
