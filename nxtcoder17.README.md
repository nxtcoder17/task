In makefile, you can do this
![screenshot-11553](https://user-images.githubusercontent.com/22402557/194401702-244b61d3-ac99-46ce-89b0-1fdaab16f0df.png)

but by default, you can't do the same thing in Taskfile, because the args go into `vars` not `env`
![screenshot-6834](https://user-images.githubusercontent.com/22402557/194401943-495ff86a-6a07-40e8-b19d-7c2fbd6536a0.png)

this PR produces the desired behaviour, if  `exportVars` is set at global level
![screenshot-26538](https://user-images.githubusercontent.com/22402557/194402126-8b41f1c6-a542-4799-8389-b631e1ab0d0f.png)
