# Week 11.5 afternoon - 11.12 morning

## Not-in-Scheduler

## TODO - stuff
- Review support for windows 7706
- Review Support Search By ID pr 752

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
    - Drop collection Doc design (pr 11450)
    - Drop collection Implementation (pr 11552)
7. [DONE] Edit compaction PR 11353

---
## TODO - pymilvus operation
- `hello_milvus.py`
- style of pymilvus docstring

---
## TODO - Communicating
- Milvus doesn't handle partition description now (issue 8668)
- [DONE] Answer emailing questions

## Tracking - Unmerged PR
- [DONE] 11255 lgtm&approve
- [DONE] 11353 lgtm&approve
- 811
- pr 11552
- 11450
- 11423

## Timeline
### 11.11 Thr.
- `hello_milvus.py`
- Make scheme print nicer (pr 811)

### 11.9 Tue.
- DropCollection handles resources (issue 11426)
    - Drop collection Doc design (pr 11450)
    - Drop collection Implementation (pr 11552)
- Clear and Unify BaseKV interface behaviour (issue 11313)
    - Fix memoryKV load and basetable (pr 11423)
- [DONE] Enhance pymilvus proto gen procedure (pr 806)
- [DONE] Add pymilvus compaction (pr 807)

### 11.8 Mon.
- [DONE] Edit compaction PR 11353
