![CLEVER DATA GIT REPO](https://raw.githubusercontent.com/LiCongMingDeShujuku/git-resources/master/0-clever-data-github.png "李聪明的数据库")

# 如何在Amazon RDS中创建SQL实例
#### How To Create An SQL Instance In Amazon RDS
**发布-日期: 2015年5月4日 (评论)**

## Contents

- [中文](#中文)
- [English](#English)
- [Build Info](#Build-Info)
- [Author](#Author)
- [License](#License) 


## 中文
如何在Amazon RDS中创建 SQL Server Database Instance。

## English
How to create an SQL Server Database Instance in Amazon RDS.


Login to AWS: Amazon Web Services 
登陆AWS: Amazon Web Services
1.
Supply your Amazon AWS Account name, Username, and Password, and click ‘Sign in’.
1. 键入你的Amazon AWS 账户名称，用户名和密码，单击“Sign in”。

![#](images/01-如何在Amazon-RDS中创建SQL实例.png?raw=true "#")
 
2.
Select ‘RDS’.

![#](images/02-如何在Amazon-RDS中创建SQL实例.png?raw=true "#")


2.选择 ‘RDS’. 

3.
Select ‘Instances’.
3.选择“Instances”

![#](images/03-如何在Amazon-RDS中创建SQL实例.png?raw=true "#")
 
4.
Select ‘Launch DB Instance’.
4.选择 ‘Launch DB Instance’.

![#](images/04-如何在Amazon-RDS中创建SQL实例.png?raw=true "#")

 
5.
Complete the following actions:
a. Select ‘SQL Server’.
b. Click the ‘Enterprise Edition’ option ( sqlserver-ee ).
5.完成以下操作：
a.选择“SQL Server”。
b.单击“Enterprise Edition”选项（sqlserver-ee）。

![#](images/05-如何在Amazon-RDS中创建SQL实例.png?raw=true "#")

 
6.
For the Dev-Cloud environment select the following options.
a. DB Engine: sqlserver-ee
b. License Model: bring-your-own-license
c. DB Engine Version: 11.00.2100.60.v1 (RTM)
Note: This is pre SP1, SP2, so updates will need to be applied following creation.
d. DB Instance Class: db.m3.medium – 1 vCpu, 3.75
e. Multi-AZ Deployment:
f. Storage Type: General Purpose SSD
There are 3 types of Storage, but ‘General Purpose SSD’ should be sufficient for most standard workloads.
6.对于Dev-Cloud环境，请选择以下选项。
a. 数据库引擎： sqlserver-ee
b. 许可证模型： bring-your-own-license
c. 数据库引擎版本：11.00.2100.60.v1（RTM）
注意：这是SP1 SP1之前的版本，因此需要在创建后更新。
d.数据库实例类：db.m3.medium  -  1 vCpu，3.75
e.多可用区部署：
F.存储类型：通用SSD
存储有3种类型，但“General Purpose SSD”应满足大多数标准工作负载的需求。

![#](images/06-如何在Amazon-RDS中创建SQL实例.png?raw=true "#")
 
1. General Purpose (SSD): Suitable for a broad range of database workloads. Provides baseline of 3 IOPS/GB and the ability to burst to 3,000 IOPS.
1.通用（SSD）：适用于广泛的数据库工作负载。具有3 IOPS /GB的基准和扩展到3,000 IOPS的能力。
2. Provisioned IOPS (SSD): Suitable for I/O-Intensive database workloads. Provides flexibility to provision I/O ranging form 1,000 to 30,000 IOPS.
2.预配置IOPS（SSD）：适用于I / O密集型数据库工作负载。 提供灵活性，可提供1,000到30,000 IOPS的I / O范围。
3. Magnetic Storage: Used for small database workloads where data is accessed less frequently.
3.磁存储：用于较少访问数据的小型数据库工作负载。
Note:
Make sure to select the Storage type that best fits your database environment. The storage type CANNOT be changed once the instance is created. ‘Scaling Storage’ is not supported for SQL Server in Amazon RDS.
注意：
确保选择最适合你的数据库环境的存储类型。创建实例后，不能更改存储类型。Amazon RDS中的SQL Server不支持“Scaling Storage”。
g. Allocated Storage*:
g.分配存储*：
Note1:
If you are selecting storage greator than 20 GB, this will disqualify the instance from being supported on the ‘free tier’.
注1：
如果你选择的存储大于20 GB，则不符合该实例在“free tier”上的支持。
Note2:
If you select a medium storage type; you must select a VPC on the following Step3 Configure Advanced Settings. Storage is dependent on the VPC.
注2：
如果选择一个中型存储类型; 你必须在步骤3配置高级设置中（Configure Advanced Settings）选择VPC。存储取决于VPC。

![#](images/07-如何在Amazon-RDS中创建SQL实例.png?raw=true "#")
 
h. DB Instance Identifier: MyInstanceName
Note: Instance Name must be under 15 characters.
h. 数据库实例标识符：MyInstanceName
注意：实例名称必须小于15个字符。
i. Master Username: MySaUserName
Note: This represents the ‘sa’ account in SQL Server.
i.主用户名：MySaUserName
注意：这表示SQL Server中的“sa”帐户。
j. Master Password: MyNewPassword
j.主密码: MyNewPassword

k. Confirm Password: MyNewPassword
k. 确认密码：MyNewPassword
Click ‘Next Step’ after the correct selections have been made.
完成正确的选择后，单击“Next Step”。

![#](images/08-如何在Amazon-RDS中创建SQL实例.png?raw=true "#")
 
7.
Click ‘Launch DB Instance’.
7. 单击“Launch DB Instance”。

![#](images/09-如何在Amazon-RDS中创建SQL实例.png?raw=true "#")
 
8.
The Wizard will proceed to create the instance at this point. No more selections need to be made.
8.Wizard将在此时继续创建实例。不需要做出更多选择。

![#](images/10-如何在Amazon-RDS中创建SQL实例.png?raw=true "#")

 
 
[![WorksEveryTime](https://forthebadge.com/images/badges/60-percent-of-the-time-works-every-time.svg)](https://shitday.de/)

## Build-Info

| Build Quality | Build History |
|--|--|
|<table><tr><td>[![Build-Status](https://ci.appveyor.com/api/projects/status/pjxh5g91jpbh7t84?svg?style=flat-square)](#)</td></tr><tr><td>[![Coverage](https://coveralls.io/repos/github/tygerbytes/ResourceFitness/badge.svg?style=flat-square)](#)</td></tr><tr><td>[![Nuget](https://img.shields.io/nuget/v/TW.Resfit.Core.svg?style=flat-square)](#)</td></tr></table>|<table><tr><td>[![Build history](https://buildstats.info/appveyor/chart/tygerbytes/resourcefitness)](#)</td></tr></table>|

## Author

- **李聪明的数据库 Lee's Clever Data**
- **Mike的数据库宝典 Mikes Database Collection**
- **李聪明的数据库** "Lee Songming"

[![Gist](https://img.shields.io/badge/Gist-李聪明的数据库-<COLOR>.svg)](https://gist.github.com/congmingshuju)
[![Twitter](https://img.shields.io/badge/Twitter-mike的数据库宝典-<COLOR>.svg)](https://twitter.com/mikesdatawork?lang=en)
[![Wordpress](https://img.shields.io/badge/Wordpress-mike的数据库宝典-<COLOR>.svg)](https://mikesdatawork.wordpress.com/)

---
## License
[![LicenseCCSA](https://img.shields.io/badge/License-CreativeCommonsSA-<COLOR>.svg)](https://creativecommons.org/share-your-work/licensing-types-examples/)

![Lee Songming](https://raw.githubusercontent.com/LiCongMingDeShujuku/git-resources/master/1-clever-data-github.png "李聪明的数据库")

