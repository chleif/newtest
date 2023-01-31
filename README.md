# newMemberSystem

資料庫：
1.開啟mssql

2.連線local伺服器
    -伺服器名稱：(localdb)\mssqllocaldb

3.新增資料庫
    -資料庫名稱：MemberSystem

4.建立資料表：
    -請執行下列語法：
    CREATE TABLE [dbo].[Member](
	[MemberID] [int] NOT NULL,
	[FirstName] [nvarchar](50) NULL,
	[LastName] [nvarchar](50) NULL,
	[password] [nvarchar](50) NULL,
	[CreaeTime] [datetime] NULL,
	[Administor] [bit] NULL,
	[UserId] [nvarchar](10) NULL,
	[SessionId] [nchar](50) NULL,
PRIMARY KEY CLUSTERED 
(
	[MemberID] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON, OPTIMIZE_FOR_SEQUENTIAL_KEY = OFF) ON [PRIMARY]
) ON [PRIMARY]
GO

5.製作假資料
    -請執行下列語法
    INSERT INTO Member(MemberID,FirstName,LastName,password,Administor,UserId)
VALUES(1,'Nihu','Bad','456',1,'123');

專案：
1.下載Visual Studio 2022社群版 (https://visualstudio.microsoft.com/zh-hant/downloads/)
2.安裝ViSual Studio 2022
    -勾選
        *ASP.NET與網頁程式開發
        *Azure開發
        *.NET桌面開發
        *適用Windows平台開發
        *資料儲存和處理
        *Visual Studio擴充功能開發

3.安裝完成後開啟檔案：
    NewMemberSystem\NewMemberSystem\NewMemberSystem.sln

4.開啟方案總管
5.在方案'NewMemberSystem' 按右鍵點選還原NuGet套件
6.按下F5執行專案

執行功能：
1.點選註冊，並自行註冊
2.點選登入，輸入註冊的帳號密碼或以假資料帳號密碼登入
3.登入後會導向編輯個人資料頁面
4.進行資料修改並送出
5.按下登出
