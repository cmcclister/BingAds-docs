# File
Represents a file in OneDrive.

|Method|Return Type|Description|
|-|-|-
getAs(String contentType)|[Blob](./Blob)|Converts the contents of this file to the given type and returns it as a blob.<br />
getBlob|[Blob](./Blob)|Returns the contents of this file as a blob.<br />
getId|String|Returns the ID of this file.<br />
getName|String|Returns the name of this file.<br />
getParents|[FolderIterator](./FolderIterator)|Returns a list of folders that are the immediate parents of this file.<br />
getUrl|String|Returns the URL where this file is located on OneDrive.<br />
setContent(String content)|[File](./File)|Replaces the content of this file with the given string. <br />
setTrashed(boolean trashed)|[File](./File)|Specifies whether this file is in the Recycle bin of the user's OneDrive.<br />
