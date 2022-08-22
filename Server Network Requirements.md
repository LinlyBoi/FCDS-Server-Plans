# Extranet Solutions
>## 1. Internal VPN with proper authentication methods in place
>Most maintenance tasks require access to the main server (leader node of cluster) such as creating kubernetes deployments, configuring existing services. Certain maintenance tasks are usually urgent and require hotfixes on the spot. Remote access can pose a security risk if it is done via SSH through the internet with password authentication and it would be bad practice to unneccesarily expose the leader node for something primarily dealing with the private network of the establishment which is the reason why we chose to have an internal vpn for said tasks with a PKI (Public Key Infrastructure) in place to ensure only authorised individuals have access to the faculty network and securing all machines with proper firewall configuration (independent from network firewall rules) and ssh access only via ssh/gpg keys for authorised individuals.



>## 2. Range of *Random high* ports forwarded for various services (VPN,ssh)


>## 3. SSL certificates for the VPN server and clients 

# Website solutions
>## 1.  Direct link with static IP OR Dynamic DNS to handle the machine IP address potentially changing (requires the port forwarding mentioned above still)
>## 2. Http/Https ports forwarded (443/80/8080) 
>## 3. After testing website initially, connect FCDS subdomain DNS record to machine with static IP/Dynamic DNS client.