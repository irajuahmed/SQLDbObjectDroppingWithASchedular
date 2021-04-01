# DB Object Dropping With a SQL Server Job Schedular From Client's Demo Hosting Environment.
Some time we need setup a demo environment to our client server for a specific time/period/days. Suppose after your trial period you may not have access to client server or you may forgot delete your setup environment. That's why I've made one/two SP &amp; a SQL Job Scheduler to delete the demo SQL environment/DB objects automatically from your client server/machine.

### File & Descriptions: Here I've added two follwing MS SQL Server Scripts.
-   [ObjectDroppingDBScriptWithData.sql](https://github.com/erajuahmed/DbObjectDroppingWithASchedular/blob/main/ObjectDroppingDBScriptWithData.sql) : In this script I've made a       simple database, created some SQL objects (table, view, procedure, trigger, function) & finally inserted some data into these tables in order to demonstrate my work process       with a real scenario visualization. If you've a database already you may skip this step. For that, please take a backup of your database for safety purpose. 
-   [uspTrialDemp.sql](https://github.com/erajuahmed/DbObjectDroppingWithASchedular/blob/main/uspSevenDaysTrial.sql): In this script I've done follwoing things to reach our       goal.
    1. Created a SP named **_"uspTrialDemo"_** : This is not our main SP. This SP will be called if don't have drop permission for our logged user.
    2. Created a SP named **_"uspTrialAlterAllObj"_**: and this is not our main SP. This SP will be primarily. If user don't have drop permission then execption will occured 
       then CATCH block will execute where we'll call our alter object SP named **_"uspSevenDaysTrialAlterAllObj"_**.
    3. At last I created a SQL Job Schedular named **_"TrialJob"_**.
     

<h3 align="left">Connect with me:</h3>
<p align="left">
<a href="https://linkedin.com/in/www.linkedin.com/in/raju-ahmed-263475126" target="blank"><img align="center" src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/linkedin.svg" alt="www.linkedin.com/in/raju-ahmed-263475126" height="30" width="40" /></a>
<a href="https://stackoverflow.com/users/5615778" target="blank"><img align="center" src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/stackoverflow.svg" alt="5615778" height="30" width="40" /></a>
</p>


<h3 align="left">Support:</h3>
<p><a href="https://www.buymeacoffee.com/https://www.buymeacoffee.com/mIUyB3X5P"> <img align="left" src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" height="50" width="210" alt="https://www.buymeacoffee.com/mIUyB3X5P" /></a></p><br><br>
