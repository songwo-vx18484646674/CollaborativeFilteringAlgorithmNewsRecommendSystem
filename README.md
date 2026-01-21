# 基于协同过滤算法的个性化新闻推荐系统
# Collaborative Filtering News Recommend System Online
 基于协同过滤算法的个性化新闻推荐系统的设计与实现（采用Java语言的SpringBoot和SSM两种框架分别实现基于用户、物品的协同过滤推荐算法）实现了UserCF和ItemCF的协同过滤推荐算法。
Java语言（SpringBoot和SSM框架都有实现）实现协同过滤算法新闻推荐系统，使用**基于用户、物品的协同过滤推荐算法**通过**python爬虫**爬取环球日报新闻实现**实时计算推荐**。
**源码获取**：[基于协同过滤算法新闻推荐系统源码.zip](https://github.com/songwo-153/CollaborativeFilteringNewsRecommendSystem/files/13557079/default.zip)

**项目系统创新点**：

使用了基于用户和基于物品，根据评分和收藏数据，进行混合推荐，及将两种协同过滤
推荐算法的结果全部输出，同时采用基于用户选择的新闻类型喜好标签统计的热点推荐解决冷启动和数据稀疏性问题。

**冷启动**：一个新用户第一次登录，没有评分和收藏数据，那么没有办法进行个性化推荐；

**数据稀疏性**：会伴随项目的整个运行过程，比如：项目刚上线，新闻数据很多，但是用户及用户的评分、收藏数据较少，用户之间没有交集，那么有些用户就没有推荐结果

**开发工具**：IDEA，jdk1.8，Mysql8，navicat数据库管理工具，Tomcat，Maven.
**后端使用**：SpringBoot和SSM(Spring+SpringMVC+Mybatis)两种开发框架实现（可选）。
**前端使用**：javascript脚本，jquery脚本，用户端使用bootstrap前端框架，管理员端使用layui前端框架，layer弹窗组件等。

## 智能新闻推荐系统项目在线演示地址：
（推荐用谷歌浏览器【1月15左右到期】 ，服务器性能较差，访问有点慢，请稍微等待）
## 项目在线演示地址：（推荐用谷歌浏览器，服务器性能较差，访问有点慢）：
服务器性能较低，可能访问比较慢，服务器到期时间（4月22日）
第1款基于协同过滤算法的个性化新闻推荐系统，在线功能演示地址。

第1款（用电脑浏览器访问）

前台用户系统访问地址：
[http://8.137.32.208:8081/NewsRecommendWeb/](http://8.137.32.208:8081/NewsRecommendWeb/)

后台管理系统访问地址：
[http://8.137.32.208:8081/NewsRecommendWeb/admin/login](http://8.137.32.208:8081/NewsRecommendWeb/admin/login) 

————————————————————————————————————————————————————————————

第2款基于协同过滤算法的个性化新闻推荐系统，在线功能演示地址。
第2款（用电脑浏览器访问）

前台用户系统访问地址：
[http://8.137.32.208:8080/NewsRecommendOnline/](http://8.137.32.208:8080/NewsRecommendOnline/)

后台管理系统访问地址：
[http://8.137.32.208:8080/NewsRecommendOnline/admin/login](http://8.137.32.208:8080/NewsRecommendOnline/admin/login)

# 功能实现

**系统前台**：用户具有注册、登录、注销、浏览新闻、搜索新闻、信息修改、密码修改、喜好标签、新闻评分、新闻收藏、新闻评论、排行榜、热点推荐、个性化推荐新闻等功能；

**后台管理系统**：管理员可以查看数据统计、用户管理、新闻管理、新闻类型管理、评分管理、收藏管理、评论管理、浏览记录管理、用户喜好标签等。

**协同过滤推荐功能**：

 1. **热点榜单**
	 根据数据库的新闻数据查询浏览数量最多的新闻进行推荐，同时查询出来的是不包括当前登录用户已经浏览过的新闻（过滤当前用户已经浏览过的新闻）；
 2. **个性化推荐**

    2.1. **游客**：根据新闻总评分和总收藏数量降序查询输出向游客推荐。
    
    2.2. **登录用户**：
    
    **基于用户的协同过滤推荐算法**：根据新闻的评分数据采用基于用户的协同过滤推荐算法实时计算向用户进行新闻推荐；如果没有推荐结果，采用根据登录用户选择的喜好标签下的新闻的总评分降序推荐，同时推荐的新闻是过滤掉当前登录用户已经评分过的新闻；
    
   **基于项目的协同过滤推荐算法**：根据新闻的收藏数量采用基于项目的协同过滤推荐算法从高到低降序向用户进行推荐；如果没有推荐结果，采用根据登录用户喜好标签下的新闻的收藏数量降序推荐，同时推荐的是当前登录用户没有收藏过的新闻。
   
4. **相关推荐**：

     推荐当前登录用户正在浏览的新闻相同类型下评分较高的新闻，同时推荐的是当前用户没有评分的新闻。
   
**新闻数据来源**：爬取环球日报新闻数据  

**源码获取：**[基于协同过滤算法新闻推荐系统源码.zip](https://github.com/songwo-153/CollaborativeFilteringNewsRecommendSystem/files/13557079/default.zip)
![image](https://github.com/user-attachments/assets/4ba0ea64-95aa-48a1-98ee-c372b28a3db4)


**项目结构**
![数据库](https://github.com/user-attachments/assets/cf42b259-4699-4059-b666-f2e4b89787e6)
![项目结构](https://github.com/user-attachments/assets/39ce7a44-8f6a-4abd-9756-e3f6157847da)

**前台用户系统**
![01](https://github.com/user-attachments/assets/c2a90c89-4dcc-4c9d-ad5a-847e33de66f5)
![02](https://github.com/user-attachments/assets/a74d4a21-4e06-48ea-b849-77308a1f2cd5)
![个人中心](https://github.com/user-attachments/assets/0784ab43-2c98-49de-9202-49f7bc56a119)
![个人中心兴趣标签](https://github.com/user-attachments/assets/87bed9ba-9aed-4eb1-a9fa-47ae87e06bbf)
![个人中心用户收藏](https://github.com/user-attachments/assets/9f74e8d9-b075-461d-900c-a23f161edb4c)

**后台管理系统**
![后台登录](https://github.com/user-attachments/assets/0ebb9706-76ee-451e-a4d1-cce2deddeede)
![后台管理首页](https://github.com/user-attachments/assets/2129910e-7d65-474c-a1ed-68b4dd8596ff)
![后台管理新闻管理](https://github.com/user-attachments/assets/7828732f-5c93-42e2-906e-0dedfa127bde)
![后台管理管理员管理](https://github.com/user-attachments/assets/59c9de84-2198-4fb5-bacc-42ff867aeba2)
![后台管理用户管理](https://github.com/user-attachments/assets/98c8f79b-bc1d-49a0-8106-8368302c37b3)

**协同过滤推荐算法**
![01基于用户推荐](https://github.com/user-attachments/assets/271a8e6b-6fce-4fb3-9a5b-6529eaf49ff3)
![基于物品的推荐](https://github.com/user-attachments/assets/bc22e8c7-1c84-4236-b2d9-b515143a19a1)
![微信图片编辑_20241210133240](https://github.com/user-attachments/assets/04b8382d-84c8-4073-8e5c-0827c8e22f7f)


**Python爬取环球网新闻**
![Pythom爬取环球网新闻数据](https://github.com/user-attachments/assets/5a102a36-2b6b-48b9-a90e-faecaee489d0)

**源码获取**：[基于协同过滤算法新闻推荐系统源码.zip](https://github.com/songwo-153/CollaborativeFilteringNewsRecommendSystem/files/13557079/default.zip)



