#BSON-GO
This is a lightweight, zero dependency library providing some of the basic functionality from [labix.org/v2/mgo/bson]

This package is primarily for those wanting to keep their microservices loosely-coupled from their database service layer
Therefore it is prudent to avoid using special types that are invariably tied to a specific database technology.

The purpose of this package is to provide the ability to create and validate Mongo ObjectIDs without having to actually deal with ObjectID types or any bson details. Creating a new objectID merely outputs a string

this is all [official bson code](labix.org/v2/mgo/bson) modified slightly to output strings instead of objectId types
