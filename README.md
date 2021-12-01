# DB Object Dropping With a SQL Server Job Schedular From Client's Demo Hosting Environment. 
Some time we need setup a demo environment to our client server for a specific time/period/days. Suppose after your trial period you may not have access to client server or you may forgot delete your setup environment. That's why I've made one/two SP &amp; a SQL Job Scheduler to delete the demo SQL environment/DB objects automatically from your client server/machine.

### File & Descriptions: Here I've added two follwing MS SQL Server Scripts.
-   [ObjectDroppingDBScriptWithData.sql](https://github.com/erajuahmed/DbObjectDroppingWithASchedular/blob/main/ObjectDroppingDBScriptWithData.sql) : In this script I've made a       simple database, created some SQL objects (table, view, procedure, trigger, function) & finally inserted some data into these tables in order to demonstrate my work process       with a real scenario visualization. If you've a database already you may skip this step. For that, please take a backup of your database for safety purpose. 
-   [uspTrialDemo.sql](https://github.com/erajuahmed/DbObjectDroppingWithASchedular/blob/main/uspTrialDemo.sql): In this script I've done follwoing things to reach our       goal.
    1. Created a SP named **_"uspTrialDemo"_** : This is not our main SP. This SP will be called if don't have drop permission for our logged user.
    2. Created a SP named **_"uspTrialAlterAllObj"_**: and this is not our main SP. This SP will be primarily. If user don't have drop permission then execption will occured 
       then CATCH block will execute where we'll call our alter object SP named **_"uspTrialAlterAllObj"_**.
    3. At last I created a SQL Job Schedular named **_"TrialJob"_**.
     
<h1 align="center">The End</h1>

<table align="center">
<tr><th>Find me on following(s)</th><th>Support me on</th></tr>
<tr><td>

| [<img src="https://github.com/irajuahmed/irajuahmed/blob/main/images/github.png" alt="github logo" width="34">](https://github.com/irajuahmed) | [<img src="https://github.com/irajuahmed/irajuahmed/blob/main/images/instagram.jpg" alt="instagram logo" width="24">](https://www.instagram.com/marginalraju/) | [<img src="https://github.com/irajuahmed/irajuahmed/blob/main/images/Linkedin.png" alt="Linkedin Logo" width="24">](https://www.linkedin.com/in/raju-ahmed-263475126/)| [<img src="https://github.com/irajuahmed/irajuahmed/blob/main/images/stack.svg" alt="stack logo" width="24">](https://stackoverflow.com/users/5615778) 
|---|---|---|---|

</td><td>

<p><a href="https://www.buymeacoffee.com/https://www.buymeacoffee.com/mIUyB3X5P"> <img align="left" src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" height="50" width="210" alt="https://www.buymeacoffee.com/mIUyB3X5P" /></a></p>

</td></tr> </table>
