# Tailscale

## Why Use Tailscale?

Tailscale allows me to securely connect to my local devices at home.  
I can use these devices as endpoints, enabling full local access — just like being physically connected to the same network.  
It works similarly to a VPN but is much easier to set up and manage.

## How Did I Install Tailscale?

1. **Create an account**  
   Go to [https://tailscale.com](https://tailscale.com) and sign up for an account.

2. **Install on a device**  
   Start by installing Tailscale on an initial device, such as a phone (just download the app).

3. **Install on a Linux device (Ubuntu 24.10)**  
   Run the following commands to set up the repository:

   ```bash
   curl -fsSL https://pkgs.tailscale.com/stable/ubuntu/oracular.noarmor.gpg | sudo tee /usr/share/keyrings/tailscale-archive-keyring.gpg >/dev/null
   curl -fsSL https://pkgs.tailscale.com/stable/ubuntu/oracular.tailscale-keyring.list | sudo tee /etc/apt/sources.list.d/tailscale.list
   ```

   Then update and install Tailscale:

   ```bash
   sudo apt-get update
   sudo apt-get install tailscale
   ```

4. **Bring the device online**  
   Run:

   ```bash
   sudo tailscale up
   ```

   Sign in using the link provided in the terminal. Once authenticated, your device will be connected to your Tailscale network.

## Where Did I Use Tailscale?

I used Tailscale on my Raspberry Pi 3 (RPI3), a low-powered device that can run 24/7 with minimal cost.  
I connect to it remotely using my iPhone, giving me secure access to my home network anytime, anywhere.
