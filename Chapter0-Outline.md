# Chapter 0 Pre-requisites

## 课程资源

课程网站

[CMU-15445-Fall2022](https://15445.courses.cs.cmu.edu/fall2022/schedule.html)

课程视频

[Youtube-CMU15445-Fall2022](https://www.youtube.com/playlist?list=PLSE8ODhjZXjaKScG3l0nuOiDTTqpfnWFf)

课本PDF

[CMU-15-445-Fall2022-EN](https://github.com/root-hbx/Database-Systems-CMU15445/tree/main/Book)

[CMU-15-445-Fall2022-CN](https://github.com/root-hbx/Database-Systems-CMU15445/tree/main/Book)

实验教程

[CMU15445-通关指北](https://zhuanlan.zhihu.com/p/637960746)

[Database](https://github.com/ysj1173886760/Learning/tree/master/db)

- Course Policies + Schedule: Course Web Page
- Discussion + Announcements: Piazza
- Homeworks + Projects: Gradescope
- Final Grades: Canvas

## EDUCATIONAL OBJECTIVES

This is an upper-level course on the internals of database management systems. This course has a heavy emphasis on programming projects. There are also readings assigned for each class, homeworks, and two exams. Upon successful completion of this course, the student should be able to:

- Use relational algebra to express database queries.
- Use SQL to interact with database management systems.
- Design appropriate database tables, using functional dependencies and normal forms.
- Implement a disk-oriented database storage manager with table heaps and indexes.
- Understand, compare, and implement the fundamental concurrency control algorithms.
- Implement database recovery algorithms and verify their correctness.
- Identify trade-offs among database systems techniques and contrast distributed/parallel alternatives for both on-line transaction processing and on-line analytical workloads.
- Interpret and comparatively criticize database system architectures.

## 实验亮点

在 15-445 中你需要在四个 Project 的推进中，实现一个面向磁盘的传统关系型数据库 Bustub 中的部分关键组件。

包括 Buffer Pool Manager (内存管理), B Plus Tree (存储引擎), Query Executors & Query Optimizer (算子们 & 优化器), Concurrency Control (并发控制)，分别对应 `Project #1` 到 `Project #4`。

在实现的过程中可以通过 `shell.cpp` 编译出 `bustub-shell` 来实时地观测自己实现部件的正确与否，正反馈非常足。

此外 bustub 作为一个 C++ 编写的中小型项目涵盖了程序构建、代码规范、单元测试等众多要求，可以作为一个优秀的开源项目学习。

## mySQL 环境配置

>在macOS上配置mySQL

__Configuration__

```sh
brew install mysql
```

```sh
brew services start mysql
mysql_secure_installation
```

__Login__

```sh
mysql -u root -p
```

And you can access your own mySQL account to test, for example:

__Create__

```sh
CREATE DATABASE your_database_name;
```

```sh
USE your_database_name;
```

```sh
CREATE TABLE your_table_name (
    id INT AUTO_INCREMENT PRIMARY KEY,
    column1 VARCHAR(255),
    column2 INT
);
```

__Set__

```sh
INSERT INTO your_table_name (column1, column2) VALUES ('bxhu', 112);
```

__Check__

```sh
SELECT * FROM your_table_name;
```

