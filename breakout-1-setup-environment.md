# Breakout 1 - Set up the Lab Environment

In this lab you will:
- Verify your web terminal access
- Verify your Grafana Cloud access
- Deploy the sample application

## I. Verify web terminal access


A. Log into the web terminal. All files for the workshop have been put here and we will be using it as a place to run kubectl commands. This URL and the credentials will be given to you by your instructor. It will look something like:

```
https://wetty-<workshopName>.work-shop.grafana.net
```

B. For this workshop, we are all working in our own Kubernetes clusters. At the root of your home directory, you will find a file called `kubeconfig`. Set an OS environment variable `KUBECONFIG` to point to this file. IMPORTANT: If you log out and log back in, you will need to repeast this step.

```shell
export KUBECONFIG=$HOME/kubeconfig
```

C. Validate that you can see the context in your list:

```shell
kubectl config get-contexts
```

## II. Validate that you can log in to Grafana

<br>
A Grafana Cloud stack has been provisioned for you for this workshop. In this section we will validate that we can log into the instance.

<br>

A. Put your grafana stack URL into a browser. This will be:

```
https://<yourloginname>.grafana.net
```

If you logged into the web terminal with `karthik`, then your url will be `https://karthik.grafana.net`.

B. On the login screen, use the same username password that you did for the web terminal. Validate that you see the Grafana home screen.

<br>

**The first time you log in it might take a few seconds**

## III. Ensure the Sample Application is running

For the rest of the workshop, we will be using [Weaveworks Sockshop](https://microservices-demo.github.io/).

A. Open up k9s in the web terminal to see the progress of the application deploying.

```shell
k9s
```

![k9s console](images/image1.png)

Validate that all of the pods are ready.

You can exit the k9s application by using `Ctrl-C` or typing `:quit<Enter>`.

B. When everything is up, you should be able to reach the application via an https url that was created already. Your URL is:

```
https://<my-login-name>.work-shop.grafana.net
```

![sockshop](images/image4.png)

That's it! You successfully deployed the sample application.
