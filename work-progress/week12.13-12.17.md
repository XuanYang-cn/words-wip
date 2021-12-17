# Week 12.13 - 12.17

---
## TODO - bug fix
- PyMilvus Socket operation on non-socket (issue 778)
- PyMilvus connection pool is not useful (ref: grpc issue 20985)

---
## TODO - enhancement
1. Don't hardcode CMAKE_INSTALL_LIBDIR (issue 8143, 9772)
3. Clear and Unify BaseKV interface behaviour (issue 11313)
    - Fix memoryKV load and basetable (pr 11423)
4. Test minIO inside configs rootPath (issue 11237)
    - minIO tests (pr 11255)
    - etcd
    - rocksDB
5. [Enhancement]: Separating knowhere from milvus project (issue 11995)
6. Optimize compilation of Arrow issue 12284
7. Milvus doesn't handle partition description now (issue 8668)

3. Pymivus api mark as deprecated
4. Ut with thirdparty services should be restricted inside the config rootPath scope
5. 推进 BaseKV enhancement #11313

## Tracking - Unmerged PR
- 11423

## Timeline - InProgress
1. Insert slow 12701 定位问题
[Bug]: [benchmark][standalone] load raise error: The specified key does not exist (issue 13250)
- No Progress
2. 问题排查工具的文档 -> dlv，pprof

## Timeline - DONE
[12-13] issue 12450
[12-14] move alias APIs from Collection to utility of pymilvus. (pr 841)
