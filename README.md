# Roblox-Game-2

Game source is kept as files and synced into Roblox Studio with [Rojo](https://rojo.space).

## Connecting to Roblox Studio

1. **Install Rokit** (toolchain manager): https://github.com/rojo-rbx/rokit#installation
2. **Clone and install tools**
   ```sh
   git clone https://github.com/Surgen-of-death/Roblox-Game-2.git
   cd Roblox-Game-2
   rokit install
   ```
3. **Install the Rojo plugin in Studio**
   ```sh
   rojo plugin install
   ```
   (Or install "Rojo" from the Creator Store.) Restart Studio afterward.
4. **Start the sync server**
   ```sh
   rojo serve
   ```
5. **Connect from Studio**: open a place (e.g. a new Baseplate), open the
   **Plugins** tab → **Rojo** → click **Connect** (default `localhost:34872`).

Edits to files under `src/` now appear in Studio immediately.

## Layout

| Folder        | Studio location                               |
|---------------|-----------------------------------------------|
| `src/shared`  | `ReplicatedStorage.Shared`                    |
| `src/server`  | `ServerScriptService.Server`                  |
| `src/client`  | `StarterPlayer.StarterPlayerScripts.Client`   |

File suffixes: `*.server.luau` → Script, `*.client.luau` → LocalScript,
plain `*.luau` → ModuleScript.

## Building a place file

```sh
rojo build -o Roblox-Game-2.rbxlx
```
