# DNS-practice
Domain Names


## This repo aims to:
- Utilize my flask app from flask-with-db repo and deploy via GCP VM
- Create an A record that links together my domain with the IP address of my flask app deployed on GCP



# Register a domain name using .TECH
- Using [get.tech](https://get.tech/github-student-developer-pack) 
- Domain Name: **briattneythomas.tech**

# Create an (A) record that links together the domain with the IP address of your flask app deployed on GCP
- Under your get.tech Control Panel, navigate to **Manage Orders > List/Search Orders**
- Select your new domain name and scroll down to **DNS Management**
- Select **Manage DNS**
- Under **(A) Records** > **Add a Record**
    -       Host Name: @
            Destination IP Address: [ VM External IP Address]
            TTL: 7200
- Under **NS Records** > **Add NS Record**
    -       Zone: @ (briattneythomas.tech)
            Value: www (briattneythomas.tech)
            TTL: 7200
           
# To create a subdomain:
- Under **(A) Records** > **Add a Record** #2
    -       Host Name: app
            Destination IP Address: [GCP VM External IP Address]
            TTL: 7200
- In your app.py file, change @app.route('/', subdomain=app)
- Verify changes work: app.briattneythomas.tech

# Set Up GCP VM 
- By following instructions from **setup_GCP.md** 
- Verify flask is deployed by refreshing your domain name in your browser


# **Images** folder
- Contains screenshots of the live flask app deployed on my website