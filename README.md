# Lokinode Full Node

Join the movement, strengthen the network, and earn your place in Flokicoin history. Run your own node and help keep Flokicoin strong, fast, and fully decentralized.

## 🚀 Onboarding Steps

Follow these steps to set up your full node from scratch:

### 1. Initial Setup
Run the `setup.sh` script. This script will:
- Check for and install the `just` command runner if it's missing.
- Create necessary data directories.
- Generate `.env` and `data/lokid.conf` from sample files.

```bash
./setup.sh
```

### 2. Configuration (Optional)
Before starting the services, you can customize your installation:
- **`.env`**: Modify the docker image version.
- **`data/lokid.conf`**: Adjust peer-to-peer and RPC settings.

### 3. Start the Node
Now that everything is configured, start the services:

```bash
just up
```

## 🛠️ Service Management

The operator uses `just` for common tasks:

| Command         | Description                                     |
| --------------- | ----------------------------------------------- |
| `just setup`    | Re-run the onboarding/setup script.             |
| `just up`       | Start the node in the background.               |
| `just down`     | Stop and remove the container.                  |
| `just restart`  | Restart the service.                            |
| `just logs`     | Follow the node logs.                           |
| `just status`   | Check the status of the container.              |

## 🔍 Troubleshooting

- **Logs**: If the node fails to start, check the logs: `just logs`.
- **Data Persistence**: All blockchain data is stored in the `./data` directory.
