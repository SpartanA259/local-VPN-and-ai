Local VPN and AI
The complete setup gives me my own private home VPN for accessing sensitive information or browsing the web on unsecured public networks. It allows me to remotely access my PC from anywhere with internet service and transfer files to and from the my phone and home PC. It also gives me access to the local LLMs running on my home PC's GPU with web search capabilities. 

Most of my work involved configuration and setup. However, I still ran into multiple large problems. For example, setting up web search tools with searxng and playwright, creating docker containers and locally hosted websites, and configuring my PC as an exit node in tailscale.

In practice, this local setup has been extremely useful in remaining productive while away from home. The WireGuard VPN proves to effectively secure my connection on public networks. RustDesk remote desktop access and Tailscale filesharing allow me to continue the work and access the resources on my home PC during my freetime in school, greatly increasing my daily productivity. The only aspect that doesn't see much use is the local LLM access. I've found that with a midrange GPU, the speed and capability of local LLMs are vastly overperformed by free cloud-based models. The questions and problems I leverage AI to answer and solve are completed faster and with much better quality using cloud AI. Nonetheless, the process of configuring local AI models greatly deepened my understanding of what AI actually is and how it works. 

In terms of remote workstation functionality, this setup is perfect for my current needs. However, in the future, perhaps when computer part prices go down in price and I have a stable income, I'd like to expand on this setup with a personal laptop and a home server, expanding remote productivity capabilities and providing remotely accessible private storage and processing power. 

My LLMs running on my AMD 6700xt GPU (12 GB of VRAM): 
gemma4:e4b - Web search and research
qwen2.5-coder:14b - Coding
gemma4:12b - Creative Writing and General Tasks
deepseek-r1:14b - Reasoning and Deep Thinking

How I set it up:
1. Downloaded and configured Tailscale on my phone and PC, connecting to my own "tailnet"
2. Configured my PC as an exit node, enabling web traffic to be routed through that device
3. Downloaded RustDesk on my phone and PC, enabling direct IP connection and inputting my PC's IP address into my phones RustDesk connection point
4. Downloaded and set up OpenWebUI, Docker, Ollama, SearXNG, and Playwright
5. Created locally hosted websites to host OpenWebUI, SearXNG (search engine), and Playwright (pulls webpages for local LLMs) in Docker containers
6. Downloaded LLM models in Ollama, and linked said models, SearXNG, and playwright to OpenWebUI
