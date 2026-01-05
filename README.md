# Lecture 1 codes

Check out `index.html` for lecture codes.

## Using `netcat` (`nc`)

`netcat` is a command-line utility for reading from and writing to network connections. We can use it to demonstrate a basic client-server interaction. You will need two separate terminal windows for this.

### Terminal 1: The Server

In one terminal, run the following command. This will start a _server_ process that listens for incoming connections on port `3491`.

```bash
nc -l 3491
```

- `nc`: The `netcat` program.
- `-l`: The "listen" flag, which puts `nc` into server mode.
- `3491`: The port number. This is an arbitrary choice; you can use other port numbers (preferably above 1024).

### Terminal 2: The Client

In a second terminal, run this command to connect to the server you just started:

```bash
nc localhost 3491
```

- `localhost`: The hostname for the local machine (IP address `127.0.0.1`).
- `3491`: The port number your server is listening on.

### Communicating

Once the connection is established, anything you type in one terminal will appear in the other, and vice-versa. This demonstrates a two-way communication channel. To end the session, press `Ctrl+C` in either terminal.

**Note:** To connect two different devices on the same network, replace `localhost` with the local IP address of the machine running the server.
