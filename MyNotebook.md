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
##### Access control is not implemented
https://discuss.ipfs.io/t/access-control/285

# ipfs browser
http://127.0.0.1:5001/webui

# Object types
##### directory
has 0+ links, has no data<br>
Qme8TAD6uZ3wQbvVQJK8CWo4PrzgfiYrVHzBkz4Twffe6Z is hash of directory which contains file gpu.jpg(QmTiNTPXNQspkhCtM4X2xC7k8dedRVsk2UooLirhbfCe5g) and index.html. gpu.jpg is split into 3 blocks.<br>
$ ipfs dag get Qme8TAD6uZ3wQbvVQJK8CWo4PrzgfiYrVHzBkz4Twffe6Z
{"data":"CAE=","links":[{"Cid":{"/":"QmTiNTPXNQspkhCtM4X2xC7k8dedRVsk2UooLirhbfCe5g"},"Name":"gpu.jpg","Size":621763},{"Cid":{"/":"QmYKz5bb4kQiLzGKF4xLmNYSLUdKcbFGbSWSQzLmJ5Wok6"},"Name":"index.html","Size":635}]} <br>
for a directroy, the name of each links(points to its children file) is non-empty. <br>

$ ipfs dag get QmTiNTPXNQspkhCtM4X2xC7k8dedRVsk2UooLirhbfCe5g<br>
{"data":"CAIYgfglIICAECCAgBAggfgF","links":[{"Cid":{"/":"QmTtPNnWGSQuBmnxKSSiGP3GcEbPF61mJbtJiXNKWiJzc2"},"Name":"","Size":262158},{"Cid":{"/":"QmWmF1wtVhUmoT8CEvdpUg7Vuv4BeD3FoUpHsEuVBV7KXJ"},"Name":"","Size":262158},{"Cid":{"/":"QmdqxhC3Y96gptRFWr3egCqUFnZ9BBuzeqLQodeDK98PEy"},"Name":"","Size":97295}]} <br>
each link's name field is empty. 

##### split block
has links(point to subblocks, has data)

# Store Abstracion
dag store, blockstore, datastore, file systems<br>
blockstore: Package blockstore implements a thin wrapper over a datastore, giving a clean interface for Getting and Putting block objects <br>
datastore: datastore is a generic layer of abstraction for data store and database access
https://github.com/ipfs/go-datastore<br>


# IPFS vs SWARM
https://ethereum.stackexchange.com/questions/2138/what-is-the-difference-between-swarm-and-ipfs

# IPLD
https://ipld.io/<br>
https://github.com/ipld/ipld

