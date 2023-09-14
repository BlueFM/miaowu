# 数据库设计文档 - 流浪猫信息分享网站

## 1. 用户表 (User)

### 字段
- `user_id` (主键): 用户唯一标识符 (整数)
- `username`: 用户名 (字符串)
- `password_hash`: 密码哈希值 (字符串)
- `email`: 电子邮件地址 (字符串)
- `created_at`: 用户账户创建时间 (日期时间)

## 2. 流浪猫信息表 (StrayCatInfo)

### 字段
- `cat_id` (主键): 流浪猫信息唯一标识符 (整数)
- `title`: 流浪猫信息标题 (字符串)
- `description`: 流浪猫信息描述 (文本)
- `image_url`: 流浪猫图片URL (字符串)
- `location_lat`: 流浪猫地理位置纬度 (浮点数)
- `location_lng`: 流浪猫地理位置经度 (浮点数)
- `created_at`: 信息发布时间 (日期时间)

## 3. 评论表 (Comment)

### 字段
- `comment_id` (主键): 评论唯一标识符 (整数)
- `cat_id` (外键): 关联的流浪猫信息 (整数)
- `user_id` (外键): 发表评论的用户 (整数)
- `content`: 评论内容 (文本)
- `created_at`: 评论发布时间 (日期时间)

