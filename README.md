# Mongodb ToDo List Assignment


>> Atlas atlas-2ig97m-shard-0 [primary] test> db.tasks.insertMany([{name:"Docker",status:"pending"},{name:"AWS",status:"completed"},{namAtlas atlas-2ig97m-shard-0 [primary] test> db.tasks.insertMany([{name:"Docker",status:"pending"},{name:"AWS",status:"completed"},{name:"Python",status:"pending"},{name:"Jenkins",status:"completed"},{name:"SonarQube",status:"pending"},{name:"Mongo",status:"completed"},{name:"Lambda",status:"pending"},{name:"Promethius",status:"completed"},{name:"Graffana",status:"pending"},{name:"Linux",status:"completed"}]);

{

  acknowledged: true,
  
  insertedIds: {
  
    '0': ObjectId('68373e61c6c9a40e996c4bd0'),
    
    '1': ObjectId('68373e61c6c9a40e996c4bd1'),
    
    '2': ObjectId('68373e61c6c9a40e996c4bd2'),
    
    '3': ObjectId('68373e61c6c9a40e996c4bd3'),
    
    '4': ObjectId('68373e61c6c9a40e996c4bd4'),
    
    '5': ObjectId('68373e61c6c9a40e996c4bd5'),
    
    '6': ObjectId('68373e61c6c9a40e996c4bd6'),
    
    '7': ObjectId('68373e61c6c9a40e996c4bd7'),
    
    '8': ObjectId('68373e61c6c9a40e996c4bd8'),
    
    '9': ObjectId('68373e61c6c9a40e996c4bd9')
    
  }
  
}

>> Atlas atlas-2ig97m-shard-0 [primary] test> db.tasks.find()

[

  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd0'),
    
    name: 'Docker',
    
    status: 'pending'
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd1'),
    
    name: 'AWS',
    
    status: 'completed'
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd2'),
    
    name: 'Python',
    
    status: 'pending'
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd3'),
    
    name: 'Jenkins',
    
    status: 'completed'
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd4'),
    
    name: 'SonarQube',
    
    status: 'pending'
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd5'),
    
    name: 'Mongo',
    
    status: 'completed'
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd6'),
    
    name: 'Lambda',
    
    status: 'pending'
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd7'),
    
    name: 'Promethius',
    
    status: 'completed'
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd8'),
    
    name: 'Graffana',
    
    status: 'pending'
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd9'),
    
    name: 'Linux',
    
    status: 'completed'
    
  }
  
]


>> Atlas atlas-2ig97m-shard-0 [primary] test> db.tasks.updateMany({status:"pending"},{$set:{status:false}})

{

  acknowledged: true,
  
  insertedId: null,
  
  matchedCount: 5,
  
  modifiedCount: 5,
  
  upsertedCount: 0
  
}

>> Atlas atlas-2ig97m-shard-0 [primary] test> db.tasks.updateMany({status:"completed"},{$set:{status:true}})

{

  acknowledged: true,
  
  insertedId: null,
  
  matchedCount: 5,
  
  modifiedCount: 5,
  
  upsertedCount: 0
  
}

>> Atlas atlas-2ig97m-shard-0 [primary] test> db.tasks.find()

[

  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd0'),
    
    name: 'Docker',
    
    status: false
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd1'),
    
    name: 'AWS',
    
    status: true
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd2'),
    
    name: 'Python',
    
    status: false
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd3'),
    
    name: 'Jenkins',
    
    status: true
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd4'),
    
    name: 'SonarQube',
    
    status: false
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd5'),
    
    name: 'Mongo',
    
    status: true
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd6'),
    
    name: 'Lambda',
    
    status: false
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd7'),
    
    name: 'Promethius',
    
    status: true
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd8'),
    
    name: 'Graffana',
    
    status: false

  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd9'),
    
    name: 'Linux',
    
    status: true
    
  }
  
]

>> Atlas atlas-2ig97m-shard-0 [primary] test> db.tasks.updateMany({},{$set:{status:false}})

{

  acknowledged: true,
  
  insertedId: null,
  
  matchedCount: 10,
  
  modifiedCount: 5,
  
  upsertedCount: 0
  
}

>> Atlas atlas-2ig97m-shard-0 [primary] test> db.tasks.find()

[

  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd0'),
    
    name: 'Docker',
    
    status: false
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd1'),
    
    name: 'AWS',
    
    status: false
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd2'),
    
    name: 'Python',
    
    status: false
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd3'),
    
    name: 'Jenkins',
    
    status: false
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd4'),
    
    name: 'SonarQube',
    
    status: false
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd5'),
    
    name: 'Mongo',
    
    status: false
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd6'),
    
    name: 'Lambda',
    
    status: false
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd7'),
    
    name: 'Promethius',
    
    status: false
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd8'),
    
    name: 'Graffana',
    
    status: false
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd9'),
    
    name: 'Linux',
    
    status: false
    
  }
  
]

>> Atlas atlas-2ig97m-shard-0 [primary] test> db.tasks.insertOne({name:'Latest',status:false})

{

  acknowledged: true,
  
  insertedId: ObjectId('68373f3ec6c9a40e996c4bda')
  
}

>> Atlas atlas-2ig97m-shard-0 [primary] test> db.tasks.updateOne({_id:ObjectId('68373f3ec6c9a40e996c4bda')},{$set:{status:true}})

{

  acknowledged: true,
  
  insertedId: null,
  
  matchedCount: 1,
  
  modifiedCount: 1,
  
  upsertedCount: 0
  
}

>> Atlas atlas-2ig97m-shard-0 [primary] test> db.tasks.find()

[

  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd0'),
    
    name: 'Docker',
    
    status: false
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd1'),
    
    name: 'AWS',
    
    status: false
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd2'),
    
    name: 'Python',
    
    status: false
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd3'),
    
    name: 'Jenkins',
    
    status: false
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd4'),
    
    name: 'SonarQube',
    
    status: false
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd5'),
    
    name: 'Mongo',
    
    status: false
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd6'),
    
    name: 'Lambda',
    
    status: false
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd7'),
    
    name: 'Promethius',
    
    status: false
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd8'),
    
    name: 'Graffana',
    
    status: false
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd9'),
    
    name: 'Linux',
    
    status: false
    
  },
  
  {
  
    _id: ObjectId('68373f3ec6c9a40e996c4bda'),
    
    name: 'Latest',
    
    status: true
    
  }
  
]

>> Atlas atlas-2ig97m-shard-0 [primary] test> db.tasks.updateMany({},{$set:{Updated_at:new Date()}})

{

  acknowledged: true,
  
  insertedId: null,
  
  matchedCount: 11,
  
  modifiedCount: 11,
  
  upsertedCount: 0
  
}

>> Atlas atlas-2ig97m-shard-0 [primary] test> db.tasks.find()

[

  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd0'),
    
    name: 'Docker',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd1'),
    
    name: 'AWS',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd2'),
    
    name: 'Python',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd3'),
    
    name: 'Jenkins',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd4'),
    
    name: 'SonarQube',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd5'),
    
    name: 'Mongo',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd6'),
    
    name: 'Lambda',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd7'),
    
    name: 'Promethius',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd8'),
    
    name: 'Graffana',
    
    status: false,

    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd9'),
    
    name: 'Linux',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373f3ec6c9a40e996c4bda'),
    
    name: 'Latest',
    
    status: true,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  }
  
]

>> Atlas atlas-2ig97m-shard-0 [primary] test> db.tasks.updateMany({name:'Linux'},{$set:{DeadLine:new Date("2025-05-29T11:19:24.767Z")}})

{

  acknowledged: true,
  
  insertedId: null,
  
  matchedCount: 1,
  
  modifiedCount: 1,
  
  upsertedCount: 0
  
}

>> Atlas atlas-2ig97m-shard-0 [primary] test> db.tasks.find()

[

  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd0'),
    
    name: 'Docker',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd1'),
    
    name: 'AWS',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd2'),
    
    name: 'Python',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd3'),
    
    name: 'Jenkins',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd4'),
    
    name: 'SonarQube',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd5'),
    
    name: 'Mongo',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {

    _id: ObjectId('68373e61c6c9a40e996c4bd6'),
    
    name: 'Lambda',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },

  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd7'),
    
    name: 'Promethius',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd8'),
    
    name: 'Graffana',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd9'),
    
    name: 'Linux',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z'),
    
    DeadLine: ISODate('2025-05-29T11:19:24.767Z')
    
  },
  
  {
  
    _id: ObjectId('68373f3ec6c9a40e996c4bda'),
    
    name: 'Latest',
    
    status: true,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  }
  
]

>> Atlas atlas-2ig97m-shard-0 [primary] test> db.tasks.updateOne({name:'Graffana'},{$set:{DeadLine:new Date()}})

{

  acknowledged: true,
  
  insertedId: null,
  
  matchedCount: 1,
  
  modifiedCount: 1,
  
  upsertedCount: 0
  
}

>> Atlas atlas-2ig97m-shard-0 [primary] test> db.tasks.find()

[

  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd0'),
    
    name: 'Docker',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd1'),
    
    name: 'AWS',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd2'),
    
    name: 'Python',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd3'),
    
    name: 'Jenkins',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd4'),
    
    name: 'SonarQube',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd5'),
    
    name: 'Mongo',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd6'),
    
    name: 'Lambda',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd7'),
    
    name: 'Promethius',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd8'),
    
    name: 'Graffana',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z'),
    
    DeadLine: ISODate('2025-05-28T16:56:13.222Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd9'),
    
    name: 'Linux',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z'),
    
    DeadLine: ISODate('2025-05-29T11:19:24.767Z')
    
  },
  
  {
  
    _id: ObjectId('68373f3ec6c9a40e996c4bda'),
    
    name: 'Latest',
    
    status: true,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  }
  
]

>> Atlas atlas-2ig97m-shard-0 [primary] test> db.tasks.find({Updated_at:{$gt: new Date(new Date().getTime()-2*60*1000)}})

>> Atlas atlas-2ig97m-shard-0 [primary] test> db.tasks.find({Updated_at:{$gt: new Date(new Date().getTime()-6*60*1000)}})

[

  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd0'),
    
    name: 'Docker',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd1'),
    
    name: 'AWS',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd2'),
    
    name: 'Python',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd3'),
    
    name: 'Jenkins',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd4'),
    
    name: 'SonarQube',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd5'),
    
    name: 'Mongo',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd6'),
    
    name: 'Lambda',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd7'),
    
    name: 'Promethius',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd8'),
    
    name: 'Graffana',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z'),
    
    DeadLine: ISODate('2025-05-28T16:56:13.222Z')
    
  },
  
  {
  
    _id: ObjectId('68373e61c6c9a40e996c4bd9'),
    
    name: 'Linux',
    
    status: false,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z'),
    
    DeadLine: ISODate('2025-05-29T11:19:24.767Z')
    
  },
  
  {

    _id: ObjectId('68373f3ec6c9a40e996c4bda'),
    
    name: 'Latest',
    
    status: true,
    
    Updated_at: ISODate('2025-05-28T16:53:25.103Z')
    
  }
  
]

>> Atlas atlas-2ig97m-shard-0 [primary] test> db.tasks.countDocuments()

11


>> Atlas atlas-2ig97m-shard-0 [primary] test> db.tasks.countDocuments({DeadLine:true})

0

>> Atlas atlas-2ig97m-shard-0 [primary] test> db.tasks.countDocuments({})

11

>> Atlas atlas-2ig97m-shard-0 [primary] test> db.tasks.countDocuments({name:'Promethius'})

1
