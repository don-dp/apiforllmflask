# Api for LLM Flask

Run the cloud-init script

`git clone https://github.com/don-dp/apiforllm-functions.git`

`cd apiforllm-functions`

`python3 build_docker_images.py`

`cd ../`

`ssh-keygen`

`cat ~/.ssh/id_rsa.pub`

Copy the public key and create a deploy key.

`git clone git@github.com:don-dp/apiforllmflask.git`

`cd apiforllmflask/`

Use the below for testing:

`sudo ufw allow 80`

`sudo ufw allow 443`

For production:

`sudo ufw allow from [your-ip-address] to any port 80`

`sudo ufw allow from [your-ip-address] to any port 443`

Enable development mode in cloudflare and setup dns A record.

`docker compose up -d`