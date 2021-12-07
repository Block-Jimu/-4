实验四
一、实验目的
掌握Java中类的定义
掌握staticfinal等修饰符的用法
了解异常的使用方法，并在程序中根据输入情况做异常处理
二、实验要求
1.基本描述
某学校为了给学生提供勤工俭学机会，选派了部分学生参与实验室的卫生清洁工作。每个学生被分配若干间实验室，视实验室的清洁打分情况给予劳务补贴。
例如：学生“张三”负责了“计算机网络实验室”、“组成原理实验室”的清洁情况，每周被检查。在某次检查中，“计算机网络实验室”卫生得“优”，“组成原理实验室”卫生得“及格”，一次“优”按x元记录补助，一次“及格”按y元记录补助。（卫生标准分级、相应的等级补助标准，自行规定）
按国家的税务制度，劳务费应按国家规定纳税，请统计一学期学生的实际收入。（国家最新工资纳税标准，请自行检索）
2.基本要求
设计系统中的类（如学生、实验室等等）
一学期按18周计
每个学生负责的实验室数量不一定相同
对学期勤工俭学收入和纳税进行统计，求得实际收入
国家最新纳税标准（系数），属于某一时期的特定固定值，与实例化对象没有关系，考虑如何用staticfinal修饰定义
根据处理情况，要在程序中考虑做异常处理
三、解题思路
首先定义student()、test()、slaray()对应录入学生信息、模拟系统导入（主体）、工资导出，之后在Student类中定义6个参数（stuName;ManageLabName1;ManageLabName2;ManageLabName3;LabNumber;getMoney;），并对这六个参数进行简单的函数构造。 运用toString() 方法返回此对象本身，为后面Test类的引用做准备。在Lab类中定义了4个参数（Labname1;Labname2;Labname3;Labgrade;），并对这四个参数进行了简单的构造。salary类按国家的税务制度统计一学期学生的实际收入。Test类对前三个类进行汇总，之后编写捕捉异常处理的方法； 输出学生信息、实验室信息、学生所获得的补助金额等基本信息
四，关键代码
Test类
public Student(String stuName, double getMoney, String ManageLabName1, String ManageLabName2,String ManageLabName3) {
	super();
}
public String toString() {
	return "姓名：" + stuName + "    收入：" + getMoney + "    负责的实验室为：" + ManageLabName1 + ", " + ManageLabName2 + "," + ManageLabName3 ;
}
public Student(String stuName, double getMoney, String ManageLabName1, String ManageLabName2) {
	super();
}
public String toString1() {
	return "姓名：" + stuName + "    收入：" + getMoney + "    负责的实验室为：" + ManageLabName1 + ", " + ManageLabName2 ;
}
public Student(String stuName, double getMoney, String ManageLabName1) {
		super();
}
public String toString3() {
		return "姓名：" + stuName + "    收入：" + getMoney + "    负责的实验室为：" + ManageLabName1;
	}
}
