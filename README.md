<p align="center">
  <a href="http://landing.ant.design">
    <img width="150px" height="150px" src="https://gw.alipayobjects.com/zos/rmsportal/hSYPdZJwZeXAgfkktcEu.svg"/>
  </a>
</p>
<h1 align="center">LUNA</h1>

<div align="center">
  

An Open Clinical Information System Development Platform - Especially For Specialist EHR

一款开放的医疗信息系统开发平台，尤其针对专科电子病历的开发
</div>

<div align="center"> 简体中文 | <a href="./README-zh_CN.md">English(not support yet)</a></div>

## What is Luna?

Luna is an openEHR based CIS(Clinical Information System) development platform.
<p align="center">
<img width="780px" height="450px" src="./luna_arc.png"/>
</p>
一、这里重点提到了openEHR，openEHR是一个致力于电子病历相关系统的国际组织；是一种muti-level,single source modelling的面向服务的软件架构；是一系列分层模型的规范；对我而言他更是一种关于电子病历的方法论：基于几十年的电子病历研发、实施经验的积累和对临床医学、电子病历发展的理解，提出了如何能让电子病历类系统成功实施-符合临床需求指导临床决策-的方向和方法（了解更多，请见reference中的链接）。Luna本质是由临床的专家通过CDML（Clinical Domain Model Language）对医疗信息系统的需求建模，系统后台根据CDM自动生成数据存储层、检索层、展示层及基础的安全等模块和组件，形成一个完整的医疗业务系统。</br>
二、说到“平台”,这个词已是在国内互联网圈中“普适”的标签。我认为平台本质是服务B端，再通过B端服务C端。不是任何一款多用户应用的软件产品都能称为平台，关键在于能为B端提供什么资源？怎样提供？这些资源是否有利于更好的服务共有的C端？Luna期望服务于医疗信息化服务商、各级医疗机构、区域卫计委（局），最终通过EHR服务医疗参与者。  
</br>
三.Luna目前仍存在于理想层面，至今甚至没有一行代码。在先辈的成果的基础上从设计每一个模块每一个组件开始积累跬步，希望Luna可以帮助国内医疗信息化的发展。 
</br>
四.Luna缘起于探月和王者，想想目前lian-med着眼于妇幼、产科领域，月亮的阴晴圆缺与妇也很配。Luna构思于在19年1月初，当时的大事件就是嫦娥工程；Luna也是我钟爱的一个英雄。
</br>
<div align="center">
背景、理念、愿景...
  <a href="./docs/whats-zh.md">For Details</a>
</div>

## Technical Roadmap

Luna的核心在于临床业务建模，没有直接用openEHR的Archetype和Template概念集的原因是尽可能采用中文中抽象的、无歧义的工科术语来表达“把现实需求用抽象、通用、人可读、机器可读的方式表达”这一概念，用数学、工程学、信息学共识的“建模”二字有丰富的内涵；所有的技术都是围绕如何将业务模型转化为包含持久层、传输层、展示层的完整软件产品；Luna的最终产品对目前团队来讲会是一个big project，一个巨大挑战，因为就目前而言这是一个理想化的roadmap。
<p align="center">
<img width="780px" src="./luna_tech.png"/>
</p>
一、CDML（Clinical Domain Model Lanuage）,是一种建模规范，未来针对医疗信息化的发展会有各种类型的版本迭代，类比WEB生态中的HTML，不夸张的说HTMLx支撑了如今的互联网生态。CMDL是医疗信息化生态的种子。
</br>
二、CDM Studio ，会是官方推荐的一款可视化建模工具，必须符合临床使用习惯，支持模型模型仓库对接、版本管理、发布测试，采用微软vs系IDE的设计理念，目的是输出人、机可读的模型语言格式的文件体系。期望模型类型包括，数据采集类、数据检索类、数据集成类、数据共享类、业务应用类等。
</br>
三、CDM Repository,官方将根据区域、专科分类进行仓库划分，仓库类型分公共、私有、商业几类，不同机构根据权限可以拥有各类仓库，理想愿景下，官方的共有仓库+大型医院（医联体）开放的仓库+第三方专业模型仓库将满足信息化应用的90%需求。为保护知识产权，私有（可医联体内共享）仓库的继承和引用会完整记录，同时系统会对高引用率的模型贡献者建立奖励机制。商业模型主要针对数据应用类和临床决策型模型，收益模式灵活主要归于模型和研究数据提供的科研单位。例如产科的妊娠风险评估，基于产科信息系统的综合数据，进行基于大数据的AI的风险评估，可以直接用于系统环境达标的应用。
</br>
四、临床数据服务层，是模型语言与数据持久层、数据展示层的桥梁。简单说就是把模型转为REST API，这是解决信息孤岛的重要一环，通过设计共享模型和开放授权，Luna体系下的各个粒度的数据可以实现全面共享，通过自动化生成接口，减少传统系统接口开发的综合工作量。
</br>
五、临床数据存储引擎，就某一独立应用而言不管采用CDA式文档化存储，关系数据库的字段集存储，nosql的灵活存储，都有利弊。针对医疗信息化的应用目标CP和CDS存储体系一定要考虑大数据应用，Luna将针对业务特色结合多种存储方式，提供存储方案，供系统建设者选择，未来将参与支持开放的专用存储引擎，针对临床数据特点而定制的医疗数据引擎（国内巨杉数据库），借助阿里、腾讯的云平台优势，让医疗存储高共享高安全。
</br>
六、前端项目生成器，将业务模型变成生动的WEB应用，当然支持移动端呈现。基础是前后端分离的体系，输出的前端（目前项目将采用React+Ant设计）可经过前端设计工具或医疗服务商美化和集成，原理是丰富的组件集与模型的映射和脚手架的项目构建。
</br>
<div align="center">
  Software Projects...
  <a href="./docs/roadmap-zh_CN.md">For Details</a>
</div>

## Luna In Obstetrics

产科专科电子病历正在国内兴起，同时各种带有医疗性质的母婴健康服务也C端市场蓬勃发展。作为医院科室的一个重要分支，产科信息化发展有着同样的大背景，同时中国地域辽阔，极强的区域性在产科业务及学术领域上有着明显体现。Lian-Med专注妇产科领域，Luna就以产科小试牛刀，通过模型驱动，建设既符合医院信息系统整体建设规划又满足科室日常高效、便捷运作的产科临床应用系统；通过约束CDML（临床建模语言），促进信息互认共享，确保系统数据的完整性、规范性，建立符合临床和区域特性健康档案建设的产科数据规范；通过产科信息的数据挖掘与综合利用，充分发挥信息在临床决策中和科学研究上的价值，充分发挥信息技术在改善产科质量方面的价值，并形成与时俱进的产科质量管理体系。妇产科相关应用包括，单病种管理（临床路径）系统、临床辅助决策系统、围产保健系统、电子病历（门、急、住院）系统、产前筛查与诊断系统、营养管理、妊娠高危管理、产后康复系统、母子健康手册管理系统、区域妇幼平台等。
<div align="center">
  业务抽象、临床领域模型、CDS...
  <a href="./docs/obis-zh_CN.md">For Details</a>
</div>

## Repository For Models & Templates 

- N/A

## Reference

- [openEHR Specifications](https://specifications.openehr.org/)
- [openEHR Website](https://www.openehr.org/)
