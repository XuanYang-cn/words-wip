# How to debug Milvus

- Logs
- Inspect meta
- Profiling Golang/CPP

## Three different types of profiling
### 1. CPU profiling
### 2. Memory profiling
### 3. Tracing

## Tools
### 1. go pprof

#### 1. How to enbale profiling

**For go unit tests, use gotest's standard `-cpuprofile` and `-memprofile` flags**
See [Testing flags](https://pkg.go.dev/cmd/go#hdr-Testing_flags)

**For a standalone program, use `runtime/pprof`**

**For a long-running server, use `net/http/pprof`**
### 2. go trace
### 2. dlv
### 3. gdb
