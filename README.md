#BSON-GO
This is a lightweight, zero dependency library providing some of the basic functionality from [labix.org/v2/mgo/bson](labix.org/v2/mgo/bson)

This package is primarily for those wanting to keep their microservices loosely-coupled from their database service layer
Therefore it is prudent to avoid using special types that are invariably tied to a specific database technology.

The purpose of this package is to provide the ability to create and validate Mongo ObjectIDs without having to actually deal with ObjectID types or any bson details. Creating a new objectID merely outputs a string

this is all [official bson code](labix.org/v2/mgo/bson) modified slightly to output strings instead of objectId types

Current FeatureList:
1. Create new Object IDs output as a string  
2. validate ObjectID strings  

###usage:
```
s := objectID.NewObjectID()
if ok := objectID.IsObjectIDHex(s); !ok {
  //handle error
}
```

######according to the BSON page, I have to include this copyright disclaimer:



```
 BSON library for Go

 Copyright (c) 2010-2012 - Gustavo Niemeyer <gustavo@niemeyer.net>

 All rights reserved.

 Redistribution and use in source and binary forms, with or without
 modification, are permitted provided that the following conditions are met:

 1. Redistributions of source code must retain the above copyright notice, this
    list of conditions and the following disclaimer.
 2. Redistributions in binary form must reproduce the above copyright notice,
    this list of conditions and the following disclaimer in the documentation
    and/or other materials provided with the distribution.

 THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND
 ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
 WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
 DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE FOR
 ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
 (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
 LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND
 ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
 (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
 SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
 gobson - BSON library for Go.
 ```
