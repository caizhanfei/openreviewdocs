# NeurIPS 2021使用报告

**NeurIPS 2021使用报告**

作者：

[Andrew McCallum](https://people.cs.umass.edu/\~mccallum/) (麻省大学阿默斯特分校教授， OpenReview项目总监)

[Melisa Bok](https://www.cics.umass.edu/people/bok-melisa) (OpenReview开发主管)

[Alina Beygelzimer](https://hunch.net/\~beygel/) (雅虎研究院高级科学家， NeurIPS 2021 程序委员会副主席)

NeurIPS是机器学习领域的顶会之一。NeurIPS的组织者们决定于20201使用OpenReview平台来进行论文的提交和评审，在此之前NeurIPS使用的是微软开发的CMT会议系统。此报告记录了NeurIPS 2021的会议流程，OpenReview所提供的功能，在使用过程中的性能表现并为次年NeurIPS所规划的提升作一小结。

提交到NeurIPS的论文数量最近十年出现了爆发式的增长，NeurIPS也一直在探索同行评仪过程中新的可能性。

NeurIPS2021的会议流程与之前几年基本相同：双盲评议，设置有领域主席(AC)，高级领域主席(SAC)和总评议。今年论文作者与审稿人之间可以进行多轮讨论而在此之前论文作者只有一次回应审稿人疑问的机会。

在会议流程和时间方面我们与OpenReview团队通过共享文档，视频会议和即时通信软件进行了紧密的配合。论文提交和评议的过程中，OpenReview的技术人员对NeurIPS程序委员会主席们的问题提供了24x7的迅速支持，还为NeurIPS提供了许多定制化的功能。

下面我们列出了一些NeurIPS2021涉及到的关键流程和服务：

**审稿人邀请**：NeurIPS程序委员会主席们共邀请了超过一万三千名审稿人、一千名领域主席和一百五十五名高级领域主席。取得国际学习表征会议ICLR组织者同意之后，OpenReview为我们提供了2016至2021年所有中稿论文的作者名单。

* **审稿人/论文作者注册**：已有将近二十三万研究人员在OpenReview平台注册有帐户。在审稿人邀请和论文提交阶段，还是有超过一万名研究人员新注册了账户并从DBLP导入了论文。在OpenReview技术人员的帮助下我们进行了账号的共指消解。为了避免论文作者与审稿人之间的利益冲突，我们要求论文列出的所有作者都注册一个OpenReview账户。2021年5月间，共有12537名新用户在OpenReview注册了账户，这打破了OpenReview账户注册的历史。
* **发现利益冲突**：论文作者与审稿人的账户中不光记录了目前的组织或企业，也记录了DBLP个人主页、谷歌学术个人主页以及其他可以用于发现潜在利益冲突的信息比如教育和工作经历、导师信息、合作者信息以及部分家庭信息。OpenReview还为NeurIPS增加了隐私利益冲突功能，即作者或审稿人所添加的利益冲突信息并不会显示在其个人主页上。这次，OpenReview使用工作经历、提交的利益冲突信息和过去三年的论文合作者信息来计算论文作者与审稿人之间的利益冲突。
* **审稿人专长模型**：我们使用OpenReview团队开发的深度学习算法使用审稿人发表过论文的标题和摘要为每一位审稿人的专长建立了模型。NeurIPS2021没有使用TPMS和Semantic Scholar提供的审稿人专长模型。
* **论文提交**：本次会议的程序委员会主席要求作者在正式提交论文之前一周提交论文标题和摘要。OpenReview平台共收到了11729篇论文。正式论文提交截止之前的24小时内，两万八千名用户在OpenReview进行了超过四万两千次论文修改再提交。截止时间前一小时有超过两千三百名作者提交了论文。在此期间OpenReview使用顺利返回迅速，系统负载还未达到最大资源的50%。在论文提交阶段，OpenReview共向论文作者发送了超过十一万封邮件。
* **投标**：高级领域主席SAC需要对领域主席AC进行投标。AC和审稿人则需对论文进行投标。AC或论文投标完成之前将在OpenReview中显示为待完成的一项任务。投标过程中，SAC、AC和审稿人可以根据相似性得分对AC和论文进行排序，也可以使用各种属性来搜索AC和论文。
* **审稿人分配**：审稿人分配的数据来源有三种：OpenReview的审稿人专长模型、审稿人投标和利益冲突。优化算法则使用了[Min-Cost-Flow](https://developers.google.com/optimization/flow/mincostflow) and [FairFlow](https://arxiv.org/abs/1905.11924v1) \[Kobren, et al, 2019]。因为优化算法的参数很容易调整，所以今年NeurIPS对审稿人分配进行了多轮优化（优化算法每次运行需要约1个小时）。每次优化的结果和统计数据都以可视化的方法展示了出来。审稿人-论文-审稿人之间的关系也可以在OpenReview中查看或者搜索调整。除了模型优化的结果，PC和AC也可以推荐没有邀请到的外部审稿人。审稿人分配的算法和模型也用于第二AC和紧急审稿人的分配。
* **控制台**：OpenReview为会议中不同的角色提供了单独的控制台来实现诸如任务列表、审稿进度、搜索过滤、更换审稿人、统计数据、投标进度、邮件提醒和数据导出等功能。
* **评审和讨论**：审稿人在OpenReview提交的评审意见对该论文的AC立即可见，而论文作者和其他审稿人需等到审稿截止日期之后才能看到。应NeurIPS的要求，OpenReview在论文的讨论区添加了将讨论按来源分类为不同标签页的功能来方便查阅。在论文评审期间，OpenReview平台共收到了37284条评审意见、8103条总评审、452条道德评审以及十万余条评论。
* **审稿质量评分**：AC可以对审稿人提交的评审进行打分，论文作者也可以对收到的评审意见提供反馈。不过AC的评分和论文作者的反馈都只对PC可见。
* **道德评审**：今年OpenReview首次为NeurIPS设置了道德评审功能。有道德评审主席对收到投诉的论文分配道德评审来判断对受举报论文的处理方式。道德评审的分配也使用了OpenReview提供的模型和算法。
* **接收结果**：PC从OpenReview把包括AC意见在内的接收结果下载为CSV文件然后做出了一些修改。接收结果确定之后OpenReview依照修改过的CSV文件公布了接收结果并以邮件的方式通知了论文作者。以后我们也可能在OpenReview上直接对论文接收结果进行浏览和修改，也可能利用Google表格与OpenReview进行信息同步。
* **最终修改版**：如果论文被NeurIPS接收，论文作者可以在OpenReview上传论文的最终修改版以及相应的版权协议、包括视频在内的补充材料和LaTeX。
* **专题会议**：OpenReview计算了确定接收论文的相似性得分，在此基础上进行聚类分析就可以形成专题会议的框架。

**系统性能**

在NeurIPS2021的论文提交过程中，OpenReview平台提供了流畅的体验。

**同行评议实验**：

在OpenReview团队的帮助下，NeurIPS2021对论文的同行评议进行了以下几个实验：

* **Consistency experiment**: In 2014, NeurIPS ran an experiment in which 10% of submissions were reviewed by two independent program committees to quantify the randomness in the review process. Since then, the number of annual NeurIPS submissions has increased more than fivefold. To check whether decision consistency has changed as the conference has grown, we ran a variant of this experiment again in 2021. Thе results of this experiment are reported here: ​[​https://blog.neurips.cc/2021/12/08/the-neurips-2021-consistency-experiment/](https://blog.neurips.cc/2021/12/08/the-neurips-2021-consistency-experiment/)
* **论文接收意见的一致性**：2014年开始，NeurIPS就对
* To discourage **resubmissions** without substantial changes, authors were asked to declare if a previous version of their submission had been rejected from another peer-reviewed venue. Like the year before, authors of resubmissions were asked to describe the improvements made. This information was entered into OpenReview during the submission process. To evaluate **resubmission bias**, resubmission information was made visible to reviewers and area chairs only for a randomly chosen 50% of submissions. While the experiment allowed us to eliminate a significant bias, we can’t confidently ascertain there is none.
* **Author perception experiment**: OpenReview implemented a two-part author survey to help NeurIPS understand how well authors’ perception of their submissions agrees with reviewing outcomes. The results of this experiment are forthcoming.

**Releasing the data to the public**:

Submissions under review were visible only to assigned program committee members, and we did not solicit comments from the general public during the review process. After the notification deadline, **accepted papers were made public and open for non-anonymous public commenting**, along with their anonymous reviews, meta-reviews, and author responses.

By default, rejected submissions were not made public, but authors of **rejected submissions were given 2 weeks to opt in** to make their de-anonymized papers public and open for commenting in OpenReview. If they chose to do so, this also opened up the reviews, meta-reviews, and any discussion with the authors for these papers. This policy does give authors a mechanism to publicly flag and expose potential problems with the review process. In the end, only about 2% of rejected papers opted in.

**Feedback from Alina Beygelzimer, NeurIPS 2021 Program Co-chair**:

“As Program Chairs for NeurIPS 2021, we decided to shift the entire reviewing workflow to OpenReview. OpenReview is a flexible platform that allows heavy customization, and will be easy to adapt as the needs of the conference evolve. It brings a number of infrastructural improvements including persistent user profiles that can be self-managed, accountability in conflict-of-interest declarations, and improved modes of interaction during the discussion process. NeurIPS has a long history of experimentation with the goal of informing and improving the review process (e.g., the widely known “NeurIPS Consistency Experiment” of 2014). This year we took full advantage of the great flexibility of OpenReview’s workflow configuration to run several key experiments (including a version of the noise audit that hasn’t been done since 2014). We are grateful to the OpenReview team for supporting all requested experimentation.

Our experience with OpenReview has been a delight. Not only did the paper deadline proceed smoothly (with sub-second system response time throughout the arrival of thousands of submissions just before the submission deadline), but OpenReview gracefully handled more than 20K authors accessing the system roughly at the same time to read and respond to preliminary reviews, and enabled 10K reviewers and Area Chairs and 20K authors to engage in discussions in the weeks that followed. The feedback we received from our authors and program committee members has been overwhelmingly positive.

I hope that NeurIPS will continue to work with OpenReview for years to come. We are hugely grateful to the OpenReview team, for their unparalleled level of support to everyone involved in the review process. OpenReview has also supported the Data & Benchmarks track (new this year) as well as the Ethics Review process for both the main conference and the Data & Benchmarks track. It is also notable that over 20 of the NeurIPS workshops have chosen to use OpenReview for their reviewing workflow this year.”

**OpenReview team’s plans for improvement**. The OpenReview system is ready for re-use for future NeurIPS conference reviewing needs. The OpenReview team continues to make improvements and new features. Current work likely to be ready for NeurIPS 2022 includes

* We are currently designing a new version of the paper reviewing discussion forum, and would be eager for feedback and feature requests. NeurIPS concerns about “rolling discussions” could be addressed here.
* Further improvements to the reviewer-paper matching system.
* Deployment of a new API providing (1) additional flexibility for fine-grained per-field control of visibility, (2) ease of changing readership permission of content, (3) better storage and access of the history of changes to a paper, review, or comment, (4) creation of “CRON”-jobs for automated sending of reminders.

In future, we will also have support for synchronous chat-style communication among reviewers, area chairs, and program chairs––which we hope will encourage more interactive, open, scientifically-flexible communication during the reviewing period. We are also building support for live conferences, integrated into the OpenReview reviewing platform.

```
```
