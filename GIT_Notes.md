##Git Notes##

I tagged the wrong commit after it was pushed.  
Steps to move it to [72edf3c] 

1. Delete the remote tag:
 ```
 $ git push origin :refs/tags/v1.0.0
 To https://github.com/jware/jware.github.io.git
  - [deleted]         v1.0.0
```

2. Add the tag to the correct commit
 ```
 $ git tag -a -m  -f v1.0.0 72edf3c4161979f1baea4517079bca83c7597e96 
 Updated tag 'v1.0.0' (was 9ca6980)
```

32. Push it to origin
 ```
$ git push -v origin refs/tags/v1.0.0
Pushing to https://github.com/jware/jware.github.io.git
Counting objects: 1, done.
Writing objects: 100% (1/1), 156 bytes | 0 bytes/s, done.
Total 1 (delta 0), reused 0 (delta 0)
POST git-receive-pack (307 bytes)
To https://github.com/jware/jware.github.io.git
 * [new tag]         v1.0.0 -> v1.0.0
```
