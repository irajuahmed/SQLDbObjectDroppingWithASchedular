# DB Object Dropping With a SQL Server Job Schedular From Demo Environment.
Some time we need setup a demo environment to our client server for a specific time/period/days. Suppose after your trial period you may not have access to client server or you may forgot delete your setup environment. That's why I've made one/two SP &amp; a SQL Job Scheduler to delete the demo SQL environment/DB objects automatically from your client server/machine.

### File & Descriptions: Here I've added two follwing MS SQL Server Scripts.
-   [ObjectDroppingDBScriptWithData.sql](https://github.com/erajuahmed/DbObjectDroppingWithASchedular/blob/main/ObjectDroppingDBScriptWithData.sql) : In this script I've made a       simple database, created some SQL objects (table, view, procedure, trigger, function) & finally inserted some data into these tables in order to demonstrate my work process       with a real scenario visualization.  
-   [uspSevenDaysTrial.sql](https://github.com/erajuahmed/DbObjectDroppingWithASchedular/blob/main/uspSevenDaysTrial.sql): In this script I've done follwoing things to reach our       goal.
    1. Created a SP named **_"uspSevenDaysTrialAlterAllObj"_** : This is not our main SP. This SP will be called if don't have drop permission for our logged user.
    2. Created a SP named **_"uspSevenDaysTrial"_**: and this is not our main SP. This SP will be primarily. If user don't have drop permission then execption will occured 
       then CATCH block will execute where we'll call our alter object SP named **_"uspSevenDaysTrialAlterAllObj"_**.
    3. At last I created a SQL Job Schedular named **_"TrialJob"_**.
     
