# FolderIterator
Provides methods to iterate through Folder objects.

|Method|Return Type|Description|
|-|-|-
hasNext|boolean|Returns true if this iterator has more Folder elements. <br />
next|[Folder](./Folder)|Advances to the next Folder in this iterator and returns it. <br />
totalNumEntities|int|Returns the total number of Folder objects indexed by this iterator. Note that if the total number of  entities returned by this method exceeds the limit for entity reads, the hasNext method will return  false and next will throw an error as soon as the latter is reached.<br />
