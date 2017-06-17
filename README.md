# Build & Run a Go application in Docker

You can quickly get started with developing a Go application by cloning this, putting in desired .go files, and building & running per below.

There is a sample Go program showing how to [encode and decode JSON](https://gobyexample.com/json).

[Go by Example](gobyexample) is a good place to get started in learning Go.

## Build & Run

```
docker build -t my-golang-app .

docker run -it --rm --name my-running-app my-golang-app
```

## Compile

If you'd like to compile but not run the app, run the following.

```
docker run --rm -v "$PWD":/usr/src/myapp -w /usr/src/myapp golang:1.8 go build -v
```