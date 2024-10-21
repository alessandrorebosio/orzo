# Orzo

Orzo is a Bash script designed to simplify the management of Docker containers. It provides commands for creating, starting, removing, and updating containers in a specified path.

## Requirements

Make sure you have the following installed on your system:

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Usage

### Syntax

```bash
orzo COMMAND CONTAINER
```

### Available Commands

- `create`: Creates and starts the container.
- `remove`: Stops and removes the container.
- `restart`: Restarts the container.
- `update`: Updates the container.
- `clean`: Cleans unused downloaded Docker images.

### Example

```bash
orzo create my_container 
```

> **Note:** The container name must be located within the `/opt` directory.

### Options

- `--help`: Displays the help message.

## Usage Examples

1. **Starting the container**:

   ```bash
   orzo create my_container 
   ```

2. **Removing the container**:

   ```bash
   orzo remove my_container
   ```

3. **Restarting the container**:

   ```bash
   orzo restart my_container
   ```

4. **Updating the container**:

   ```bash
   orzo update my_container
   ```

5. **Cleaning unused container images**:

   ```bash
   orzo clean
   ```

## Warnings

- Ensure that you run the script with sufficient permissions to modify files in the `/opt` directory.

## Contributing

If you would like to contribute to this project, feel free to open a Pull Request or report issues.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
