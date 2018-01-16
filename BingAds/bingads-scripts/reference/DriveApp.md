# DriveApp
This class provides methods to manage the OneDrive account of the user.

|Method|Return Type|Description|
|-|-|-
createFile(BlobSource blob)|[File](./File)|Creates a new file in the root folder of the user's OneDrive using the contents in the specified blob.<br />
createFile(String name, String content)|[File](./File)|Creates a new file in the root folder of the user's OneDrive using the contents in the specified string and with the given name.<br />
getFileById(String id)|[File](./File)|Returns a file in the user's OneDrive that matches the specified ID.<br />
getFiles|[FileIterator](./FileIterator)|Returns all files in the user's OneDrive.<br />
getFilesByName(String)|[FileIterator](./FileIterator)|Returns all files in the user's OneDrive that match the given name.<br />
getFolderById(String)|[Folder](./Folder)|Returns a folder in the user's OneDrive that matches the specified ID.<br />
getFoldersByName(String)|[FolderIterator](./FolderIterator)|Returns all folders in the user's OneDrive that match the given name.<br />
getRootFolder|[Folder](./Folder)|Returns the root folder of the user's OneDrive.<br />
