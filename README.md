
# WebSocket Server for the "Simple Multiplayer" Addon by Godot

This repository contains the source code for the Node.js server designed to work with the [Simple WebSocket Multiplayer for Godot](https://github.com/welson-rodrigues/GodotWebSocketMultiplayer).

The server is built with Express and the `ws` library, providing a lightweight and efficient solution for managing game rooms, players, and basic data synchronization.

## Features

* Management of client connections via WebSocket.

* Creation of rooms with unique codes.

* Management of player entry and exit from rooms.

* Broadcast of events (new player, disconnection, positions) to players in the same room.

* Basic structure for adding new gameplay messages (e.g., chat, attacks).

## How to Run

### Prerequisites

* Node.js (version 14 or higher recommended)
* npm (usually installed with Node.js)
* 
### 1. Local Setup (for Development)

1. Clone this repository:

``sh
git clone https://github.com/welson-rodrigues/GodotWebSocketMultiplayer

``
2. Navigate to the project folder:

``sh
cd GodotWebSocketMultiplayer

```
3. Install the necessary dependencies:

``sh
npm install

```
4. Start the server:

``sh
node server.js

```

By default, the server will run on port `9090`. Your Godot client should connect to `ws://localhost:9090`.

### 2. Online Deployment (for Production)

This server is ready to be hosted on various "Platform as a Service" (PaaS) platforms.

#### Example with Render.com

Render.com offers a free plan ideal for hosting this type of server. 1. Fork this repository to your own GitHub account.

2. Create an account on [Render.com](https://render.com/).

3. In your dashboard, click on **"New +"** and select **"Web Service"**.

4. Connect your GitHub account and select the server repository.

5. In the settings, Render usually detects that it is a Node.js project and automatically fills in the commands:

* **Build Command:** `npm install`
* **Start Command:** `node server.js`
6. Click on **"Create Web Service"**. After deployment, Render will provide a public URL (e.g., `https://my-server.onrender.com`).

7. In your Godot project, configure the connection URL to `wss://my-server.onrender.com` (note the **wss://** for secure connections).

License

This project is distributed under the MIT License.

---
*Created by Zee GameDev
