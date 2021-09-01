PS：本次西班牙语使用研发翻译工具进行，所以设计验收的内容仅为界面的 UI 显示；其次在部分错误反馈及系统反馈方面未能复现全部的反馈状态，测试在此内容下需要特别注意。

本次验收内容有登录模块、用户信息绑定模块、报告列表模块、其他（设置和修改密码）等。
研发修改以下的问题后，记得修改问题状态（给问题打横线，如：~~问题一，UI 显示错误；~~）

---

### 登录模块

~~1、底部的记住登录状态和忘记密码的文案因长度问题，连在一起了。~~
![image.png](https://cdn.nlark.com/yuque/0/2021/png/124638/1629700086459-11c29bb6-34ce-4c26-9498-66361b808ee7.png#height=235&id=JQ3yr&margin=%5Bobject%20Object%5D&name=image.png&originHeight=315&originWidth=530&originalType=binary&ratio=1&size=121194&status=done&style=none&width=396)
修改建议：忘记密码的文案增加换行，或整体输入模块内容的宽度增加。
~~2、登录模块的错误反馈~~

- [ ] ~~显示位置不一致如图的 ① 和 ② 分别对应左侧红色线的距离不一致。~~
- [ ] ~~其次 ① 位置的文案本身又是居中对齐的方式，需改成左对齐。~~

![image.png](https://cdn.nlark.com/yuque/0/2021/png/124638/1629703304084-42a77373-fb71-4ec3-94bc-5c66a74fa408.png#height=658&id=Rfu8c&margin=%5Bobject%20Object%5D&name=image.png&originHeight=1316&originWidth=1132&originalType=binary&ratio=1&size=700941&status=done&style=none&width=566)
3、~~当输入密码错误时，页面反馈“登录密码错误”，但如上图在邮箱输入错误时，页面反馈“请输入正确的邮箱地址”，两种反馈不一致~~
![image.png](https://cdn.nlark.com/yuque/0/2021/png/124638/1629703966725-1b248845-5a0c-48ce-856c-8b751bd152cb.png#height=133&id=m9Hog&margin=%5Bobject%20Object%5D&name=image.png&originHeight=380&originWidth=2418&originalType=binary&ratio=1&size=423134&status=done&style=none&width=844)
4、~~在关于我们页面，页面中的背景元素显示不完整，~~
![image.png](https://cdn.nlark.com/yuque/0/2021/png/124638/1629704052776-56df2cd1-c3ac-4b5a-9c04-9b71e2d15fb8.png#height=336&id=jwxdQ&margin=%5Bobject%20Object%5D&name=image.png&originHeight=495&originWidth=675&originalType=binary&ratio=1&size=36102&status=done&style=none&width=458)

### 用户信息绑定模块

1、在用户信息绑定页面的问题比较多。

- [ ] ~~首先左侧的导航图标部分，有换行闪烁，录屏动画如右侧连接；~~[展开全部.mp4](https://visbodydev.yuque.com/attachments/yuque/0/2021/mp4/124638/1629704775165-c721fffc-6c88-41ad-bcd4-9da076d16d84.mp4?_lake_card=%7B%22src%22%3A%22https%3A%2F%2Fvisbodydev.yuque.com%2Fattachments%2Fyuque%2F0%2F2021%2Fmp4%2F124638%2F1629704775165-c721fffc-6c88-41ad-bcd4-9da076d16d84.mp4%22%2C%22name%22%3A%22%E5%B1%95%E5%BC%80%E5%85%A8%E9%83%A8.mp4%22%2C%22size%22%3A3045224%2C%22type%22%3A%22video%2Fmp4%22%2C%22ext%22%3A%22mp4%22%2C%22status%22%3A%22done%22%2C%22uid%22%3A%221629704771770-0%22%2C%22progress%22%3A%7B%22percent%22%3A99%7D%2C%22percent%22%3A0%2C%22id%22%3A%22ZfNXc%22%2C%22card%22%3A%22file%22%7D)
- [ ] ~~日历部分的文案显示不完整，字母 n 显示了一半，看起来像是 r，~~以及中间连接线左右两侧距离不一致； 第三方组件
- [ ] ~~日历的顶部标题布局尽可能保持一行（右侧位置比较宽）~~，并内容间距均分； 第三方组件
- [ ] ~~头像和门店名称的间距太近了，几乎是挨在一起的；~~
- [ ] ~~展开菜单的宽度增加，尽可能减少换行。~~

![image.png](https://cdn.nlark.com/yuque/0/2021/png/124638/1629704396192-9ca64c1b-0bf2-4a1d-acde-a2bc1074598b.png#height=543&id=OQnvC&margin=%5Bobject%20Object%5D&name=image.png&originHeight=1158&originWidth=1920&originalType=binary&ratio=1&size=307329&status=done&style=none&width=901)
2、~~第一，序列号的位置可以向右侧移动，视觉上与前后的间距保持均分；~~
~~第二，页码的位置考虑是否能够固定，如图在第二页数量不多的情况下，页码就跑到上面去了。~~ 第三方组件

![image.png](https://cdn.nlark.com/yuque/0/2021/png/124638/1629705186110-c4637569-2413-4c96-b362-f5760623bec1.png#height=434&id=vhgNx&margin=%5Bobject%20Object%5D&name=image.png&originHeight=1079&originWidth=2233&originalType=binary&ratio=1&size=264535&status=done&style=none&width=898)
3、~~测量项目的位置使用居中对齐； ~~文案中有句中大写的部分，需要修改。保持不变
![image.png](https://cdn.nlark.com/yuque/0/2021/png/124638/1629707068561-d0182670-a3e6-4d00-9bff-c9cbbd90b6e4.png#height=241&id=d0RiO&margin=%5Bobject%20Object%5D&name=image.png&originHeight=367&originWidth=476&originalType=binary&ratio=1&size=44853&status=done&style=none&width=313)
4、~~文案的行高修改，现在超过了右侧输入框的高度；输入框内的文案太贴近边缘了，给预留一部分空间。~~
![image.png](https://cdn.nlark.com/yuque/0/2021/png/124638/1629707219471-df39da9f-4f82-4d1e-a87e-5d88f7d40f62.png#height=184&id=EkYrC&margin=%5Bobject%20Object%5D&name=image.png&originHeight=367&originWidth=1466&originalType=binary&ratio=1&size=115992&status=done&style=none&width=733)
5、~~显示文案内容的问题，两句针对的翻译，都是“请输入测量用户的邮箱”~~
![image.png](https://cdn.nlark.com/yuque/0/2021/png/124638/1629707275239-db88ef27-712a-4b9c-b65b-4778089e9505.png#height=177&id=NXk66&margin=%5Bobject%20Object%5D&name=image.png&originHeight=354&originWidth=456&originalType=binary&ratio=1&size=48277&status=done&style=none&width=228)
6、~~输入用户信息部分，输入框内的文案显示到边框边缘距离太近；左侧文案和右侧的输入框没有居中对齐；输入框大小不一致。~~
![image.png](https://cdn.nlark.com/yuque/0/2021/png/124638/1629707638904-c30ba0f6-f209-4241-8aec-c2fd70496862.png#height=223&id=aseqK&margin=%5Bobject%20Object%5D&name=image.png&originHeight=390&originWidth=496&originalType=binary&ratio=1&size=31128&status=done&style=none&width=283)
7、~~性别选择这里的颜色对比度不够，~~ (无需修改)
![image.png](https://cdn.nlark.com/yuque/0/2021/png/124638/1629707724077-34cf3a3c-c9eb-4d0c-84bc-b5e559a629c5.png#height=151&id=kbUD5&margin=%5Bobject%20Object%5D&name=image.png&originHeight=302&originWidth=497&originalType=binary&ratio=1&size=27480&status=done&style=none&width=248.5)

### 测量报告列表模块

1、~~日历部分如前面所述，测量项目名称部分的换行建议左对齐方式~~
![image.png](https://cdn.nlark.com/yuque/0/2021/png/124638/1629708092022-4e5a56fb-89f6-40f7-8f34-90db393c89e5.png#height=531&id=PPKrg&margin=%5Bobject%20Object%5D&name=image.png&originHeight=1158&originWidth=1920&originalType=binary&ratio=1&size=258695&status=done&style=none&width=880)
2、~~在打开数据预览后的列表中，关于 ID 和昵称的前后的间距需要调整，以及测量项目的换行对齐方式~~
![image.png](https://cdn.nlark.com/yuque/0/2021/png/124638/1629708310020-ee741d14-f2fb-46e7-b3ad-07e055ee64e5.png#height=531&id=rprd4&margin=%5Bobject%20Object%5D&name=image.png&originHeight=1158&originWidth=1920&originalType=binary&ratio=1&size=277504&status=done&style=none&width=880)
3、~~有新的报告后，新的提示重叠了~~
![image.png](https://cdn.nlark.com/yuque/0/2021/png/124638/1629708359230-4e6f7cee-45c2-4d51-89ab-14d34f30aaed.png#height=530&id=aicti&margin=%5Bobject%20Object%5D&name=image.png&originHeight=1158&originWidth=1921&originalType=binary&ratio=1&size=312525&status=done&style=none&width=880)
4、~~昵称未填写的提示错误，应该提示“请输入昵称”~~ (无需修改)
![image.png](https://cdn.nlark.com/yuque/0/2021/png/124638/1629708410122-5f200b90-d039-468b-bb78-5fab408d3507.png#height=531&id=fMbNX&margin=%5Bobject%20Object%5D&name=image.png&originHeight=1158&originWidth=1920&originalType=binary&ratio=1&size=268743&status=done&style=none&width=880)
5~~、数据预览部分的大小检查，以及在体围测量的文档中，有简写文案。~~
![image.png](https://cdn.nlark.com/yuque/0/2021/png/124638/1629709219650-d0581de7-9b71-41e3-b183-e9f6afad19f7.png#height=334&id=YBCTK&margin=%5Bobject%20Object%5D&name=image.png&originHeight=763&originWidth=2008&originalType=binary&ratio=1&size=189251&status=done&style=none&width=880)
6、~~文案、数据之间的对齐方式不一致 ~~
![image.png](https://cdn.nlark.com/yuque/0/2021/png/124638/1629709644410-7c35ea18-1f8c-43ff-8196-7f89a45850b2.png#height=336&id=YqT5T&margin=%5Bobject%20Object%5D&name=image.png&originHeight=766&originWidth=2009&originalType=binary&ratio=1&size=212860&status=done&style=none&width=880)
7、~~单位的样式和名称修改~~
![image.png](https://cdn.nlark.com/yuque/0/2021/png/124638/1629709810618-bfd02206-a64d-40da-ba0d-ee5450577a24.png#height=336&id=ktys0&margin=%5Bobject%20Object%5D&name=image.png&originHeight=766&originWidth=2009&originalType=binary&ratio=1&size=189079&status=done&style=none&width=880)

### 其他模块

1、~~账号设置模块的对齐方式采用右对齐；长传 logo 部分有文案遮挡；提示文案修改文本框的大小。~~
![image.png](https://cdn.nlark.com/yuque/0/2021/png/124638/1629710001265-05a8accb-1907-47ad-9044-d5d5cf35470f.png#height=531&id=RSCQU&margin=%5Bobject%20Object%5D&name=image.png&originHeight=1158&originWidth=1920&originalType=binary&ratio=1&size=235463&status=done&style=none&width=880)
2、~~账号设置部分的西班牙字符长度约束，是不是考虑修改一下；~~ 无需修改
![image.png](https://cdn.nlark.com/yuque/0/2021/png/124638/1629710399221-eccfb433-eab0-4b78-843e-7906c120c77b.png#height=452&id=AcUhz&margin=%5Bobject%20Object%5D&name=image.png&originHeight=904&originWidth=796&originalType=binary&ratio=1&size=140629&status=done&style=none&width=398)​
3、~~修改密码部分的确认密码文案行高和换行修改，建议不换行；修改密码的错误反馈位置和对齐方式不对； 其次原始密码的检查机制好像不对；~~ 无需修改
![image.png](https://cdn.nlark.com/yuque/0/2021/png/124638/1629710335891-f0859d20-e713-480b-986e-633329028bb3.png#height=364&id=TMUKK&margin=%5Bobject%20Object%5D&name=image.png&originHeight=727&originWidth=654&originalType=binary&ratio=1&size=84886&status=done&style=none&width=327)
4、~~时区设置部分文档中没有找到这部分的记录~~ (无需修改)
![image.png](https://cdn.nlark.com/yuque/0/2021/png/124638/1629710450702-e9720bbe-b956-48ec-917b-d27a550633af.png#height=531&id=SiVn6&margin=%5Bobject%20Object%5D&name=image.png&originHeight=1158&originWidth=1920&originalType=binary&ratio=1&size=148311&status=done&style=none&width=880)

### 打印报告模块

- [ ] ~~骨外含量仅中文显示~~
- [ ] ~~节段脂肪和节段肌肉的文案不需要加粗；~~
- [ ] ~~调节建议处的图标左对齐，不需要换行~~；​
- [ ] ~~名称部分的长文案处理方式，接受换行显示，但换行后的行高需要单独处理一下；~~
- [ ] ~~与上次对比的变化数据对齐方式统一；~~
- [ ] ~~右侧的节段数据与底部的项目名称解释做到顶部和底部对齐，中间平均分布；~~
- [ ] ~~体态评估中，顶部体态图片的间距建议调整；~~
- [ ] ~~骨盆前后倾的文本换行需要检查一下，换行后尽可能两行显示；~~
- [ ] ~~体态结论和测量数据左移，给右侧的长文本留多些空间；~~
- [ ] ~~体围数据展示部分，换行的名称部分需要保证单词显示的完整性；~~
- [ ] ~~肩部功能没有分数；~~
- [ ] ~~文案显示部分左对齐；~~
- [ ] ~~底部结论部分有重叠；~~
- [ ] ~~结论中的文案部分有溢出重叠，一处没有添加空格。~~

![image.png](https://cdn.nlark.com/yuque/0/2021/png/124638/1629711118537-ffc32590-96e8-49d4-9462-ca3c768234c9.png#height=2428&id=rUgIv&margin=%5Bobject%20Object%5D&name=image.png&originHeight=4855&originWidth=1921&originalType=binary&ratio=1&size=1722462&status=done&style=none&width=960.5)
问题检查：按钮位置的一致性，左轻右重。

### 会议讨论部分

#### 1、研发文档的标准

现有的问题：文档中的重复性问题（需要给重复的内容打标签，避免翻译不一致：不一致需要考虑到使用场景是否有语法的要求）
文档的测试验证问题（测试需要能够找到这个翻译大概率是什么内容，以及异常反馈和系统反馈对应的文案是否正确）
文档再翻译的可用性（给到用户时，如何可以直接翻译，以及那句和那句是需要组合使用的，以及是否有语法差异，文档的组合使用后，是否有长度字符的约束）

#### 2、关于工作流程和工作效率

设计在验收的时候，部分文案和场景无法复现。
这里需要讨论两个问题，第一是设计验收是否需要走全量，正常来讲是需要走全量的，但如果走全量，就需要测试帮忙。
第二个问题是，设计在此过程中，对于验收的内容和质量需要严格把关，这就要设计花费的时间比较多，以及责任很重。
（我的建议是，研发在文档中加入异常反馈和系统反馈的标签，测试总结一下正常内容的测试和异常反馈的测试方法，主要是教我如何快速全量走查；二是走查内容的分工，研发对应的翻译工具肯定不会出错，但是文档的可靠性是第一档防线，然后翻译的内容会不会用错是第二档防线）
工作效率：当本次的结果来看，显示的问题居多，但这些问题其实都不需要做高保真来校对，研发在做的过程中我们提前对齐如何修改的标准即可，但问题在于我们如何配合？

## 会议结论：

1、设计走查的时候，需检查文案和样式问题。设计走冒烟测试的部分，特殊类反馈文案和样式，待测试验证。
2、设计检查研发文档的重复性内容，8 月 26 日输出给研发；研发检查文档中的英文部分大小写是否需要区分（西班牙语大小写仅句首的首字母大写即可），并检查重复性问题后整理和修改研发文档，8 月 27 日答复。
3、研发检查文档中关于 WEB 端是否存在文案拼凑，有的话需要转化成完整的句子，避免拼凑文案；并提前规划设备端的文案拼凑检查整理，及修改。
4、德语的文档整理设计按照当前研发文档进行，待研发确定最终文档后，研发按照最新整理的文档及样式进行德语版本的转换。
