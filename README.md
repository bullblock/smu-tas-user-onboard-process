# Singapore Management University Tanzu Application Service User on-bording process
<br/>
<br/>
This is bash shell script helping SMU users on-bording process, which will create and remove users from TAS.<br/>
Command syntax:<br/>
<br/>
__./tob-create -u|--adminid _admin_user_id_ -p|--adminpwd _admin_password_ -s|--server _api_server_url_ -f|--file _user_list.csv_ -r|--result _result.csv_<br/>__
<br/>
Prerequst:<br/>
A user list file is required, and the format is:<br/>
<br/>
========================================================<br/>
Item,First Name,Last Name,eMail Address,Password,Enabled<br/>
1,Steven,Liang,steven.liang@email.com,,yes<br/>
========================================================<br/>
<br/>
Example:<br/>
./tob-create -u admin -p password -s api.domain.com -f user_list.csv -r user_result.csv<br/>
./tob-clean -u admin -p password -s api.domain.com -f remove_user_list.cvs -r remove_user_result.csv<br/>
<br/>
when user creation, "Enabled" must be "yes" user will be created.<br/>
when user remove, "Enabled" will not work.<br/>
