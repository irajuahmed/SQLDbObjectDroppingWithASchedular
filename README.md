# DB Object Dropping With a SQL Server Schedular
Some time we need setup a demo environment to our client server for a specific time/period/days. Suppose after your trial period you may not have access to client server or you may forgot delete your setup environment. That's why I've made one/two SP &amp; a SQL Job Scheduler to delete the demo SQL environment/DB objects automatically from your client server/machine.

### Get Started: Here I've added two follwing MS SQL Server Scripts.
-   [ObjectDroppingDBScriptWithData.sql](https://github.com/erajuahmed/DbObjectDroppingWithASchedular/blob/main/ObjectDroppingDBScriptWithData.sql) : In this script I've made a simple database, created some sql objects (table,view,porcedue, trigger, function) & finally inserted some data into these tables in order to demonstrate my work process with a real scenario visualisation.
-   [uspSevenDaysTrial.sql](https://github.com/erajuahmed/DbObjectDroppingWithASchedular/blob/main/uspSevenDaysTrial.sql)
