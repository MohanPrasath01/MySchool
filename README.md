# MySchool
MySchool is a application built for school students with in-app notification system.It contains section tabs like Home,Me,Notifications,Approvals etc.,
Through this application a student can view the announcements from the student during this lockdown period when new assignments or modules has been posted.
Not only through the application the students can receive the notification through their registered mail id.
There is a option with academic calender which shows the timeline of exams,holidays and events.
Through the approval tab the students can notify the admin/teacher that they finished their assingments and they verified their grades.
There is a another tab called 'Tasks'.In that they can view their assignments separately.
As a admin,he/she can maintain the student database separately.
Admin can post announcements that will visible to the students.
The admin can send announcements via the calendar option that will be more graphical with colors.
In the approval tab there is two sections pending tasks and completed tasks.In the pending tasks the students can verify them and in the completed task the verified tasks are visible for further referneces.
The grades for specific exams are posted and visible for the students for their approvals.
Though it is a in-app notification enabled it is very usefull for the students.It is more efficient.
# Database
The students details are stored in the admin database.
So the informations are easily fetched.
# Language
The language used is Deluge which is a Data Enriched Language.
It is one of the fastest and most flexible scripting languages available.
it is a one-stop solution for performing actions and integrations across the suite.
It is cloud offering that provides infrastructure for serverless development and deployment of application functionalities.
# Admin
<%{
	currentYear = Add_Current_Academic_Year[ID != 0].Academic_Year;
	studentsCount = Add_Grade[Drop_Down == currentYear].Students.getAll().size();
	employeeCount = Add_Employee[Employee_Status == "Active"].count();
	subjectCount = Add_Subject[ID != 0].count();
	holidaysCount = Add_to_Academic_Calender[Type == "Holiday" && Academic_Year == currentYear].sum(No_of_Days);
	%>
<style>
.col-sm-6 {
    width: 100%;
}
.view-header>.row h3 {
    font-size: 19px;
    color: #333945;
    line-height: 40px;
    font-weight: inherit;
}
.view-header>.row {
    margin-left: -21px;
	
}
.row {
    padding-top: 4px;
    margin-left: -15px;
    margin-right: 0px;
}
.customBadge
						  {
						  width:100%;
						  //height:100%;
						  border:1px solid white;
						  border-radius:3px;
						  background:white;
						  display:inline-block;
						  height: 92px;
						  }
						  .iconDiv
						  {
						  width: 35%;
						  //height:100%;
						  border-radius: 3px 0px 0px 3px;
						  //padding:20px 0px 20px 0px;
						  padding:6% 0px;
						  float:left;
						  padding-left : 5%;
						  }
						  .iconDiv .zc-li-solid
						  {
						  font-size: 60px;
						  //color: white;
						  }
						   .contentDiv
						  {
						  //height:100%;
						  float:right;
						  width:60%;
						  text-align:center;
						  //padding-top: 12px;
						  //padding-bottom: 11px;
						  padding-top: 5%;
						  padding-bottom: 4%;
						  color: #9e9e9e;
						  }
						  .numSpan
						  {
						  font-size: 33px;
						  }
						  .contentDiv font
						  {
							  font-size : 14px;
						  }
						  .row
						  {
							  padding-top: 4px;
							  margin-left : 0px;
							  margin-right : 0px;
						  }
/* 						  .zcp-col span i{
							  color: #594DFB;
						  } */
</style>
 <div class="row" >
						  <div class="col-md-3" >
						  <div class="customBadge" style="border-right:2px solid #6acbca;">
						  <div class="iconDiv" style="color: #6acbca;">
						  <i class="education-hat zc-li-solid" ></i>
						  </div>
						  <a href="#Report:Student_Details?Status=Active" target="_blank">
						  <div class="contentDiv">
						  <span class="numSpan"><%=studentsCount%></span><br>
						  <font >Total Students</font>
						  </div>
						  </a>
						  </div>
						  </div>
						  <div class="col-md-3" >
						  <div class="customBadge" style="border-right:2px solid #fb6c5e;">
						  <div class="iconDiv" style="color: #fb6c5e;">
						  <i class="zc-li-solid users-multiple-19" ></i>
						  </div>
						  <a href="#Report:Employee_Details?Status=Active" target="_blank">
						  <div class="contentDiv">
						  <span class="numSpan"><%=employeeCount%></span><br>
						  <font >Total Employees</font>
						  </div>
						  </a>
						  </div>
						  </div>
						  <div class="col-md-3" >
						  <div class="customBadge" style="border-right:2px solid #f8d347;">
						  <div class="iconDiv" style="color: #f8d347;">
						  <i class="zc-li-solid files-book-08" style="font-size: 55px;" ></i>
						  </div>
						  <a href="#Report:All_Subjects" target="_blank">
						  <div class="contentDiv">
						  <span class="numSpan"><%=subjectCount%></span><br>
						  <font >Total Subjects</font>
						  </div>
						  </a>
						  </div>
						  </div>
						  <div class="col-md-3" >
						  <div class="customBadge">
						  <div class="iconDiv" style="color: #55c8f1;">
						  <i class="zc-li-solid ui-1-calendar-check-62" style="font-size: 53px;" ></i>
						  </div>
						  <a href="#Report:Holidays" target="_blank">
						  <div class="contentDiv">
						  <span class="numSpan"><%=holidaysCount%></span><br>
						  <font>Total Holidays</font>
						  </div>
						  </a>
						  </div>
						  </div>
						  </div>
<%





