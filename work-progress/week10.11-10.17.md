# Week 10.11 - 10.17

## Maybe ....

1. Compilation plans

## Reminder

1. Don't hardcode CMAKE_INSTALL_LIBDIR

2. Maybe PyMilvus weekly report

## Todo - Speech PPT and video recording (due 10.20)

## Not in schedule
**10.15 Fri.**

- [Bug]: Data race in DataCoord ut #9929

- Wangting: Benchmark panic for check_pass_param bug (issue #755, pr #756)

**10.14 Wed.**

- Xiangyu build protobuf failed and let me know about the mess in build-protobuf. Fixed Xiangyu's problem.
    but need to fix the compilation in protobuf (issue #9876)(pr #9881)

- Zhenshan: DataNode metrics

- Meeting: Flush redesign


**10.12 Tue.**

- Meeting about PyMilvus

- Use config as parameters (9707)

- Yunmei's issue: Insert 10,000,000 in 10,000 batch, the result num_entites is lesser than 10 million
    - In the middle of the insert, pulsar is out-of-service for a while, and some messages seemed not produced successfully.

**10.11 Mon.**

- Reviewed delete implementation (8050)

----------------------------

## Todo - Review
### [**DONE**] PyMilvus review

**10.14 Thur.** Reviewed

----------------------------

### [**DONE**] 1. Arrow compilation review
**10.11 Mon.**

- Figuring out what's this PR and why do we need it. a + b needs in memory arrow

- Gave Guan suggestions on how to make PR

----------------------------

### [**DONE**] 2. Knowhere compilation review
**10.13 Wed.**
- Work arround `set(CMAKE_INSTALL_LIBDIR lib)` for centOS compilation, fix later.

**10.12 Tue.**

- Setting up centOS 7 environment is a hard work, but successfully make all on CentOS 7.

- `make test-cpp` failed because openblas is installed on `lib64`, but other libraries is installed on `lib`. We only add `lib` into `$LD_LIBRARY_PATH`

    - It's a long way to fix, the easiest might be recording this and change the centOS Dockerfile line 42, from `/usr/local/lib` into `/usr/local/lib64`.

    - So it's recommended to download OpenBLAS on the system.

**10.11 Mon.**

- I reviewed the codes again, despite some tiny problems, it's ready to merge.

- Before merging, Shen needs to squash all commit messages,
and I need to double check on **Ubuntu18.04 and CentOS7**.

- Found bug in build.sh under index/ `-u` config, konwhere had never built and run unit tests.

- Tested knowhere on Ubuntu18.04 from a clean environment without/with OpenBLAS

    - `./build.sh -u` passed

    - `./test_knowhere` ut passed

- Tested Milvus on Ubuntu18.04 from a clean environment without/with OpenBLAS

    - `make all` passed

    - `make test-cpp` passed

- Build unit tests in knowhere failed for the first time

    `CMAKE_INSTALL_LIBDIR` is in `GNUInstallDirs` module, need to include the latter before
    using the former.

---------------------------

## Todo - Create

### **[DONE]** 1. Sum up 7313 problems and sulotions.

**This is done by Thursday's meeting of flush redesign**

### **[DONE]** 2. Design DataNode flush task scheduler.

 **This is done by Thursday's meeting of flush redesign**

### 3. Write PyMilvus contributing doc.

### 4. Refactor PyMilvus error handler.

### 5. DataNode compaction implementation

    - FlushManager (congqi)
    - BinlogReader
    - BinlogWriter

**10.15 Fri.**

1. Update SegmentInfo proto to support stats-binlog and delta-binlog(issue #9922, pr #9925)

**10.14 Thur.**
1. Meeting after meeting, resiponsibility is roughly clear.

**10.13 Wed.**
1. Deep understanding of `io.Reader` interface. Use it in the right way.(9790)


---------------------------

## Enhancement plan

1. If a function has many parameters, change it into a config struct

```go
type serverOption struct {
    address string
    port    int
    path    string
    timeout time.Duration
}

func newOption() *serverOption{ // default parameters
    return &serverOption{
        address: "0.0.0.0",
        port:    8080,
        path:    "/var/test",
        timeout: time.Second * 5,
    }
}

func server(option *serverOption){}
```
