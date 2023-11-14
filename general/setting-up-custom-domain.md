# Setting up a Custom Domain with Crowdbotics Projects

Once the project is ready to go live and we have received a confirmation from the client:
- Go to CB Dashboard for the project
- From the left menu column, choose **Settings**
- On the Settings page, choose the **API** tab and then the **Production** tab
- Under **Custom Domain**, click on the **Update** button
- On the **Set Custom Domain** dialogbox please enter the desired domain name. Please ensure to prefix the domain name with **www**, like **www.mywebsite.com**

Please follow the steps as described in the official manual from CB:
https://knowledge.crowdbotics.com/how-do-i-create-a-custom-domain-for-my-build

- Once you have the CNAME ( which looks something like **a-very-long-string.....herokudns.com** ), copy this value.
- Log into GoDaddy (or your Domain Registrar)
- Under **Domain DNS** records, paste the copied value for the CNAME record for Name=www. Save the changes.
- Then, under **Forwarding**, add forwarding for primary domain to **https://www.mywebsite.com**

HTTPS will apply automatically from the CB infrastructure.

Check the website on browser in 10 min (DNS propagation usually takes around 10 minutes to 4 hours)
