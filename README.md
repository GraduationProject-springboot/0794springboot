# [首页查询更多项目](https://github.com/GraduationProject-springboot) 包安装运行


# 0794springbootspringcloud房产销售平台

![picture](https://raw.githubusercontent.com/GraduationProject-springboot/.github/main/img/wx.png)

### 点击播放视频 ▼
[![Watch the video](https://i.sstatic.net/Vp2cE.png)]()


﻿黑龙江八一农垦大学毕业论文（设计）




![IMG\_256](/md/blog.001.jpeg "IMG\_256")![1126666711382834012031](/md/blog.002.png "1126666711382834012031")



学士学位毕业设计


基于Spring cloud房产销售平台的设计与实现




|**学生姓名：**||
| - | - |
|**学    号：**||
|**指导教师：**|**刘某某**|
|**所在学院：**|**信息与电气工程学院**|
|**专    业：**|**计算机科学与技术**|



黑龙江八一农垦大学教务处制

20ⅩⅩ 年 Ⅹ 月





II

**摘  要**

信息技术的发展推动了管理系统的进步，目前各种行业都积极参与管理系统的建设工作。特别是疫情带来的影响，让传统行业逐渐认识到只有通过在线管理才能继续的发展。房产销售平台是为求租者提供房源必备的平台，如何找到一个好的房源是生活中很重要的事情。传统的签约模式是依靠同学介绍，签约中心推荐等，这种模式下会造成传播效率低，发生问题不能及时处理，还有一些没有资质的二手房东浑水摸鱼，耽误时间。而通过发展基于JAVA的房产销售平台，可以快速的找到房源，对于房东，也可以委托给房源中介，实现双赢。

房产销售平台采用Spring cloud开发，数据库MySQL存放信息。本文首先进行理论分析，提出房产销售平台的建设可行性，然后通过需求分析，设计房产销售平台的功能，最后进行代码实现。房产销售平台包括两种用户，管理员管理用户和房源信息，客户登录后，查看房源信息，在线签约。房产销售平台的开发，实现了各用户实际需求，对房源行业产生积极影响。

关键词：房源，MySQL，房源签约，Spring cloud

# **Abstract**
The development of information technology has promoted the progress of management system, and all kinds of industries are actively involved in the construction of management system. Especially the impact of epidemic, the traditional industry gradually realized that only through online management can continue to develop. The real estate sales platform is a necessary platform for the renters to provide the housing resources. How to find a good source of housing is very important in life. The traditional leasing mode relies on the introduction of students, the recommendation of leasing center, etc. in this mode, the communication efficiency is low, problems can not be dealt with in time, and some unqualified second-hand landlords fish in the water, which delays time. And through the development of the real estate sales platform based on Java, we can quickly find the source of the house, for the landlord, can also entrust to the housing source intermediary, to achieve a win-win situation.

The real estate sales platform is developed by spring cloud, and MySQL database stores information. This paper first carries on the theoretical analysis, proposes the construction feasibility of the real estate sales platform, then through the demand analysis, designs the function of the real estate sales platform, and finally carries on the code realization. The real estate sales platform includes two kinds of users, the administrator manages the user and the house source information. After the customer logs in, the user can view the information of the house source and rent online. The development of the real estate sales platform has realized the actual needs of all users, and has a positive impact on the real estate industry.

**Keywords:** source, mysql, rental, spring cloud.




目  录

[前言	1]()

[1 绪论	1]()

[1.1背景和意义	1]()

[1.2国内外现状	2]()

[1.3相关技术概述	2]()

[1.3.1 JAVA技术	2]()

[1.3.2 编程环境	3]()

[1.3.3 Mysql数据库	3]()

[1.3.4 Spring cloud技术	4]()

[2 系统分析	5]()

[2.1系统需求分析	5]()

[2.2系统使用者	5]()

[2.3系统用例分析	5]()

[2.4可行性分析	8]()

[3 系统设计	10]()

[3.1系统体系结构	10]()

[3.1.1 界面层设计	10]()

[3.1.2 数据库层设计	10]()

[3.1.3 业务逻辑层设计	10]()

[3.2系统功能设计	10]()

[3.2.1 管理员功能	11]()

[3.2.2 客户功能	11]()

[3.3 系统流程设计	12]()

[3.4 数据库设计原则	13]()

[3.5 系统数据库E-R图	13]()

[3.6 数据库表的设计	15]()

[4 系统实现	17]()

[4.1登陆模块的实现	17]()

[4.2房源信息管理模块实现	17]()

[4.3签约信息管理模块实现	19]()

[4.4申请看房管理实现	20]()

[4.5平台前台首页实现	20]()

[4.6在线留言模块实现	21]()

[总 结	23]()

[参考文献	24]()

[致  谢	25]()



前言

现如今，人们日渐关注互联网的发展，同时人们也开始大量使用自动管理技术来对各行各业进行管理。早前的人工管理方式所存在的缺陷开始不断显现，例如管理成效差，处理信息的速度缓慢，工作量大，处理信息的精准度不高等。基于此，怎样扭转此种情况，尽可能的使以上问题得到解决，切实解放劳动力，其关键在于提高处理信息过程中的准确率。经济因时代的发展而迅速发展，当下的市场更是变幻莫测，在此种背景之下，如今的房产销售平台需要面对很多的挑战，与此同时，它还应具备较强的扩展性。

计算机技术已经渗透到人们生活的方方面面，使得大家工作、学习以及生活方式都发生了翻天覆地的改变，从最初的必须面对面求租，到通过互联网观看房源，甚至通过手机、iPad进行互动，突破了房源签约资源受时间、空间、地域的限制，随时随地都可以通过网络获得自己想要的房源信息，帮助求租者提高查找信息的效率。当前社会，竞争日益激烈，只有使用管理系统才能提高管理效率。目前，我国网络环境和市场经济发展良好，各行业分布广泛，工作精细化程度高。对于各项工作流程的管理更加的重视，使用管理系统对企业进行流程化管理，控制业务，提高工作效率，对流程化进行统一控制，方便用户快速的解决相关事务。

房产销售平台采用Spring cloud开发，数据库MySQL存放信息。本文首先进行理论分析，提出房产销售平台的建设可行性，然后通过需求分析，设计房产销售平台的功能，最后进行代码实现。房产销售平台包括两种用户，管理员管理用户和房源信息，客户登录后，查看房源信息，在线签约。房产销售平台的开发，实现了各用户实际需求，对房源行业产生积极影响。


第 1 页 

1 绪论

1.1背景和意义

在我国技术持续发展的同时，电脑的发展也日渐成熟，世人对它的依赖性也变得越来越高，人们开始借助电脑来对房源销售、签约等进行管理。从世界上第一台电脑出现至今，其发展已经完全超出了人们的想象。它在带给人们便利的同时，也使人们的生活发生了极大变化，如今电脑已完全融入了人们生活的各个方面，也因此出现了很多的管理系统。人类社会渐渐开始进入信息时代，网络成了当下媒体传播的重要场所。在互联网飞速发展的潮流中，房产销售平台为相关人员提供了高效服务。

从传统房源签约的操作流程看来，存在不利于管理，偏差大，难以查询的情况，只要数据量大，以人工方式进行管理的话就非常难维持。在信息技术的运用大量推广的同时，人们开始运用信息技术管理来不断取缔人工管理方式，运用计算机软件来对房源信息进行管理，其优势是便于查询，信息精准度高，同时提高了工作效率。此次系统开发针对的是对房东房源签约的管理，并经需求分析后展开功能方面的设计。

现如今，人们日渐关注互联网的发展，同时人们也开始大量使用自动管理技术来对各行各业进行管理。早前的人工管理方式所存在的缺陷开始不断显现，例如管理成效差，处理信息的速度缓慢，工作量大，处理信息的精准度不高等。基于此，怎样扭转此种情况，尽可能的使以上问题得到解决，切实解放劳动力，其关键在于提高处理信息过程中的准确率。经济因时代的发展而迅速发展，当下的市场更是变幻莫测，在此种背景之下，如今的房产销售平台需要面对很多的挑战，与此同时，它还应具备较强的扩展性。

信息化程度日益普及，日常遇到的难题，第一反应就是上网搜，网上找房源是当前社会发展趋势，只需要上网就可以搜索到对应的签约信息，寻找在线房源，双方还可以进行沟通。这样每个人都可以自主选择，有较好的灵活性和机动性，免除了不必要的程序和手续。

计算机技术已经渗透到人们生活的方方面面，使得大家工作、学习以及生活方式都发生了翻天覆地的改变，从最初的必须面对面求租，到通过互联网观看房源，甚至通过手机、iPad进行互动，突破了房源签约资源受时间、空间、地域的限制，随时随地都可以通过网络获得自己想要的房源信息，帮助求租者提高查找信息的效率。

1.2国内外现状

在国外，计算机普及早，信息化程度高，房产销售平台管理规范。在美国，房产销售平台是基于十年行业开发经验和技术积累，融合SOA架构的先进理念，以服务为向导，数据资源共享，为房东、人员、管理者提供高效、便捷的一站式服务。

在国内，泊寓都是已经成功过的，所以他们的可取之处并不少。自如推出“亿元补贴”，堪称史上最大优惠。覆盖北京等地区指定房源最高能免两个月的租金，是真实的优惠。自如的这个操作将利于提振市场消费活力，助推下半年房源签约市场的经济增长。蛋壳公寓是以数据驱动为核心,提供高品质租住生活的资产管理和居住服务平台,产品形态涵盖合租公寓、整租公寓等,满足都市年轻白领多元化的居住需求。

现在没有房子就相当于没有家，许多漂泊异乡和刚踏入社会的人们居住是个很大的问题。所以目前签约是很普遍的现状。但是有些房租价格高昂，还有中介费用，价格令许多刚毕业的大学生和其他的签约的打会员望而兴叹，为了避免高昂的中介费，可谓煞费苦心。而目前市场上关于签约系统大多是中介，微信小程序的签约系统也是一样，不过也有些房东直租小程序，例如房东直租、果果直租、暖房直租以及同城直租等小程序都还在萌芽试运行阶段。它们有的功效不全，有的使用不便，有的无法使用。

计算机的应用变得十分广泛，同时也应用在房源方面，房产销售平台就是一种基于互联网技术诞生的房源签约系统。房产销售平台设计符合操作简便、易操作不繁杂。本系统采用Spring cloud技术开发本网站，运用css+JavaScript进行布局，MYSQL数据库进行数据管理。在信息的管理方面，有着独特的设计方法，实现了房产销售平台操作的智能化、科学化。

1.3相关技术概述
### 1.3.1 JAVA技术
JAVA技术是目前开发管理系统应用最广泛的语言之一，在JAVA技术框架下，允许使用一致性的模型，重复使用相同的组件，采用多种方法进行事务控制。

本系统开发工具选择IDEA，是企业级的开发平台，通过对Eclipse的扩展，完善成为功能齐全的编译工具。IDEA完成JAVA代码编写后，可以发布代码，部署环境。程序员在IDEA的可视化开发环境中，对代码进行调试，提高开发效率。IDEA功能强大，对各种源码提供支持，可以编译Servlet、SSH、SSM、EJB3、JDBC等工具。

在结构上，IDEA具有多个功能特性，可以进行JavaEE、WEB、EJB、项目部署、数据库操作等。IDEA的快捷键很丰富，如进行快速修复、定位在某行、删除当前行、切换到下一个、上一个、格式化当前代码。IDEA引入了全新的JavaScript编辑器，提供代码高亮支持。增加了Struts2图形编辑器、通过授权获取用户的工作台、共享工作台配置、也支持更多的程序服务器。

通过IDEA新建项目，创建和mysql数据库的链接，在Openconnection中，输入数据库的密码，数据库链接成功后，选择项目的框架形式，完成项目目录的创建。运行IDEA时，可以通过配置tomcat服务器，也可以使用IDEA自带的服务器进行运行。
### 1.3.2 编程环境
本房产销售平台使用JAVA语言开发，IDEA开发平台。在开发房产销售平台前，需要安装IDEA工具，和Tomcat服务器。对于计算机硬件的要求一般，下面整理了系统需要的软硬件条件，见表1.1所示。

表1.1 房产销售平台软硬件条件表

|房产销售平台服务器配置|
| - |
|房产销售平台主机CPU|双核2.0以上|
|房产销售平台主机内存|2G，4G以上更好|
|房产销售平台主机硬盘|100G以上|
|房产销售平台服务器软件配置|
|房产销售平台系统|Windows 10 /Windows7即可|
|房产销售平台开发平台|IDEA |
|房产销售平台运行服务器|Tomcat7.0或者以上|
|房产销售平台运行数据库|MYSQL5.1或者以上|
|房产销售平台语言|JAVA语言|
|房产销售平台浏览器|360、谷歌、遨游等|

### 1.3.3 Mysql数据库
MYSQL是开源的关系型数据库，使用SQL语言进行管理。因为MYSQL是开放的，所以任何人都可以根据需要进行更改。MYSQL的速度快，数据存储完全，得到众多用户的肯定。

掌握MYSQL数据库，首先需要对结构化查询语言比较了解，SQL语言的语法简单，功能强大。通过SQL语言进行数据库的创建，有了数据库后，进行数据库表的设计，并设置数据库表的主外键，索引，主键等。最后通过SQL语言进行数据的增删改查。SQL语言应用非常广泛，目前大多数关系型数据库都支持SQL语言。SQL语言包括数据查询语言、数据操纵语言、数据定义语言、数据库中语言。

使用SQL语言具有多个好处，首先SQL语言针对的是非过程处理，操纵的是集合，而不是某一个数据。输入的是集合对象，输出的也是集合，并可以把一个处理结果作为另外一个语句的输入对象。SQL语句关注的是结果的处理，而不是数据的存储方法。其次，SQL语言被多种用户身份对象所掌握，如程序员、数据库管理者、数据仓库分析员等。通过SQL命令进行数据的操作和查询。最后，SQL语言是通用的命令，程序员可以方便的将程序支持的数据库更换为其它关系型数据库，而不需要修改太多的代码。
### 1.3.4 Spring cloud技术
Spring cloud的产生完全是为了解决企业公司级的开发所产生的一系列复杂问题而创建。通俗的讲，Spring就是一个轻量级的IoC（控制反转）和AOP（面向切面）的容器。

Spring cloud它是属于Spring Framework的一个后继，是基于Java的实现了Web MVC设计模式的请求驱动类型的轻量级Web框架。Spring cloud框架是基于传统MVC架构模式，我们所讲的基于系统请求的驱动即指请求-响应模型，并且分离了分派器、控制器、模型对象以及处理程序对象的角色，这种概念上所讲的分离更方便的让这些去进行定制化操作。框架的目的就是帮助开发人员去简化开发。

Spring cloud框架是一个Java的数据持久层框架。Spring cloud把几乎所有的JDBC代码和参数的手动设置还有resultSet的检索都消除了，这个框架它所提供的持久层的技术包括SQLMaps和Data Access Objects（DAO）。MyBatis框架它使用了比较简单的XML或者是注解方式用来配置和原始的一个映射，将接口和Java的POJOs（Plain Old Java Objects，普通的 Java对象）来专门映射成数据库中的一条条记录。Spring cloud就是一个用来帮助开发人员管理数据的增删改查的框架，该框架支持定制化 SQL。



2 系统分析

2.1系统需求分析

对房产销售平台的分析，分析总结出系统包括三种类型的用户，一个是客户，还有一个是后台的管理员用户和房产中介。后台管理员在这个系统中具备最高的管理权限，他主要实现对房产销售平台的后台数据信息的控制和管理。客户在本网站中的角色就是需要查看信息，获取推荐房源等。

房产销售平台是一个典型的数据库应用程序，其需求包括系统管理：对系统信息进行管理，维护个人信息，用户登录等。房源信息管理：包括房源信息检索和浏览房源信息功能。在线签约管理：包括新在线签约信息、所有的账单查询和在线签约信息。看房管理：客户在线提出看房申请，管理员管理申请。还有留言管理、系统信息等。

2.2系统使用者

房产销售平台使用者包括系统管理员用户、客户管理、中介管理。其中管理员房源信息，而客户可以查看房源，在线预约和签约。

系统使用者之间的关系图如2.2所示：

![](/md/blog.003.png)

图 2.2 系统使用者关系

系统管理者控制系统的后台信息以及对基本信息进行管理。

2.3系统用例分析

房产销售平台用户包括客户、中介和系统管理员。系统管理员是系统预设的用户，而客户是管理员添加的用户。系统管理员通过后台登陆的方式管理系统信息。

用户管理用例图如图2.3所示。

![](/md/blog.004.png)

图2.3用户管理用例图

用户管理用例规约如表2.1所示。

表2.1 用户管理用例规约

|编号|Fangwu001|
| - | - |
|名称|房产销售平台用户管理|
|描述|对用户管理。包括用户的录入、用户的查询、用户的修改、用户的删除以及用户相关联的其它操作。|
|前置事件|服务器运行、网络正常|
|后置事件|在界面进行相关操作后，数据库信息发生变化。|
|<p></p><p>主</p><p>事</p><p>件</p><p>流</p><p></p><p></p><p></p><p></p>|用户输入|系统操作|
||1、在用户信息录入页面，输入所有的用户信息，并保存。在用户查询页面，查询所有的用户信息。在用户修改页面，更新内容并保存。用户的列表中，点击删除，根据提示进行删除操作。|<p>2、在用户录入页面，通过客户端验证方法，验证输入是否正确，并到数据库验证是否重复录入，验证失败，执行子事件流a1步骤。通过验证，保存用户记录到数据库。</p><p>3、用户信息查询页面中，加载数据库的用户信息。</p><p>4、在用户修改页面，通过客户端验证方法，验证输入是否正确，验证失败，执行子事件流a1步骤。通过验证，更新用户记录到数据库。</p><p>5、删除用户操作，并更新数据库记录，遇到有外键关联记录，执行子事件流a2步骤。</p><p></p>|
|子事件流|<p>a1. 提示用户重新输入用户的信息，注意特殊字符和不能为空的情况。</p><p>a2. 提示先删除关联的记录。</p>|
|异常情况|跳转到主面。|

用户登录后进行房源信息管理、签约管理、看房管理，其中各个功能实现流程类似，下面对房源信息的实现进行说明。房源信息管理用例图如图2.4所示。

![](/md/blog.005.png)

图2.4房源信息管理用例图

其中房源信息管理用例规约如表2.2所示。

表2-2房源用例规约

|编号|Fangwu002|
| - | - |
|名称|房产销售平台房屋管理|
|描述|对房屋管理。包括房屋的录入、房屋的查询、房屋的修改、房屋的删除以及房屋相关联的其它操作。|
|前置事件|服务器运行、网络正常|
|后置事件|在界面进行相关操作后，数据库信息发生变化。|
|<p></p><p>主</p><p>事</p><p>件</p><p>流</p><p></p><p></p><p></p><p></p>|用户输入|系统操作|
||1、在房屋信息录入页面，输入所有的房屋信息，并保存。在房屋查询页面，查询所有的房屋信息。在房屋修改页面，更新内容并保存。房屋的列表中，点击删除，根据提示进行删除操作。|<p>2、在房屋录入页面，通过客户端验证方法，验证输入是否正确，并到数据库验证是否重复录入，验证失败，执行子事件流a1步骤。通过验证，保存房屋记录到数据库。</p><p>3、房屋信息查询页面中，加载数据库的房屋信息。</p><p>4、在房屋修改页面，通过客户端验证方法，验证输入是否正确，验证失败，执行子事件流a1步骤。通过验证，更新房屋记录到数据库。</p><p>5、删除房屋操作，并更新数据库记录，遇到有外键关联记录，执行子事件流a2步骤。</p><p></p>|
|子事件流|<p>a1. 提示用户重新输入房屋的信息，注意特殊字符和不能为空的情况。</p><p>a2. 提示先删除关联的记录。</p>|
|异常情况|跳转到主面。|

其中签约管理用例规约如表2.3所示。

表2.3签约信息管理用例规约

|编号|Fangwu003|
| - | - |
|名称|房产销售平台签约管理|
|描述|对签约管理。包括签约的录入、签约的查询、签约的修改、签约的删除以及签约相关联的其它操作。|
|前置事件|服务器运行、网络正常|
|后置事件|在界面进行相关操作后，数据库信息发生变化。|
|<p></p><p>主</p><p>事</p><p>件</p><p>流</p><p></p><p></p><p></p><p></p>|用户输入|系统操作|
||1、在签约信息录入页面，输入所有的签约信息，并保存。在签约查询页面，查询所有的签约信息。在签约修改页面，更新内容并保存。签约的列表中，点击删除，根据提示进行删除操作。|<p>2、在签约录入页面，通过客户端验证方法，验证输入是否正确，并到数据库验证是否重复录入，验证失败，执行子事件流a1步骤。通过验证，保存签约记录到数据库。</p><p>3、签约信息查询页面中，加载数据库的签约信息。</p><p>4、在签约修改页面，通过客户端验证方法，验证输入是否正确，验证失败，执行子事件流a1步骤。通过验证，更新签约记录到数据库。</p><p>5、删除签约操作，并更新数据库记录，遇到有外键关联记录，执行子事件流a2步骤。</p><p></p>|
|子事件流|<p>a1. 提示用户重新输入签约的信息，注意特殊字符和不能为空的情况。</p><p>a2. 提示先删除关联的记录。</p>|
|异常情况|跳转到主面。|

2.4可行性分析

在开发房产销售平台时，需要对系统可行性进行分析。本系统可行性包括：

本房产销售平台使用web开发模式，系统操作流程使用市面上常见的软件布局，用户通过点击菜单操作后，系统自动反馈结果。另外，系统通过不同用户的权限进行控制，用户登录后，展现了可以操作的功能模块，不存在误操作的风险。因此，只要具有一般经验的用户就可以使用，在操作上具有可行性。

开发房产销售平台需要对经济可行性进行调研，首先说明的是系统投入情况。建设房产销售平台系统成本主要在服务器硬件和软件开发费用较少，而房产销售平台投入使用后，可以降低工作量；提高管理员的工作积极性；节约推广成本。总体来说，降低的用人成本已经高于开发系统的费用，对签约市场来说，无论从眼前还是可持续发来说，都具有很大优势。 

房产销售平台选择的技术都是目前成熟的语言和数据库，并使用MVC架构开发的web系统，对于初学者都可以完成。市场上也有许多小程序技术开发的成功案例，证明开发语言具有可行性。而mysql数据库作为关系型数据库比较经典的数据库，更是占据很大比例，所以，开发本系统，在选择的技术上，具有可行性。



3 系统设计
## 3.1系统体系结构
房产销售平台使用Spring cloud三层架构开发。分别对应着视图层、控制器和模型层。房产销售平台的视图层使用Jsp和HTML开发，后台使用Java的控件显示数据。在分层的开发模式中，视图层可以和控制层分开开发，通过接口实现相互调用。房产销售平台的控制器层主要来获取视图层的响应，并可以单独实现业务逻辑层进行调用，也可以在业务逻辑层中直接实现相关逻辑进行数据处理，判断结果返回到界面层。模型层是比较简单的层次，和数据库表进行对应，一个数据库表往往对应一个实体类，创建模型层后，编程人员不需要关注数据库，通过模型即可明确对应的字段信息。
### 3.1.1 界面层设计
系统界面层是与用户交互的界面，界面层反映出系统的功能。通过制定规则，可以将界面层和逻辑层分离，单独进行开发。界面层要求简单大方，功能整洁，便于操作。本房产销售平台通过H5技术进行布局，使用java标签获取业务逻辑层的数据进行显示。收集数据是使用form表单进行控制，数据验证使用jquery技术。所有的界面层设计规范合理，各种图片，界面，js和css样式文件分别管理。
### 3.1.2 数据库层设计
数据层通过实体表现，一个数据库表对应一个实体类，一个字段对应一个属性。字段类型对应属性类型，但是实体属性包括但是不限于字段个数。其中视图也对应实体。其中属性名称一般采用大写的格式。

其中管理数据库链接操作的类单独出来，数据库连接串放置配置文件中，方便管理，本文使用mysql数据库，对应的是mysql驱动包。数据库操作类管理数据库访问接口、对数据库进行单表的增删改查操作。
### 3.1.3 业务逻辑层设计
业务逻辑层是系统核心层次，对数据处理进行控制，接收到界面层请求后，对具体的业务进行管理，把数据通过数据库层进行操作后返回给界面。业务逻辑层先完成系统通用的逻辑操作，如用户注册、用户登录、用户权限判断、数据库操作等。然后分析系统业务规则，对系统核心业务进行编写。

3.2系统功能设计

基于Web的房产销售平台是一个交互式查询系统，在明确了系统目标与数据库结构的前提下，设计出该系统的主要功能：系统登录、数据输入与修改、数据综合查询、数据统计等。 系统的整体主要模块图如图3-1所示：

基于Spring cloud房产销售平台

权限管理

用户管理

新闻管理

看房申请

在线签约

留言管理

房源管理

后台登录

前台登录

中介管理

客户管理

添加维护新闻

客户申请

理员处理

确定租赁

签约管理

在线留言

留言回复

房源管理

![](/md/blog.006.png)

![](/md/blog.007.png)	图3-1系统整体模块图
### 3.2.1 管理员功能
其中管理员规划功能模块如下：

1、管理员管理：添加新的管理员，管理历史管理员信息。

2、系统管理：对系统信息进行管理，维护个人信息，用户登录等。

3、房源信息管理：包括房源信息检索和浏览房源信息功能。

4、签约管理：包括新增租金信息、所有的账单查询和已退租信息。

5、看房管理：客户在线提出看房申请，管理员管理申请，处理退租申请信息。

6、留言管理：对客户提出的留言信息进行管理。包括留言删除和留言回复等。

7、新闻公告管理：录入新的公告信息，修改信息和删除公告信息。
### 3.2.2 客户功能
其中客户角色功能模块如下：

1）客户使用注册的用户名和密码进行登录。

2）客户维护个人信息。

3）查看房源列表，在线申请看房，在线签约，在线留言，查看新闻信息等。

3.3 系统流程设计

管理员管理房产销售平台房产信息，会员通过前台搜索信息，然后点击房产，查看房产信息。对感兴趣的房产进行看房申请，管理员管理签约。系统流程图如图3-2所示。

添加房源

房源列表

申请看房

房源信息

处理房源

签约

![](/md/blog.008.png)

图3-2 房产销售平台流程图

其中管理员登录部分的登录验证流程图为：

用户登录

验证

进入后台的主界面，显示基本信息

验证不通过，给出错误信息，并返回登录界面

![](/md/blog.009.png)

图3-3 登录验证流程图

管理员登录后，对房源信息进行管理，添加新的信息后，保存到数据库中，通过查询方法，查询数据库记录，然后删除或者修改信息。管理员管理信息流程图：

管理员登陆

添加

信息

新的信息

添加成功

信息需要修改

修改

信息

修改成功

删除

信息

信息过期或有误

删除成功

系统数据库

更新数据库

更新数据库

更新数据库
![](/md/blog.010.png)

图3-4管理员管理信息流程图

3.4 数据库设计原则

数据库设计是管理系统必不可少的步骤，所有的数据都可以组成一个数据库存储起来。数据的关系组成了表与表之间的关系。数据库的设计关系到房产销售平台的成败，良好的设计，可以提升系统的性能。

从数据库的设计中，对数据库字段进行关联，汇集为网状形式，数据库的实体对应多个属性，属性是根据现实的实体对象确定，比如人员的属性必然包括姓名、性别、电话等，但是也存在特殊情况，管理员属于一种类型的人员，但是其属性可以仅仅包括用户名和密码即可。另外，属性的关联可以抽象出为外键联系，这种设计要特别注意，存在外键的实体，属性设置上不能重复。还有诸如属性的类型、索引设置、为空等的设计。

3.5 系统数据库E-R图

本系统从整体上分为签约信息、客户信息和房源信息三大部分。系统数据库设计E-R图，如图4-1所示。


![](/md/blog.011.png)

图4-1房源实体



![](/md/blog.012.png)

图4-2客户实体及属性

![](/md/blog.013.png)

图4-3看房申请实体及属性

![](/md/blog.014.png)

图4-4签约信息实体及属性

3.6 数据库表的设计

根据本系统实现的功能，房产销售平台主要的数据表信息如下所示：

1. 表: 房产签约信息表 

|ID|名称|类型|是否主键|空|解释|
| - | - | - | - | - | - |
|1|id|int|是|不能||
|2|fangjian|varchar|不是主键|可以||
|3|kehu|varchar|不是主键|可以||
|4|jinge|int|不是主键|可以||
|5|shijian|date|不是主键|可以||
|6|yuangong|varchar|不是主键|可以||
|7|hetongmingcheng|varchar|不是主键|可以||
|8|zongjinge|int|不是主键|可以||
|9|hetongneirong|text|不是主键|可以||


1. 表: 客户信息表 

|ID|名称|类型|是否主键|空|解释|
| - | - | - | - | - | - |
|1|id|int|是|不能||
|2|name|varchar|不是主键|可以||
|3|xingbie|varchar|不是主键|可以||
|4|nianling|varchar|不是主键|可以||
|5|dianhua|varchar|不是主键|可以||
|6|dizhi|varchar|不是主键|可以||
|7|youxiang|varchar|不是主键|可以||
|8|quyu|varchar|不是主键|可以||
|9|xihuangequ|varchar|不是主键|可以||
|10|yhm|varchar|不是主键|可以||
|11|mm|varchar|不是主键|可以||


1. 表: 房产登记信息表 

|ID|名称|类型|是否主键|空|解释|
| - | - | - | - | - | - |
|1|id|int|是|不能||
|2|xiaoqumingcheng|varchar|不是主键|可以||
|3|louhao|varchar|不是主键|可以||
|4|duanyuan|varchar|不是主键|可以||
|5|fanghao|varchar|不是主键|可以||
|6|mianji|int|不是主键|可以||
|7|geju|varchar|不是主键|可以||
|8|gongtan|varchar|不是主键|可以||
|9|wuyefei|varchar|不是主键|可以||
|10|jiage|varchar|不是主键|可以||
|11|shuoming|text|不是主键|可以||
|12|quyu|varchar|不是主键|可以||
|13|louceng|varchar|不是主键|可以||
|14|dianti|varchar|不是主键|可以||
|15|chewei|varchar|不是主键|可以||
|16|zushou|varchar|不是主键|可以||
|17|zt|varchar|不是主键|可以||


1. 表: 看房信息表 

|ID|名称|类型|是否主键|空|解释|
| - | - | - | - | - | - |
|1|id|int|是|不能||
|2|fangjian|varchar|不是主键|可以||
|3|kehu|varchar|不是主键|可以||
|4|shijian|date|不是主键|可以||


1. 表: 管理员信息表 

|ID|名称|类型|是否主键|空|解释|
| - | - | - | - | - | - |
|1|userId|int|是|不能||
|2|userName|varchar|不是主键|可以||
|3|userPw|varchar|不是主键|可以||


1. 表: 留言信息表 

|ID|名称|类型|是否主键|空|解释|
| - | - | - | - | - | - |
|1|Id|int|是|不能||
|2|Title|varchar|不是主键|可以||
|3|Con|varchar|不是主键|可以||
|4|UserID|varchar|不是主键|可以||
|5|Riqi|varchar|不是主键|可以||
|6|Huifu|varchar|不是主键|可以||


1. 表: 新闻公告信息表 

|ID|名称|类型|是否主键|空|解释|
| - | - | - | - | - | - |
|1|Id|int|是|不能||
|2|Title|varchar|不是主键|可以||
|3|Con|varchar|不是主键|可以||




4 系统实现

4.1登陆模块的实现

使用脚本把数据库导入到mysql中，配置tomcat服务器，运行程序。其中用户登录的界面如下所示。登录界面如图4-1所示：

![](/md/blog.015.png)

图4-1登录窗口界面

管理员登录中，通过点击button按钮，调用check1方法，通过IF判断用户名和密码是否输入，后调用loginService.login的方法，进行数据库查询，返回是或者否。

输入信息后，选择角色类型，进行登录，登录验证需要经过两个步骤。第一个步骤是客户端验证，通过js实现必填项校验，一般情况，js也可以校验是否为数字，字符串大小等。通过验证后提交到服务器端进行验证，服务器验证是查询数据库的记录，得到数据后，返回验证通过信息。

用户登录成功后，第一步进行用户角色判断，不同的用户角色权限不一样。就需要根据登录信息，判断用户具有什么权限，然后显示对应的操作菜单，系统主界面样式是统一的，用户操作菜单根据用户权限来显示。主界面一般包括logo图标、菜单和主操作内容页面。

4.2房源信息管理模块实现

房源信息管理模块由如下几个部分组成，房源信息显示，房源信息删除，房源信息更改和房源信息查询，其主要功能是对系统房源信息进行管理。

界面设计如下图4-2所示：

![](/md/blog.016.png)

图4-2房源信息管理窗口界面

点击左边菜单树下房源管理中的所有房源，中间区域就会显示出所有的房源信息列表，点击编辑操作就可以跳转到编辑房源页面，点击删除可以对选择的行进行删除。

其中房源添加中，通过管理类，实现了业务逻辑层的数据传递方法。实现通过房源添加页面，通过配置文件，找到对应的方法，获取用户输入的房源信息，构造sql语句，调用业务层的方法，实现房源的数据库保存操作，并返回保存成功信息，即房源录入成功。

在房源删除中，点击需要删除的房源行，调用逻辑类的删除方法；在该方法中，先通过要删除的ID对象，查找房源行的模型，持久层通过连接数据库，调用逻辑类的删除方法，通过数据库删除方法，把数据库中的房源对象进行删除。完成删除操作后，返回房源的页面。

点击需要修改的房源行，调用逻辑类的修改；在该方法中，先通过要修改的ID对象，查找房源行的模型，持久层通过连接数据库，调用查询方法，返回房源的模型，使对象赋值给模型驱动的房源绑定到修改页面。用户完成修改后，点击保存，调用调用逻辑类的方法，持久层把对象返回到方法中，然后调用逻辑类的修改方法，通过数据库的修改方法，把数据库中的房源对象进行修改。完成修改操作后，返回房源的刷新页面。

在查询页面，管理员通过Web页面层URL访问链接进入到房源主页；当管理员点击所有房源时，跳转到房源管理jsp页面，通过配置文件，找到对应的查询方法，数据库层方法完成查询处理。调用业务层的查询，调用房源类中的对象，返回整数，即所有房源个数。业务层调用持久层的方法，返回房源的模型集合，使用<>()返回结果到业务层，业务层把对象保存到值栈中，返回到房源集合循环中，后台主页数据显示区的通过循环把当前页的房源数据从值栈中取出来显示在页面上。

4.3签约信息管理模块实现

签约信息管理模块由如下几个部分组成，签约信息显示，签约信息删除，签约信息更改和签约信息查询，其主要功能是对系统签约信息进行管理。

界面设计如下图4-4所示：

![](/md/blog.017.png)

图4-4签约信息管理窗口界面

点击左边菜单树下签约管理中的所有签约，中间区域就会显示出所有的签约信息列表，点击编辑操作就可以跳转到编辑签约页面，点击删除可以对选择的行进行删除。

其中签约添加中，通过管理类，实现了业务逻辑层的数据传递方法。实现通过签约添加页面，通过配置文件，找到对应的方法，获取用户输入的签约信息，构造sql语句，调用业务层的方法，实现签约的数据库保存操作，并返回保存成功信息，即签约录入成功。

在签约删除中，点击需要删除的签约行，调用逻辑类的删除方法；在该方法中，先通过要删除的ID对象，查找签约行的模型，持久层通过连接数据库，调用逻辑类的删除方法，通过数据库删除方法，把数据库中的签约对象进行删除。完成删除操作后，返回签约的页面。

点击需要修改的签约行，调用逻辑类的修改；在该方法中，先通过要修改的ID对象，查找签约行的模型，持久层通过连接数据库，调用查询方法，返回签约的模型，使对象赋值给模型驱动的签约绑定到修改页面。用户完成修改后，点击保存，调用调用逻辑类的方法，持久层把对象返回到方法中，然后调用逻辑类的修改方法，通过数据库的修改方法，把数据库中的签约对象进行修改。完成修改操作后，返回签约的刷新页面。

在查询页面，管理员通过Web页面层URL访问链接进入到签约主页；当管理员点击所有签约时，跳转到签约管理jsp页面，通过配置文件，找到对应的查询方法，数据库层方法完成查询处理。调用业务层的查询，调用签约类中的对象，返回整数，即所有签约个数。业务层调用持久层的方法，返回签约的模型集合，使用<>()返回结果到业务层，业务层把对象保存到值栈中，返回到签约集合循环中，后台主页数据显示区的通过循环把当前页的签约数据从值栈中取出来显示在页面上。

4.4申请看房管理实现

客户提出申请看房，管理员管理申请。看房后，可以进行同意签约或者拒绝签约操作。界面设计如下图4-5所示：

![](/md/blog.018.png)

图4-5看房申请界面

`	`在查询页面，管理员通过Web页面层URL访问链接进入到看房申请主页；当管理员点击所有看房申请时，Web页面端组件会调用处理查询所有看房申请的逻辑类中的方法；查询所有看房申请；调用逻辑类中的查找方法，该类调用数据库操作，参数为查询所有看房申请个数的SQL语句，返回一个整数集合，然后获取它的第一个元素，即所有看房申请个数，并把它转换成整数类型；把所有看房申请个数返回给业务层，业务层接收到该数值，把它赋值给总记录数，通过每页显示的记录数计算出总页数；业务层接收到该集合，并赋值给每页显示的数据集合，把集合返回给页面；后台主页数据显示区的通过循环把当前页的看房申请数据从值栈中取出来显示在页面上。

4.5平台前台首页实现

前台首页包括房源信息、房产资讯、留言反馈、个人中心等。界面设计如下图4-6所示：

![](/md/blog.019.png)

图4-6首页界面

通过Web页面层URL访问链接进入到房源主页；当点击所有房源时，Web页面端组件会调用处理查询所有房源的逻辑类中的方法；查询所有房源；调用逻辑类中的查找方法，该类调用数据库操作，参数为查询所有房源个数的SQL语句，返回一个整数集合，然后获取它的第一个元素，即所有房源个数，并把它转换成整数类型；把所有房源个数返回给业务层，业务层接收到该数值，把它赋值给总记录数，通过每页显示的记录数计算出总页数；业务层接收到该集合，并赋值给每页显示的数据集合，把集合返回给页面；后台主页数据显示区的通过循环把当前页的房源数据从值栈中取出来显示在页面上。

4.6在线留言模块实现

在线留言需要用户登录后进行发布信息，没有登录的用户不能留言。界面设计如下图4-7所示：

![](/md/blog.020.png)

图4-7在线留言界面

用户点击留言的添加，跳转到留言页面，当用户完成保存后，通过配置文件，找到对应的方法，完成保存操作。调用业务层的保存方法，参数为模型驱动的评论对象，保存方法中，调用逻辑类,通过数据库逻辑类的保存对象，将评论模型序列化到数据库表中。逻辑类完成操作后，返回留言列表页面。

在查询页面，通过Web页面层URL访问链接进入到留言主页；当点击所有留言时，Web页面端组件会调用处理查询所有留言的逻辑类中的方法；查询所有留言；调用逻辑类中的查找方法，该类调用数据库操作，参数为查询所有留言个数的SQL语句，返回一个整数集合，然后获取它的第一个元素，即所有留言个数，并把它转换成整数类型；把所有留言个数返回给业务层，业务层接收到该数值，把它赋值给总记录数，通过每页显示的记录数计算出总页数；业务层接收到该集合，并赋值给每页显示的数据集合，把集合返回给页面；后台主页数据显示区的通过循环把当前页的留言数据从值栈中取出来显示在页面上。
**


总 结

计算机科学的发展，应用到社会各个领域，作用也愈发重要。当前社会，竞争日益激烈，只有使用管理系统才能提高管理效率。目前，我国网络环境和市场经济发展良好，各行业分布广泛，工作精细化程度高。对于各项工作流程的管理更加的重视，使用管理系统对企业进行流程化管理，控制业务，提高工作效率，对流程化进行统一控制，方便用户快速的解决相关事务。

本文设计研究了房产销售平台的巨大发展前景，对现有的房产销售平台运行现状进行了总结和归纳并研发设计了一款集成了JAVA技术和数据库处理分析技术的房产销售平台。因此，该系统在大幅度提升房源签约管理提出了一定的看法和意见。同时，本研究设计还对房产销售平台的后台处理系统进行了升级和改良，起到提升系统稳定性和运行有效性的作用。

本研究设计的房产销售平台达到了研究设计预设的目标。但由于系统整体运行的时期较短，同时本人还相对缺失一定的实践基础以及受到了时间和财力的限制，本研究设计目前还存在以下问题：

（1）本研究设计的房产销售平台在使用权限上受到了一定的限制，目前只有运营商内部以及一些线下的服务网点可以使用此套系统。

（2）本文实施的角色权限管理操作在层级上有所划分和限制，就目前的设计水平而言只能设置为部门级别。因此，未来相关研究可以引入层次化角色控制机制从而实现灵活管理的目标。



参考文献

[1]	侯宇.基于web的商业地产管理系统的设计与实现[D].电子科技大学,2016.

[2]	王颖.房源中介一体化管理信息系统的研究与实现[D].上海交通大学,2015.

[3]	梅承茏.房源中介管理系统的研究与分析[D].云南大学,2016.

[4]	James R.Frew.Multiple listing service participation in the real estate brokerage industry:Cooperation or competition[J].Journal of Urban Economics,May1987,21(3):27-286.

[5]	陆克华,倪吉信.美国房地产经纪人管理制度简介[J].中国房源信息,2001(12):43-45.

[6]	AI Nicolaou,DH Mcknight.Perceived Information Quality in Data Exchanges Effects on Risk,Trust,and Intention to Use[J].Information Systems Research,2006,17(4):332-351.

[7]	赵军,李佳,刘泽俊.房源中介管理系统[J].软件工程, 2017,20(2):44-46.

[8]	段江玲,王峰.房源网站搜索可用性研究--以搜房网为例[J].艺术与设计(理论),2011,2(11): 110-112.

[9]	徐洁云.移动中的安居客[J].21世纪商业评论,2013年06期:60-62.

[10]	余雄，郭龙.高校实用技术BBS论坛的设计与应用[J].科研,2016(4):60-60.

[11]	程仲涛,施冬.基于百度地图API的房源信息查询平台的设计与实现[J].数字技术与应用,2015(03):144-145.

[12]	潘卫艳,曾熙.曾熙:房多多在提高行业的效率[J].中国房地产业,2015(05):74-75.

[13]	林倩.为行业而生--链家地产的成长之路[C].中国房地产估价师与房地产经纪人学会（China Institute of Real Estate Appraisers and Agents）.中国房地产估价与经纪2014年第4期（总第107期）. [14]	B.P.Hayes,S.Thakur,J.G.Breslin. Co-simulation of electricity distribution networks and peer to peer energy trading platforms[J].International Journal of Energy Systems,2020,115.

[15]	奉国和,梁晓婷.协同过滤推荐研究综述[J].图书情报工作,2011,55(16):126-130.

[16]	余强.基于B/S的房源中介系统的设计与实现[D].电子科技大学,2014.






致  谢

首先要感谢我的指导老师。此次毕业设计从选题到资料的收集，再到具体设计和论文的完成都是在他的亲切关怀和悉心指导下完成的。他在我完成整个论文作品过程中，起到了不可替代的作用，对我在开发过程中遇到的困难给予及时的指导和帮助，使我少走了许多的弯路，非常的感谢！

多谢所有帮助过我的同学、朋友和老师，感谢他们热心的帮助！














