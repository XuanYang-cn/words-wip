# Week 11.5 afternoon - 11.12 morning

## Not-in-Scheduler

## TODO - stuff
- Review support for windows 7706

---
## TODO - bug fix
- PyMilvus Socket operation on non-socket (issue 778)
- PyMilvus connection pool is not useful (ref: grpc issue 20985)

---
## TODO - enhancement
1. Don't hardcode CMAKE_INSTALL_LIBDIR (issue 8143, 9772)
2. [DONE for now] msgStream ut timeout (issue 11146 pr 11164)
3. Clear and Unify BaseKV interface behaviour (issue 11313)
4. Test minIO inside configs rootPath (issue 11237)
    - minIO tests (pr 11255)
    - etcd
    - rocksDB
5. DropCollection handles resources (issue 11426)
    - Drop collection Doc design
    - Drop collection Implementation
7. Merge compaction PR 11353

---
## TODO - pymilvus operation

---
## TODO - Communicating
- Milvus doesn't handle partition description now (issue 8668)

## Tracking - Unmerged PR
- [DONE] 11255 lgtm&approve
- 11353 lgtm&approve

## Timeline
### 11.8 Mon.
- Merge compaction PR 11353
- DropCollection handles resources (issue 11426)
    - Drop collection Doc design
    - Drop collection Implementation
- Clear and Unify BaseKV interface behaviour (issue 11313)
    - Fix memoryKV load and basetable (pr 11423)
