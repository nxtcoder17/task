Extra Functionalities over go-task:

- [ ] `CLI ARGS` in env vars (like Makefile)

In makefile, you can do this
![screenshot-11553](https://user-images.githubusercontent.com/22402557/194401702-244b61d3-ac99-46ce-89b0-1fdaab16f0df.png)

but by default, you can't do the same thing in Taskfile, because the args go into `vars` not `env`
![screenshot-6834](https://user-images.githubusercontent.com/22402557/194401943-495ff86a-6a07-40e8-b19d-7c2fbd6536a0.png)

this PR produces the desired behaviour, if  `exportVars` is set at global level
![screenshot-26538](https://user-images.githubusercontent.com/22402557/194402126-8b41f1c6-a542-4799-8389-b631e1ab0d0f.png)

***
- [ ] Individual Tasks can have their DotEnvs

```yaml
version: 3
tasks:
  example:
    dotenv:
      - .env
    silent: true
    cmds:
      - echo "$KEY"
```
![screenshot-25579](https://user-images.githubusercontent.com/22402557/199872487-e6987c76-aa16-4618-92da-535ca8fdee8d.png)
