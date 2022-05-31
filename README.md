# template-remix

Boilerplate web app using the following tech:

- remix.run
- typescript
- tailwind css
- prisma
- terraform
- github actions

This boilerplate deploys apps to my Kubernetes cluster, although it would be
portable to most Kubernetes clusters. The design of my cluster is detailed on
my blog:

https://jackdevries.com/blog/myCluster

## Usage Steps

1. Uncomment deploy step in the github action
2. In `./Makefile`, change the `CONTAINER_NAME` variable, and `DOCKER_ACCOUNT`
   variable as well if you're not me.
3. In `./infra.tf`, change arguments to the _basic-deployment_ resource. In
   particular, change the `app_name` to something appropriate, change the
   `container` to match the container name in the Makefile, and put the target
   application domain.
4. The tailwind config is basically empty, but it's always good to do this
   early in a new project as you put together the design system.
