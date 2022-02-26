# [ceeveetemplate](https://www.styleshout.com/free-templates/ceevee/)
## Just view this on my website https://j0hnniewa1ker.com/

## Just run from my image
```
podman run --name ceevee --rm -d -p 8080:80 quay.io/j0hnniewa1ker/ceevee
```

## An online ceevee template in reactjs  
Instruction to run: 
1) forked the repo from [Saurabh Mhatre](https://github.com/smhatre59/resumetemplate)

2) Modified these files
```
        deleted:    public/images/header.jpg
        deleted:    public/images/portfolio/phone.jpg
        deleted:    public/images/portfolio/project.jpg
        deleted:    public/images/portfolio/project2.png
        deleted:    public/images/testimonials-bg.jpg
        modified:   package-lock.json
        modified:   package.json
        modified:   public/css/layout.css
        modified:   public/images/profilepic.jpg
        modified:   public/index.html
        modified:   src/App.js
        modified:   src/components/about/about.js
        modified:   src/components/header/header.js
        modified:   src/components/portfolio/portfolio.js
        modified:   src/components/resume/resume.js
        modified:   src/resumeData.js
        modified:   README.md
        added:      Dockerfile
```
3) copied these photos but didn't add them to the repo:
```
        public/images/IMG_0788.png
        public/images/portfolio/DJI_0110.jpg
        public/images/portfolio/IMG_0085.jpg
        public/images/portfolio/IMG_7076.jpg
        public/images/portfolio/e.jpg
```



4) Generated build using command:  
 ```
 npm run build
 ```
 
5) Build a [nginx](https://hub.docker.com/_/nginx) image including the build folder
```
podman build -t quay.io/j0hnniewa1ker/ceevee .
podman login quay.io
podman push quay.io/j0hnniewa1ker/ceevee
```

6) run a container from the image
```
podman run --name ceevee --rm -d -p 8080:80 quay.io/j0hnniewa1ker/ceevee
```

7) hit `http://localhost:8080`


For detailed instructions on how the ceevee template was created go to Saurabh Mhatre's [Medium Article](https://medium.com/technoetics/create-a-developer-portfolio-using-reactjs-d34ea1bfb18e)
