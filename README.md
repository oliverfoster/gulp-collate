# gulp-collate

Take all files from gulp.src, collate/rename all files to come from 'foldername':

  
Given: 
```
/path/src/
├── a.txt
├── b.txt
├── c.txt
├── path1
├──		└──assets
├──			├── z.txt
├──	    	├── a.txt
├──	    	└── b.txt
├──path2
		└──path3
			├──
	    	├── y.txt
	    	├── z.txt
			└──assets
				├──
	 	    	├── 1.txt
	    		└── 2.txt
```
  
And:
```
gulp.src( "/path/src/" )
	.pipe(collate("assets"))
	.pipe(gulp.dest("/path/dest/"));

```
  
Outputs:
```
/path/dest/
├──	z.txt
├──	a.txt
├──	b.txt
├── 1.txt
└──	2.text

```