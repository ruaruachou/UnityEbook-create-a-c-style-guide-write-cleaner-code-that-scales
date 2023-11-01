# CREAT A C# STYLE GUIDE   
## Contnets
# Table of Contents
 [Introduction](#introduction)  
 
 [Chapter 1](#chapter-1)  
     <span style="font-size: smaller; margin-left: 2em;"><a href="#section-1-1">Section 1.1</a></span>  
     <span style="font-size: smaller; margin-left: 2em;"><a href="#section-1-2">Section 1.2</a></span>

---

## <span id="introduction">Introduction</span>

Creativity can be messy .  
创造力可能是混乱的。  

A flash of inspiration becomes a flurry of code, which then spawns a working 
prototype . Success! Congratulations on passing the first hurdle . However, 
simply getting your code to work won’t be enough . There’s much more to game 
development.  
一闪而过的灵感变成了一阵代码风暴，然后孕育出一个可用的原型。成功了！恭喜你通过了第一个难关。然而，仅仅让你的代码运行起来是不够的。游戏开发还有更多内容。  
  
Once your logic is functional, then the process of refactoring and cleaning up
begins.    
一旦你的逻辑功能正常，重构和清理的过程就开始了。  
  

This guide compiles advice from industry experts on how to create a code
style guide. Establishing ssuch a guide for each member of your team to follow
will help ensure your codebase can grow your project to a commercial-scale
production.  
本指南汇集了行业专家的建议，介绍了如何创建代码风格指南。为团队中的每个成员建立这样的指南，将有助于确保您的代码库能够将您的项目发展成商业规模的产品。  

These tips and tricks will help your development process in the long term, even
if they cost you extra effort up front. A cleaner, more scalable codebase also
facilitates the efficient onboarding of new developers as you expand your team.  
即使这些技巧在前期会花费你额外的精力，但它们将有助于你的长期开发过程。一个更干净、更可扩展的代码库也有助于在扩展团队时有效地吸引新开发人员。  
  
Keep your code clean to make life easier for yourself and everyone involved in
the project.  
保持你的代码整洁，让你自己和项目中的每个人的生活更轻松。  

### Contributors  
贡献者  

This guide was written by Wilmer Lin, a 3D and visual effects artist with over
15 years of industry experience in film and television, who now works as an
independent game developer and educator. Significant contributions were also
made by senior technical content marketing manager Thomas Krogh-Jacobsen
and senior Unity engineers Peter Andreasen, Scott Bilas, and Robert LaCruise.  
本指南由Wilmer Lin撰写，他是一名3D和视觉特效艺术家，在电影和电视行业拥有超过15年的行业经验，现在是一名独立的游戏开发者和教育工作者。高级技术内容营销经理Thomas Krogh-Jacobsen和高级Unity工程师Peter Andreasen、Scott Bilas和Robert LaCruise也做出了重大贡献。  

 ### What is clean code, anyway?  
Most game developers would agree that clean code is any code that’s easy to
read and maintain.  
大多数游戏开发者都会认为，干净的代码是任何易于阅读和维护的代码。  
  

Clean code is elegant, efficient, and readable.  
干净的代码是优雅的、高效的和可读的。  

There’s good reasons for this congruence. Something that might be obvious to
you as the original author might be less apparent to another developer. By the
same token, when you implement some logic now, you might not remember
what that same code snippet does three months later.  
这种一致性有很好的理由。对你作为原始作者来说可能是显而易见的，但对另一个开发者来说可能就不那么明显了。同样，当你现在实现一些逻辑时，你可能不会记得三个月后同样的代码片段是做什么的。 

Clean code aims to make development more scalable and conform to a set of  
production standards, including:  
干净的代码旨在使开发更具可扩展性，并符合一组生产标准，包括：  

— Follow consistent naming conventions  
遵循一致的命名约定  

— Format your code for legibility  
格式化你的代码以便阅读  

— Organize classes and methods to keep them small and readable  
组织类和方法，使它们小而易读  

— Comment on any code that isn’t self-explanatory  
对任何不是自我解释的代码进行评论  

Whether you’re building a puzzler for mobile or a massive MMORPG targeted
at consoles, keeping your codebase clean reduces the total cost of software
maintenance. You can then implement new features or patch your existing
software more easily.  
无论你是为移动设备构建一个解谜游戏，还是为主机构建一个大型MMORPG，保持你的代码库干净，都会降低软件维护的总成本。然后，你可以更容易地实现新功能或修补现有的软件。  

Your future teammates – and your future self – will be thankful for that.  
你未来的队友——和你未来的自己——会为此感激。       
---

## <span id="chapter-1">Chapter 1</span>
    
> ANY FOOL CAN WRITE CODE THAT A COMPUTER CAN UNDERSTAND. GOOD PROGRAMMERS WRITE CODE THAT HUMANS CAN UNDERSTAND.”  
– Martin Fowler, author of Refactoring  
任何傻瓜都可以写出计算机能理解的代码。好的程序员写出人类能理解的代码。——Martin Fowler，*Refactoring* 的作者  
  
No developer is an island. As the technical needs of your game application grow,
you’ll need help. Inevitably, you’ll add more team members with diverse skill
sets. Clean code introduces coding standards for your ever-expanding team so
everyone is on the same page. Now everybody can work on the same project
with a more uniform set of guidelines.  
没有开发者是孤岛。随着你的游戏应用程序的技术需求的增长，你将需要帮助。不可避免的是，你将增加更多具有不同技能的团队成员。干净的代码为你不断扩大的团队引入了编码标准，这样每个人都在同一个页面上。现在，每个人都可以在同一个项目上使用更统一的指南。  

Before looking into how to create the style guide, let’s go over some general
rules to help you scale up your Unity development.   
在研究如何创建样式指南之前，让我们先看一些通用规则，以帮助你扩展你的Unity开发。  

### KISS (keep it simple, stupid)  KISS原则（保持简单，愚蠢）

Let’s face it: Engineers and developers can overcomplicate things, even though
computing and programming are hard enough. Use the KISS principle of “keep
it simple, stupid” as a guide for finding the simplest solution to the problem
at hand.  
让我们面对现实吧：工程师和开发人员可能会过于复杂化事情，即使计算和编程已经够难了。使用“保持简单，愚蠢”的KISS原则作为指南，找到手头问题的最简单解决方案。  

There’s no need to reinvent the wheel if a proven and simple technique solves
your challenge. Why use a fancy new technology just for the sake of using it?
Unity already includes numerous solutions in its Scripting API. For example, if
the existing [Hexagonal Tilemap](https://docs.unity3d.com/Manual/Tilemap-Hexagonal) works for your strategy game, skip writing your
own. The best code you can write is no code at all.   
如果一个经过验证的简单技术可以解决你的挑战，就没有必要重新发明轮子。为什么要为了使用而使用一个新的花哨的技术呢？Unity已经在其脚本API中包含了许多解决方案。例如，如果现有的[六角形Tilemap](https://docs.unity3d.com/Manual/Tilemap-Hexagonal)适用于你的策略游戏，请跳过编写你自己的代码。你可以写的最好的代码就是没有代码。  

>#### The KISS principle KISS原则  
>  
>The well-known KISS principle emphasizes simplicity in design, an idea that’s
been popular throughout different times, as these quotes attest:  
众所周知的KISS原则强调设计的简单性，这是一个在不同时代都很流行的想法，正如下面的引用所证明的那样：  
>
>“Simplicity is the ultimate sophistication.”
>– Leonardo da Vinci  
>“简单是终极的复杂。”  ——— Leonardo da Vinci  
>
>“Make simple tasks simple!”
– Bjarne Stroustrup  
“让简单的任务变得简单！”  ——— Bjarne Stroustrup  
>
>“Simplicity is a prerequisite for reliability.”
>– Edsger W. Dijkstra  
“简单是可靠的先决条件。”  ——— Edsger W. Dijkstra  
>
>“Everything should be made as simple as possible, but no simpler.”
– Albert Einstein  
“一切都应该尽可能简单，但不要太简单。”  ——— Albert Einstein  
>
>In programming, that means keeping your code as streamlined as possible.
>Avoid adding unnecessary complexity  
在编程中，这意味着尽可能简化你的代码。避免增加不必要的复杂性。  
>
>#### The YAGNI principle YAGNI原则  
>
>The related YAGNI principle (“you aren’t gonna need it”) instructs you to
implement features only as you need them. Don’t worry about features that you
might need once the stars align. Build the simplest thing that you need now and
build it to work.  
相关的YAGNI原则（“你不会需要它”）指示你只在需要时实现功能。不要担心你可能需要的功能，一旦星星排>成一条线。构建你现在需要的最简单的东西，并使其工作。  

### Don’t code around the problem  不要绕过问题编码  

The first step of software development is to understand what you are trying to
solve. This idea might seem like common sense, but too often developers get
bogged down in implementing code without understanding the actual problem,
or they'll modify the code until it works without fully grasping why.  
软件开发的第一步是了解你要解决的问题。这个想法可能看起来像是常识，但是开发人员经常陷入实现代码而不了解实际问题的泥潭，或者他们会修改代码，直到它工作，而不完全掌握为什么。  

What if, for example, you fixed a Null Reference Exception with a quick if-null
statement at the top of a method. Are you sure that was the real culprit, or was
the problem a call to another method deeper inside?  
例如，如果你在一个方法的顶部用一个快速的if-null语句修复了一个空引用异常。你确定这是真正的罪魁祸首吗，还是问题出在了内部更深的另一个方法的调用上？  

Instead of adding code to fix a problem, investigate the root cause. [Ask yourself
why](https://en.wikipedia.org/wiki/Five_whys) it’s happening rather than applying a band-aid solution.  
不要添加代码来解决问题，而是调查根本原因。问问自己[为什么](https://en.wikipedia.org/wiki/Five_whys)会发生这种情况，而不是应用一个临时解决方案。  
  

### Improve incrementally, every day  每天逐步改进  

Making clean code is a fluid and ongoing process. Get the whole team into this
mindset. Expect code cleanup to be part of your day-to-day life as a developer.
Most people don’t intend to write broken code. It just evolves that way over
time. Your codebase needs constant maintenance and upkeep. Budget time for
that and make sure it happens.  
制作干净的代码是一个流动的、持续的过程。让整个团队进入这种心态。期望代码清理成为你作为开发人员日常生活的一部分。大多数人并不打算写破损的代码。随着时间的推移，它就会这样发展。你的代码库需要不断的维护和保养。为此预算时间，并确保它发生。  

### Make it good, not perfect 做好，但不苛求完美  

On the flip side, don’t strive for perfection. When your code meets production
standards, it’s time to commit it and move on.  
另一方面，不要追求完美。当你的代码符合生产标准时，就是时候提交它并继续前进了。  

Ultimately your code needs to do something. Balance implementing new
functionality with code cleanup. Don’t refactor for the sake of it. Refactor when
you think it will provide a benefit to you or somebody else.  
最终你的代码需要做一些事情。平衡实现新功能和代码清理。不要为了重构而重构。当你认为它会给你或其他人带来好处时，再重构。  

### Plan, but adapt 计划，但适应  

In The Pragmatic Programmer, Andy Hunt and Dave Thomas write, “Rather than
construction, programming is more like gardening.” Software engineering is an
organic process. Be prepared if everything does not go according to plan.  
在《务实的程序员》中，Andy Hunt和Dave Thomas写道：“与其说是建筑，不如说是园艺。”软件工程是一个有机的过程。如果一切不按计划进行，请做好准备。  

Even if you make the most elaborate drawing, designing a garden on paper will
not guarantee results. Your plants may bloom differently than you expected.
You’ll need to prune, transplant, and replace parts of your code to make this
garden successful.  
即使你做出最精心的图纸，设计一座花园也不能保证结果。你的植物可能会开出你意想不到的花。你需要修剪、移植和替换你的代码的一部分，使这个花园成功。  

Software design isn’t quite like an architect drawing blueprints because it's more
malleable and less mechanical. You’ll need to react as your codebase grows.  
软件设计不像建筑师绘制蓝图，因为它更加可塑，不那么机械。你需要随着你的代码库的增长而做出反应。

### Be consistent 保持一致  

Once you decide how to tackle a problem, approach similar things the same
way. It’s not difficult but will take constant effort. Apply this principle to
everything from naming (classes and methods, casing, etc.) to organizing
project folders and resources.  
一旦你决定如何解决一个问题，以相同的方式处理类似的事情。这并不困难，但需要不断的努力。将这个原则应用于从命名（类和方法、大小写等）到组织项目文件夹和资源的所有内容。  

Above all, have your team agree on a style guide and then follow it.  
最重要的是，让你的团队同意一个样式指南，然后遵循它。  

### It takes a village 一个村庄  

Although keeping code clean and simple is in everyone’s best interest, “clean
and simple” is not the same as “easy.” Clean and simple takes effort and is hard
work for beginners and experienced developers alike.  
尽管保持代码的整洁和简单符合每个人的最大利益，但“整洁和简单”并不等于“简单”。对于初学者和有经验的开发人员来说，整洁和简单需要努力和艰苦的工作。  

Your project will become messy if left unchecked. It’s a natural consequence of
so many people working on different parts of a project. Everyone is responsible
for pitching in and preventing code clutter, and each team member will need to
read and follow the style guide. Cleanup is a group effort.  
如果不加控制，你的项目将变得混乱。这是许多人在项目的不同部分工作的自然结果。每个人都有责任投入并防止代码混乱，每个团队成员都需要阅读并遵循样式指南。清理是一个集体的努力。  

>### A style guide for you and your team 你和你的团队的样式指南  
>
>This guide focuses on the most common coding conventions you’ll encounter
during Unity development. These are a subset of the [Microsoft Framework
Design Guidelines](https://learn.microsoft.com/en-us/dotnet/standard/design-guidelines/), which include an extensive number of rules beyond what is
presented here.  
本指南重点介绍了Unity开发过程中遇到的最常见的编码约定。这些是[Microsoft Framework Design Guidelines](https://learn.microsoft.com/en-us/dotnet/standard/design-guidelines/)的一个子集，其中包括大量的规则，超出了本文介绍的范围。   
>
>These guidelines are recommendations, not hard and fast rules. Customize
them according to your team’s preferences. Pick a style that suits everyone,
and ensure they apply it.  
这些准则是建议，而不是硬性规定。根据你的团队的喜好来定制它们。选择一种适合每个人的风格，并确保他们应用它。  
>
>Consistency is king. If you follow these suggestions and need to modify your
style guide in the future, a few find-and-replace operations can migrate your
codebase quickly.  
一致性是王道。如果你遵循这些建议，并且需要在将来修改你的样式指南，一些查找和替换操作可以快速迁移你的代码库。  
>
>When your style guide conflicts with this document or the Microsoft Framework
Design Guidelines, it should take precedence over them because this will allow
your team to maintain a uniform style throughout your project.  
当你的样式指南与本文档或Microsoft Framework Design Guidelines冲突时，它应该优先于它们，因为这将允许你的团队在整个项目中保持统一的风格。  
>  

## CREATE A C# STYLE GUIDE  创建一个C#样式指南  
"THERE ARE ONLY TWO HARD THINGS IN COMPUTER SCIENCE: CACHE INVALIDATION & NAMING THINGS.”– Phil Karlton, software engineer  
“计算机科学中只有两件难事：缓存失效和命名事物。”——Phil Karlton，软件工程师  

Your application is the collective product of individuals who might think
differently from one another. A style guide helps rein in those differences to
create a cohesive final product. No matter how many contributors work on a
Unity project, it should feel like it’s been developed by a single author.  
你的应用程序是个体的集体产品，他们可能彼此思维不同。样式指南有助于控制这些差异，创造一个有凝聚力的最终产品。无论有多少贡献者在Unity项目上工作，它都应该感觉像是由一个作者开发的。  

Microsoft and Google both offer comprehensive example guides:  
Microsoft和Google都提供了全面的示例指南：  

— [Microsoft C# Coding Conventions Microsoft C#编码约定](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions)  

— [C# at Google Style Guide Google样式指南](https://google.github.io/styleguide/csharp-style.html)  

These are excellent starting points for managing your Unity development. Each
guide offers solutions for naming, formatting, and commenting. If you’re a solo
developer, this might feel like a constraint at first, but following a style guide is
essential when working in teams.  
这些都是管理你的Unity开发的绝佳起点。每个指南都提供了命名、格式化和注释的解决方案。如果你是一个独立的开发者，这可能会一开始就感觉像是一个限制，但是在团队中工作时遵循一个样式指南是必不可少的。  

Think of a style guide as an initial investment that will pay dividends later.
Maintaining a single set of standards can reduce the time spent on relearning if
you move anyone onto another project.  
把样式指南看作是一项最初的投资，它将在以后产生回报。维护一套标准可以减少在将任何人移动到另一个项目时重新学习的时间。  

Style guides take the guesswork out of coding conventions and formatting.  
样式指南消除了编码约定和格式化的猜测。  

Consistent style then becomes a matter of following directions.  
一致的风格就成了遵循指示的问题。  

We created an [example](https://github.com/thomasjacobsen-unity/Unity-Code-Style-Guide) C# style sheet that you can also use as a reference as
you assemble your own guide. Feel free to copy and tweak it as needed.  
我们创建了一个[示例](https://github.com/thomasjacobsen-unity/Unity-Code-Style-Guide)C#样式表，你也可以在组装你自己的指南时使用它作为参考。随时根据需要复制和调整它。  

Let’s dive in.  
让我们深入研究一下。  

### Naming conventions 命名约定  

There’s a deep psychology involved in giving something a name. A name tells us
how that entity fits into the world. What is it? Who is it? What can it do for us?  
给某物命名涉及到深层的心理学。一个名字告诉我们这个实体如何适应这个世界。它是什么？它是谁？它能为我们做什么？  

The names of your variables, classes, and methods aren’t mere labels. They
carry weight and meaning. Good naming style impacts how someone reading
your program can comprehend the idea you’re trying to convey.  
你的变量、类和方法的名称不仅仅是标签。它们承载着重量和意义。良好的命名风格影响着阅读你的程序的人如何理解你试图传达的思想。  

Here are some guidelines to follow for naming.  
以下是一些命名的指导原则。  

### Identifier names 标识符名称  

An [identifier](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/language-specification/lexical-structure#identifiers) is any name you assign to a type (class, interface, struct, delegate,
or enum), member, variable, or namespace. Identifiers must begin with a letter
or an underscore (_).  
[标识符](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/language-specification/lexical-structure#identifiers)是你分配给类型（类、接口、结构、委托或枚举）、成员、变量或命名空间的任何名称。标识符必须以字母或下划线（_）开头。  

Avoid special characters (backslashes, symbols, Unicode characters) in your
identifiers, even though C# permits them. These can interfere with certain Unity
command-line tools. Steer clear of unusual characters to ensure compatibility
with most platforms.  
避免在你的标识符中使用特殊字符（反斜杠、符号、Unicode字符），即使C#允许它们。这些可能会干扰某些Unity命令行工具。避免使用不寻常的字符，以确保与大多数平台的兼容性。
  
>### Casing terminology 大小写术语  
>
>You can’t define variables with spaces in the name because C# uses the space
character to separate identifiers. Casing schemes can alleviate the problem of
using compound names or phrases in source code. There are several wellknown
naming and casing conventions.  
你不能用空格来定义变量的名称，因为C#使用空格字符来分隔标识符。大小写方案可以缓解在源代码中使用复合名称或短语的问题。有几种众所周知的命名和大小写约定。  
>
>#### Camel case 骆驼命名法  
>
>Also known as camel caps, camel case is the practice of writing phrases
without spaces or punctuation, separating words with a single capitalized
letter. The very first letter is lowercase. Local variables and method parameters
are camel case.  
也称为骆驼大写，骆驼命名法是一种不使用空格或标点符号的短语写法，用一个大写字母分隔单词。第一个字母是小写的。局部变量和方法参数是骆驼命名法。  
>
>For example:  
&emsp;examplePlayerController  
&emsp;maxHealthPoints  
&emsp;endOfFile  
>
>#### Pascal case 帕斯卡命名法  
>
>Pascal case is a variation of camel case, where the initial letter is capitalized.
Use this for class and method names in Unity development. Public fields can
be pascal case as well. For example:  
帕斯卡命名法是骆驼命名法的一种变体，其中初始字母是大写的。在Unity开发中使用这个类和方法名。公共字段也可以是帕斯卡命名法。例如：  
>
>&emsp;ExamplePlayerController  
>&emsp;MaxHealthPoints  
>&emsp;EndOfFile  
>
>#### Snake case 蛇命名法  
>
>In this case, spaces between words are replaced with an underscore character.
For example:  
在这种情况下，单词之间的空格被下划线字符替换。例如：  
>
>&emsp;example_player_controller  
&emsp;max_health_points  
&emsp;end_of_file  
>
>#### Kebab case 烤肉串命名法  
>
>Here, spaces between words are replaced with dashes. The words appear on a
“skewer” of dash characters. For example:  
在这里，单词之间的空格被破折号替换。这些单词出现在一个破折号字符的“串”上。例如：  
>
>&emsp;example-player-controller  
&emsp;Max-health-points  
&emsp;end-of-file  
&emsp;naming-conventions-methodology  
>
>The problem with kebab case is that many programming languages use the
dash as a minus sign. Some languages interpret numbers separated by dashes
as calendar dates.  
烤肉串命名法的问题在于，许多编程语言使用破折号作为减号。一些语言将用破折号分隔的数字解释为日历日期。  
>
>#### Hungarian notation 匈牙利命名法  
>
>The variable or function name often indicates its intention or type. For example:  
变量或函数名通常表示其意图或类型。例如：  
>
>&emsp;int iCounter  
&emsp;string strPlayerName  
>
>Hungarian notation is an older convention and is not common in Unity
development.  
匈牙利命名法是一个较旧的约定，在Unity开发中并不常见。  

### Fields and variables 字段和变量  

Consider these rules for your variables and [fields](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/fields):  
考虑一下你的变量和[字段](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/fields)的规则:  
— Use nouns for variable names: Variable names must be descriptive, clear,
and unambiguous because they represent a thing or state. So use a noun
when naming them except when the variable is of the type bool (see
below).  
用名词来命名变量:变量名必须是描述性的、清晰的和不含糊的，因为它们代表了一个事物或状态。所以在命名它们时使用名词，除非变量是bool类型(见下文)。  

— Prefix Booleans with a verb: These variables indicate a true or false value.
Often they are the answer to a question, such as – is the player running?
Is the game over? Prefix them with a verb to make their meaning more
apparent. Often this is paired with a description or condition, e.g.,
isDead, isWalking, hasDamageMultiplier, etc.  
用动词前缀布尔值:这些变量表示一个真或假的值。通常它们是一个问题的答案，比如——玩家在跑步吗？游戏结束了吗？用一个动词前缀来使它们的意义更明显。通常这与描述或条件配对，例如，isDead，isWalking，hasDamageMultiplier等。  

— Use meaningful names. Don’t abbreviate (unless it’s math): Your variable
names will reveal their intent. Choose names that are easy to pronounce
and search for.  
使用有意义的名字。不要缩写(除非是数学):你的变量名将揭示它们的意图。选择易于发音和搜索的名称。  

— Single letter variables are fine for loops and math expressions, but
otherwise, don’t abbreviate. Clarity is more important than any time saved
from omitting a few vowels.  
单字母变量对于循环和数学表达式来说是可以的，但是除此之外，不要缩写。清晰比省略几个元音节节省的时间更重要。  

— When doing quick prototyping, you can use short “junk” names and then
refactor to meaningful names later.  
在快速原型开发时，你可以使用短的“垃圾”名称，然后再重构为有意义的名称。  

|  Examples to avoid 错误示范   |  Use instead 正确示范 |  Notes 注意 |
|  ----  | ----  | ----
| int d  | intelapsedTimeInDays | Avoid single letter abbreviations unless a counter or expression. <br>避免使用单个字母的缩写，除非用于计数器或表达式。|
| int hp,  <br>string tName,<br>int mvmtSpeed  | int healthPoints,<br>string teamName,<br>int movementSpeed | Variable names reveal intent. Make names searchable and pronounceable. <br>变量名揭示意图。使名称易于搜索和发音。 |
| int getMovemementSpeed  | int movementSpeed | Use nouns. Reserve verbs for methods unless it’s a bool (below). <br>使用名词。除非是布尔类型（见下文），否则将动词保留给方法。 |
| bool dead  | bool isDead <br>bool isPlayerDead | Booleans ask a question that can be answered true or false. <br>bool会问一个可以用是或否回答的问题|  
  

— **Use pascal case for public fields. Use camel case for private variables:**
For an alternative to public fields, use Properties with a public getter (see
Formatting below).  
**对公共字段使用帕斯卡命名法。对私有变量使用骆驼命名法:** 用公共getter的属性作为公共字段的替代方法(见下文的格式化)。  

— **Avoid too many prefixes or special encoding: **You can prefix private
member variables with an underscore (_) to differentiate them from local
variables.   
**避免过多的前缀或特殊编码:** 你可以用下划线(_)作为前缀来区分私有成员变量和局部变量。  

Alternatively, use the this keyword to distinguish between member and
local variables in context and skip the prefix. Public fields and properties
generally don’t have prefixes.  
或者，使用this关键字来区分上下文中的成员和局部变量，并跳过前缀。公共字段和属性通常没有前缀。  

Some style guides use prefixes for private member variables (m_),
constants (k_), or static variables (s_), so the name can reveal more about
the variable at a glance.  
一些样式指南使用前缀来表示私有成员变量(m_)、常量(k_)或静态变量(s_)，因此名称可以一目了然地揭示变量的更多信息。  

Many developers eschew these and rely on the editor instead. However,
not all IDEs support highlighting and color coding, and some tools can’t
show rich context at all. Consider this when deciding how (or if) you will
apply prefixes together as a team.  
许多开发人员避免使用这些，而是依赖于编辑器。然而，并不是所有的IDE都支持高亮和颜色编码，有些工具根本不能显示丰富的上下文。在决定如何（或是否）将前缀作为一个团队一起应用时，请考虑这一点。  

— **Specify (or omit) access level modifiers consistently:** If you leave off the
access modifier, the compiler will assume the access level to be private.
This works well, but be consistent in how you omit the default access
modifier. Remember that you’ll need to use protected if you want this in a
subclass later.  
**一致地指定(或省略)访问级别修饰符:** 如果你省略了访问修饰符，编译器将假定访问级别为private。这很好用，但是在省略默认访问修饰符的方式上要保持一致。记住，如果你想在后面的子类中使用这个，你需要使用protected。  

>### Example code snippets 示例代码片段  
>
>The code snippets in this guide are non-functional and abbreviated. They’re
presented here to show style and formatting.  
本指南中的代码片段是非功能性的和缩写的。它们在这里被呈现出来以显示样式和格式。  
>
>You can also reference this example C# style sheet for Unity developers,
based on a modified version of Microsoft’s Framework Design Guidelines. This
represents just one example of how you can set up your team’s style guide.  
你也可以参考这个基于微软框架设计指南修改版本的Unity开发人员的C#样式表示例。这只是一个例子，说明你如何设置你的团队的样式指南。  
>
>Note the specific style rules found in these code examples:  
注意这些代码示例中的具体样式规则:  
>
>— The default private access modifier is not omitted.  
默认的私有访问修饰符没有被省略。  
>
>— Public member variables use pascal case.  
公共成员变量使用帕斯卡命名法。  
>
>— Private member variables are camel case and use underscores (_) as a
prefix.  
私有成员变量是骆驼命名法，并使用下划线(_)作为前缀。  
>
>— Local variables and parameters use camel case with no prefix.   
局部变量和参数使用骆驼命名法，没有前缀。  
>
>— Public and private member variables are grouped together.   
公共和私有成员变量被分组在一起。  
>
>Review each rule in the example style guide and customize it to your team’s
preferences. The specifics of an individual rule are less important than having
everyone agree to follow it consistently. When in doubt, rely on your team’s own
guide to settle any style disagreements.  
审查每个规则在示例样式指南，并根据你的团队的偏好进行自定义。一个单独规则的具体内容比起每个人都同意一致地遵循它来说并不重要。当你怀疑的时候，依靠你的团队自己的指南来解决任何风格上的分歧。  
  
  ```csharp
// EXAMPLE: public and private variables
public float DamageMultiplier = 1.5f;
public float MaxHealth;
public bool IsInvincible;

private bool _isDead;
private float _currentHealth;

// parameters
public void InflictDamage(float damage, bool isSpecialDamage)
{
    // local variable
     int totalDamage = damage;
    // local variable versus public member variable
    if (isSpecialDamage)
    {
      totalDamage *= DamageMultiplier;
    }
    // local variable versus private member variable
    if (totalDamage > _currentHealth)
    {
      /// ...
    }
}
```  
— Use one variable declaration per line: It’s less compact, but enhances
readability.  
每行使用一个变量声明:它不够紧凑，但增强了可读性。  

— Avoid redundant names: If your class is called Player, you don’t need
to create member variables called PlayerScore or PlayerTarget. Trim
them down to Score or Target.  
避免冗余的名称:如果你的类被称为Player，你不需要创建名为PlayerScore或PlayerTarget的成员变量。把它们缩减到Score或Target。  

— Avoid jokes or puns: While they might elicit a chuckle now, the
infiniteMonkeys or dudeWheresMyChar variables won’t hold up after a
few dozen reads.  
避免开玩笑或双关语:虽然它们现在可能会引起一阵笑声，但是在读了几十次之后，无限的猴子或者是我的角色在哪里的变量就不会坚持下去了。  

— Use the var keyword for implicitly typed local variables if it helps
readability and the type is obvious: Specify when to use var in your
style guide. For example, many developers avoid var when it obscures the
variable’s type or with primitive types outside a loop.  
如果它有助于可读性并且类型是显而易见的，使用var关键字来隐式地声明局部变量:在你的样式指南中指定何时使用var。例如，许多开发人员在它模糊了变量的类型或在循环外使用原始类型时避免使用var。  

Generally, use var when it makes the code easier to read (e.g., with long
type names) and the type is not ambiguous.  
通常，当它使代码更容易阅读(例如，使用长类型名称)并且类型不是模糊的时候，使用var。  

```csharp
// EXAMPLE: good use of var
var powerUps = new List<PowerUps>();
var dictionary = new Dictionary<string, List<GameObject>>();
// AVOID: potential ambiguity
var powerUps = PowerUpManager.GetPowerUps();
```  

#### Enums 枚举
Enums are special value types defined by a set of named constants. By default,
the constants are integers, counting up from 0.  
枚举是由一组命名常量定义的特殊值类型。默认情况下，常量是整数，从0开始计数。  

Use pascal case for enum names and values. You can place public enums
outside of a class to make them global. Use a singular noun for the enum name.  
对枚举名称和值使用帕斯卡命名法。你可以将公共枚举放在类外面，使它们成为全局的。对枚举名称使用单数名词。  

>Note: Bitwise enums marked with the [System.FlagsAttribute attribute](https://learn.microsoft.com/en-us/dotnet/api/system.flagsattribute?view=net-5.0) are the
exception to this rule. You typically pluralize these as they represent more than
one type.  
注意:用[System.FlagsAttribute](https://learn.microsoft.com/en-us/dotnet/api/system.flagsattribute?view=net-5.0)属性标记的位枚举是这个规则的例外。你通常把它们变成复数，因为它们代表的不止一种类型。  

```csharp
// EXAMPLE: enums use singular nouns
public enum WeaponType
{
    Knife,
    Gun,
    RocketLauncher,
    BFG
}

public enum FireMode
{
    None = 0,
    Single = 5,
    Burst = 7,
    Auto = 8,
}

// EXAMPLE: but a bitwise enum is plural
[Flags]
public enum AttackModes
{
    // Decimal // Binary
    None = 0, // 000000
    Melee = 1, // 000001
    Ranged = 2, // 000010
    Special = 4, // 000100
    // It seems like the code snippet is incomplete for MeleeAn
}

```  
#### Classes and interfaces 类和接口  

Follow these standard rules when naming your classes and interfaces:  
在命名类和接口时，请遵循这些标准规则:  

— **Use pascal case nouns for class names.**   
**对类名使用帕斯卡命名法。**  

— **If you have a Monobehaviour in a file, the source file name must
match:** You may have other internal classes in the file, but only one
Monobehaviour should exist per file.  
**如果你在一个文件中有一个Monobehaviour，源文件名必须匹配:** 你可能在文件中有其他内部类，但是每个文件中只能有一个Monobehaviour。  

— **Prefix interface names with a capital I:** Follow this with an adjective that
describes the functionality.  
**用大写的I前缀接口名称:** 用一个描述功能的形容词来跟随它。  
```csharp
// EXAMPLE: Class formatting
public class ExampleClass : MonoBehaviour
{
    public int PublicField;
    public static int MyStaticField;

    private int _packagePrivate;
    private int _myPrivate;

    private static int _myPrivate;

    protected int _myProtected;

    public void DoSomething()
    {

    }
}

// EXAMPLE: Interfaces
public interface IKillable
{
    void Kill();
}

public interface IDamageable<T>
{
    void Damage(T damageTaken);
}

```  

#### Methods 方法  

In C#, every executed instruction is performed in the context of a method.  
在C#中，每个执行的指令都是在方法的上下文中执行的。  

>**Note**: “function” and “method” are often used interchangeably in Unity
development. However, because you can’t write a function without incorporating
it into a class in C#, “method” is the accepted term.  
注意:在Unity开发中，“function”和“method”经常可以互换使用。然而，因为你不能在C#中写一个不包含在类中的函数，“method”是被接受的术语。

Methods perform actions, so apply these rules to name them accordingly:  
方法执行操作，所以根据这些规则来命名它们:  

— **Start the name with a verb:** Add context if necessary. e.g.,
GetDirection, FindTarget, etc.  
**用动词开头:** 如果需要，添加上下文。例如，GetDirection，FindTarget等。  

— **Use camel case for parameters:** Format parameters passed into the
method like local variables.  
**对参数使用骆驼命名法:** 对传递到方法中的参数进行格式化，就像对局部变量进行格式化一样。  

— **Methods returning bool should ask questions:** Much like Boolean
variables themselves, prefix methods with a verb if they return a true-false
condition This phrases them in the form of a question, e.g., IsGameOver,
HasStartedTurn.  
**返回bool的方法应该提出问题:** 就像布尔变量本身一样，如果方法返回一个真假条件，就用一个动词作为前缀。这样就可以用一个问题来表达它们，例如，IsGameOver，HasStartedTurn。  

```csharp
// EXAMPLE: Methods start with a verb
public void SetInitialPosition(float x, float y, float z)
{
transform.position = new Vector3(x, y, z);
}
// EXAMPLE: Methods ask a question when they return bool
public bool IsNewPosition(Vector3 currentPosition)
{
return (transform.position == newPosition);
}
```
  
#### Events and event handlers 事件和事件处理程序

Events in C# implement the Observer pattern. This software design pattern
defines a relationship in which one object, the subject (or publisher), can notify
a list of dependent objects called observers (or subscribers). Thus, the subject
can broadcast state changes to its observers without tightly coupling the
objects involved.  
C#中的事件实现了观察者模式。这种软件设计模式定义了一种关系，其中一个对象，主题(或发布者)，可以通知一组称为观察者(或订阅者)的依赖对象。因此，主题可以向它的观察者广播状态变化，而不会紧密地耦合涉及的对象。  

Several naming schemes exist for events and their related methods in the
subject and observers. Try these practices:  ]
存在许多命名方案来命名主题和观察者中的事件及其相关方法。试试这些做法:  

— **Name the event with a verb phrase:*** Choose a name that communicates
the state change accurately. Use the present or past participle to indicate
events “before” or “after.” For example, specify “OpeningDoor” for an event
before opening a door or “DoorOpened” for an event afterward.  
**用动词短语命名事件:** 选择一个准确地传达状态变化的名称。使用现在时或过去分词来表示“之前”或“之后”的事件。例如，为打开门之前的事件指定“OpeningDoor”，为打开门之后的事件指定“DoorOpened”。  

— **Use the System.Action delegate for events:** In most cases, the [Action&lt;T>](https://docs.microsoft.com/en-us/dotnet/api/system.action-1?view=net-5.0)
delegate can handle the events needed for gameplay. You may pass
anywhere from 0 to 16 input parameters of different types with a return
type of void. Using the predefined delegate saves code.  
**对事件使用System.Action委托:** 在大多数情况下，[Action&lt;T>](https://learn.microsoft.com/en-us/dotnet/api/system.action-1?view=net-5.0)委托可以处理游戏过程中需要的事件。你可以传递0到16个不同类型的输入参数，返回类型为void。使用预定义的委托可以节省代码。  

>**Note**: You can also use the [EventHandler](https://learn.microsoft.com/en-us/dotnet/api/system.eventhandler?view=net-5.0) or [EventHandler&lt;TEventArgs>](https://learn.microsoft.com/en-us/dotnet/api/system.eventhandler-1?view=net-5.0)
delegates. Agree as a team on how everyone will implement events.  
注意:你也可以使用EventHandler或EventHandler<TEventArgs>委托。作为一个团队，你们可以商定如何实现事件。  

```csharp
// EXAMPLE: Events

// using System.Action delegate

public event Action OpeningDoor; // event before
public event Action DoorOpened; // event after

public event Action<int> PointsScored;
public event Action<CustomEventArgs> ThingHappened;
```  

— **Prefix the event raising method (in the subject) with “On”:** The subject
that invokes the event typically does so from a method prefixed with “On,”
e.g. “OnOpeningDoor” or “OnDoorOpened.”  
**用“On”前缀事件引发方法(在主题中):** 调用事件的主题通常是从一个以“On”为前缀的方法中调用的，例如“OnOpeningDoor”或“OnDoorOpened”。  
```csharp
// raises the Event if you have subscribers
public void OnDoorOpened()
{
  DoorOpened?.Invoke();
}
public void OnPointsScored(int points)
{
  PointsScored?.Invoke(points);
}
```  
— **Prefix the event handling method (in the observer) with the subject’s
name and underscore (_):** If the subject is named “GameEvents,” your
observers can have a method called “GameEvents_OpeningDoor” or
“GameEvents_DoorOpened.”  
**用主题的名称和下划线(_)前缀事件处理方法(在观察者中):** 如果主题的名称是“GameEvents”，你的观察者可以有一个名为“GameEvents_OpeningDoor”或“GameEvents_DoorOpened”的方法。  
  

Note that this is called the “event handling method”, not to be confused
with the EventHandler delegate.  
注意，这被称为“事件处理方法”，不要与EventHandler委托混淆。  

Decide a consistent naming scheme for your team and implement those
rules in your style guide.  
为你的团队决定一个一致的命名方案，并在你的样式指南中实现这些规则。  

— **Create custom EventArgs only as necessary:** If you need to pass custom
data to your Event, create a new type of EventArgs, either inherited from
[System.EventArgs](https://learn.microsoft.com/en-us/dotnet/api/system.eventargs?view=net-5.0) or from a custom struct.  
**只在必要时创建自定义的EventArgs:** 如果你需要向你的事件传递自定义数据，请创建一个新的EventArgs类型，它要么继承自[System.EventArgs](https://learn.microsoft.com/en-us/dotnet/api/system.eventargs?view=net-5.0)，要么继承自自定义结构。  

```csharp
// define an EventArgs if needed
// EXAMPLE: read-only, custom struct used to pass an ID and Color
public struct CustomEventArgs
{
  public int ObjectID { get; }
  public Color Color { get; }

  public CustomEventArgs(int objectId, Color color)
 {
  this.ObjectID = objectId;
  this.Color = color;
 }
}
```  
### Namespaces  命名空间  

Use a [namespaces](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/types/namespaces) to ensure that your classes, interfaces, enums, and so
on won’t conflict with existing ones from other namespaces or the global
namespace. Namespaces can also prevent conflicts with third-party assets from
the Asset Store.  
使用[命名空间](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/types/namespaces)来确保你的类、接口、枚举等不会与其他命名空间或全局命名空间中的现有命名空间发生冲突。命名空间也可以防止与来自资产商店的第三方资产发生冲突。  

When applying namespaces:  
在应用命名空间时:  

— Use pascal case without special symbols or underscores.  
使用帕斯卡命名法，不使用特殊符号或下划线。  

— Add a using directive at the top of the file to avoid repeated typing of the
namespace prefix.  
在文件顶部添加一个using指令，以避免重复输入命名空间前缀。  

— Create sub-namespaces as well. Use the dot(.) operator to delimit
the name levels, allowing you to organize your scripts into hierarchical
categories. For example, you can create MyApplication.GameFlow,
MyApplication.AI, MyApplication.UI, and so on to hold different logical
components of your game.  
也可以创建子命名空间。使用点(.)运算符来分隔名称级别，允许你将你的脚本组织成分层的类别。例如，你可以创建MyApplication.GameFlow，MyApplication.AI，MyApplication.UI等来保存游戏的不同逻辑组件。  

```csharp
namespace Enemy
{
  public class Controller1 : MonoBehaviour
  {
    ...
  }
  public class Controller2 : MonoBehaviour
  {
    ...
  }
}
```  
In code, these classes are referred to as Enemy.Controller1 and Enemy.
Controller2, respectively. Add a using line to save typing out the prefix:  
在代码中，这些类分别被称为Enemy.Controller1和Enemy.Controller2。添加一个using行来保存输入前缀:  

When the compiler finds the class names Controller1 and Controller2, it
understands you mean Enemy.Controller1 and Enemy.Controller2.  
当编译器找到类名Controller1和Controller2时，它会理解你的意思是Enemy.Controller1和Enemy.Controller2。  

```csharp
using Enemy;
```  
If the script needs to refer to classes with the same name from different
namespaces, use the prefix to differentiate them. For instance, if you have a
Controller1 and Controller2 class in the Player namespace, you can write
out Player.Controller1 and Player.Controller2 to avoid any conflicts.
Otherwise, the compiler will report an error.  
如果脚本需要引用来自不同命名空间的相同名称的类，请使用前缀来区分它们。例如，如果你在Player命名空间中有一个Controller1和Controller2类，你可以写出Player.Controller1和Player.Controller2来避免任何冲突。否则，编译器将报告一个错误。  



## Formatting 格式化  
"IF YOU WANT YOUR CODE TO BE EASY TO WRITE, MAKE IT EASY TO READ.”
– Robert C. Martin, author of Clean Code and Agile Software Development  
“如果你想让你的代码易于编写，那就让它易于阅读。”——《代码整洁之道》和《敏捷软件开发》的作者罗伯特·C·马丁  
Along with naming, formatting helps reduce guesswork and improves code
clarity. By following a standardized style guide, code reviews become less about
how the code looks and more about what it does.  
除了命名，格式化还有助于减少猜测，提高代码的清晰度。通过遵循标准化的样式指南，代码审查变得不再关注代码的外观，而是关注代码的功能。  

When constructing a style guide, personalize how your team will format your
code. Consider each of the following code formatting suggestions when setting
up your Unity dev style guide. Omit, expand, or modify these example rules to fit
your team’s needs.  
在构建样式指南时，个性化你的团队将如何格式化你的代码。在设置Unity开发样式指南时，请考虑以下每个代码格式化建议。省略、扩展或修改这些示例规则以适应你的团队的需求。  

In all cases, consider how your team will implement each formatting rule and
then have everyone apply it uniformly. Refer back to your team’s style to resolve
any discrepancies. The less you think about formatting, the more you can work
on something else.  
在所有情况下，考虑你的团队将如何实现每个格式化规则，然后让每个人都统一地应用它。回顾你团队的风格来解决任何不一致。你越少考虑格式，你就越能在其他事情上工作。  

Let’s take a look at formatting guidelines.  
让我们来看看格式化指南。  

#### Properties 属性  

A property provides a flexible mechanism to read, write, or compute class
values. Properties behave as if they were public member variables, but in fact
they’re special methods called [accessors](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/using-properties). Each property has a get and set method to access a private field, called a [backing field](https://learn.microsoft.com/en-us/ef/core/modeling/backing-field?tabs=data-annotations).  
属性提供了一种灵活的机制来读取、写入或计算类值。属性的行为就像它们是公共成员变量一样，但实际上它们是称为[accessors](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/using-properties)的特殊方法。每个属性都有一个get和set方法来访问一个私有字段，称为[backing field](https://learn.microsoft.com/en-us/ef/core/modeling/backing-field?tabs=data-annotations)。  

In this way, the property [encapsulates](https://en.wikipedia.org/wiki/Encapsulation_(computer_programming)#Information_hiding) the data, hiding it from unwanted
changes by the user or external objects. The getter and setter each have their
own access modifier, allowing your property to be read-write, read-only, or
write-only.  
这样，属性[封装](https://en.wikipedia.org/wiki/Encapsulation_(computer_programming)#Information_hiding)了数据，将其隐藏在用户或外部对象的不需要的更改中。getter和setter各自有自己的访问修饰符，允许你的属性是读写、只读或只写的。  

You can also use the accessors to validate or convert the data (e.g., verify that
the data fits your preferred format or change a value to a particular unit).  
你还可以使用访问器来验证或转换数据(例如，验证数据是否符合你的首选格式或将值更改为特定的单位)。  

The syntax for properties can vary, so your style guide should define how to
format them. Use these tips to keep properties consistent in your code:  
属性的语法可能会有所不同，所以你的样式指南应该定义如何格式化它们。使用这些提示来保持代码中的属性一致:  

— **Use expression-bodied properties for single line read-only properties
(=>)**: This returns the private backing field.  
**对单行只读属性使用表达式主体属性(=>):** 这将返回私有的backing field。  
```csharp
// EXAMPLE: expression-bodied properties
public class PlayerHealth
{
    // the private backing field
    private int maxHealth;

    // read-only, returns backing field
    public int MaxHealth => maxHealth;

    // equivalent to:
    // public int MaxHealth { get; private set; }
}

```  
— **Everything else uses the older { get; set; } syntax:** If you just want
to expose a public property without specifying a backing field, use the
[Auto-Implemented Property](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/auto-implemented-properties).  
**其他所有的都使用旧的{ get; set; }语法:** 如果你只想公开一个属性而不指定一个backing field，请使用[Auto-Implemented Property](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/auto-implemented-properties)。  

Apply the expression-bodied syntax for the set and get accessors.   
对set和get访问器应用表达式主体语法。  

Remember to make the setter private if you don’t want to give write
access. Align the closing with the opening brace for multi-line code
blocks.  
如果你不想给写入访问权限，请记住将setter设置为私有。将关闭与打开大括号对齐以进行多行代码块。  

```csharp
// EXAMPLE: expression bodied properties
public class PlayerHealth
{
    // backing field
    private int _maxHealth;

    // explicitly implementing getter and setter
    public int MaxHealth
    {
        get => _maxHealth;
        set => _maxHealth = value;
    }

    // write-only (not using backing field)
    public int Health { private get; set; }

    // write-only, without an explicit setter
    public void SetMaxHealth(int newMaxValue) => _maxHealth = newMaxValue;
}
```  
#### Serialization 序列化  

Script serialization is the automatic process of transforming data structures
or object states into a format that Unity can store and reconstruct later. For
performance reasons, Unity handles serialization differently than in other
programming environments.  
脚本序列化是将数据结构或对象状态自动转换为Unity可以存储和重建的格式的过程。出于性能的考虑，Unity处理序列化的方式与其他编程环境不同。  

Serialized fields appear in the Inspector, but you cannot serialize static,
constant, or read-only fields. They must be either public or tagged with the
[SerializeField] attribute. Unity only serializes certain field types, so refer
to the [documentation page](https://docs.unity3d.com/Manual/script-Serialization.html) for the complete set of serialization rules.  
序列化字段出现在检查器中，但你不能序列化静态、常量或只读字段。它们必须是公共的，或者用[SerializeField]属性标记。Unity只序列化某些字段类型，所以请参考[文档页面](https://docs.unity3d.com/Manual/script-Serialization.html)以获取完整的序列化规则集。  

Observe a few basic guidelines when working with serialized fields:  
在使用序列化字段时，请遵循一些基本准则:  

— **Use the [SerializeField] attribute:** The SerializeField attribute can
work with private or protected variables to make them appear in the
Inspector. This encapsulates the data better than marking the variable
public and prevents an external object from overwriting its values.  
**使用[SerializeFiled]属性:** SerializeField属性可以与私有或受保护的变量一起使用，使它们出现在检查器中。这比将变量标记为public更好地封装了数据，并防止外部对象覆盖其值。  

— **Use the Range attribute to set minimum and maximum values:** The
[Range(min, max)] attribute is handy if you want to limit what the user
can assign to a numeric field. It also conveniently represents the field as a
slider in the Inspector.  
**使用Range属性来设置最小值和最大值:** 如果你想限制用户可以分配给数字字段的内容，[Range(min, max)]属性是很方便的。它还可以方便地在检查器中将字段表示为滑块。  

— **Group data in serializable classes or structs to clean up the Inspector:**
Define a public class or struct and mark it with the [Serializable]
attribute. Define public variables for each type you want to expose in the
Inspector.  
**在可序列化的类或结构中对数据进行分组，以清理检查器:** 定义一个公共类或结构，并用[Serializable]属性标记它。为你想在检查器中公开的每种类型定义一个公共变量。  

```csharp
// EXAMPLE: a serializable class for PlayerStats
using System;
using UnityEngine;

public class Player : MonoBehaviour
{
    [Serializable]
    public struct PlayerStats
    {
        public int MovementSpeed;
        public int HitPoints;
        public bool HasHealthPotion;
    }

    // EXAMPLE: The private field is visible in the Inspector
    [SerializeField]
    private PlayerStats _stats;
}

```  
Reference this serializable class from another class. The resulting variables
appear within collapsible units in the Inspector.  
从另一个类引用这个可序列化的类。结果变量出现在检查器中的可折叠单元中。  

[图片]  
A serializable class or struct can help organize the Inspector.  
可序列化的类或结构可以帮助组织inspector。

#### Brace or indentation style 大括号或缩进样式  

There are two common indentation styles in C#:  
C#中有两种常见的缩进样式:  

— The [Allman style](https://en.wikipedia.org/wiki/Indentation_style#Allman_style) places the opening curly braces on a new line, also known as the BSD style (from BSD Unix).  
[Allman style](https://en.wikipedia.org/wiki/Indentation_style#Allman_style)将左大括号放在新行上，也称为BSD样式(来自BSD Unix)。  

— The [K&R style](https://en.wikipedia.org/wiki/Indentation_style#K&R_style), or “one true brace style,” keeps the opening brace on the
same line as the previous header.  
[K&R style](https://en.wikipedia.org/wiki/Indentation_style#K&R_style)，或者“one true brace style”，将左大括号保持在与前一个头相同的行上。  

```csharp
// EXAMPLE: Allman or BSD style puts opening brace on a new line.
void DisplayMouseCursor(bool showMouse)
{
    if (!showMouse)
    {
        Cursor.lockState = CursorLockMode.Locked;
        Cursor.visible = false;
    }
    else
    {
        Cursor.lockState = CursorLockMode.None;
        Cursor.visible = true;
    }
}

// EXAMPLE: K&R style puts opening brace on the previous line.
void DisplayMouseCursor(bool showMouse){
    if (!showMouse) {
        Cursor.lockState = CursorLockMode.Locked;
        Cursor.visible = false;
    }
    else {
        Cursor.lockState = CursorLockMode.None;
        Cursor.visible = true;
    }
}

```  
There are variations on these [indentation styles](https://en.wikipedia.org/wiki/Indentation_style) as well. The examples in this guide use the Allman style from the [Microsoft Framework Design Guidelines](https://learn.microsoft.com/en-us/dotnet/standard/design-guidelines/).Regardless of which one you choose as a team, make sure everyone follows the same indentation and brace style.  
这些[缩进样式](https://en.wikipedia.org/wiki/Indentation_style)也有变化。本指南中的示例使用了[Microsoft Framework Design Guidelines](https://learn.microsoft.com/en-us/dotnet/standard/design-guidelines/)中的Allman样式。无论你的团队选择哪种样式，都要确保每个人都遵循相同的缩进和大括号样式。  

Try these tips:  
试试这些提示:  

— **Decide on a uniform indentation:** This is typically four or two spaces. Get
everyone on your team to agree on a setting in your Editor preferences
without igniting a [tabs versus spaces flame war](https://thenewstack.io/spaces-vs-tabs-a-20-year-debate-and-now-this-what-the-hell-is-wrong-with-go/). Note that Visual Studio provides the option to convert tabs to spaces.  
**决定统一的缩进:** 通常是四个或两个空格。在不引发[制表符与空格的战争](https://thenewstack.io/spaces-vs-tabs-a-20-year-debate-and-now-this-what-the-hell-is-wrong-with-go/)的情况下，让你的团队中的每个人都同意在你的编辑器首选项中设置一个选项。注意，Visual Studio提供了将制表符转换为空格的选项。  

In Visual Studio (Windows), navigate to **Tools > Options > Text Editor >
C# > Tabs**.  
在Visual Studio(Windows)中，导航到**Tools > Options > Text Editor > C# > Tabs**。  

[图片]  
Tabs settings in Visual Studio  
Visual Studio中的制表符设置  

On Visual Studio for Mac, navigate to **Preferences > Source Code > C# Source
Code**. Select the Text Style to adjust the settings.  
在Visual Studio for Mac上，导航到**Preferences > Source Code > C# Source Code**。选择文本样式来调整设置。  

[图片]  
Convert tabs to spaces to make indentation uniform.  
将制表符转换为空格，使缩进统一。  

— **Where possible, don’t omit braces, even for single-line statements:** This
increases consistency, keeping your code easier to read and maintain. In
this example, the braces clearly separate the action, DoSomething, from
the loop.  
**在可能的情况下，不要省略大括号，即使是单行语句:** 这增加了一致性，使你的代码更容易阅读和维护。在这个例子中，大括号清楚地将动作DoSomething与循环分开。  

If later you need to add a Debug line or to run DoSomethingElse, the
braces will already be in place. Keeping the clause on a separate line
allows you to add a breakpoint easily.  
如果以后你需要添加一个Debug行或运行DoSomethingElse，大括号将已经就位。将子句保持在单独的一行上可以让你轻松地添加断点。  

```csharp
// EXAMPLE: keep braces for clarity...
for (int i = 0; i < 100; i++) { DoSomething(i); }

// … and/or keep the clause on a separate line.
for (int i = 0; i < 100; i++)
{
    DoSomething(i);
}

// AVOID: omitting braces
for (int i = 0; i < 100; i++) DoSomething(i);

```  
— **Don’t remove braces from nested multi-line statements:** Removing
braces in this case won’t throw an error, but can be confusing. Apply
braces for clarity, even if they are optional.  
**不要从嵌套的多行语句中删除大括号:** 在这种情况下删除大括号不会抛出错误，但可能会令人困惑。即使可选，也要应用大括号来保持清晰。  

```csharp
// EXAMPLE: keep braces for clarity
for (int i = 0; i < 10; i++)
{
    for (int j = 0; j < 10; j++)
    {
        ExampleAction();
    }
}

// AVOID: removing braces from nested multi-line statements
for (int i = 0; i < 10; i++)
    for (int j = 0; j < 10; j++)
      ExampleAction();

```  
— **Standardize your switch statements:** Formatting can vary, so document
your team preference in your style guide. Here is one example where you
indent the case statements.  
**标准化你的switch语句:** 格式可以有所不同，所以在你的样式指南中记录你的团队偏好。这是一个例子，你可以缩进case语句。  

```csharp
// EXAMPLE: indent cases from the switch statement
switch (someExpression)
{
    case 0:
        DoSomething();
        break;
    case 1:
        DoSomethingElse();
        break;
    case 2:
        int n = 1;
        DoAnotherThing(n);
        break;
}

```  
>#### What is EditorConfig? 什么是EditorConfig?  
>
>Do you have multiple developers working on the same project with different
editors and IDEs? Consider using an [EditorConfig](https://learn.microsoft.com/en-us/visualstudio/ide/create-portable-custom-editor-options?view=vs-2019) file.  
你是否有多个开发人员在同一个项目上使用不同的编辑器和IDE?考虑使用[EditorConfig](https://learn.microsoft.com/en-us/visualstudio/ide/create-portable-custom-editor-options?view=vs-2019)文件。  
>
>The EditorConfig file can help you define a coding style that works across your
entire team. Many IDEs, like Visual Studio and Rider, come bundled with native
support and do not require a separate plugin.  
EditorConfig 文件可以帮助你定义一个在整个团队中都有效的编码风格。许多IDE，如Visual Studio和Rider，都内置了本地支持，不需要单独的插件。  
>
>[EditorConfig](https://editorconfig.org/) files are easily readable and work with version control systems. You can see an [example file here](https://editorconfig.org/#example-file). The code styling from EditorConfig travels with your code and can enforce coding styles even outside of Visual Studio.  
[EditorConfig](https://editorconfig.org/)文件易于阅读，并且可以与版本控制系统一起使用。你可以在[这里看到一个示例文件](https://editorconfig.org/#example-file)。来自EditorConfig的代码样式与你的代码一起传播，甚至可以在Visual Studio之外强制执行代码样式。  
>
>EditorConfig settings take precedence over the global Visual Studio text editor
settings. Your personal editor preferences still apply whenever you’re working in
a codebase without a .editorconfig file, or when the .editorconfig file doesn’t
override a particular setting.  
EditorConfig设置优先于全局Visual Studio文本编辑器设置。只要你在没有.editorconfig文件的代码库中工作，或者.editorconfig文件没有覆盖特定的设置，你的个人编辑器首选项仍然适用。  
>
>See the GitHub repo for some [real-world samples](https://github.com/editorconfig/editorconfig/wiki/Projects-Using-EditorConfig).  
请参阅GitHub repo中的一些[真实样本](https://github.com/editorconfig/editorconfig/wiki/Projects-Using-EditorConfig)。