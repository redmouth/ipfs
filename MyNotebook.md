# npm IPFS

##### ipfs merkle dag node
https://www.npmjs.com/package/ipfs-merkle-dag-node<br>
https://github.com/noffle/ipfs-merkle-dag-node<br>
multihash - for convenience, the base58-encoded string of hash.

##### examples
https://ipfs.io/docs/examples/<br>


##### repo path/repo location
ipfs uses a repository in the local file system. By default, the repo is located
at ~/.ipfs. To change the repo location, set the $IPFS_PATH environment variable:
    export IPFS_PATH=/path/to/ipfsrepo

# problems
##### reorganize exchanges, dag and blockstore
https://github.com/ipfs/notes/issues/255

# ipfs browser
http://127.0.0.1:5001/webui

# Object types
##### directory
has 0+ links, has no data

##### split block
has links(point to subblocks, has data)

# Store Abstracion
dag store, blockstore, datastore, file systems<br>
blockstore: Package blockstore implements a thin wrapper over a datastore, giving a clean interface for Getting and Putting block objects <br>
datastore: datastore is a generic layer of abstraction for data store and database accesshttps://github.com/ipfs/go-datastore<br>


# IPLD
https://ipld.io/<br>
https://github.com/ipld/ipld

