
# kubernetes
create the storage class and than apply it
crete pvc and than apply it
Create the statefullset and headless service and apply it
For replication

kubectl exec -it mongo-0 -- mongo

rs.initiate(
   { 
      _id: "rs0",
      members: [
         { _id: 0, host : "mongo-0.mongo.default.svc.cluster.local:27017"},
         { _id: 1, host : "mongo-1.mongo.default.svc.cluster.local:27017"},
         { _id: 2, host : "mongo-2.mongo.default.svc.cluster.local:27017"}
         ]
    }
)
use test
db.todos.insert({title: "write a blog post"})
db.todos.find()

to check status
rs.status
rs
to make secondary to read the data of primary switch to secondary pod and run the command
rs.slaveOk()
