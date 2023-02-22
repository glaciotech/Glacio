# Glacio

### !!!ALPHA!!!

**Glacio is currently in alpha, as such we appreciate your patience with any issues you may find. All feedback is welcome and can be submitted at support@glacio.tech**

---

**NOTE: Currently GlacioCLI will only run on Apple platforms running macOS 10.15 or higher**

GlacioCLI is a tool that wraps a Glacio node allowing you to run it from command line. This node is generally used
to provide another sync point and storage location on a Glacio Network.



## Usage

To run a node download the `GlacioCLI` binary.

Then from within the location the GlacioCLI binary was downloaded on the shell type:

```shell
GlacioCLI
```

This will start up a Glacio Node with a default chain with chainId "main" and the following default settings.

**NOTE: The first time you run the node it will ask for network permissions, please allow**

```
- Port: 8417
- Chain Directory : chaindata  
- seedNodes: none
```

## Command Line Options

GlacioCLI currently offers a limited set of configuration options:

- `port` allows you to set the port which Glacio runs on
- `chain-dir` changes the default location chain data is stored
- `noMain` starts a node without a main chain. Node will have no registered chains available
- `chains` a list of chains to add on startup. If you connect to another node this will cause those chains to sync

Example of starting the node up on port 9999, with a non-default chaindir, noMain chain and 2 additional chains.

```shell
GlacioCli --port 9999 --chain-dir "/newChainDir" --no-main --chains "TestChain1","TestChain2"
```

## Troubleshooting
- As GlacioCLI is currently in alpha it is not signed. As such you'll need to allow it to be run from within System Preferences -> Security & Privacy -> Allow Apps Downloaded from. After you run it for the first time you should see an option to Allow or Open here.
- You may need to change the downloaded binary to have execute permissions on Mac you can do this by running `chmod +x GlacioCLI`

