# Install Python

# Install DER simulator

1. Install the der_simulator source code. 

2. Configure docker to point to the 

3. 



# Add Users

1. Create `deruser` account with password `secret`

	`sudo adduser deruser`

2. Create `deradmin` account with password `password1`. 

	`sudo adduser deradmin` 
	
	Update the `deradmin` password to the following with `sudo nano /etc/shadow`
	
		deradmin:$6$VIAfkbqt58HrKuUp$knTnUiA4D1H.lNh2v0FnKdU32fRBtkcqXiMrw4lCAQmqgVgvznYFUhGJ.hjb4JZb.CTCGs98SVQMjjUMx5J8v1:19069:0:99999:7:::
	
	Add `deradmin` to root/administrator group with:

		`sudo usermod -aG root deradmin`
		`sudo usermod -aG administrator deradmin`
		`sudo usermod -aG sudo deradmin`
		`sudo groups deradmin`

# Create VNC interface

1. Install TigerVNC: 

	`sudo apt install tigervnc-standalone-server tigervnc-common tigervnc-xorg-extension tigervnc-viewer`
 
1. Follow these [instructions](https://www.cyberciti.biz/faq/install-and-configure-tigervnc-server-on-ubuntu-18-04/)

2. Create `vnc` user with `superman` password. 

		sudo adduser vnc
		sudo passwd vnc
		
3. Create VNC password with `vncpasswd` and set password to `superman`. Do not have a view only password. 

4. Allow remove VNC sessions: `vncserver -localhost no`

4. Start server `vncserver` and verify it's running `vncserver -list` and `ss -tulpn | egrep -i 'vnc|590'`

5. Update the firewall rules to allow tcp connections to ports 5900, 5901, 5902, and 5903. 

	`sudo ufw enable`

	`sudo ufw allow 5900/tcp`
	
	`sudo ufw allow 5901/tcp`
	
	`sudo ufw allow 5902/tcp`
	
	`sudo ufw allow 5903/tcp`
	
	`sudo ufw status`

6. 

# Install SSH server

1. Install the service an open the port through the firewall.  

	`sudo apt install openssh-server`
	
	`sudo systemctl status ssh`
	
	`sudo ufw allow ssh`

2. Create a banner (for fun)

	`sudo nano /etc/ssh/der_banner`

	Enter the following: 
	
		 __          __  _                           
		 \ \        / / | |                          
		  \ \  /\  / /__| | ___ ___  _ __ ___   ___  
		   \ \/  \/ / _ \ |/ __/ _ \| '_ ` _ \ / _ \ 
			\  /\  /  __/ | (_| (_) | | | | | |  __/ 
		  _  \/  \/ \___|_|\___\___/|_| |_| |_|\___| 
		 | |        | | | |                          
		 | |_ ___   | |_| |__   ___                  
		 | __/ _ \  | __| '_ \ / _ \                 
		 | || (_) | | |_| | | |  __/                 
		  \__\___/   \__|_| |_|\___|                 
		  / ____|     | |                            
		 | (___   ___ | | __ _ _ __                  
		  \___ \ / _ \| |/ _` | '__|                 
		  ____) | (_) | | (_| | |                    
		 |_____/ \___/|_|\__,_|_|                    
		  _____    ______   _____    _               
		 |  __ \  |  ____| |  __ \  | |              
		 | |  | | | |__    | |__) | | |              
		 | |  | | |  __|   |  _  /  | |              
		 | |__| | | |____  | | \ \  |_|              
		 |_____/  |______| |_|  \_\ (_)              
		 
		 
	`sudo nano /etc/ssh/der_banner`
	
	Add `sudo nano /etc/ssh/der_banner`
	
3. Restart SSH service

	`sudo systemctl reload ssh.service`
	

# Install the code signing key

1. Generate keypair in `~/solarflask/solarflask`: 

	`openssl genrsa -out private-key-der.pem`
	
	`openssl rsa -in private-key-der.pem -pubout -out solarflask_pub.key.pem`
	
2. Copy private key over to Kali: 

	On Kali: `sudo service ssh start`

	On DER: `scp private-key-der.pem kali@10.10.0.10:~/`
	
3. Move the private key on Kali into `~/code_signing_key/`. 

# Helpful debugging commands:

* DER current operations: `docker-compose logs --follow`
* DER startup: `docker-compose logs | grep -v 'sensor' | grep -v influx | head -n 20`
* Configure IP manually: `sudo ip link set dev ens33 up`, `sudo ip addr add 10.10.0.100/24 dev ens33`
* 
