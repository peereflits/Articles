# Failing to pull docker images from mcr.microsoft.com?

**TL;DR; Turn off IPv6.**

Just recently (possibly after a Windows update) I encountered issues with docker my docker files and compose scripts: it wouldn't build anymore.

After some investigation I could narrow the issue down to a failed `docker pull` from `mcr.microsoft.com`. At least the following images failed:

``` script
docker pull mcr.microsoft.com/mssql/server:2022-latest
docker pull mcr.microsoft.com/dotnet/sdk:8.0
docker pull mcr.microsoft.com/dotnet/aspnet:8.0
```

And they failed with an message like

``` script
... failed to resolve source metadata for mcr.microsoft.com/image/name:version: failed to do request: Head "https://mcr.microsoft.com/some-long-url": EOF
# or 
... failed to copy: httpReadSeeker: to do request: Get "https://mcr.microsoft.com/long-url-with-sha": EOF
```

Strangely enough did `docker pull nginx:alpine` succeed. ???

GitHub issue [#165](https://github.com/microsoft/containerregistry/issues/165) files this issue, but the suggestion of downgrading docker desktop did not work. During further investigation I stumbled upon [#166](https://github.com/microsoft/containerregistry/issues/166). Some of the error messages mentioned occurred also om my machine. 

Some reasoning and Google queries further I experimented with turning off IPv6 in the network adapter on my machine.

![Network adapter settings](./2024-10-23-network-adapter.png)

After some testing (turn on, reboot, fail, turn off, reboot, success) I concluded: when IPv6 turned off I was able to build my docker(-compose) files, otherwise it failed.

It worked!

At least on my machine :grin:!

---

**Note:** In reply of this article some readers noted that they didn't have any issues with pulling 
images from `mcr.microsoft.com`. It turned out they're using Win 10. 

My machine runs on Win 11 pro 23H2. 
I assume it has to do with cipher suites. It looks like the issue started to happen after a Windows update, although I cannot pinpoint the exact time frame.
