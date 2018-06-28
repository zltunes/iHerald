> 先声iOS客户端 
[在 itunes 查看](https://itunes.apple.com/cn/app/xian-sheng/id871801426?mt=8)

# 编译环境
    OS X 10.11.1
    Xcode-Version 7.1.1
# 支持平台
	iOS 7.1 以上
# 测试机型
	iPhone 4S
	iPhone 5
	iPhone 5S
	iPhone 6
	iPhone 6 Plus
	iPhone 6S
	iPhone 6S Plus
	
主  页|校园生活|学习讲座|图书馆
------------ | ------------- | ------------| ------------
![图片1][1]|![图片2][2]|![图片3][3]|![图片4][4]

抽屉交互|校园外卖|simisimi|设 置
------------ | ------------- | ------------| ------------
![图片5][5]|![图片6][6]|![图片7][7]|![图片8][8]

# 项目目录简介

1. **Libraries/** 第三方库
2. **Herald/** 主目录
	1. **LoginControllers/** 信息门户登录和个人资料补全
	
	2. **SchoolLifeControllers/** 校园功能：
		+ **RunningViewController** 跑操查询  
		+ **EmptyRoomViewController** 空闲教室  
		+ **CurriculumViewController** 课表查询  
		+ **AcademicViewController** 教务查询  
		+ **NicViewController** 校园网查询  
		+ **SeuCardViewController** 一卡通查询  
		+ **SeuCardTableViewController** 一卡通详情查询  
	3. **StudyLectureControllers** 学习讲座功能：
		+ **GradeViewController** GPA查询  
		+ **SRTPViewController** SRTP查询  
		+ **ExamViewController** 考试查询
		+ **LabTableViewController** 物理实验查询  
		+ **LectureViewController** 人文讲座查询  
		+ **LecturePredictTableViewController** 人文讲座预告
		+ **LecturePredictDetailViewController** 人文讲座详情
	3. **LibraryControllers/** 图书馆功能：  
		+ **LibNavViewController** 图书馆地图  
		+ **SearchBookViewController** 图书搜索  
		+ **BorrowedBooksViewController** 已借图书查询  
		+ **BorrowedBooksViewController** 图书续借  
		+ **SchoolBusViewController** 校车时刻  
	
	4. **TakeOutControllers/** 外卖模块  
	
	5. 其他视图控制器：  
		+ **CenterViewController.swift** 首页模块  
		+ **LeftDrawerTableViewController** 左侧抽屉列表导航模块  
		+ **CommonNavViewController** 左侧抽屉视图控制器  
		+ **SimsimiViewController.swift** SimSimi模块  
		+ **SettingsViewController.swift** 设置页面 
	 
	6. 其他工具类或者代理类：  
		1. **AppDelegate.swift** 应用入口代理 
		2. **Tool.swift** 加载动画效果的封装，以及一个便携初始化普通VC的方法initNavigationAPI()    
		3. **Config.swift** 包括了所有需要存储在用户本地UserDefault的控制类    
		4. **API.swift**    核心API封装类，对于普通的VC，首先要声明实现APIGetter接口，然后定义一个HeraldAPI全局对象，并且设置代理为自己，即可以使用相应的API，包括：    
	***sendAPI()***   //通过API标签tag和参数列表String...来调用响应API请求    
	***getResult()***   //获得结果    
	***getError()***    //错误处理

3. **Pictures/** 图片资源
4. **Supporting Files/** 存放属性表    
	1. **API List.plist** 核心API列表的数据，用XML存储，确保URL是正确，参数列表里面，uuid或者appid一定放在最后一个，并且所有参数顺序和代码中传入参数顺序一致即可。加入新的API请在这里改动，并在对应的VC中加入调用参数和方法，API.swift不需要做任何改动！    
	2. **Info.plist** 项目配置文件

  [1]: http://ww4.sinaimg.cn/large/005tGCqhjw1f1mb94249dj30ku112agq.jpg
  [2]: http://ww2.sinaimg.cn/large/005tGCqhjw1f1mb9q16oyj30ku112n1p.jpg
  [3]: http://ww1.sinaimg.cn/large/005tGCqhjw1f1mba6c1z3j30ku112aft.jpg
  [4]:http://ww4.sinaimg.cn/large/005tGCqhjw1f1mbfsw6pxj30ku112n5j.jpg
  [5]:http://ww3.sinaimg.cn/large/005tGCqhjw1f1mbi5hmq6j30ku1127al.jpg
  [6]:http://ww2.sinaimg.cn/large/005tGCqhjw1f1mbjybgg5j30ku1120yn.jpg
  [7]:http://ww2.sinaimg.cn/large/005tGCqhjw1f1mbinbwf8j30ku112jxn.jpg
  [8]:http://ww4.sinaimg.cn/large/005tGCqhjw1f1mbah0i1zj30ku112whi.jpg
