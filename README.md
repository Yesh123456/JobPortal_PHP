
# Job Portal

The online job portal application allows job seekers and recruiters to connect.The application provides the ability for job seekers to create their accounts, upload their profile and resume, search for jobs, apply for jobs, view different job openings. The application provides the ability for companies to create their accounts, search candidates, create job postings, and view candidates applications.
## Installation

Install my-project as zip or clone.

```bash
    git clone https://github.com/Yesh123456/Job-Portal.git
```
Install PHP and PHPmyadmin.(For Ubuntu)

```bash
    sudo apt install php
    sudo apt install php-myadmin
```
Install Lampp or Zampp.
```bash
    sudo apt install lampp
```
Run your application and create and import sql file from folder.

Check db.php file and change configuration accordingly
```bash
    $servername = "localhost";
    $username = "root";
    $password = "";
    $dbname = "Your db name";
```
Now you login as candidate with following details
```bash
    Email: tushar@gmail.com	
    Password: isco123
```
Now you login as Company with following details

```bash
    Email: abhi@gmail.com
    Password: abhi123
```
Now you login as Admin with following details
```bash
    Username: admin
    Password: 123456
```
Candidates Email Confirmation:
>You CANNOT send emails from localhost server. So when you create a new candidate account it will not send any emails. So you must go to database, find that user and set ```active=1``` in order to make that account login. 

>If you are testing on real server then you can uncomment the following code from ```adduser.php```

```php
// Send Email
$to = {CANDIDATE_EMAIL ADDRESS};
$subject = "Job Portal - Confirm Your Email Address";
$message = '
    <html>
    	 <head>
		    <title>Confirm Your Email</title>
		</head>
		<body>
		    <p>Click Link To Confirm</p>
		    <a href="{YOUR_REAL_DOMAIL}/verify.php?token='.$hash.'&email='.$email.'">Verify Email</a>
		</body>
	</html>
';
$headers[] = 'MIME-VERSION: 1.0';
$headers[] = 'Content-type: text/html; charset=iso-8859-1';
$headers[] = 'To: '.$to;
$headers[] = 'From: hello@yourdomain.com';
// You can add more headers like Cc, Bcc;
$result = mail($to, $subject, $message, implode("\r\n", $headers)); // \r\n will return new line. 
if($result === TRUE) {
//If email sent successfully then Set some session variables and redirect to login page
	$_SESSION['registerCompleted'] = true;
	header("Location: login.php");
	exit();
}
```

## Features

- Relevent scheme
- Live previews
- Responsive
- Web Application

  
## Screenshots

![App Screenshot](screenshot_1.png)

## Feedback

If you have any feedback, please reach out to us at isco30427@gmail.com

  
## Badges

Add badges from somewhere like: [shields.io](https://shields.io/)

[![MIT License](https://img.shields.io/apm/l/atomic-design-ui.svg?)](https://github.com/tterb/atomic-design-ui/blob/master/LICENSEs)
[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)
[![AGPL License](https://img.shields.io/badge/license-AGPL-blue.svg)](http://www.gnu.org/licenses/agpl-3.0)

  
