In today's fast-paced digital world, effective communication is the backbone of productivity and success. Whether you're managing a complex DevSecOps pipeline, running a small business, or organizing personal tasks, timely and efficient notifications are critical. Enter NTFY.sh, a lightweight, open-source notification tool that offers simplicity, flexibility, and power.

In this blog post, we'll explore what NTFY.sh is, its potential use cases, and how individuals and businesses can benefit from integrating it into their daily workflows. We'll also provide practical examples and highlight best practices to make the most out of this tool. Let's dive in.

The demo and Installation Guide you will find at the end of this article and also in my YouTube video which is right under here: 

YouTube Video https://youtu.be/NtlztHT-sRw <br>
[![IMAGE ALT TEXT HERE](https://i9.ytimg.com/vi/NtlztHT-sRw/mqdefault.jpg?v=676b14cb&sqp=CLSDhMcG&rs=AOn4CLBdgvqpVtT9s6UnBWvdzwUUifeCXg)](https://youtu.be/NtlztHT-sRw)


## What is NTFY.sh?
NTFY.sh is a simple, HTTP-based notification service that allows you to send and receive notifications via REST API, Python, CURL or command-line tools. Think of it as a highly customizable and platform-independent tool for managing alerts and updates, without the overhead of more complex notification systems.

It supports real-time push notifications and integrates seamlessly with your existing workflows. You can use it with shell scripts, CI/CD pipelines, IoT devices, or even to send reminders to yourself.

## **Key Features:**

- **Easy-to-use HTTP API:** Send notifications with a single command or HTTP request.
- **Cross-platform compatibility:** Works on Windows, Linux, macOS, and mobile devices.
- **Self-hosting capability:** Secure your data by running NTFY.sh on your own server.
- **Integration-ready:** Works with tools like Docker, Home Assistant, and shell scripts.

## Why Use NTFY.sh?
While many tools promise comprehensive notification systems, NTFY.sh stands out because of its focus on simplicity and adaptability. Here's why it's worth your attention:

**1. Minimal Setup**
With no heavy dependencies or complex configurations, NTFY.sh can be up and running in minutes. Its lightweight design makes it perfect for developers and sysadmins who need quick solutions.

**2. Versatile Applications**
From alerting you about a failing server to reminding you about your next coffee break, NTFY.sh's applications are virtually endless. Its generic approach makes it useful across a wide spectrum of personal and professional tasks.

**3. Privacy and Security**
For sensitive environments, the option to self-host NTFY.sh ensures complete control over your data, unlike cloud-dependent alternatives.

**4. Cost-Effective**
Being open-source, it eliminates the licensing costs associated with commercial notification systems. Even when self-hosted, the resource requirements are minimal.

## Top Use Cases for NTFY.sh

**1. DevOps and Monitoring Alerts**
In a DevSecOps workflow, timely notifications can mean the difference between resolving an issue in seconds and dealing with hours of downtime. NTFY.sh can:

- Notify team members about failing builds in a CI/CD pipeline.
- Alert admins about anomalies detected by monitoring tools like Prometheus, Zabbix or Nagios.
- Send real-time updates when a deployment succeeds or fails.

**2. IoT and Smart Home Notifications**
With its lightweight design, NTFY.sh is an excellent choice for IoT projects:

- Receive alerts when your smart doorbell detects motion.
- Notify yourself when the temperature in your greenhouse exceeds a threshold.
- Get reminders to refill your pet's feeder when the weight sensor goes low.

**3. Personal Productivity**
For individual users, NTFY.sh can serve as a personal assistant:

- Schedule reminders for meetings, deadlines, or errands.
- Receive real-time notifications about calendar events or emails.
- Get updates on the status of long-running scripts or downloads.

**4. Small Business Operations**
NTFY.sh can streamline operations for small teams:

- Inform staff about updates in shared spreadsheets or documents.
- Alert inventory managers when stock levels are low.
- Notify customers about order statuses or service outages.

**5. Custom App Development**
For developers building apps, integrating NTFY.sh adds a robust notification layer:

- Send alerts to users for key actions, such as password resets or order confirmations.
- Implement push notifications without relying on third-party APIs.
- Use it for live monitoring during app testing.

## Benefits of Using NTFY.sh in Daily Life

**1. Improved Efficiency**
NTFY.sh reduces the cognitive load of manually checking logs, emails, or dashboards. Instead, it brings relevant information to you at the right time.

**2. Enhanced Collaboration**
Teams can stay in sync without the need for constant meetings or check-ins. NTFY.sh sends instant updates about critical events or changes.

**3. Increased Flexibility**
Unlike rigid notification systems, NTFY.sh adapts to your workflow rather than forcing you to adapt to it.

**4. Lower Costs**
No subscriptions or additional software are required. Even for advanced use cases, the cost of self-hosting is negligible.

## Best Practices for Using NTFY.sh

**1. Define Clear Notification Triggers**
Ensure that each notification serves a purpose. For example, send alerts only for critical errors in your CI/CD pipeline rather than for every minor log entry.

**2. Organize Topics**
Use topic-based notifications to categorize your alerts. For instance:
- _build-alerts_ for CI/CD pipelines
- _iot-home_ for smart home updates
- _personal-reminders_ for productivity tasks

**3. Secure Your Notifications**
If you're using NTFY.sh in a sensitive environment, enable HTTPS and configure API keys to prevent unauthorized access.

**4. Integrate with Automation Tools**
Leverage tools like **Zapier**, **IFTTT**, or custom scripts to automate notification triggers. This can save time and ensure consistency.

**5. Monitor and Optimize**
Review your notification logs periodically to identify spam or redundant alerts. This keeps your system efficient and user-friendly.

## Examples of Daily Use
**Scenario 1: Monitoring Server Uptime**
1. Use a monitoring tool like Nagios to detect server outages.
2. Configure it to send alerts via NTFY.sh when a downtime is detected.
3. Receive instant updates on your phone, ensuring prompt action.

**Scenario 2: Reminder for Routine Tasks**
1. Create a shell script that sends reminders to NTFY.sh based on a cron job or Just set NTFY schedule to do all the work.
2. Use topics like **morning-tasks** and **evening-routines**.
3. Stay on top of your daily schedule without relying on external apps.

**Scenario 3: Notification for Long-Running Scripts**
1. Add a command at the end of your script to notify NTFY.sh upon completion.
2. Get a message on your preferred device when the task is done.

## Getting Started with NTFY.sh
To help you dive into NTFY.sh, I've prepared a **step-by-step installation tutorial**, covering:

- Setting up a self-hosted instance. ( we will be using [](https://www.zone.eu)https://www.zone.eu VPS )
- Setup Docker
- Setup Docker Nginx reverse proxy and Nginx Let's encrypt
- Setup Portainer for Docker management
- Sending your first notification.

Check out the next section to get started on your journey with NTFY.sh.

## Installation

To start the installation we will need a VPS, you can host it in your Home Lab or your office server, and you can even do it locally on your laptop. But in our tutorial, we will be using [ZONE.EU](https://www.zone.eu) is a European Estonian-based hosting provider of VPS servers.

Hop over to [www.zone.eu](https://www.zone.eu) and check their offerings, you can use even the cheapest cloud VPS 1 for NTFY docker.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/f52xv6bdauapnjfzdnx4.png)

**Once you have your VPS ready we need to install docker.**
1. In many cases hosting providers ask you for security reasons to login as an Ubuntu user instead of root, this is due to security thing. So when you log into your VPS machine execute

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/8ssyc95e5uavzyqw9iqk.png)

```
sudo su
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/hq7n00xm7cqpv22z5iv1.png)

To become a root user which has all the rights and privileges to do whatever you like with your VPS server, in some cases it can ask to enter a password, but in many, it is either you become a root user or in a password place need to Just press enter.


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/mpq9czgrmdlk5o4i4a6b.png)

2. Once you are root, you can update Linux repositories and packages that are not up to date in my case zone.eu already has up-to-date repositories. To do the update Just execute
```
apt-get update && apt-get upgrade -y
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/2bwueuxf3pjhbjimvycj.png)

3. Now we can install the required software to add the Docker repository to our Ubuntu.
```
sudo apt-get install ca-certificates curl -y
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/epg3edysgj3yj6nwsvsy.png)

4. Let's add a folder where to store newly added repository keys
```
sudo install -m 0755 -d /etc/apt/keyrings
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/qjxwo8i57vp8200feegm.png)

5. Download Docker repository keys by executing the following command
```
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/2domi260uax0jm0c0y7y.png)

6. Let's add the repository to our APT sources so that Ubuntu knows where to download our requested docker software

```
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/i9jzdd69rzzufz8rbse9.png)

7.Let's update our repositories
```
sudo apt-get update
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/96h39ubr4up3g8fx1b08.png)

8. Let's now execute the following command to install the Docker
```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin -y
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/i3osjpmx1loj1na61wd2.png)

9. Let's check if Docker and Docker-compose have been installed

```
docker --version
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/i4wgc1u1226torsn16uj.png)


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ygjt0uy0uspv9u1vrhjw.png)

Docker-compose:
```
docker-compose --version
```

As you can see it isn't installed, so we need to install it separately by executing the following command.


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/573j36g0ea2wlcsvsv5v.png)

To install execute:
```
apt-get install docker-compose -y
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/cuck52jaaml1f4r0vkxa.png)

After the installation, let's check the version.
```
docker-compose --version
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/n15kd60lndwjaxi27yzr.png)


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/tvsi5mu1shnpwp6voz9v.png)

As you can see we have docker-compose installed and running. Now we can move to the next step creating a Docker network and louching Nginx Reverse proxy container to have a beautiful 95% port forwarding after that we will set Nginx Let's Encrypt to keep our containers that host web secure with Let's Encrypt SSL free certificates this is an automated process and it also renews certificates so we don't need to worry about them. Just add a few lines when we run our docker containers.

## Docker Network, Nginx Reverse proxy and Let's Encrypt SSL free.

To create a Docker network you need to execute a simple command of course you can replace valtersit with your desired network name:
```
docker network create valtersit
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/d2f6wflwvj2ic7y070h3.png)

Just like that the network is created.
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/3s7d70pdtef6aou9de8p.png)

Let's now execute our 1 Container Nginx reverse proxy to forward incoming traffic to ports 80 and 443 to the correct containers based on the hostname and port forwardings. Execute the following command:
```
docker run -d -p 80:80 -p 443:443  --net=valtersit --name=nginx-proxy --restart=always \
 -v /home/docker/containers/management/nginx:/etc/nginx/conf.d \
 -v /home/docker/containers/dhparam:/etc/nginx/dhparam  \
 -v /home/docker/containers/management/vhost.d:/etc/nginx/vhost.d  \
 -v /home/docker/containers/management/html:/usr/share/nginx/html  \
 -v /home/docker/containers/management/certs:/etc/nginx/certs \
 -v /var/run/docker.sock:/tmp/docker.sock:ro jwilder/nginx-proxy
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/sqwnq0gsoz5ox3vjcud9.png)

It will start quickly to download a docker image from Docker Hub, which will be executed once it is finished. In the above command, we are giving the container 80 and 443 ports, - net=valters ( to use our network as other containers also will be on this network ) - you can have several networks attached to each container, which can be useful if some systems you want to be only accessible between containers, not the public. -restart=always means that once we start our VPS or VPS is restarted to bring up the container.


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/h35jo0o1bpqifjmhql3a.png)

The thing that I like about [zone.eu](https://www.zone.eu) is that they have 1 Gbp/s network speed which is not cut between VPS and you get the best speed performance over the network.

Let's check how our newly created NGINX reverse proxy container is doing by executing:


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/04401xy3pevw9fbd47lj.png)

```
docker ps -a
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/yvpyndw4bdvltwmimzwm.png)

we can see that our container is up 1 minute and that is great if it is restarting then it has issues and we need to remove it by executing _docker rm <container name >_ or _docker rm <contaienr id >_, but since all is working in our case we don't need to remove. You can also inspect container logs by executing _docker logs <container name>_ or _docker logs <container id >_ the same is if you want to know more about your container you can do _docker inspect < container name >_ or _docker inspect <container id >_

## Let's now get our Nginx free Let's encrypt the container up and running, by executing:

```
sudo docker run --detach --net=valtersit --name nginx-proxy-letsencrypt --restart=always \
 -v /home/docker/containers/management/dhparam:/etc/nginx/dhparam \
 -v /home/docker/containers/management/vhost.d:/etc/nginx/vhost.d \
 -v /var/run/docker.sock:/var/run/docker.sock \
 -v /home/docker/containers/management/html:/usr/share/nginx/html \
 -v /home/docker/containers/management/certs:/etc/nginx/certs \
 -v /home/docker/containers/management/nginx:/etc/nginx/conf.d \
 -e "DEFAULT_EMAIL=myssls@valtersit.com" \
 -e "NGINX_PROXY_CONTAINER=nginx-proxy" \
 jrcs/letsencrypt-nginx-proxy-companion
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/sfinkdy5w5bjxtncobb3.png)

We have linked some folders to the same locations as our [Nginx reverse proxy](https://hub.docker.com%2Fr%2Fjwilder%2Fnginx-proxy), which is needed for [Let's Encrypt](https://hub.docker.com%2Fr%2Fjrcs%2Fletsencrypt-nginx-proxy-companion) to know about new hosts and share the generated certificates also keep an eye on expiration. Default e-mail you need to input yours, that is not a valid e-mail which I have currently inputted as it is for demo purposes. Nginx Proxy container we need to specify the name of the container that we created before this which is Nginx reverse proxy so that they can work hand in hand and the Nginx proxy is needed to work to create certificates.


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ojcvnx9q7u6n0zyzmf5v.png)

And again after execution, let's wait for 1–2 minutes and check if all is working like it should:
```
docker ps -a
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/s5y33c8xp37gj4o0yhsp.png)

We see that both of our containers are working and no restarting issues. So all looks good at first glance. Now we can move to the next step. We could now deploy [NTFY](https://ntfy.sh) container, but I would like to deploy a [Portainer](https://www.portainer.io). Why?

Because Portainer is ideal for simplifying container management, especially for teams new to Docker or Kubernetes. Its user-friendly design reduces the learning curve and helps maintain complex containerized infrastructures efficiently.

**Simplified Container Management:**
Manage Docker containers, images, volumes, and networks through an easy-to-use web interface.

**Multi-Environment Support:**
Works with standalone Docker, Docker Swarm, Kubernetes, and Azure Container Instances.

**Role-Based Access Control (RBAC):**
Assign specific roles and permissions for team collaboration.

**Container Deployment:**
Deploy and monitor containers directly from the UI without writing complex commands.

**Monitoring and Logs:**
Access real-time container performance metrics and view logs for troubleshooting.

**Template Support:**
Use pre-configured application templates to quickly deploy services.

**Remote Management:**
Manage containers on remote servers from a centralized dashboard.

## To deploy the Portainer execute:

```
docker run --detach --net=valtersit -p 9443:9443 -p 9000:9000 --name=portainer --restart=always --hostname=portainer.valtersit.com \
 -v /var/run/docker.sock:/var/run/docker.sock \
 -v /home/docker/containers/portainer:/data \
 -v /home/docker/containers/management/certs:/certs \
 -e VIRTUAL_HOST=portainer.valtersit.com \
 -e LETSENCRYPT_EMAIL=myssl@valtersit.com \
 -e LETSENCRYPT_HOST=portainer.valtersit.com \
 portainer/portainer-ce \
 --sslcert /certs/portainer.valtersit.com/cert.pem \
 --sslkey /certs/portainer.valtersit.com/key.pem
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/i3dug6hhubezt365bczt.png)


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/rb6rtz4nwqeduk21d989.png)

If you want you can play with ports to gain the benefit with port forwarding, but that I will be covering in YouTube and X shorts, so be sure to follow:

YouTube: [https://www.youtube.com/@valtersit](https://www.youtube.com/@valtersit)
X: [https://x.com/hugovalters](https://x.com/hugovalters)
Rumble: [https://rumble.com/HugoValters](https://rumble.com/HugoValters)

Key points change all hostnames and the folder names in the above command also the e-mail from portainer.valtersit.com and myssl@valters.com to your subdomain, that is active since once we run it let's encrypt will start issuing SSL certificates, so we need active working subdomain.

After executing the command, let's wait 1–2 minutes and check if our portainer is in a running state.

```
docker ps -a
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/5bi30yusm74ixp12imxg.png)

As you can see all is working no issues

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/yam3p5a0gu7s5kk8c6mg.png)

Once our portainer is working we can now go and create the portainer user: Open your browser and go to [https://www.valters.eu](https://your-subdomain.com:9443)
You should see something like this:

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/bq4et3b0ourijdhukh53.png)

Enter your desired username and password. I suggest that the password is 14 characters long including digits, capital letters, small letters, and special symbols in a shuffled mode, so that your instance is secure and the password is not well known or easy to guess. Also, Just a reminder that the full setup and walk-thru you can find here on my YouTube channel: 

[https://www.youtube.com/@valtersit](https://www.youtube.com/@valtersit)

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/jqqguasoanu407pq6zoj.png)

Once you have created your account, you should see something like this. You need to select Get Started as we don't have remote docker instances at the moment.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/zx83nyn7y824wiislraa.png)

This is our portainer where you can manage your docker environment and several settings. Also, create deploy docker containers and images. The quick review can be found on my [YouTube](https://www.youtube.com/@hugovalters) as I will not extend this article with all that and maybe will create an also separate article.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/dsfduac2mf6y57ts0476.png)

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/u000ifsg0ydm8r36c24v.png)

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/fvtan7je1fyj7hudhh5q.png)

So since we have all that also easily manageable docker environment for you, let's go back to our terminal and deploy the NTF. To do that we need to create a docker-compose.yml file, we can do that by executing the following.

To keep all clean I will create a directory under /srv/
```
mkdir /srv/docker/ && mkdir /srv/docker/startup
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/25lmhezrfvy5k5y1662x.png)

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/y4thtyqywjf0vqno7zt0.png)

Let's go to our newly created directory:
```
cd /srv/docker/startup
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/zwice83v6pwla8ss12lc.png)

Using nano ( you can use vi or vim with what you feel comfortable) create a docker-compose.yml with a following content
```
nano docker-compose.yml
```

**Content:**
```
version: '3.8'
services:
  ntfy:
    hostname: ntfy.valtersit.com
    image: binwiederhier/ntfy
    container_name: ntfy.valtersit.com
    command:
 - serve
    environment:
 - TZ=UTC
 - VIRTUAL_HOST=ntfy.valtersit.com
 - LETSENCRYPT_EMAIL=myssl@valtersit.eu
 - LETSENCRYPT_HOST=ntfy.valtersit.com
 - NTFY_BASE_URL=https://ntfy.valtersit.com
 - NTFY_AUTH_DEFAULT_ACCESS=deny-all
 - NTFY_BEHIND_PROXY=true
 - NTFY_ENABLE_LOGIN=true
    volumes:
 - /srv/docker/ntfy/cache:/var/cache/ntfy
 - /srv/docker/ntfy/config:/etc/ntfy
 - /srv/docker/ntfy/lib/:/var/lib/ntfy/
    ports:
 - 838:80
 - 438:443
    networks:
      valtersit:
    restart: unless-stopped
networks:
  valtersit:
    external: true
```
**Or you can grab it from: [https://github.com/ValtersIT/Valters-Tech-Turf/tree/main/NTFY](https://github.com/ValtersIT/Valters-Tech-Turf/tree/main/NTFY)**

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ugu13ixuqxhnyyi0xatv.png)

Save it with the nano you need to click **CTRL + X** then **Y** and **CTRL + M**
Now we can start our NTFY by executing:
```
docker-compose up -d
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/tpfu5peyxvvz9s8cefmx.png)

It quickly pulled the image and started our container, let's check what is happening by executing
```
docker ps -a
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/4xhqdncotdm84y45k5zx.png)

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/jcwwbsrhm5r496ti35ck.png)

We can see that our NTFY is working. That means that we can now create topics by going to our browser and https://<your NTFY subdomain>/ you should see something like this. I know it is insecure to have something open like this, but we will create what we need and close it down so that nobody from the internet can access it.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/k1dx8tf2tvj1ujh1ledu.png)

To create a topic we need to go to + Subscribe to topic
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/0axo84c9cpf80qezzik5.png)

Enter the topic name, you can create as many topics as you want for each case, for example
servers
deployment
alerts
etc

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/hhj4gbz2euqbo1b42hxz.png)

To do so you need to repeat this action each time. But for this example, I will be creating a one topic valtersit once I enter the name, I will click SUBSCRIBE

This is our new topic where we can post messages from the web interface and also respond to and acknowledge the messages. Your computer will also make a sound if there is a new message and the browser window is open.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/otgb6fvazi1ieq453s6n.png)

Since we have our topic, we can now close down the web-ui to do so. Let's go to our terminal and execute
```
cd /srv/docker/startup && docker-compose down
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/pj3axjcxmsk820242oti.png)

Let's create a config file in the appropriate directory.
```
cd /srv/docker/ntfy/config/
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/5vt0nrjrd74n0s113595.png)
```
nano server.yml
```

You can get the latest file with content from the NTFY official Git repository **[https://github.com/binwiederhier/ntfy/blob/main/server/server.yml](https://github.com/binwiederhier/ntfy/blob/main/server/server.yml)**
or
**[https://github.com/ValtersIT/Valters-Tech-Turf/tree/main/NTFY](https://github.com/ValtersIT/Valters-Tech-Turf/tree/main/NTFY)** - _Mine already has all the config, Just change website url_

Some changes that we need to do, is to change

add:
```
base-url: https://ntfy.valtersit.com
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/6x4kc5cdfni0cw8jf92z.png)

Add:
```
cache-file: "/var/cache/ntfy/cache.db"
cache-duration: "82h"
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/kao4c76frbej2ggmpp81.png)

Add:
```
auth-file: "/etc/ntfy/slogins.db"
auth-default-access: "deny-all"
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/0t6z6l8qlou5phqdxhmw.png)

add:
```
behind-proxy: true
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/m9ql8fu2wvv4am8f1k6r.png)

add:
```
web-root: disable
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/8y7b44kn06lvql78w449.png)

Add ( Since Apple iOS is developed differently with more security, then we need to give upstream to NTFY, the Docker container will not send any content to NTFY server, but Just say hey, ping this phone that there is a new message this is needed so that we get the push notification and don't miss any important things )
```
upstream-base-url: "https://ntfy.sh"
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/wrehyiuwb5x4mcmykjnd.png)

And that is it from the config side. Now let's save the file. If you use nano then **CTRL +X** then **Y** then **CTRL +M**

Let's start our docker container with the new configuration. Go to our directory:
```
cd /srv/docker/startup/
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/edda6r43lqt5a2kph2k8.png)

**Start docker container:**
```
docker-compose up -d
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/baaxd9ez0coipwvztmv9.png)

If we do a refresh, we can see that the website is no longer publically accessible.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/zlmzq7ewlmj84x5l62v2.png)

All is great, now you will need to create a user and token to use remote curl, python, cli and etc to send the alerts, information, etc to your apps.
You can do that from your portainer by going to your docker container and selecting terminal and sh. Or we can do that from the Linux terminal which I'm going to show you. Let's enter our docker container by executing:
```
docker exec -it ntfy.valtersit.com sh
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/pqeyxayk51zl4s0wsdwp.png)

You can find your docker container name by executing docker ps -a or use container ID instead of name.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/9mfhvjjz74vt10ulx3ys.png)

and we are in our container

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/csyq6cxfeutmq0xd1gna.png)

To create a new admin user we need to execute:
```
ntfy user add --role=admin valtersit
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/sxjrtlh673u0ir71t6dl.png)

Enter a secure password. The password will not be visible also while you type it will not show anything. When you are finished press Enter

Confirm your password
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/djpk9egjykwqjsz70ftn.png)

And our user is ready, so now let's create a token:
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/3ql7r5o4kwk64mjvkphv.png)

Create token:
```
ntfy token add valtersit
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/cpwjhgxlknmvl23ljk7p.png)

Our token is ready! With the token, we can send messages and have a layer of protectivity. To exit the docker container type exit and press Enter
```
exit
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/8yfc8lyyqlgxqkugdi6y.png)

So now all is created and we can send the messages, but to receive the messages we need to install an Android or iOS app from Google Play or Apple App store. That and how to connect them to the server is covered in my YouTube video:

{% embed https://youtu.be/NtlztHT-sRw %}

Once you have installed the apps you can now send a test message from your terminal or any terminal using curl:
```
curl -u :tk_gnrbtidohd3ggk0xenx5ubx0chufo -d "this is Just a test demo for valtersit.com" https://ntfy.valtersit.com/valtersit
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/yrp1opptshielvu81wcs.png)

You need to replace the token with your token, and the server name + topic. And as you can see I have received the message on my Phone:

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/1c24zjzak6lj09fpuyvd.png)

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/cbby5s9clwfopsn8ms76.png)

## Conclusion:
So this is NTFY or as we can call it notify. It is a great simple to have tool in your day-to-day life as an IT expert. This is not only to get critical notifications but also to save your time. For example, I needed to Download a 40 GB large file and instead of waiting I could just go for a walk, play with my daughter or create coffee and receive notification once that is done. Lately, I started to integrate the NTFY into my GitHub pipelines and Grafana, and Zabbix. Over one year of NTFY usage, I have saved my time and I'm pretty happy with how it works and delivers me the important things. I have integrated it into PowerShell, Bash, and Python scripts and it hasn't failed me. The use cases grow each day.

Thank you for reading, don't forget to 
Follow for more:<br>
X.com: https://x.com/hugovalters<br>
bsky.app: https://bsky.app/profile/hugovalters.bsky.social<br>
YouTube: https://www.youtube.com/@hugovalters<br>
Homepage: https://www.valters.eu<br>
GitHub: https://github.com/hugovalters<br>
Medium: https://blog.valters.eu

Have a nice day.
By Hugo Valters
