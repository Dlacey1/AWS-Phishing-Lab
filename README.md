<h1>AWS-Phishing-Lab</h1>




<h2>Description</h2>
This AWS Phishing Lab is a robust cybersecurity project designed to assess and enhance an organization's resilience against phishing attacks. Leveraging the power of GoPhish, this platform provides a secure environment within Amazon Web Services (AWS) to conduct simulated phishing campaigns. The project allows users to seamlessly deploy and manage phishing simulations, customize phishing emails, and analyze user interactions—all within the scalable and flexible infrastructure of AWS.



<h2>Key Features:</h2>

Secure Phishing Simulations: Create and execute simulated phishing campaigns in a controlled AWS environment.
Customizable Email Templates: Design convincing phishing emails tailored to specific scenarios and organizational needs.
User Behavior Analysis: Track and analyze user interactions to gauge the effectiveness of phishing awareness training.
AWS Integration: Utilize the scalability and security features of AWS to deploy and manage phishing simulations.
This project serves as a valuable tool for organizations looking to educate and train their personnel on recognizing and mitigating phishing threats. It emphasizes responsible and ethical use for educational purposes, helping strengthen cybersecurity defenses in today's dynamic threat landscape.

<h2>Languages and Utilities Used</h2>

- <b>AWS</b> 
- <b>EC2</b>
- <b>VPC</b>
- <b>S3</b>
- <b>GoPhish</b>




<h2>Program walk-through:</h2>

<p align="center">
1.	Go to AWS Marketplace and subscribe GoPhish from HailBytes. There is a Free Trial for one week so clean up after lab as necessary.  <br/>
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture1.png>
<br />
<br />
2.	Next click continue to configuration  <br/>
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture2.png>
<br />
<br />
3.	Leave Default configuration and click Continue to Launch  <br/>
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture3.png>
<br />
<br />
4.	Next Go to VPC Settings and click on the Create VPC in EC2 hyperlink <br/>
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture4.png>
<br />
<br />
5.	Click Create VPC button in top right corner.   <br/>
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture5.png>
<br />
<br />
6.	Enter this configuration for the VPC  <br/>
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture6.png>
<br />
<br />
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture7.png>
<br />
<br/>
Result:  
<br/>
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture8.png>
<br />
<br />  
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture9.png>
<br />
<br />
7.	Click view VPC and ensure that the VPC you created matches the selected VPC for GoPhish (You may need to hit refresh for it to show).  <br/>
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture10.png>
<br />
<br />
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture11.png>
<br />
<br />
8.	Ensure your VPC is Public (it will say it in the name).   <br/>
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture12.png>
<br />
<br />
9.	Next confirm you have the correct subnet connected from you VPC <br/>
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture13.png>
<br />
<br />
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture14.png>
<br />
<br />
10.	Next click on Create New Based On Seller Settings to create a new security group.    <br/>
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture15.png>
<br />
<br />
11.	Create a new key pair for GoPhish
 <br/>
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture16.png>
<br />
<br />
12.	And select it in the new security group you created.  <br/>
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture17.png>
<br />
<br />
13.	Now go back to the subnet of your VPC from earlier and enable Auto Assign public IPV4 Address (Click actions and select subnet setting from the dropdown menu). Don’t forget to click save!  <br/>
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture18.png>
<br />
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture19.png>
<br />
<br />
14.	After saving you can now click launch on your EC2 instance (If you launch before you enable Auto Assign Public IP then your instance will not have a public IP and you will not be able to access it properly for the lab.) If this happens terminate your current instance and then create a new instance from your GoPhish subscription, enter in the setting and groups already created for your vpc, security group, etc and then launch the new EC2 instance.
  <br/>
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture20.png>
<br />
<br />
15.	Next go you your EC2 dashboard and select the new EC2 instance (It probably has no name as show here). Go ahead and assign it a name.  <br/>
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture21.png>
<br />
16.	Now select the instance and go inside. Click open address next to the Public IPV4 DNS.
 <br/>
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture22.png>
<br />
<br />
17.	The page will say it cannot be reached.   <br/>
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture23.png>
<br />
<br />
18.	In the taskbar select the address and add :3636 to the end and hit enter. 
The page will now say you connection is not private. Click on Advanced then select to proceed at the bottom of the page. 
You page will now display the GoPhish login screen. 
  <br/>
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture24.png>
<br />
<br />
19.	As per GoPhish’s instructions, the login will be admin, and the password will be the instance ID. 
  <br/>
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture25.png>
<br />
<br />
20.	Congratulations! You now have an EC2 instance running GoPhish and can create a phishing campaign.   <br/>
<img src=https://github.com/Dlacey1/AWS-Phishing-Lab/blob/main/images/Picture26.png>
<br />
<br />
