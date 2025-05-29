# MongoDB Assignment: Todo List
📦 Database Selection
use Mongo_Assignment // Output: switched to db Mongo_Assignment

## Insert Multiple Todos
db.todos.insertMany([ { taskName: "Buy groceries", status: false, priority: "Medium", description: "Purchase fruits, vegetables, milk, and bread from the supermarket." }, { taskName: "Complete project report", status: false, priority: "High", description: "Finish writing and editing the final report for the marketing project." }, // ... (other 8 records) ]);

## Output:
{ acknowledged: true, insertedIds: { "0": ObjectId("..."), "1": ObjectId("..."), // ... } }

## View All Todos
db.todos.find()

## Sample Output:
{ _id: ObjectId("..."), taskName: "Buy groceries", status: false, priority: "Medium", description: "Purchase fruits, vegetables, milk, and bread from the supermarket." }

## Update All Status to false
db.todos.updateMany({}, { $set: { status: false } })

## Output:
{ acknowledged: true, matchedCount: 10, modifiedCount: 3 }

## Set Priority Levels
// High Priority db.todos.updateMany( { taskName: { $in: [ "Complete project report", "Review team presentation", "Pay utility bills", "Backup laptop data" ]} }, { $set: { priority: "High" } } )

// Medium Priority db.todos.updateMany( { taskName: { $in: [ "Buy groceries", "Morning workout", "Plan weekend trip" ]} }, { $set: { priority: "Medium" } } )

// Low Priority db.todos.updateMany( { taskName: { $in: [ "Call the dentist", "Clean the garage", "Read a book" ]} }, { $set: { priority: "Low" } } )

## Schema Validation
db.runCommand({ collMod: "todos", validator: { priority: { $in: ["Low", "Medium", "High"] } }, validationLevel: "moderate" })

## Test Invalid Insert:
db.todos.insertOne({ taskName: "Test invalid priority", status: false, priority: "Higher", description: "This should fail if schema validation is enforced." })

## Output:
MongoServerError: Document failed validation

## Add Dates
db.todos.updateMany({}, { $set: { updatedDate: null, dueDate: null } })

## Set Dates for One Todo:
db.todos.updateOne( { taskName: "Buy groceries" }, { $set: { updatedDate: new Date(), dueDate: ISODate("2025-06-15T00:00:00Z") } } )

## Update Status
db.todos.updateOne( { _id: ObjectId("68371a905ac635fb39d1b8ca") }, { $set: { status: true } } ) db.todos.find()

❗ Output:
{ _id: ObjectId('68371a905ac635fb39d1b8ca'), taskName: 'Buy groceries', status: true, priority: 'Medium', description: 'Purchase fruits, vegetables, milk, and bread from the supermarket.', dueDate: 2025-06-15T00:00:00.000Z, updatedDate: 2025-05-28T16:33:42.612Z } { _id: ObjectId('68371a905ac635fb39d1b8cb'), taskName: 'Complete project report', status: false, priority: 'High', description: 'Finish writing and editing the final report for the marketing project.', dueDate: null, updatedDate: null } { _id: ObjectId('68371a905ac635fb39d1b8cc'), taskName: 'Morning workout', status: false, priority: 'Medium', description: '30-minute workout session including cardio and stretching exercises.', dueDate: null, updatedDate: null } { _id: ObjectId('68371a905ac635fb39d1b8cd'), taskName: 'Call the dentist', status: false, priority: 'Low', description: 'Schedule a routine dental check-up appointment.', dueDate: null, updatedDate: null } { _id: ObjectId('68371a905ac635fb39d1b8ce'), taskName: 'Review team presentation', status: false, priority: 'High', description: 'Go through the slides and provide feedback to the design team.', dueDate: null, updatedDate: null } { _id: ObjectId('68371a905ac635fb39d1b8cf'), taskName: 'Clean the garage', status: false, priority: 'Low', description: 'Organize tools and remove old boxes from the garage.', dueDate: null, updatedDate: null } { _id: ObjectId('68371a905ac635fb39d1b8d0'), taskName: 'Pay utility bills', status: false, priority: 'High', description: 'Paid electricity, water, and internet bills online.', dueDate: null, updatedDate: null } { _id: ObjectId('68371a905ac635fb39d1b8d1'), taskName: 'Plan weekend trip', status: false, priority: 'Medium', description: 'Research locations and accommodations for a short weekend getaway.', dueDate: null, updatedDate: null } { _id: ObjectId('68371a905ac635fb39d1b8d2'), taskName: 'Backup laptop data', status: false, priority: 'High', description: 'Create a backup of important files to an external hard drive or cloud.', dueDate: null, updatedDate: null } { _id: ObjectId('68371a905ac635fb39d1b8d3'), taskName: 'Read a book', status: false, priority: 'Low', description: 'Finished reading “Atomic Habits” by James Clear.', dueDate: null, updatedDate: null }
