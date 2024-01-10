### Group routes

这个例子展示了如何在各自的文件中对不同的路由进行分组，并以有序的方式将它们分组在一起，就像这样:
```go
func getRoutes() {
	v1 := router.Group("/v1")
	addUserRoutes(v1)
	addPingRoutes(v1)

	v2 := router.Group("/v2")
	addPingRoutes(v2)
}
```
