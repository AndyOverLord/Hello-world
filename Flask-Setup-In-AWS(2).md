


> Written with [StackEdit](https://stackedit.io/).
> ## How to start a easiest app with flask in AWS

- We need to set Security Group for the instance we created in AWS.
	1. choose the SG, create a new rule for 'custom TCP rule' as flask set the port 5000, otherwise we could just create HTTP which will default open port 80. 
	2. A more secure way is to write your own IP address so that only you can access the development server.
	3. When trying the [Quick Start](http://flask.palletsprojects.com/en/1.1.x/quickstart/), remember to set the Debug Mode and allow it accessible for us.
	`export FLASK_ENV=development`
	`flask run --host=0.0.0.0`
	As AWS SG has taking care of the security responsiblity for us if you follow above settting.

- After the above final set up, you can then use the URL that AWS provided (public one) adding the port 5000 to  access the easiest app in browser.
- At this point, we basically have a proper setup development server in AWS which we use VSCode remote SSH connected with. And we can also use local broswer (or any broswers we trust to test it -- if we provide a range of IP address in AWS SG) 

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc1Nzk2NTgzOV19
-->