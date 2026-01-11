### Write the post

Posts need to live in /myblog/content/posts
Each post should have its own folder, that way you can put post images in their own folder.

### Creating posts from the command line
1. `cd ~/myblog` 
	1. `cd` means **change directory.** This brings you to the myblog directory
2. `hugo new` is the command to create a new post, then you tell it where to write
3. `posts/foldername/post-name.md
4. Altogether: `hugo new posts/foldername/post-name.md`
	1. Hugo will create the folder if it doesn't exist yet
	2. Hugo will create the markdown file as well.

### Creating posts from your OS
1. Navigate to `myblog/content/posts/`
2. Create a new folder for the post
3. Create a new markdown file in that folder 
	1. `Right click > new document > Empty document
4.  Change the front matter
5. Write the post
6. Preview locally
7. hugo server > Click localhost link

### Sample front matter

```
+++
title = "Niall: Character Creation"
date = 2025-12-30T22:10:11-05:00
draft = false
categories = ["Fiction"]
tags = ["solorpg", "Niall"]
image = "image.jpg"
+++
```

* You need `+++` before and after to distinguish front matter
* If you create from the command line, `date` will be generated automatically
* 
### Handling images
* Store images directly in the folder of the post.*

#### For post preview / feature images:
In the metadata (front matter) include:

`image = "cover.jpg"`  or full path like `"images/tyov/cover.jpg"
Hugo will know to check the folder first.

#### For in-line pictures
**If the image is in the post's own folder**
`![Description](image.jpg)`
### Otherwise where can I put pictures?
* In the Static folder `myblog/static/folder/image.jpg`

## Publishing

#### 1. Change draft status
* Make sure that the posts you want to publish are changed from `draft = true` to `draft = false` otherwise it won't post.
#### 2. Tell Git what you want to post in two ways:
**Option 1: Specify which posts 
* `git add content/posts/my-new-post.md` Will add only that post.

**Option 2: Publish all changes
* `git add . ` # Will include any and all changes rather than a specific file.
### 3. Commit the change.
* `git commit -m "Add new post"`
* `-m` means "message"

### 4. Push the change
* `git push`

## Categories and Tags
Categories are the big subjects that you will use your blog for.
Tags are individual, smaller subjects 
### Category structure
`Fiction
`Essays
`Poetry
`Recommendations`
`Projects`

### Tag structure
`TYOV (thousand year old vampire)`
`TTPRG`
`poem`
`creativity`
`writing`
`consciousness`
`identity`
`worldbuilding`
``