# 代码整洁之道 #

- [代码整洁之道](#代码整洁之道)
  - [第1章 整洁代码](#第1章-整洁代码)
    - [1.3.5 什么是整洁代码](#135-什么是整洁代码)
    - [1.6 童子军军规](#16-童子军军规)
  - [第2章 有意义的命名](#第2章-有意义的命名)
    - [2.2.2 名副其实](#222-名副其实)
  - [2.5 使用读得出来的名称](#25-使用读得出来的名称)
  - [2.6 使用可搜索的名字](#26-使用可搜索的名字)
  - [2.7 避免使用编码](#27-避免使用编码)
  - [2.12 每个概念对应一个词](#212-每个概念对应一个词)
  - [2.13 别用双关语](#213-别用双关语)
  - [第6章 对象和数据结构](#第6章-对象和数据结构)
    - [6.2 数据、对象和反对称性](#62-数据对象和反对称性)
    - [6.3得墨尔忒耳定律](#63得墨尔忒耳定律)
  - [第10章 类](#第10章-类)
    - [10.1 类的组织](#101-类的组织)
      - [封装](#封装)
    - [10.2 类应该短小](#102-类应该短小)
    - [10.3 为了修改而组织](#103-为了修改而组织)
      - [隔离修改](#隔离修改)
  - [第12章 迭进](#第12章-迭进)
    - [12.1 通过迭进设计达到整洁目的](#121-通过迭进设计达到整洁目的)
    - [12.2 简单设计规则1：运行所有测试](#122-简单设计规则1运行所有测试)
    - [12.3 简单设计规则2~4：重构](#123-简单设计规则24重构)
    - [12.4 不可重复](#124-不可重复)
    - [12.5 表达力](#125-表达力)
    - [12.6 尽可能少的类和方法](#126-尽可能少的类和方法)
  - [第17章 味道与启发](#第17章-味道与启发)
    - [17.1 注释](#171-注释)
    - [17.2 环境](#172-环境)
    - [17.3 函数](#173-函数)
    - [17.4 一般性问题](#174-一般性问题)
    - [17.5 Java](#175-java)
    - [17.6名称](#176名称)
    - [17.7测试](#177测试)

## 第1章 整洁代码 ##

### 1.3.5 什么是整洁代码 ###

- **Bjarne Stroustrup, C++语言发明者。C++ Programming Language 一书作者。** 我喜欢优雅和高效的代码。代码逻辑应当直接了当，叫缺陷难以隐藏；尽量减少依赖关系，使之便于维护；依据某种分层战略完善错误处理代码；性能调至最优，省得引诱别人做没规矩的优化，搞出一堆混乱来。整洁的代码只做好一件事。

> 内容很多，很C++。
>
> - *逻辑简单直接，简单就容易犯错。尽量少用复杂的算法，或者进行合适的分层及封装*
> - *减少依赖。在各个层面。比如DLL 依赖。模块级别的依赖。类级别的依赖。函数级别的依赖。关系约少越好*
> - *要写的清楚明了，改无可改，避免别人想着优化。避免不必要的麻烦*
> - *专注！专注！！专注！！！ 只做一件事*

- **Michael Features, Working Effectively with Legacy Code.** 我可以列出我留意到的整洁代码的所有特别，但其中有一条是根本性的。整洁的代码总是看起来像是某位特别**在意** 它的人写的。几乎没有修改的余地。代码作者什么都想到了，如果你企图改进它，总会回到原点，赞叹某人留给你的代码--全心投入的某人留下的代码。

> *在意代码。需要做的是反复推敲，看看有没有改进的空间。*

- **Ron Jeffiers, Extreme Programming Installed 作者。** 减少重复代码，提高表达力，提早构建简单抽象。 这就是我写代码的整洁之道。  

> 有很多方法论：
>
> - *不要重复代码!*
> - *好好想想变量名、函数名、类名，只在必须出现加注释的地方加上合适的注释*
>  *需要代码优化的时候要今早开始。包括help函数的抽取。重复代码的去除。数据结构及类的引入等等*
>

[20190623]

### 1.6 童子军军规 ###

- **保持代码整洁：** 让营地比你来时更干净。

---
[20190623]

## 第2章 有意义的命名 ##

### 2.2.2 名副其实 ###

> *花些时间想个好名字，尽量体现本意*
  
---
[20190623]

## 2.5 使用读得出来的名称 ###

## 2.6 使用可搜索的名字 ###

## 2.7 避免使用编码 ###

## 2.12 每个概念对应一个词 ###

## 2.13 别用双关语 ###

- *以一以贯之的方式想个好名字，符合系统的命名规则，并且保证拼写是正确的*
  
---
[20190728]

## 第6章 对象和数据结构 ##

### 6.2 数据、对象和反对称性 ###

- **对象把数据隐藏与抽象之后，暴露操作数据的函数。数据结构暴露其数据，没有提供有意义的函数。**
- **过程式代码（不使用数据结构的代码）便于在不改动既有数据结构的前提下添加新函数。面向对象代码便于在不改动既有函数的前提下添加新类。**
- **过程式代码难以添加新数据结构，因为必须修改所有函数。面向对象代码难以添加新函数，因为必修修改所有类。**

### 6.3得墨尔忒耳定律 ###

- 模块不应该了解它所操作**对象**的内部情形。
- 类C的方法f只应该调用以下对象的方法：
  - C
  - 由f创建的对象
  - 作为参数传递给f的对象
  - 由C的实体变量持有的对象
- 方法**不应**调用由任何函数返回的对象的方法。

---
[20190728]

## 第10章 类 ##

### 10.1 类的组织 ###

#### 封装 ####

- 保持变量和工具函数私有。有时，也需要用到受保护变量或者工具函数，好让测试可以访问到。

### 10.2 类应该短小 ###

- 10.2.1 单一权责原则
  - 类或模块应有且只有一条加以修改的理由。
  - 系统应该由许多短小的类而不是少量巨大的类组成。 每个小类封装一个权责，只有一个修改原因，并与少数其他类一起协同达成期望的系统行为。
- 10.2.2 内聚
  - 类应该只有少量实体变量。类中的方法都应该操作一个或多个这种变量。通常而言，方法操作的变量越多，就越黏聚到类上。
- 10.2.3 保持内聚性就会得到许多短小的类

### 10.3 为了修改而组织 ###

- 在理想的系统中，我们通过扩展系统而非修改现有代码来添加新特性。

#### 隔离修改 ####

- 具体类包含实现细节（代码），而抽象类则只呈现概念。依赖于具体细节的客户类，当细节改变时，就会有风险。我们可以借助接口和抽象类来隔离这些细节带来的影响。

---
[20190728]

## 第12章 迭进 ##

### 12.1 通过迭进设计达到整洁目的 ###

### 12.2 简单设计规则1：运行所有测试 ###

### 12.3 简单设计规则2~4：重构 ###

### 12.4 不可重复 ###

### 12.5 表达力 ###

### 12.6 尽可能少的类和方法 ###

---
[20190707]

## 第17章 味道与启发 ##

### 17.1 注释 ###

- **C1: 不恰当的信息** 让注释传达本该更好地在源代码控制系统、问题追踪系统或者任何其他记录系统中保存的信息，是不恰当的。 例如，修改历史记录只会用大量过时而无趣的文本搞乱源代码文件。 通常，作者、最后修改时间、SPR等元数据不该在注释中出现。注释只应该描述有关代码和设计的技术性信息。
- **C2: 废弃的注释**  
  - 过时、无关或不正确的注释就是废弃的注释。注释会很快过时。最好别编写将被废弃的注释。如果发现废弃的注释，最好尽快更新或删除掉。废弃的注释会远离他们曾经描述的代码，变成代码中无关和误导的浮岛。
- **C3: 冗余注释**
  - 如果注释描述的是某种充分自我描述了的东西，那么注释就是多余的。例如：

 ```Java
 i++; //increment i
```

 另一个例子是除函数签名外什么也没多说（或少说）的javadoc

 ```Java
 /***
  *@param sellRequest
  *@return 
  *@throws ManagedComponentException */ 
    
  public SellRequest beginSellItem(SellRequest sellRequest) throws ManageComponentException
```

 注释应该谈及代码自身没提到的东西。

- **C4:糟糕的注释**
  - 值得编写的注释，也值得好好写。 如果要编写一条注释，就花时间保证写出最好的注释。字斟句酌。使用正确的语法和拼写。别扯淡，别画蛇添足，保持简洁。
- **C5:注释掉的代码**
  - 注释掉的随着时间推移，越来越与系统没关系。它调用了不复存在的函数。它使用已改名的变量。它遵守已被废弃的约定。它污染了所属的模块，分散了想要读它的人的注意力。注释掉的代码纯属**厌物**。
  - 看到注释掉的代码，就**删除它!** 别担心，源代码控制系统还会记得它。如果有人真的需要它，可以签出比较前的版本。别被它搞的死去活来。

### 17.2 环境 ###

- **E1: 需要多步才能实现的构建**
  - 构建系统应该是单步的小操作。 不应该从源代码控制系统中一小点一小点签出代码。不应该需要一系列神秘指令或环境依赖脚本来构建单个元素。不应该四处寻找额外的小jar， XMl文件和其他系统需要的杂物。你应当能能够用单个命令签出系统，并用单个命令构建它。

```shell
  svn get mySystem cd mySystem ant all 
```

- **E2: 需要多步才能做到的测试**
  - 你应当能够发出单个指令就可以运行全部测试。能够运行全部测试是如此重要，应该快速、轻易和直截了当地做到。

### 17.3 函数 ###

- **F1：过多的参数**
  - 函数的参数量应该尽量的少。没参数最好，一个次之，两个、三个再次之。三个以上的参数非常值得质疑，应坚决避免。
- **F2: 输出参数**
  - 输出参数违反直觉。读者期望参数用于输入而非输出。如果函数非要修改什么东西的状态不可，就修改它所在对象的状态好了
- **F3:标识参数**
  - 布尔值参数大声宣告函数做了不止一件事。它们令人迷惑，应该消失掉。
- **F4: 死函数**
  - 永不被调用的方法应该丢弃。保留死代码纯属浪费。别害怕删除函数。记住，源代码控制系统还会记得它。

 [20190721]

### 17.4 一般性问题 ###

- **G1: 一个原文件中存在多种语言**
- **G2: 明显的行为未被实现。**
  - 如果明显的行为未被实现，读者和用户就不能再依靠他们对函数的直觉。他们不再信任原作者，不得不阅读代码细节。
- **G3: 不正确的边界行为**
  - 每种边界条件、每种极端情形、每个异常都代表了某种可能搞乱优雅而直白的算法的东西。**别依赖直觉。**追索每种边界条件，并编写测试。
- **G4:忽视安全**
  - 忽视安全相当危险。
- **G5:重复**
  - 每位编写有关软件设计的作者都提到这条规则
  - 每次看到重复代码，都代表遗漏了抽象。
  - 较隐蔽色形态是在不同模块中不断重复出现、检测同一组条件的switch/case 或者if/else链。可以用多态来替代之。
  - 更隐蔽的形态是采用类似算法但具体代码行不同的模块。这也是一种重复，可以使用模块方法或者策略模式来修正。
  - **尽可能找到并消除重复。**
- **G6:在错误的抽象层级上的代码**
  - 创建分离较高层级一般性概念与较低级细节概念的抽象模型。这很重要。有时，我们创建抽象类来容纳较高层级概念，创建派生类来容纳较低层次概念。这样做的时候，需要确保分离完整。**所有**较低级概念放在派生类中，**所有**较高层级概念放在基类中。
  - 只与细节实现相关的常量、变量或工具函数不应该在基类中出现。基类应该对这些东西一无所知。
  - 这条规则对于源文件、组件、和模块也适用。
- **G7:基类依赖于派生类**
  - 将概念分解到基类和派生类最普遍的原因是较高级基类概念可以不依赖于较低层级派生类概念。这样，如果看到基类提到派生类名称，就可能发现了问题。通常来说，基类对派生类应该一无所知。
- **G8:信息过多**
  - 设计良好的模块有着非常小的接口。
  - 优秀的软件开发人员学会限制类或模块中暴露的接口数量。类中的方法越少越好。函数知道的变量越少越好。类使用的实体变量越少越好。
  - 隐藏你的数据。隐藏你的工具函数。隐藏你的常量和临时变量。不要创建拥有大量方法或者大量实体变量的类。不要为子类创建大量受保护变量和函数。尽力保持接口紧凑。通过限制信息来控制耦合度。
- **G9：死代码**
  - 如果你找到死代码，就体面地埋葬它，将它从系统中删除掉。
- **G10:垂直分隔**
  - 变量和函数应该在靠近被使用的地方定义。本地变量应该正好在首次被使用的位置上面声明，垂直距离要短。
  - 私有函数应该刚好在其首次被使用的位置下面定义。私有函数属于整个类，但我们还是要限制调用和定义之间的垂直距离。
- **G11:前后不一致**
  - 从一而终。这可追溯到最小惊异原则。小心选择约定，一旦选中，就小心持续遵循。
- **G12:混淆视听**
  - 没有实现的默认构造器有何用处呢？它只会用无意义的杂碎搞乱对代码的理解。没有用到的变量，从不调用的函数，没有信息量的注释，等等。这些都是应该移除的废物。保持文件整洁，良好地组织，不被搞乱。
- **G13:人为耦合**
  - 不互相依赖的东西不该耦合。
  - 人为耦合是指两个没有直接目的之间的模块的耦合。其根源是将变量、常量或者函数不恰当地放在临时方便的位置。这是种漫不经心的偷懒行为。
  - 花点时间研究应该在什么地方声明函数、常量和变量。不要为了方便随手放置，然后置之不理。
- **G14:特性依赖**
  - 类的方法只应对其所属类中的变量和函数感兴趣，不该垂青其他类中的变量和函数。当方法通过某个其他对象的访问器和修改器来操作该对象内部数据时，它就**依恋与**该对象所属类的范围。
    > *类中方法只使用类的成员变量，或者入参，不应使用入参的方法获取的值*

- **G15:选择算子参数**
  - 选择算子参数只是一种避免把大函数切分为多个小函数的偷懒做法。
  - 使用多个函数，通常优于向单个函数传递某些代码来选择函数行为。
- **G16:晦涩的意图**
  - 代码要尽可能具有表达力。联排表达式、匈牙利标记法和魔术数都屏蔽了作者的意图。
- **G17:位置错误的权责**
  - 软件开发者做出的最重要决定之一就是在哪里放代码。o
  - 代码应该放在读者自然而然期待它所在的地方。
- **G18:不恰当的静态方法**
  - 通常应该倾向于选用非静态方法。如果有疑问，就用非静态函数。如果的确需要静态函数，确保没机会打算让他们有多态行为。
- **G19:使用解释性变量**
- **G20:函数名称应该表达其行为**
- **G21:理解算法**
  - 在你认为自己完成某个函数之前，确认自己**理解了**它是怎么工作的。通过全部测试还不够好，你必须**知道**解决方案是正确的。
  - 获得这种知识和理解的最好途径，往往是重构函数，得到某种整洁而足具表达力、清楚呈示如何工作的东西。
  
    > *下面的注释写的很好，不确定算法是否恰当司空见惯，而不确定代码做什么确是一种懒惰行为。 你可以不理解代码为啥这么写，但没有搞清楚实现细节就是懒惰不负责任。*
   
  ---
  [20190728]
- **G22:把逻辑依赖改为物理依赖**
  - 如果某个模块依赖于另一个模块，依赖就应该是物理上的而不是逻辑上的。依赖者模块不应对被一来者模块有假定（换言之，逻辑依赖）。

  - *使用一个模块时，不要对模块有任何的假定。在自己的模块中使用自己定义的条件或者第三方条件来约束依赖模块的行为是不对的。应该将这种约束放在被调用模块，由被调用模块显示的获取约束条件。*

- **G23: 用多态替代if/Else或Switch/Case**
  - 在使用switch 之前，先考虑使用多态。
  - 函数变化甚于类型变化的情形相对罕见。**每个**switch语句都值得怀疑。

  - 单个“switch”规则：对于给定的选择类型，不应有多于一个的switch语句。在那个switch语句中的多个case，必须创建多态对象，取代系统中其他类似switch语句。

- *没有真正地理解，先记在这里吧*

- **G24: 遵守标准约定**
  - 每个团队都应遵循基于通用行业规范的一套编码标准。
  - 团队中的每个成员都应遵守这些约定。
- **G25:用命名常量替代魔术数**
- **G26:准确**
  - 在代码中做决定时，确认自己足够**准确**。
  - 代码中的含糊和不准确要么是意见不同的结果，要么源于懒惰。无论什么原因，都要消除。
- **G27：结构甚于约定**
  - 坚守结构甚于约定的设计决策。命名约定很好，但却次于强制性的结构。例如，用到良好命名的枚举的switch/case要弱于拥有抽象方法的基类。没人会被强迫每次都以同样的方式实现switch/case 语句，但基类却让具体类型必须实现所有抽象方法。
    - *这个观点着实有趣。这里的结构我认为翻译的不好。翻译成架构可能更合理。把一些约束放在架构层面，而不是细节的约束。放在架构层面可以保证约束不得不执行，不遵守规则没法完成。细节的约束固然好，但不是最优雅的解决办法。*
- **G28：封装条件**
- **G29: 避免否定性条件**
- **G30：函数只该做一件事情**
- **G31: 掩蔽时序耦合**
  - 常常有必要使用时序耦合，但你不应该掩蔽它。

- **G32：别随意**
  - 构建代码需要理由，而且理由应与代码结构相契合。如果结构显得太随意，其他人就会想修改它。如果结构自始至终保持一致，其他人就会使用它，并且遵守其约定。

- **G33: 封装边界条件**
  - 边界条件难以追踪。把处理边界条件的代码集中到一处，不要散落于代码中。

- **G34：函数应该只在一个抽象层级上**
  - 函数中的语句应该在同一抽象层级上，该层级应该是函数名所示操作的下一层。
    - *我的理解这里强调两个层面。第一个层面是函数内部的逻辑应该是平的。只在一层操作数据。不同层操作数据需要重构。另外一个层面，当前函数可以操作哪一层的数据是看函数命名的。从这个层面讲，函数的名字应该反映出操作数据的层级，这进一步提高了对于函数命名的要求.*
- **G35: 在较高层级放置可配置数据。**
  - 如果你有个已知并该在较高抽象层级的默认常量或者配置值，不要将它埋藏到较低层级的函数中。把它作为较高层级函数调用较低函数时的一个参数。
  - 位于较高层级的配置性常量易于修改。它们能向下贯穿整个应用。应用程序的较低层级并不拥有这些常量的值。

- **G36: 避免传递浏览**
  - 通常我们不想让某个模块了解太多其写协作者的信息。更具体地说，如果A与B协作，B与C协作，我们不想让使用A的模块了解C的信息。
  - 这就是所谓的得墨忒耳定律。

### 17.5 Java ###

### 17.6名称 ###

- **N1:采用描述性名称**
- **N2:名称应与抽象层级相符**
  - 不要取沟通实现的名称；取反应类或函数抽象层级的名称。
- **N3:竟可能使用标准命名法**
- **N4:无歧义的名称**
- **N5：为较大作用域范围选用较长名称**
  - 名称的长度应与作用范围的广泛度相关。
- **N6：避免编码**
- **N7：名称应该说明副作用**
  - 名称应该说明函数、变量或类的一切信息。不要用名称掩蔽副作用。不要用简单的动词来描述做了不止一个简单动作的函数。

### 17.7测试 ###

- **T1：测试不足**
  - 只要还有没被测试探测过的东西，或是还没有没被验证过的计算，测试就还不够。
- **T2：使用测试覆盖率工具**
- **T3：别略过小测试**
- **T4：被忽略的测试就是对不确定事务的疑问**
- **T5：测试边界条件**
- **T6：全面测试相近的缺陷**
- **T7：测试失败的模式有启发性**
- **T8：测试覆盖率的模式有启发性**
- **T9：测试应该快速**