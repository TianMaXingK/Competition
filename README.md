# 认知博弈评测

## 评测内容
本届认知博弈评测共下设两个任务，分别为任务一：多模态谣言检测和任务二：智慧论辩，其相应的任务描述、数据集描述、评测指标描述及提交格式描述如下。

### 任务一：多模态谣言检测
随着互联网的快速发展和普及，社交媒体被广泛应用起来，这就为虚假信息传播提供了肥沃的温床，过多的虚假信息充斥社交媒体平台将误导公众舆论，损害企业形象，影响政治选举，对公民经济生活、公共安全和社会稳定构成巨大威胁。

本届多模态中的谣言检测评测任务旨在识别社交媒体中的虚假消息，通过所给的一切信息对消息进行二分类，真实（True）还是虚假(False)。本次评测任务不提供训练数据集，仅提供测试数据集。

#### 数据集描述

1. 测试数据集主要来自互联网平台，以中文信息为主，包含从2017年-2023年的数据。 
2. 测试数据集共包含11515条数据样本，其中包含两个标签，“虚假信息(False)”有2288条，“真实信息(True)”有9227条。 
3. 测试数据集为多模态数据，单个待测试数据样本除了文本之外，可能还包括图像信息。  
4. 测试数据集中，部分数据会包含互动信息。

本任务的文件夹中包括所有文件数据，文件夹内具有ID的子文件夹代表一则微博的信息，子文件夹内的json文件包括该微博的文本、用户、评论、转发信息，其他文件则为该微博附带的图片。
json文件内的字段说明如下：
<table class=MsoNormalTable border=0 cellspacing=0 cellpadding=0 width=588
 style='width:441.0pt;border-collapse:collapse'>
 <tr style='height:14.15pt'>
  <td width=73 nowrap style='width:55.0pt;border:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><b><span
  style='font-family:宋体;color:black'>字段</span></b></p>
  </td>
  <td width=120 nowrap style='width:90.0pt;border:solid windowtext 1.0pt;
  border-left:none;padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><b><span
  style='font-family:宋体;color:black'>子字段</span></b></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border:solid windowtext 1.0pt;
  border-left:none;padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><b><span
  style='font-family:宋体;color:black'>说明</span></b></p>
  </td>
 </tr>
 <tr style='height:14.15pt'>
  <td width=193 nowrap colspan=2 style='width:145.0pt;border:solid windowtext 1.0pt;
  border-top:none;padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>id</span></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>信源</span><span lang=EN-US style='font-family:"Times New Roman",serif;
  color:black'>ID (</span><span style='font-family:宋体;color:black'>已脱敏</span><span
  lang=EN-US style='font-family:"Times New Roman",serif;color:black'>)</span></p>
  </td>
 </tr>
 <tr style='height:14.15pt'>
  <td width=73 nowrap rowspan=6 style='width:55.0pt;border:solid windowtext 1.0pt;
  border-top:none;padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>content</span></p>
  </td>
  <td width=120 nowrap style='width:90.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>created_at</span></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>信源发布时间</span></p>
  </td>
 </tr>
 <tr style='height:14.15pt'>
  <td width=120 nowrap style='width:90.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>text</span></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>信源文本</span></p>
  </td>
 </tr>
 <tr style='height:14.15pt'>
  <td width=120 nowrap style='width:90.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>comments_count</span></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>信源评论数</span></p>
  </td>
 </tr>
 <tr style='height:14.15pt'>
  <td width=120 nowrap style='width:90.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>reposts_count</span></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>信源转发数</span></p>
  </td>
 </tr>
 <tr style='height:14.15pt'>
  <td width=120 nowrap style='width:90.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>attitudes_count</span></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>信源点赞数</span></p>
  </td>
 </tr>
 <tr style='height:14.15pt'>
  <td width=120 nowrap style='width:90.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>created_at_str</span></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>信源发布时间字符串</span></p>
  </td>
 </tr>
 <tr style='height:14.15pt'>
  <td width=73 nowrap rowspan=7 style='width:55.0pt;border:solid windowtext 1.0pt;
  border-top:none;padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>user</span></p>
  </td>
  <td width=120 nowrap style='width:90.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>uid</span></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>用户</span><span lang=EN-US style='font-family:"Times New Roman",serif;
  color:black'>ID (</span><span style='font-family:宋体;color:black'>已脱敏</span><span
  lang=EN-US style='font-family:"Times New Roman",serif;color:black'>)</span></p>
  </td>
 </tr>
 <tr style='height:14.15pt'>
  <td width=120 nowrap style='width:90.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>description</span></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>用户描述</span></p>
  </td>
 </tr>
 <tr style='height:14.15pt'>
  <td width=120 nowrap style='width:90.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>follow_count</span></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>用户关注数</span></p>
  </td>
 </tr>
 <tr style='height:14.15pt'>
  <td width=120 nowrap style='width:90.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>followers_count</span></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>用户粉丝数</span></p>
  </td>
 </tr>
 <tr style='height:14.15pt'>
  <td width=120 nowrap style='width:90.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>gender</span></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>用户性别</span></p>
  </td>
 </tr>
 <tr style='height:14.15pt'>
  <td width=120 nowrap style='width:90.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>verified</span></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>用户是否认证，共两类：</span><span lang=EN-US style='font-family:"Times New Roman",serif;
  color:black'>true</span><span style='font-family:宋体;color:black'>认证用户、</span><span
  lang=EN-US style='font-family:"Times New Roman",serif;color:black'>false</span><span
  style='font-family:宋体;color:black'>非认证用户</span></p>
  </td>
 </tr>
 <tr style='height:14.15pt'>
  <td width=120 nowrap style='width:90.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>verified_reason</span></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>用户认证理由</span></p>
  </td>
 </tr>
 <tr style='height:14.15pt'>
  <td width=73 nowrap rowspan=4 style='width:55.0pt;border:solid windowtext 1.0pt;
  border-top:none;padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>comments</span></p>
  </td>
  <td width=120 nowrap style='width:90.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>id</span></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>评论</span><span lang=EN-US style='font-family:"Times New Roman",serif;
  color:black'>ID (</span><span style='font-family:宋体;color:black'>已脱敏</span><span
  lang=EN-US style='font-family:"Times New Roman",serif;color:black'>)</span></p>
  </td>
 </tr>
 <tr style='height:14.15pt'>
  <td width=120 nowrap style='width:90.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>created_at</span></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>评论时间</span></p>
  </td>
 </tr>
 <tr style='height:14.15pt'>
  <td width=120 nowrap style='width:90.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>text</span></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>评论文本</span></p>
  </td>
 </tr>
 <tr style='height:14.15pt'>
  <td width=120 nowrap style='width:90.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>uid</span></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>用户</span><span lang=EN-US style='font-family:"Times New Roman",serif;
  color:black'>ID (</span><span style='font-family:宋体;color:black'>已脱敏</span><span
  lang=EN-US style='font-family:"Times New Roman",serif;color:black'>)</span></p>
  </td>
 </tr>
 <tr style='height:14.15pt'>
  <td width=73 nowrap rowspan=6 style='width:55.0pt;border:solid windowtext 1.0pt;
  border-top:none;padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>reposts</span></p>
  </td>
  <td width=120 nowrap style='width:90.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>id</span></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>转发</span><span lang=EN-US style='font-family:"Times New Roman",serif;
  color:black'>ID (</span><span style='font-family:宋体;color:black'>已脱敏</span><span
  lang=EN-US style='font-family:"Times New Roman",serif;color:black'>)</span></p>
  </td>
 </tr>
 <tr style='height:14.15pt'>
  <td width=120 nowrap style='width:90.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>created_at</span></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>转发时间</span></p>
  </td>
 </tr>
 <tr style='height:14.15pt'>
  <td width=120 nowrap style='width:90.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>raw_text</span></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>转发附带评论纯文本</span></p>
  </td>
 </tr>
 <tr style='height:14.15pt'>
  <td width=120 nowrap style='width:90.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>text</span></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>转发附带评论文本</span></p>
  </td>
 </tr>
 <tr style='height:14.15pt'>
  <td width=120 nowrap style='width:90.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>pid</span></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>转发父节点</span><span lang=EN-US style='font-family:"Times New Roman",serif;
  color:black'>ID (</span><span style='font-family:宋体;color:black'>已脱敏</span><span
  lang=EN-US style='font-family:"Times New Roman",serif;color:black'>)</span></p>
  </td>
 </tr>
 <tr style='height:14.15pt'>
  <td width=120 nowrap style='width:90.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span lang=EN-US
  style='font-family:"Times New Roman",serif;color:black'>uid</span></p>
  </td>
  <td width=395 nowrap style='width:296.0pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0cm 5.4pt 0cm 5.4pt;height:14.15pt'>
  <p class=MsoNormal align=left style='text-align:left'><span style='font-family:
  宋体;color:black'>用户</span><span lang=EN-US style='font-family:"Times New Roman",serif;
  color:black'>ID (</span><span style='font-family:宋体;color:black'>已脱敏</span><span
  lang=EN-US style='font-family:"Times New Roman",serif;color:black'>)</span></p>
  </td>
 </tr>
</table>

除以上json文件外，本任务还为参赛选手们提供了汇总的info.xlsx文件，该文件存储了微博的ID（已脱敏）、信源发布时间、信源文本内容以及信源包含的图片文件信息，字段说明如下：
| 字段 | 说明 |
| ----- | ----- |
|  new_id      |   脱敏后ID     |
|  created_at  |   信源发布时间 |
|  text        |   信源文本     |
|  pic         |   信源包含的图片文件 |

#### 评测指标描述
本任务以Marco F1值作为评测指标。

#### 提交格式
评测使用邮箱提交结果。参赛队伍需要将包含结果文件的邮件发送至邮箱liumingrui@uir.edu.cn，邮件的标题为“Competition-参赛队名”，邮件附件为任务的结果文件。任务一结果文件为无BOM的以utf-8为编码格式的csv文件，使用逗号“,”作为分隔符，使用“\n”作为每行结尾的换行符，任务一的命名格式为：参赛队名_任务1.csv。

例如：参赛队名为“Winners”，则任务1的提交文件名为“Winners_任务1.csv”，提交结果的样例格式如下（提交的结果文件格式不正确不予计算成绩）：

| new_id | label |
| ----- | ----- |
|  1  |   TRUE    |
|  2  |   FALSE   |
| ... |    ...    |


### 任务二：智慧论辩
论辩是人类智慧的一项重要技能，在诸多人类活动中承担着不可或缺的作用。计算论辩技术关注机器对人类论辩过程的理解和模仿， 广泛应用于决策辅助、写作支持和逻辑审查等场景，于近年来逐渐成为人工智能研究的新兴重要分支。本次智慧论辩任务关注中、英文辩论赛场景下的论辩挖掘， 鼓励参赛者使用计算论辩相关技术对辩论陈词中的论辩要点等成分做识别或生成，旨在推动计算论辩相关研究的发展，并试图为学界研究着与相关产业从业者提供良好的沟通交流平台。

智慧论辩任务包含两个子任务，反论点生成及基于辩题的论点生成。其中反论点生成任务提供了一个英文数据集，基于辩题的论点生成任务则提供了一个中文数据集。  
子任务一 基于辩题的反论点生成：针对给定的话题和原始论点，由参赛模型自动生成反驳原始论点的5个句子（称为反论点）。  
子任务二 基于辩题的论点生成：针对既定的辩题，由参赛模型自动生成贴合辩题的5个论点。

#### 子任务一：基于辩题的反论点生成

##### 数据集描述
该数据集为英文数据集，来源于ChangeMyView论坛(CMV)，标注员针对用户的交互内容进行了反驳关系标注，整理为带格式的txt文件。

##### 数据样例
输入：Should the phrase "under God" be retained in the Pledge of Allegiance?<tab>the under God line is actually a relatively new addition and can therefore be easily removed without significant consequences.  
输出：
Just because something is new doesn't mean it lacks importance or significance, and removing it can have unforeseen consequences.
Ignoring the historical and constitutional significance of the "under God" line in the Pledge of Allegiance is a dangerous oversimplification that fails to recognize the phrase's cultural and symbolic importance to American identity.  
......

基于辩题的论点生成任务（中文数据集）：数据集来源于2007至2021年的近700场知名华语辩论比赛，经由语音转译及人工校验得到了每场比赛的单环节、单方陈词文本，由标注员进行了论点句和互动论点对等标注，整理为带格式的txt文件。

#### 子任务二：基于辩题的论点生成

##### 数据集描述
该数据集为中文数据集，来源于2007至2021年的近700场知名华语辩论比赛，经由语音转译及人工校验得到了每场比赛的单环节、单方陈词文本，由标注员进行了论点句和互动论点对等标注，整理为带格式的txt文件。
##### 数据样例
输入：公众事件中不应该批评不完美受害者  
输出：
将矛头调转向批评不完美的受害者，使受害者与加害者之间的力量进一步失衡，不符合媒体伦理。  
舆论的变动可能影响案件的走向。  
如果秉持着应该批评不完美的心态，无疑会使得将来更少受害者敢于向公众发声。  

##### 提交格式
评测使用邮箱提交结果。参赛队伍需要将包含结果文件的邮件发送至邮箱liumingrui@uir.edu.cn，邮件的标题为“Competition-参赛队名”，邮件附件为任务的结果文件。结果文件为无BOM的以utf-8为编码格式的txt文件，使用逗号“,”作为分隔符，使用“\n”作为每行结尾的换行符，任务二的命名格式为：参赛队名_任务2_子任务x.txt。  

例如：参赛队名为“Winners”，则提交文件名为“Winners_任务2_子任务1.txt”和“Winners_任务2_子任务2.txt”的两个结果文件。两个任务提交结果的样例格式如下（提交的结果文件格式不正确不予计算成绩）：

#### 评测指标描述
两个子任务均以ROUGE-L值作为评测指标。以下为基线模型的分数，参赛模型的指标如果低于基线，则无法参与后续评奖。
| Track | Model |Rouge-L Score|
| ----- | ----- | ----|
|  反论点生成  |   GPT-2    |  0.143    |
|  论点生成    |   Mengzi   |  0.101    |


## 奖金

## 报名网站
参赛数据集将会在填写报名表后1~2个工作日内发放  
[认知博弈评测报名表](https://docs.qq.com/form/page/DYVBhY09aV3dLakt4)

## 注意事项
1.	本次评测使用的数据集由网络获取，仅限于本次技术评测及学术研究使用，未经许可不能作为商业用途或其他目的。
2.	如需使用本数据集进行课题研究及论文发表，请联系评测工作人员：liumingrui@uir.edu.cn。
3.	仅允许使用所有参赛者均可获得的开源代码、工具以及外部数据。
4.	算法与系统的知识产权归参赛队伍所有，要求最终结果排名前5的队伍提供算法代码与系统报告（包括方法说明、数据处理、参考文献和使用开源工具等信息），供会议交流。
5.	奖金可折算为差旅费使用。
6.	本评测联系人：柳明睿（liumingrui@uir.edu.cn）

## 重要日期
时区：GMT+08:00
| 事项  | 时间 |
| ------------- | ------------- |
| 任务发布与报名启动  | 2023年10月1日  |
| 数据集发布  | 2023年10月7日  |
| 提交截止（报名结束）  | 2023年11月10日  |
| 比赛结果公布  | 2023年11月12日  |
| 评测论坛 | 2023年11月24日（暂定）  |

## 比赛结果

## 评测论坛安排

## 评测评委会委员
李斌阳 魏忠钰 毛存礼 李岩 孔祥宇 柳明睿 陈蕾

