IPFSのインストール
2種類
- GUI
- ソースコード
  - こちらに関しては後日詳細 (Linuxで行う)

ターミナルで 　deamon を起動させようとして
'''
ipfs daemon
Initializing daemon...
go-ipfs version: 0.10.0
Repo version: 11
System version: amd64/darwin
Golang version: go1.16.8

Error: lock /Users/hoge/.ipfs/repo.lock: someone else has the lock
'''
とエラーが出たので
https://github.com/ipfs-inactive/support/issues/12
を参考にしたら新たに
'''
ipfs daemon
Initializing daemon...
go-ipfs version: 0.10.0
Repo version: 11
System version: amd64/darwin
Golang version: go1.16.8

Error: resource temporarily unavailable
'''
となってしまった。
加えてGUIまで起動しなくなってしまった
*GUIが常時起動ではなくメニューバーから開けることを確認

追記
一旦IPFSを切って
https://docs.ipfs.io/how-to/command-line-quick-start/#initialize-the-repository
を参照にしてみた
IPFSに対してパスを通して ipfs deamon を実行してみたら
'''
Initializing daemon...
go-ipfs version: 0.10.0
Repo version: 11
System version: amd64/darwin
Golang version: go1.16.8
Swarm listening on /ip4/127.0.0.1/tcp/4001
Swarm listening on /ip4/127.0.0.1/udp/4001/quic
Swarm listening on /ip4/192.168.100.7/tcp/4001
Swarm listening on /ip4/192.168.100.7/udp/4001/quic
Swarm listening on /ip6/::1/tcp/4001
Swarm listening on /ip6/::1/udp/4001/quic
Swarm listening on /p2p-circuit
Swarm announcing /ip4/118.18.234.56/udp/56122/quic
Swarm announcing /ip4/127.0.0.1/tcp/4001
Swarm announcing /ip4/127.0.0.1/udp/4001/quic
Swarm announcing /ip4/192.168.100.7/tcp/4001
Swarm announcing /ip4/192.168.100.7/udp/4001/quic
Swarm announcing /ip6/::1/tcp/4001
Swarm announcing /ip6/::1/udp/4001/quic
API server listening on /ip4/127.0.0.1/tcp/5001
WebUI: http://127.0.0.1:5001/webui
Gateway (readonly) server listening on /ip4/127.0.0.1/tcp/8080
Daemon is ready
'''
となった。どういうこと？
推測だが、ノードとして立っているだけと感じた。
ここからはファイルのアップロードは不可能かもしれない(要調査)
おそらくGUIからでないとアップロードできないと思う。

## ipfsコマンド
コマンド系はLinuxで検証する


'''
ipfs --help
USAGE
  ipfs  - Global p2p merkle-dag filesystem.

SYNOPSIS
  ipfs [--config=<config> | -c] [--debug | -D] [--help] [-h] [--api=<api>] [--offline] [--cid-base=<base>] [--upgrade-cidv0-in-output] [--encoding=<encoding> | --enc] [--timeout=<timeout>] <command> ...

OPTIONS

  -c, --config               string - Path to the configuration file to use.
  -D, --debug                bool   - Operate in debug mode.
  --help                     bool   - Show the full command help text.
  -h                         bool   - Show a short version of the command help text.
  -L, --local                bool   - Run the command locally, instead of using the daemon.
                                      DEPRECATED: use --offline.
  --offline                  bool   - Run the command offline.
  --api                      string - Use a specific API instance (defaults to
                                      /ip4/127.0.0.1/tcp/5001).
  --cid-base                 string - Multibase encoding used for version 1 CIDs in output.
  --upgrade-cidv0-in-output  bool   - Upgrade version 0 to version 1 CIDs in output.
  --enc, --encoding          string - The encoding type the output should be encoded with (json, xml,
                                      or text). Default: text.
  --stream-channels          bool   - Stream channel output.
  --timeout                  string - Set a global timeout on the command.

SUBCOMMANDS
  BASIC COMMANDS
    init          Initialize local IPFS configuration
    add <path>    Add a file to IPFS
    cat <ref>     Show IPFS object data
    get <ref>     Download IPFS objects
    ls <ref>      List links from an object
    refs <ref>    List hashes of links from an object

  DATA STRUCTURE COMMANDS
    dag           Interact with IPLD DAG nodes
    files         Interact with files as if they were a unix filesystem
    block         Interact with raw blocks in the datastore

  TEXT ENCODING COMMANDS
    cid           Convert and discover properties of CIDs
    multibase     Encode and decode data with Multibase format

  ADVANCED COMMANDS
    daemon        Start a long-running daemon process
    mount         Mount an IPFS read-only mount point
    resolve       Resolve any type of name
    name          Publish and resolve IPNS names
    key           Create and list IPNS name keypairs
    dns           Resolve DNS links
    pin           Pin objects to local storage
    repo          Manipulate the IPFS repository
    stats         Various operational stats
    p2p           Libp2p stream mounting
    filestore     Manage the filestore (experimental)

  NETWORK COMMANDS
    id            Show info about IPFS peers
    bootstrap     Add or remove bootstrap peers
    swarm         Manage connections to the p2p network
    dht           Query the DHT for values or peers
    ping          Measure the latency of a connection
    diag          Print diagnostics
    bitswap       Inspect bitswap state
    pubsub        Send and receive messages via pubsub

  TOOL COMMANDS
    config        Manage configuration
    version       Show IPFS version information
    update        Download and apply go-ipfs updates
    commands      List all available commands
    log           Manage and show logs of running daemon

  Use 'ipfs <command> --help' to learn more about each command.

  ipfs uses a repository in the local file system. By default, the repo is
  located at ~/.ipfs. To change the repo location, set the $IPFS_PATH
  environment variable:

    export IPFS_PATH=/path/to/ipfsrepo

  EXIT STATUS

  The CLI will exit with one of the following values:

  0     Successful execution.
  1     Failed executions.

  For more information about each command, use:
  'ipfs <subcmd> --help'
'''


ipfs mount をするにはソースコードからインストールしないといけないらしい


'''
ipfs mount
Error: unable to check fuse version.

Dear User,

Before mounting, we must check your version of OSXFUSE. We are protecting
you from a nasty kernel panic we found in OSXFUSE versions <2.7.2.[1]. To
make matters worse, it's harder than it should be to check whether you have
the right version installed...[2]. We've automated the process with the
help of a little tool. We tried to install it, but something went wrong[3].
Please install it yourself by running:

	go get github.com/jbenet/go-fuse-version/fuse-version

You can also stop ipfs from running these checks and use whatever OSXFUSE
version you have by running:

	ipfs config --bool DontCheckOSXFUSE true

[1]: https://github.com/ipfs/go-ipfs/issues/177
[2]: https://github.com/ipfs/go-ipfs/pull/533
[3]: exit status 1
can't load package: package github.com/jbenet/go-fuse-version/fuse-version: cannot find package "github.com/jbenet/go-fuse-version/fuse-version" in any of:
	/usr/local/go/src/github.com/jbenet/go-fuse-version/fuse-version (from $GOROOT)
	/Users/naoki/go/src/github.com/jbenet/go-fuse-version/fuse-version (from $GOPATH)
'''


画像のアップロード

