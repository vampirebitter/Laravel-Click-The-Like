# Laravel-Click-The-Like
在Laravel中，使用Ajax，Redis，Amaze UI实现点赞功能的简单实例
*能实现的效果* 
点赞之后显示1,取消后显示0,没有总计数统计(因为没有加入用户登录之类的东西)
首页会显示后台当前的点赞情况
### 基本思路
#### Redis 
使用 `redis` 代替 数据库的一部分功能。

- 主要思路是设计`Ajax`计数器，当用户点赞之后，计数器加一，把数据提交到对应的后台控制器。
- 然后控制器中执行`Redis`相关操作

注意：因为只是一个简单的demo，这里并没有写相关的用户生成cookie来判断是否已点过赞而是直接通过查询来拿到的
#### Ajax
通过返回的json数据来拿到当前是否点赞

### 部署方式

- clone the repository

```
$ git clone https://github.com/vampirebitter/Laravel-Click-The-Like.git
```

- composer compoents

```
$ composer install
```

注意这里webpack的方式是通过gulp实现
