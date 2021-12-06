# Week 11.29 - 12.03

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
- [WIP] PyMilvus sig meeting enhancement agenda
- Milvus doesn't handle partition description now (issue 8668)

## Tracking - Unmerged PR
- 11423

## Timeline - InProgress
[12.01 Wed.] PyMilvus seperate orm and Milvus client, and mark them as dup.

## Timeline - DONE
[12.01 Wed.] Debug The insert time of first run is too long and after scale up, a search time is very large (issue 12081)
[11.30 Tue.] 11423 all configs not in helm will panic[fix 2]
[11.30 Tue.] Investigate how to make git-rivision into a certain python package
[11.30 Tue.] Try to reproducing issue 9997 - No Progress
[11.29 Mon.] Debug night CI 234 stuck problem -> same problem as issue 12259
[11.29 Mon.] remove pymilvus hacktoberfest banner
[11.29 Mon.] Openblas built by Milvus is not installed properly (issue 8143, closed)
