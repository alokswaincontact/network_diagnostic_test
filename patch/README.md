### Clone the NDT Server code.
First we have to clone the NDT Server code. The code is kept here.
https://github.com/m-lab/ndt-server

```git
git clone https://github.com/m-lab/ndt-server
```

### Go to the Correct Checkout
We made these changes in an older source code release. 
First we have to checkout that older source release.
The release that we made changes to have a SHA #id of 8032c57

```git
git checkout 8032c57
```

### Apply Patch 
Then apply the patch 

```git
git apply no_bbr.patch
```
