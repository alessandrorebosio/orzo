# Orzo

**Orzo** is a Bash script designed to simplify the management of Docker containers. It provides commands for creating, starting, removing, and updating containers in a specified path.

## Requirements

Ensure you have the following installed on your system:

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Installation

### 1. Download the script

Use `curl` to download the script:

```bash
sudo curl -o /usr/local/bin/orzo https://raw.githubusercontent.com/alessandrorebosio/orzo/refs/heads/main/orzo
```

### 2. Make the script executable

```bash
sudo chmod +x /usr/local/bin/orzo
```

## Usage

### Syntax

```bash
orzo [OPTION] COMMAND [CONTAINER or FOLDER_PATH]
```

### Available Commands

- `setup`: Set the folder for the container with docker-compose.yml and .env files. (Don't use with -a flag)
- `create`: Create and start the specified container.
- `remove`: Stop and remove the specified container.
- `restart`: Restart the specified container.
- `update`: Update the specified container with the latest image.
- `clean`: Clean up unused Docker images.

### Options

- `-f FOLDER_PATH`: Specify the folder path of the container instead of the container name.
- `-a FOLDER_PATH`: Execute the command in all subdirectories of the specified folder.
- `--help`: Display the help message.

### Example Usage

1. **Setup the container**:

   ```bash
   orzo setup my_container
   ```

   > This command sets up the folder for the container and creates a `docker-compose.yml` file.

2. **Starting the container**:

   ```bash
   orzo create my_container
   ```

   > This command creates and starts the specified container defined in the `docker-compose.yml` file.

3. **Removing the container**:

   ```bash
   orzo remove my_container
   ```

   > This command stops and removes the specified container.

4. **Restarting the container**:

   ```bash
   orzo restart my_container
   ```

   > This command restarts the specified container.

5. **Updating the container**:

   ```bash
   orzo update my_container
   ```

   > This command updates the specified container with the latest image after confirming changes.

6. **Cleaning unused container images**:

   ```bash
   orzo clean
   ```

   > This command removes unused Docker images from the system.

7. **Specifying a custom folder path using `-f`**:

   ```bash
   orzo -f create /path/to/custom_folder
   ```

   > This command creates and starts the container defined in the `docker-compose.yml` file located in `/path/to/custom_folder`.

8. **Executing a command in all subdirectories using `-a`**:

   ```bash
   orzo -a create /path/to/base_folder
   ```

   > This command creates and starts containers in all subdirectories of `/path/to/base_folder` that contain a `docker-compose.yml` file.

## Warnings

- Ensure that you run the script with sufficient permissions to modify files in the `/opt` directory.

## Contributing

If you would like to contribute to this project, feel free to open a Pull Request or report issues.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
