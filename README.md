# Self Hosting Ollama and OpenWebUi on Docker

## Introduction:

This is a project showcase on self hosting a [Deepseek](https://www.deepseek.com/) instance on [Ollama](https://ollama.com/) through [docker](https://www.docker.com/) on my local network. This showcase is designed for enthusiasts and hobbyists who would like to replicate this setup and leverage the power of Docker and open source tools like Ollama and OpenWebUI to access freely available LLMs on thier local network.

In this showcase, I will walk through the steps of up setting up Deepseek (through Ollama) and OpenWebUI on Docker. While my setup is split between my homeserver running on a [Raspberry Pi 4(4GB)](https://www.raspberrypi.com/products/raspberry-pi-4-model-b/) and a [gaming laptop](https://rog.asus.com/laptops/rog-zephyrus/rog-zephyrus-g15-2022-series/), it would be possible to run this on multiple hardware and network configurations. The project is primarily focused on setting up Ollama with Deepseek and OpenWebUI on docker and will not include steps to access the LLM over the internet, it would be relatively simple to use [Cloudflare Tunnels](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/) or a self hosted VPN to access the LLMs from the World Wide Web.

## What I Learned:
- Setting Up Docker
- Installing and Using Ollama
- Deploying OpenWebUI
- Basic Networking
- Troubleshooting

## Prerequisites:
- Hardware:
  - A Machine to host Docker and Ollama: For my setup, I set up Docker on both my gaming laptop and Raspberry Pi. Running LLMs requires significant compute, so make sure to choose your LLMs based on the resources available to you.
- Local Network Access:
  - Although not a strict requirement, it would be preferred to have access to the admin setting on your Local Network as this will let you assign static IPs to all the devices and let you keep a persistent environment for your services.
- Software:
  - Docker
  - Ollama
  - OpenWebUI
  - Linux (Preferred)

    
