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
[11.29 Mon.] Openblas built by Milvus is not installed properly (issue 8143)

## Timeline - DONE
[11.29 Mon.] remove pymilvus hacktoberfest banner
