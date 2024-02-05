# VersionManager
Tool to manage cache versions in houdini (used houdini19.5 to create). 

## Features
* Presents a list of available versions of all the caches in the houdini scene
* Enables switching to any available version
* Provides the option to delete unused versions of a cache

## Usage
Place the version_manager.shelf file in any of the toolbar locations recognized by houdini and relaunch houdini

## UI

![image](https://github.com/jroy1992/VersionManager/assets/22520387/026cf87b-8eb2-4191-9b31-420b5bd4113c)


**Name:** Name of the cache in the scene file

**Version:** The current version of the cache in the scene file. The dropdown allows switching to any available version of the cache.

**Delete Older Versions:** Displays the available older versions of the cache based on the selected version in the *Version* column. Provide the option to delete the older versions by toggling on the checkbox.
If there are no older versions available, --- is displayed with the checkbox disabled.

**Apply:** Updates the version(s) of cache(s) in the scene based on version selected in *Version* column and deletes the older version(s) of the cache(s) if enabled


After hitting the *Apply* button, a dialog pops up with the summary of actions undertaken. If version deletion fails for any reason, it's notified in the dialog as well.
* Both updation and deletion successful
  
  ![image](https://github.com/jroy1992/VersionManager/assets/22520387/44418387-3a48-4515-9051-445268bb4b1e)


* Deletion failed

  ![image](https://github.com/jroy1992/VersionManager/assets/22520387/75bed838-9a1f-452a-9983-f40017d6ea4e)

  > [!NOTE]
  > 
  > Found that when switched to a new later version, sometimes houdini keeps hold of the previously selected version file and prevents deletion. Houdini needs to be closed to release the locked file. 


* Apply button pressed without any operation selected

  ![image](https://github.com/jroy1992/VersionManager/assets/22520387/5de95f27-38d6-4e89-8f1a-6390f04fc3f9)

