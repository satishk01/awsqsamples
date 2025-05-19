
#### q installter
https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line-installing.html


#####unzip installer

sudo apt update
sudo apt --fix-broken install
####logout and relogin
sudo apt upgrade


sudo apt install libayatana-appindicator3-1 libwebkit2gtk-4.1-0 libgtk-3-0


sudo apt clean
sudo apt update
sudo apt install unzip


##### UV installater
curl -LsSf https://github.com/astral-sh/uv/releases/latest/download/uv-x86_64-unknown-linux-gnu.tar.gz | tar zxf - -C /tmp
sudo mv /tmp/uv-x86_64-unknown-linux-gnu/uv /usr/local/bin/
sudo chmod +x /usr/local/bin/uv
uv --version



##### aws cli installation

curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
aws --version

##### AWS Configure
aws configure



###### Configure mcp.json
mkdir -p ~/.aws/amazonq
nano ~/.aws/amazonq/mcp.json


{
  "mcpServers": {
    "awslabs.core-mcp-server": {
      "command": "uvx",
      "args": ["awslabs.core-mcp-server@latest"],
      "env": {
        "FASTMCP_LOG_LEVEL": "ERROR"
      },
      "autoApprove": ["prompt_understanding"],
      "disabled": false
    },
    "awslabs.terraform-mcp-server": {
       "command": "uvx",
       "args": ["awslabs.terraform-mcp-server@latest"],
       "env": {
         "FASTMCP_LOG_LEVEL": "ERROR"
       },
       "disabled": false,
       "autoApprove": []
     },
    "awslabs.cost-analysis-mcp-server": {
      "command": "uvx",
      "args": ["awslabs.cost-analysis-mcp-server@latest"],
      "env": {
        "AWS_PROFILE": "default",
        "FASTMCP_LOG_LEVEL": "ERROR"
      }
    } 
  }
}


