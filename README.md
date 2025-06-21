# 基于 AI 助手的个人博客系统-前端

* 本项目是AI驱动型个人博客系统。
* 前端地址：https://github.com/FanWeiyi/carolynblog-front

## 🔧 技术栈

- **前端**：Vue3 + TypeScript + Pinia + Vite
- **后端**：Spring Boot + MySQL + DeepSeek API + Docker
- **AI 功能**：集成 DeepSeek API，智能推荐相关文章或总结

## 📦 功能模块

- 主页
![主页](images\ce3424046938647c2c351cbc79877f8.png)
- 博客发布/编辑/展示:Markdown 格式支持
![博客](images\3c0185a3e6183675378d358e55cde88.png)
- 登录/注册功能
![登录](images\a9fc7517208c75a8d0a8a6f3c544763.png)
- AI 快捷助手（检索数据库内容，推荐或总结）
![AI](images\0ddb607450cfcd4281dbc1f6353f5a9.png)
- 美图分享模块（支持跳转来源链接）
![生活](images\fd2c09b8d53fdf942c710f248a4d6d2.png)

## 🧠 AI 模块功能

用户输入关键词 → AI 自动分析意图 → 检索数据库博客标题 → 返回推荐结果或摘要内容或总结

## 🚀 快速启动

## 项目设置
1. 打开文件
   `src/main/java/com/example/studytwo/controller/DeepseekController.java`，配置你的 **DeepSeek API Key**：

2. 编辑后端配置文件
   `studytwo/src/main/resources/application.yml`，`docker-compose.yml` 设置数据库连接信息：

    ```application.yml
    environment:
      MYSQL_ROOT_PASSWORD: 你的密码
      MYSQL_DATABASE: my-blog         
    ```

   ```application.yml
   spring:
     datasource:
       url: jdbc:mysql://localhost:3306/你的数据库名字?useSSL=false&serverTimezone=Asia/Shanghai
       username: root
       password: 你的密码
       driver-class-name: com.mysql.cj.jdbc.Driver
   ```

3. 运行docker compose

   * 命令行运行：

     ```bash
     docker-compose up
     ```
     
4. 将提供的 SQL 文件导入至本地 MySQL 数据库，确保包含：

    * `user` 表
    * `blog` 表
    * `user_file` 等核心表结构


5. 使用 Maven 重载依赖：

    * IDEA：右侧 Maven 面板点击刷新 🔄
    * 或命令行运行：

      ```bash
      mvn clean install
      ```

6. 启动 IDEA，运行后端项目（`CarolynBlogApplication.java` 主类）或命令行执行：

   ```bash
   mvn spring-boot:run
   ```

---

## ✅ 系统配置完成，前后端即可联动运行 🎉

访问地址示例：

* 前端： [http://localhost:5173/](http://localhost:5173/)
* 后端： [http://localhost:8080/](http://localhost:8080/)

