This repository uses git-annex and git-remote-gcrypt to manage files. The files' contents are available in a [public Amazon S3 special remote](https://git-annex.branchable.com/tips/public_Amazon_S3_remote/) that is backed by this [S3 Bucket](http://s3.amazonaws.com/liujoshua-public-files?prefix=git-annex).

## Setup 
Obtain GPG key 8B545223, which is used to by gcrypt to encrypt the git repository contents, and also to encrypt/decrypt from S3.
Obtain 

AWS access key and secret key

Clone and navigate into the repository

    # git clone gcrypt::git@github.com:liujoshua/files.git
    # cd files
    
We be using GitHub for managine the directory tree but not for syncing file contents, so tell git-annex not to store file contents to origin by default

    # git config remote.origin.annex-ignore true
    
Initialize the repository for git-annex

    # git annex init
    
