コピペ
http://nesv.github.io/golang/2014/02/25/worker-queues-in-go.html

## ビルド

```
$ go build -o queued *.go
$ ./queued -n 2048
```

- 別tmuxのペインで

```
$ for i in {1..4096}; do curl localhost:8000/work -d name=$USER -d delay=$(expr $i % 11)s; done
```
