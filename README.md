

# 🧑‍💻 SEU校园在线聊天系统（SEULink）

> 本项目是东南大学22级软工课程项目设计

> 一个基于 Spring Boot + FreeMarker + WebSocket + MySQL 实现的高可扩展性在线即时聊天系统，支持用户好友管理、群聊管理、消息通信等功能。

---

## 📌 项目简介

本项目为基于 B/S 架构设计的即时聊天系统，致力于提供一个安全、高效、可扩展的在线沟通平台。项目采用 Spring Boot 构建后端服务，FreeMarker 渲染前端页面，结合 WebSocket 实现即时消息通信，数据持久化采用 MySQL 数据库。

适用于：

* 小型社交平台
* 内网通讯工具
* Java Web 开发教学项目

---

## 🚀 项目特性

* 👥 **用户系统**：注册、登录、资料修改、聊天状态管理
* 💬 **消息通信**：点对点聊天、群聊、聊天记录查看
* 👨‍👩‍👧‍👦 **好友系统**：好友申请、黑名单、备注管理
* 🧑‍🏫 **管理员系统**：系统设置、用户管理、聊天记录监管
* 📊 **数据库设计**：ER 图设计完善，13张核心业务表
* 🔐 **权限控制**：基于角色管理系统权限
* 📄 **系统日志**：后台操作日志记录

---

## 🧰 技术栈

| 层级   | 技术                                      |
| ---- | --------------------------------------- |
| 前端   | HTML, CSS, JavaScript, Ajax, FreeMarker |
| 后端   | Java 8, Spring Boot, Spring MVC, JPA    |
| 实时通信 | WebSocket                               |
| 数据库  | MySQL 5.7                               |
| 项目管理 | Maven                                   |
| 开发工具 | IntelliJ IDEA / Eclipse                 |
| 部署方式 | 本地部署 / JAR 启动                           |

---

## 🖥️ 系统架构

标准的 MVC + DAO 分层架构：

```
View(Freemarker) ↔ Controller(Spring MVC) ↔ Service(Business Logic) ↔ DAO(JPA) ↔ MySQL
```

支持多人群聊、消息状态同步、好友状态推送、管理后台等。

---

## 📷 界面预览

> 部分前端页面使用 FreeMarker + Bootstrap 构建，样式简洁现代。

| 登录页面                                                    | 主聊天页面                                                 | 后台管理                                                     |
| ------------------------------------------------------- | ----------------------------------------------------- | ------------------------------------------------------- |
| ![login](https://github.com/poloSnow-0926/SEULink/blob/master/src/main/resources/static/admin/images/login.png) | ![chat](https://github.com/poloSnow-0926/SEULink/blob/master/src/main/resources/static/admin/images/chat.png) | ![group](https://github.com/poloSnow-0926/SEULink/blob/master/src/main/resources/static/admin/images/home_1.png) |

---

## 📦 快速部署指南

### 1. 克隆项目

```bash
git clone https://github.com/yourname/chat-online.git
cd chat-online
```

### 2. 配置数据库

修改 `src/main/resources/application-dev.properties`：

```properties
spring.datasource.url=jdbc:mysql://127.0.0.1:3306/db_chatonline
spring.datasource.username=root
spring.datasource.password=your_password
```

导入数据库脚本（可参考文档 `doc/db_chatonline.sql`）

### 3. 启动项目

```bash
mvn clean install
java -jar target/chatonline-1.0-SNAPSHOT.jar
```

访问地址：[http://localhost:8081](http://localhost:8081)

---

## 📁 项目结构简述

```
├── src
│   ├── main
│   │   ├── java/com/seu/base/        # 核心后端逻辑
│   │   ├── resources
│   │   │   ├── templates/                # FreeMarker 页面
│   │   │   ├── static/                   # 静态资源
│   │   │   └── application.properties
├── doc/                                  # 开发文档
├── pom.xml
└── README.md
```

---

## 🧪 测试说明

系统包含完整测试用例，涵盖功能测试和用户行为模拟。支持使用 `JUnit + Jacoco` 进行覆盖率检测。





