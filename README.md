# SMP2021-ECISA “XXXX”中文隐式情感分析评测

## 一、评测背景

欢迎来到SMP2021“XXXX”中文隐式情感分析评测（The Evaluation of Chinese Implicit Sentiment Analysis，SMP-ECISA 2021）。

“第十届全国社会媒体处理大会（The eighth China National Conference on Social Media Processing）”将于2021年9月3日-5日在北京召开。全国社会媒体处理大会专注于以社会媒体处理为主题的科学研究与工程开发，为传播社会媒体处理最新的学术研究与技术成果提供广泛的交流平台，旨在构建社会媒体处理领域的产学研生态圈，成为中国乃至世界社会媒体处理的风向标，会议将以社交网络的形式改变传统的学术会议交流体验。全国社会媒体处理大会每年举办一次，现已成为社会媒体处理的重要学术活动。第十届全国社会媒体处理大会（SMP 2021）由中国中文信息学会主办，中国中文信息学会社会媒体处理专委会、北京邮电大学、北京大学承办。

在本届SMP 2021会议上，我们将举办“XXX”中文隐式情感分析评测（SMP-ECISA 2021）。该任务是SMP-ECISA 2019的进一步延续。近年来，显式情感分析已经取得了良好的进展与丰硕的成果，但隐式情感分析仍属于一个较为新颖的研究问题。隐式情感分析作为情感分析的重要组成部分，其研究成果将有助于更全面、更精确地提升在线文本情感分析的性能，可为文本表示学习、自然语言理解、用户建模、知识嵌入等方面研究起到积极的推动作用，也可进一步促进基于文本情感分析相关领域的应用和产业的快速发展。

本届“XXX”中文隐式情感分析评测由中国中文信息学会社会媒体处理专委会主办，山西大学计算机与信息技术学院承办并提供数据集，XXX赞助并提供丰厚的奖励：一等奖奖金 XXX元、二等奖奖金XXX 元、三等奖奖金XXX元，旨在促进中文隐式情感分析相关研究的发展，为本领域的学术研究人员和产业界从业人员提供一个良好的沟通平台。热烈欢迎对中文隐式情感分析感兴趣的个人和团队积极报名参赛！

## 二、评测任务

本届“XXX”中文隐式情感分析评测任务为中文隐式情感句识别与情感分类。任务描述如下：

文本情感分析是对带有情感色彩的主观性文本进行分析、处理、归纳和推理的过程。从文本的语言表达层面，依照是否含有显式情感词，可分为显式情感分析和隐式情感分析。显式文本情感分析作为该领域的基础性研究，已有大量的相关研究成果。然而，在日常表达中，人们在对客观事物体验及其行为所反映出的情感是丰富而抽象的，除采用显式情感词表达情感外，还采用客观陈述或者修辞方式来隐式地表达自己的情感。根据我们对收集的文本数据的标注结果，隐式情感句占总情感句的15%-20%左右。

我们将隐式情感定义为：“**不含有显式情感词，但表达了主观情感的语言片段**”，并将其划分为**事实型隐式情感**和**修辞型隐式情感**。其中，修辞型隐式情感又可细分为**隐喻/比喻型**、**反问型**以及**反讽型**。本次评测任务中，**仅针对隐式情感的识别与情感倾向性分类**。

【中文隐式情感句示例】

例1 你们公司一年的销售额也赶不上我们一个月的。(贬义隐式情感)

例2 有种活着诗里的感觉：烟笼寒水月笼沙，夜泊秦淮近酒家。(褒义隐式情感)

例3  我去的时候，客栈标间大多开价100元一间，还价到70元住下。(不含情感)

## 三、评测报名

评测报名时间为：

**2021年5月20日-2021年6月30日**

本次评测采用在线报名，请点击下面的链接或扫描二维码进行填写。

[SMP2021-ECISA 中文隐式情感分析评测报名表](https://docs.qq.com/form/page/DWVRnblBYY1FSZHNp?_w_tencentdocx_form=1)

![报名二维码](https://i0.hdslb.com/bfs/album/3d6fc0c473f9c9319d7248788e2f261ecc526595.png)

## 四、数据集与赛程安排

### 4.1 评测数据集

本次“XXX”中文隐式情感分析评测使用的数据集由山西大学提供，数据来源主要来自微博，主要领域/主题包括但不限于：开学延期、英国脱欧、美国大选、肖战227事件、黑人遭暴力执法等。

本次评测中，我们将使用一个大规模情感词典<sup id="a1">[[1]](#f1)</sup>，过滤掉所有包含显式情感词的文本。对这类不含显式情感词的数据进行标注，将数据标注为：褒义隐式情感、贬义隐式情感以及不含情感倾向的句子。评测数据以切分句子的篇章形式发布，保留了完整的上下文内容信息。

| 数据集  | 篇章   | 句子  | 褒义 | 贬义 | 不含情感 |
| ------- | ------ | ----- | ---- | ---- | -------- |
| 训练集  | 17055  | 19917 | 5060 | 5315 | 9542     |
| 验证集* | 6380   | 3800  | 919  | 979  | 1902     |
| 测试集* | 待发布 |       |      |      |          |

数据集以xml格式发布，内容形式为：
```
<Doc ID="5">

<Sentence ID="1">因为你是老太太</Sentence>

<Sentence ID="2" label="1">看完了，满满的回忆，很多那个时代的元素</Sentence>

</Doc>
```
带有label="1"标记的标注句子，含有完整的上下文，标签为：0-不含情感，1-褒义隐式情感，2-贬义隐式情感。

*注：验证集和测试集中均包含有大量混淆数据，混淆数据不作为测点，在提交结果时系统会自动去除混淆数据，仅对标注的测点数据进行评价。

### 4.2 赛程安排

#### 第一阶段（2021.5.20-2021.7.30）

本阶段由国家自然科学基金重点项目——[社交媒体中文本情感语义计算理论和方法](http://sa-nsfc.com/)开发的[在线评测平台](http://sa-nsfc.com/evaluation/)提供支持。参赛队伍需登录该平台注册报名[SMP2019“拓尔思杯”中文隐式情感分析评测(SMP-ECISA2019)](http://sa-nsfc.com/evaluation/ecisa/scheme)获取数据集。其中训练集由SMP2019-ECISA的训练、验证集构成，验证集由SMP2019-ECISA的测试集构成。

在该阶段，参赛队伍可在测试平台提交验证集结果，提交结果会在评测平台[排行榜](http://sa-nsfc.com/evaluation/ecisa/rank)上实时公布。提交文件格式详见平台[提交说明](http://sa-nsfc.com/evaluation/ecisa/description)页面。

**提交第一阶段成绩不作为最终成绩，仅为参赛队伍迭代模型提供参考。**


#### 第二阶段（2021.8.1-2021.8.22）

**评测完整测试集将于8月1日发布**，参赛队伍需在最终截止日期前提交完整测试集结果。**每个队伍每周有一次提交机会**。

**本阶段结果提交方式：**
参赛队伍需要将包含结果文件的邮件发送至评测官方邮箱sxu_nlp@163.com，邮件的标题为“SMP2021-参赛队名-提交次数”，邮件附件为结果文件。

**提交文件说明：**

- 因测试集中含有混淆数据，参赛队伍需对测试集中**所有句子**进行分类标注，标签为：0-不含情感，1-褒义隐式情感，2-贬义隐式情感。系统进行评价时，会自动去除所有混淆数据。

- 提交的结果文件必须是无BOM的UTF-8格式文本文件
- 每行为一个句子标签，格式形如：篇章号-句子号     标签
- 各列以制表符\t进行间隔。文件中不要有多余的空格和空行

组织方会根据参赛队伍在测试集上的得分进行排名，并在8月8日、15日、22日在在GitHub上公布该周各个队伍的排名及分数信息。以8月22日的排名结果作为本次评测的最终结果，并将会在SMP2021官方网站公布。

## 五、评价指标

   宏平均准确率（P）、召回率（R）及F1值。

## 六、评测规则

1. 所有参赛队伍都必须填写SMP2021-ECISA 中文隐式情感分析评测报名表，同时在[在线评测平台](http://sa-nsfc.com/evaluation/)中注册。**报名表与平台注册信息中的队伍名、邮箱、所属单位、成员姓名等信息需保持一致**。
2. 每支队伍最多不超过5名队员。 每名选手只能参加一支队伍，一旦发现某选手以注册多个账号的方式参加多支队伍，将取消所有相关队伍的参赛资格。
3. 各参赛单位可以开放地获取除承办方提供的数据之外的训练及开发数据。

## 七、评测奖励

**评测奖金由XXX公司赞助**，奖池共计XXX元：

- 一等奖(1名)：奖金人民币XXX元
- 二等奖(2名)：每名奖金人民币XXX元
- 三等奖(3名)：每名奖金人民币XXX元

以上奖金均为税前。

全部获奖队伍均可获得由中国中文信息学会社会媒体处理专委会（CIPS-SMP）颁发的获奖证书，并被邀请在SMP2021大会举办的技术评测论坛上进行汇报交流。

## 八、委员会

**主办单位：**

中国中文信息学会社会媒体处理专业委员会

**承办单位：**

山西大学计算机与信息技术学院
山西大学计算智能与中文信息处理教育部重点实验室

**赞助单位：**

XXXXX

**评测委员会：**

评测指导：秦兵(哈尔滨工业大学)、林鸿飞 (大连理工大学)、徐睿峰(哈尔滨工业大学(深圳))

主席：王素格（山西大学）

委员：XXX（XXX)、赵妍妍（哈尔滨工业大学）、廖健 （ 山西大学）

联系人：廖健　　联系方式：[liaojian_reg@163.com](mailto:liaojian_reg@163.com)


### 参考文献

<span id="f1">[1]. [^](#a1)</span> 徐琳宏, 林鸿飞, 潘宇,等. 情感词汇本体的构造[J]. 情报学报, 2008, 27(2):180-185.
