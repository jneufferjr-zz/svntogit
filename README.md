# svntogit
Description  : Aid in migrating existing SVN Repos to a Git Repos.

It is expected that this script will be executed against a 
SVN Working Copy and not a SVN repository.

This script will pull the user names from an SVN working copy
and populate a file with the user name and an arbitrary email 
address for each user name found.  The file with the user 
name and email address is used during the Git "svn clone". 

I have 12 SVN Repositories and I wanted to automate this
process of creating a file, adding the related user names and 
generating their arbitrary email addresses. 

I keep all of my working copies in a single directory.

It looks like this, 

```             
/dir_top+
        |
     ^  /dir_repos_1/
     |  |
     |  /dir_repos_2/
     |
     |         ^         
     |         |         
 Top level   Repos      
 Directory    Dir
```
 Place this script (list_svn_users.sh) in the top level
 directory (dir_top).
 
 Since SVN doesn't care about email addresses the following
 was chosen: migrated@import.pvt
