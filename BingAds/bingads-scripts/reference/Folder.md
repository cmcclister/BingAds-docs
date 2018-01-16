# Folder
Provides methods to iterate through Folder objects.

|Method|Return Type|Description|
|-|-|-
addFile(File child)|[Folder](./Folder)|Adds the specified file to this folder.<br />
createFile(BlobSource blob)|[File](./File)|Creates a file in this folder using the content represented by the given Blob<br />
createFolder(String name)|[Folder](./Folder)|Creates a folder with the specified name in this folder.<br />
getFiles|[FileIterator](./FileIterator)|Returns a collection of all the files contained within this folder.<br />
getFilesByName(String name)|[FileIterator](./FileIterator)|Returns a collection of all the files contained within this folder and have the specified name.<br />
getFoldersByName|[FolderIterator](./FolderIterator)|Returns a collection of all folders contained within this folder which match the specified name.<br />
getName|String|Returns the name of this folder.<br />
getUrl|String|Returns the URL where this folder is located on OneDrive.<br />
removeFile(String child)|[Folder](./Folder)|Removes the file with the specified name from this folder and moves it to the Recycle bin folder on the user's OneDrive.<br />
