# Week 11.12 afternoon - 11.19 morning

## Not-in-Scheduler

## TODO - stuff
- Review support for windows 7706
- Review Support Search By ID pr 752
- Minio cleaning config
- [DONE] Review pr 789

---
## TODO - bug fix
- PyMilvus Socket operation on non-socket (issue 778)
- PyMilvus connection pool is not useful (ref: grpc issue 20985)
- [DONE] The num_entities remains the same after delete and compact (issue 11757)
    - Fix compaction bug(pr 11784)

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
- Set next PyMilvus Agenda

---
## TODO - pymilvus operation
- [DONE] `hello_milvus.py`, pr 818
- Next meeting agenda

---
## TODO - Communicating
- Milvus doesn't handle partition description now (issue 8668)

## Tracking - Unmerged PR
- 11423
- 818
- [DONE] 11784
- [DONE] 11984
- [DONE] 12071

## Timeline
**11.19 Fri.**
- [WIP] Debug 12075, yesterdays CI hangs bug

**11.18 Thr.**
- [WIP] PyMilvus sig meeting enhancement agenda
- [DONE] QueryCoord Ut DataRace (issue 12070, pr 12071)

**11.17 Wed.**
- [DONE] Fixes: Load collection failed after compact and merge segments (issue 11970, pr 11984)
- [DONE] Help Debug Milvus is crashed during CI (issue 11987)


**11.16 Tue.**
- [DONE] `hello_milvus.py`, pr 818
- Debug Distributed CI hangs (issue 11915)

**11.15 Mon.**
- [DONE] The num_entities remains the same after delete and compact (issue 11757)
    - [DONE] Fix compaction bug(pr 11784)
