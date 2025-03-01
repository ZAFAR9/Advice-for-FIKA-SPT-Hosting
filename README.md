# SPT FIKA Hosting Guide and FAQ

Welcome to the **SPT FIKA Hosting Guide**! This guide is designed to help you host SPT Tarkov servers with large modlists (80+ mods) while ensuring a smooth and enjoyable experience for your friends. Whether you're completely new to hosting or have some experience, this guide will walk you through every step, explain the tools you need, and provide solutions to common problems.

---

## Table of Contents
1. [Introduction](#introduction)
2. [What You Need to Know Before Hosting](#what-you-need-to-know-before-hosting)
3. [Mod Sharing and Syncing](#mod-sharing-and-syncing)
4. [Bundle Optimization](#bundle-optimization)
5. [Hosting Methods: VPN vs. Port Forwarding](#hosting-methods-vpn-vs-port-forwarding)
6. [Best Practices for Hosting](#best-practices-for-hosting)
7. [Tools and Resources](#tools-and-resources)
8. [FAQ](#faq)
9. [Contributing](#contributing)
10. [License](#license)

---

## Introduction

Hosting an SPT Tarkov server with a large modlist can be a rewarding experience, but it also comes with challenges. From ensuring all players have the same mods to optimizing bundle loading times and managing player connections, there’s a lot to consider. This guide is here to help you navigate these challenges and create a stable, secure, and fun co-op experience for you and your friends.

---

## What You Need to Know Before Hosting

Before diving into the technical details, here are some key concepts and terms you should understand:

1. **SPTarkov (Single Player Tarkov)**:  
   - SPTarkov is a modded version of Escape from Tarkov that allows you to play offline or host private servers for co-op play. It is not affiliated with Battlestate Games (BSG), the developers of Escape from Tarkov.

2. **Mods**:  
   - Mods are custom modifications that enhance or change the game. These can include new weapons, traders, AI behavior, and more. Hosting a server with mods requires all players to have the exact same mod setup as the host.

3. **Bundles**:  
   - Bundles are game assets (like textures, sounds, and models) that need to be loaded by the game. When hosting a server, clients (your friends) must load the same bundles as the host.

4. **Networking**:  
   - Hosting a server requires a way for players to connect to your computer. This can be done through **port forwarding** or **VPN hosting** (explained in detail later).

5. **Tools**:  
   - There are several tools available to help you manage mods, optimize bundles, and host your server. These tools will be explained in the sections below.

---

## Mod Sharing and Syncing

One of the most important steps in hosting an SPT server is ensuring that all players have the exact same mod setup as the host. If even one mod is missing or out of date, players may experience errors or be unable to connect.

### How to Share Mods with Your Friends

1. **Zip Your Mod Folders**:  
   - Locate the following folders in your SPT installation directory:
     - `user/mods`
     - `BepInEx/plugins`
     - `BepInEx/patches`
   - Compress these folders into a `.zip` file using a tool like WinRAR or 7-Zip.
   - Share the `.zip` file with your friends using a file-sharing service like Google Drive, Dropbox, or OneDrive.

2. **Use SP-EFT Manager**:  
   - SP-EFT Manager is a tool that automates mod downloads, organizes your load order, and helps debug errors. It’s especially useful for large modlists.
   - With SP-EFT Manager, you can:
     - List all mods installed on your server.
     - Reorder mods to resolve compatibility issues.
     - Debug errors by reading logs from BepInEx and the server.

3. **Sync Mods with Corter’s ModSync**:  
   - Corter’s ModSync is a tool that allows you to sync mods between the host and clients. After the initial setup, it ensures that all players have the same mods without needing to manually share files every time you update or add a mod.

---

## Bundle Optimization

Bundle loading is one of the most time-consuming parts of hosting an SPT server, especially with a large modlist. Without optimization, it can take hours for clients to load the necessary bundles.

### Why Do Bundles Take So Long to Load?

When a client connects to your server, their game must load the exact same bundles as the host. Even if the client has similar bundles from their own play, they will still need to download and load the host’s bundles. This process can be slow, especially for large modlists.

### Tools for Optimizing Bundles

1. **Bundle Archiver**:  
   - Compresses and optimizes bundles, significantly reducing loading times for clients.
   - Highly recommended for hosts with large modlists.

2. **ELBL (Efficient Local Bundle Loader)**:  
   - Another tool for improving bundle loading efficiency. It works by streamlining the way bundles are loaded into the game.

3. **Avoid Waiting Without Tools**:  
   - Without tools like Bundle Archiver or ELBL, bundle loading can take hours. Always use these tools to save time and improve the experience for your friends.

---

## Hosting Methods: VPN vs. Port Forwarding

When hosting an SPT server, you need a way for players to connect to your computer. There are two main methods: **VPN hosting** and **port forwarding**.

### VPN Hosting (Recommended)

VPN hosting uses a virtual private network to simulate a local network environment. Tools like **Radmin VPN** make this process simple and secure.

#### Advantages of VPN Hosting:
- **Better Security**:  
  - Your public IP address is hidden, reducing the risk of attacks.
- **Easier Setup**:  
  - No need to configure your router or deal with NAT issues.
- **Player Management**:  
  - You can control who joins your server by managing access to the VPN network.
- **Improved Stability**:  
  - Simulates a local network, reducing connection issues like packet loss.

#### How to Set Up Radmin VPN:
1. Download and install Radmin VPN from [here](https://www.radmin-vpn.com/).
2. Create a new network and share the network name and password with your friends.
3. Once connected, your friends can join your server as if they were on the same local network.

### Port Forwarding (Not Recommended)

Port forwarding involves manually configuring your router to allow incoming connections to your server.

#### Disadvantages of Port Forwarding:
- **Security Risks**:  
  - Exposes your public IP address, making you vulnerable to attacks.
- **Complex Setup**:  
  - Requires manual configuration of your router, which can be difficult for beginners.
- **Limited Control**:  
  - Managing who can join your server is more difficult without additional tools.

---

## Best Practices for Hosting

1. **Prepare Your Setup**:  
   - Use tools like SP-EFT Manager, Bundle Archiver, and Corter’s ModSync to streamline the process.

2. **Optimize Bundle Loading**:  
   - Always use Bundle Archiver or ELBL to reduce loading times for your clients.

3. **Share Files Efficiently**:  
   - Zip and share your mod and plugin folders via Google Drive or a dedicated Gmail account.

4. **Stay Organized**:  
   - Maintain a shared Google Doc or similar resource to catalog and share your mod setup.

5. **Avoid Problematic Tools**:  
   - Avoid RAM cleaners, which can cause lag spikes, and use FPS unlockers for better performance on lower-end PCs.

---

## Tools and Resources

Here are the tools mentioned in this guide:

- **SP-EFT Manager**: For mod management, load order editing, and debugging.
- **Corter’s ModSync**: For syncing mods between the host and clients.
- **Bundle Archiver**: For compressing and optimizing bundles.
- **ELBL (Efficient Local Bundle Loader)**: For faster bundle loading.
- **Radmin VPN**: For secure and user-friendly VPN hosting.

---

## FAQ

### How can I make it easier for my friends to join my server?
- Zip and share your `user/mods` and `BepInEx` folders.
- Use tools like SP-EFT Manager and Corter’s ModSync to automate mod syncing.

### Why is VPN hosting better than port forwarding?
- VPN hosting provides better security, easier setup, and improved player management. Tools like Radmin VPN simulate a local network, making it more stable and user-friendly.

### What should I do if bundle loading takes too long?
- Use Bundle Archiver or ELBL to optimize bundles and reduce loading times.

### Can clients generate their own bundles based on the host’s setup?
- No, clients must load the exact bundles from the host. Tools like Bundle Archiver help minimize waiting times.

---

## Contributing

If you have additional tips or tools to recommend, feel free to submit a pull request or open an issue. Let’s make hosting SPT servers easier for everyone!

---

## License

This guide is open-source and available under the MIT License. Feel free to use and share it!
[LICENSE](./LICENSE)
