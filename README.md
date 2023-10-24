# Api for LLM Flask

Run the cloud-init script and reboot the server.

To check the cloud-init logs:

`sudo cat /var/log/cloud-init-output.log`

`sudo cat /var/log/cloud-init.log`

## Setup

`git clone https://github.com/don-dp/apiforllm-functions.git`

`cd apiforllm-functions`

`python3 build_docker_images.py`

`cd ../`

`git clone https://github.com/don-dp/apiforllmflask.git`

`cd apiforllmflask/`

`sudo ufw allow from [your-ip-address] to any port 80`

`sudo ufw allow from [your-ip-address] to any port 443`

Enable development mode in cloudflare and setup dns A record.

`docker compose up -d`