# NJUSE影院管理系统MAMS(Museum Activity Management System)用例文档

# V1.2 正式版

## 2019/03/17

## 更新历史

| 修改人员 | 日期 | 变更原因 | 版本号 |
| --- | --- | --- | --- |
| 许竣博 | 2019/03/17 | 最初的草稿 | V0.9 beta版 |
| 江辉 | 2019/03/19 | 统一文档格式 | V0.91 beta版 |
| 周际宇 | 2019/03/28 | 修改文档互评中对方指出的不合适的地方 | V1.0 正式版 |

## 目录

* [1.引言](#1%E5%BC%95%E8%A8%80)
  * [1.1 目标](#11-%E7%9B%AE%E6%A0%87)
  * [1.2 阅读说明](#12-%E9%98%85%E8%AF%BB%E8%AF%B4%E6%98%8E)
  * [1.3 参考文献](#13-%E5%8F%82%E8%80%83%E6%96%87%E7%8C%AE)
* [2.用例图](#2%E7%94%A8%E4%BE%8B%E5%9B%BE)
* [3.用例列表](#3%E7%94%A8%E4%BE%8B%E5%88%97%E8%A1%A8)
* [4.详细用例描述](#4%E8%AF%A6%E7%BB%86%E7%94%A8%E4%BE%8B%E6%8F%8F%E8%BF%B0)
  * [用例1 上架影片](#%E7%94%A8%E4%BE%8B1-%E4%B8%8A%E6%9E%B6%E5%BD%B1%E7%89%87)
  * [用例2 查看影片详情](#%E7%94%A8%E4%BE%8B2-%E6%9F%A5%E7%9C%8B%E5%BD%B1%E7%89%87%E8%AF%A6%E6%83%85)
  * [用例3 统计预售影片的想看人数](#%E7%94%A8%E4%BE%8B3-%E7%BB%9F%E8%AE%A1%E9%A2%84%E5%94%AE%E5%BD%B1%E7%89%87%E7%9A%84%E6%83%B3%E7%9C%8B%E4%BA%BA%E6%95%B0)
  * [用例4 标记某电影为想看](#%E7%94%A8%E4%BE%8B4-%E6%A0%87%E8%AE%B0%E6%9F%90%E7%94%B5%E5%BD%B1%E4%B8%BA%E6%83%B3%E7%9C%8B)
  * [用例5 搜索电影(日期，名称等)](#%E7%94%A8%E4%BE%8B5-%E6%90%9C%E7%B4%A2%E7%94%B5%E5%BD%B1%E6%97%A5%E6%9C%9F%E5%90%8D%E7%A7%B0%E7%AD%89)
* [5.需求分析模型](#5%E9%9C%80%E6%B1%82%E5%88%86%E6%9E%90%E6%A8%A1%E5%9E%8B)
  * [5.1 系统顺序图](#51-%E7%B3%BB%E7%BB%9F%E9%A1%BA%E5%BA%8F%E5%9B%BE)
    * [用例1 上架电影](#%E7%94%A8%E4%BE%8B1-%E4%B8%8A%E6%9E%B6%E7%94%B5%E5%BD%B1)
    * [用例2 查看影片详情](#%E7%94%A8%E4%BE%8B2-%E6%9F%A5%E7%9C%8B%E5%BD%B1%E7%89%87%E8%AF%A6%E6%83%85-1)
    * [用例3 统计预售影片想看人数](#%E7%94%A8%E4%BE%8B3-%E7%BB%9F%E8%AE%A1%E9%A2%84%E5%94%AE%E5%BD%B1%E7%89%87%E6%83%B3%E7%9C%8B%E4%BA%BA%E6%95%B0)
    * [用例4 标记影片为想看](#%E7%94%A8%E4%BE%8B4-%E6%A0%87%E8%AE%B0%E5%BD%B1%E7%89%87%E4%B8%BA%E6%83%B3%E7%9C%8B)
    * [用例5 搜索电影](#%E7%94%A8%E4%BE%8B5-%E6%90%9C%E7%B4%A2%E7%94%B5%E5%BD%B1)
  * [5.2 概念类图](#52-%E6%A6%82%E5%BF%B5%E7%B1%BB%E5%9B%BE)
    * [用例1 上架影片](#%E7%94%A8%E4%BE%8B1-%E4%B8%8A%E6%9E%B6%E5%BD%B1%E7%89%87)
    * [用例2 查看影片详情](#%E7%94%A8%E4%BE%8B2-%E6%9F%A5%E7%9C%8B%E5%BD%B1%E7%89%87%E8%AF%A6%E6%83%85)
    * [用例3 统计预售影片想看人数](#%E7%94%A8%E4%BE%8B3-%E7%BB%9F%E8%AE%A1%E9%A2%84%E5%94%AE%E5%BD%B1%E7%89%87%E6%83%B3%E7%9C%8B%E4%BA%BA%E6%95%B0)
    * [用例4 标记影片为想看](#%E7%94%A8%E4%BE%8B4-%E6%A0%87%E8%AE%B0%E5%BD%B1%E7%89%87%E4%B8%BA%E6%83%B3%E7%9C%8B)
    * [用例5 搜索电影](#%E7%94%A8%E4%BE%8B5-%E6%90%9C%E7%B4%A2%E7%94%B5%E5%BD%B1)
  * [5.3状态图](#53%E7%8A%B6%E6%80%81%E5%9B%BE)
    * [用例1 上架影片](#%E7%94%A8%E4%BE%8B1-%E4%B8%8A%E6%9E%B6%E5%BD%B1%E7%89%87)
    * [用例2 查看影片详情](#%E7%94%A8%E4%BE%8B2-%E6%9F%A5%E7%9C%8B%E5%BD%B1%E7%89%87%E8%AF%A6%E6%83%85)
    * [用例3 统计预售影片想看人数](#%E7%94%A8%E4%BE%8B3-%E7%BB%9F%E8%AE%A1%E9%A2%84%E5%94%AE%E5%BD%B1%E7%89%87%E6%83%B3%E7%9C%8B%E4%BA%BA%E6%95%B0)
    * [用例4 标记影片为想看](#%E7%94%A8%E4%BE%8B4-%E6%A0%87%E8%AE%B0%E5%BD%B1%E7%89%87%E4%B8%BA%E6%83%B3%E7%9C%8B)
    * [用例5 搜索电影](#%E7%94%A8%E4%BE%8B5-%E6%90%9C%E7%B4%A2%E7%94%B5%E5%BD%B1)

## 1.引言

本文档描述了影院活动管理系统的用户及管理者需求。开发小组的软件系统实现与验证工作都以此文档为依据。

本文档所包含的需求等级用数字表示，数值越高优先级越高。

本文档的内容可能在项目实施过程中发生变更，但是必须由项目小组成员发出变更请求，小组讨论，最终决定，建立持续有效的版本控制。

### 1.1 目标

本文档描述了影院活动管理系统的用户需求。

### 1.2 阅读说明

无

### 1.3 参考文献

1.IEEE std 1471-2000
2.《影院管理系统MAMS需求最新版0418》
3.丁二玉，刘钦.计算与软件工程（卷二）[M]机械工业出版社，2012：134~182
4.Frank Buschmann, Regine Meunier, Hans Rohnert, Peter Sommerlad, Micheael Stal.Pattern-Oriented Software Architecture Volume 1: A system of Patterns [M]机械工业出版社,2003

## 2.用例图

![](https://cdn.nlark.com/yuque/0/2019/png/291791/1553083674015-ed88f39f-1159-4a77-9887-4daf68fd8100.png#align=left&display=inline&height=531&originHeight=1025&originWidth=1440&size=0&status=done&width=746#align=left&display=inline&height=531&originHeight=1025&originWidth=1440&status=done&width=746)

## 3.用例列表


## 4.详细用例描述



## 5.需求分析模型


### 5.1 系统顺序图


#### 用例1 上架电影

![](https://raw.githubusercontent.com/D-Mer/learngit/master/%E5%A4%A7%E4%BD%9C%E4%B8%9A%E5%9B%BE/%E6%B5%81%E7%A8%8B%E5%9B%BE/%E6%B5%81%E7%A8%8B%E5%9B%BE-%E4%B8%8A%E6%9E%B6%E5%BD%B1%E7%89%87.jpg#align=left&display=inline&height=818&originHeight=1021&originWidth=931&status=done&width=746)


#### 用例2 查看影片详情

![](https://raw.githubusercontent.com/D-Mer/learngit/master/%E5%A4%A7%E4%BD%9C%E4%B8%9A%E5%9B%BE/%E6%B5%81%E7%A8%8B%E5%9B%BE/%E6%B5%81%E7%A8%8B%E5%9B%BE-%E6%9F%A5%E7%9C%8B%E5%BD%B1%E7%89%87%E8%AF%A6%E6%83%85.jpg#align=left&display=inline&height=1003&originHeight=1121&originWidth=834&status=done&width=746)


#### 用例3 统计预售影片想看人数

![](https://raw.githubusercontent.com/D-Mer/learngit/master/%E5%A4%A7%E4%BD%9C%E4%B8%9A%E5%9B%BE/%E6%B5%81%E7%A8%8B%E5%9B%BE/%E6%B5%81%E7%A8%8B%E5%9B%BE-%E7%BB%9F%E8%AE%A1%E9%A2%84%E5%94%AE%E5%BD%B1%E7%89%87%E7%9A%84%E6%83%B3%E7%9C%8B%E4%BA%BA%E6%95%B0.jpg#align=left&display=inline&height=1003&originHeight=1121&originWidth=834&status=done&width=746)


#### 用例4 标记影片为想看

![](https://raw.githubusercontent.com/D-Mer/learngit/master/%E5%A4%A7%E4%BD%9C%E4%B8%9A%E5%9B%BE/%E6%B5%81%E7%A8%8B%E5%9B%BE/%E6%B5%81%E7%A8%8B%E5%9B%BE-%E6%A0%87%E8%AE%B0%E6%9F%90%E7%94%B5%E5%BD%B1%E4%B8%BA%E6%83%B3%E7%9C%8B.jpg#align=left&display=inline&height=1007&originHeight=1007&originWidth=686&status=done&width=686)


#### 用例5 搜索电影

![](https://raw.githubusercontent.com/D-Mer/learngit/master/%E5%A4%A7%E4%BD%9C%E4%B8%9A%E5%9B%BE/%E6%B5%81%E7%A8%8B%E5%9B%BE/%E6%B5%81%E7%A8%8B%E5%9B%BE-%E6%90%9C%E7%B4%A2%E7%94%B5%E5%BD%B1.jpg#align=left&display=inline&height=814&originHeight=814&originWidth=544&status=done&width=544)


### 5.2 概念类图


#### 用例1 上架影片

![](https://raw.githubusercontent.com/D-Mer/learngit/master/%E5%A4%A7%E4%BD%9C%E4%B8%9A%E5%9B%BE/%E6%A6%82%E5%BF%B5%E7%B1%BB%E5%9B%BE/%E6%A6%82%E5%BF%B5%E7%B1%BB%E5%9B%BE-%E4%B8%8A%E6%9E%B6%E5%BD%B1%E7%89%87.jpg#align=left&display=inline&height=507&originHeight=519&originWidth=764&status=done&width=746)


#### 用例2 查看影片详情

![](https://raw.githubusercontent.com/D-Mer/learngit/master/%E5%A4%A7%E4%BD%9C%E4%B8%9A%E5%9B%BE/%E6%A6%82%E5%BF%B5%E7%B1%BB%E5%9B%BE/%E6%A6%82%E5%BF%B5%E7%B1%BB%E5%9B%BE-%E6%9F%A5%E7%9C%8B%E5%B7%B2%E4%B8%8A%E6%9E%B6%E7%94%B5%E5%BD%B1.jpg#align=left&display=inline&height=562&originHeight=562&originWidth=334&status=done&width=334)


#### 用例3 统计预售影片想看人数

![](https://raw.githubusercontent.com/D-Mer/learngit/master/%E5%A4%A7%E4%BD%9C%E4%B8%9A%E5%9B%BE/%E6%A6%82%E5%BF%B5%E7%B1%BB%E5%9B%BE/%E6%A6%82%E5%BF%B5%E7%B1%BB%E5%9B%BE-%E7%BB%9F%E8%AE%A1%E9%A2%84%E5%94%AE%E5%BD%B1%E7%89%87%E7%9A%84%E6%83%B3%E7%9C%8B%E4%BA%BA%E6%95%B0.jpg#align=left&display=inline&height=491&originHeight=493&originWidth=749&status=done&width=746)


#### 用例4 标记影片为想看

![](https://raw.githubusercontent.com/D-Mer/learngit/master/%E5%A4%A7%E4%BD%9C%E4%B8%9A%E5%9B%BE/%E6%A6%82%E5%BF%B5%E7%B1%BB%E5%9B%BE/%E6%A6%82%E5%BF%B5%E7%B1%BB%E5%9B%BE-%E6%A0%87%E8%AE%B0%E6%9F%90%E7%94%B5%E5%BD%B1%E4%B8%BA%E6%83%B3%E7%9C%8B.jpg#align=left&display=inline&height=504&originHeight=504&originWidth=721&status=done&width=721)


#### 用例5 搜索电影

![](https://raw.githubusercontent.com/D-Mer/learngit/master/%E5%A4%A7%E4%BD%9C%E4%B8%9A%E5%9B%BE/%E6%A6%82%E5%BF%B5%E7%B1%BB%E5%9B%BE/%E6%A6%82%E5%BF%B5%E7%B1%BB%E5%9B%BE-%E6%90%9C%E7%B4%A2%E7%94%B5%E5%BD%B1(%E6%97%A5%E6%9C%9F%EF%BC%8C%E5%90%8D%E7%A7%B0%E7%AD%89).jpg#align=left&display=inline&height=488&originHeight=491&originWidth=750&status=done&width=746)


### 5.3状态图


#### 用例1 上架影片

![](https://raw.githubusercontent.com/D-Mer/learngit/master/%E5%A4%A7%E4%BD%9C%E4%B8%9A%E5%9B%BE/%E7%B3%BB%E7%BB%9F%E7%8A%B6%E6%80%81%E5%9B%BE/%E7%B3%BB%E7%BB%9F%E7%8A%B6%E6%80%81%E5%9B%BE-%E4%B8%8A%E6%9E%B6%E5%BD%B1%E7%89%87.jpg#align=left&display=inline&height=308&originHeight=530&originWidth=1282&status=done&width=746)


#### 用例2 查看影片详情

![](https://raw.githubusercontent.com/D-Mer/learngit/master/%E5%A4%A7%E4%BD%9C%E4%B8%9A%E5%9B%BE/%E7%B3%BB%E7%BB%9F%E7%8A%B6%E6%80%81%E5%9B%BE/%E7%B3%BB%E7%BB%9F%E7%8A%B6%E6%80%81%E5%9B%BE-%E6%9F%A5%E7%9C%8B%E5%BD%B1%E7%89%87%E8%AF%A6%E6%83%85.jpg#align=left&display=inline&height=351&originHeight=589&originWidth=1252&status=done&width=746)


#### 用例3 统计预售影片想看人数

![](https://raw.githubusercontent.com/D-Mer/learngit/master/%E5%A4%A7%E4%BD%9C%E4%B8%9A%E5%9B%BE/%E7%B3%BB%E7%BB%9F%E7%8A%B6%E6%80%81%E5%9B%BE/%E7%B3%BB%E7%BB%9F%E7%8A%B6%E6%80%81%E5%9B%BE-%E6%90%9C%E7%B4%A2%E7%94%B5%E5%BD%B1(%E6%97%A5%E6%9C%9F%EF%BC%8C%E5%90%8D%E7%A7%B0%E7%AD%89).jpg#align=left&display=inline&height=401&originHeight=538&originWidth=1001&status=done&width=746)


#### 用例4 标记影片为想看

![](https://raw.githubusercontent.com/D-Mer/learngit/master/%E5%A4%A7%E4%BD%9C%E4%B8%9A%E5%9B%BE/%E7%B3%BB%E7%BB%9F%E7%8A%B6%E6%80%81%E5%9B%BE/%E7%B3%BB%E7%BB%9F%E7%8A%B6%E6%80%81%E5%9B%BE-%E6%A0%87%E8%AE%B0%E5%BD%B1%E7%89%87%E4%B8%BA%E6%83%B3%E7%9C%8B.jpg#align=left&display=inline&height=449&originHeight=473&originWidth=786&status=done&width=746)


#### 用例5 搜索电影

![](https://raw.githubusercontent.com/D-Mer/learngit/master/%E5%A4%A7%E4%BD%9C%E4%B8%9A%E5%9B%BE/%E7%B3%BB%E7%BB%9F%E7%8A%B6%E6%80%81%E5%9B%BE/%E7%B3%BB%E7%BB%9F%E7%8A%B6%E6%80%81%E5%9B%BE-%E8%B4%AD%E7%A5%A8.jpg#align=left&display=inline&height=522&originHeight=522&originWidth=521&status=done&width=521)
