# Week 11.12 afternoon - 11.19 morning

## Not-in-Scheduler

## TODO - stuff
- Review support for windows 7706
- Review Support Search By ID pr 752
- Minio cleaning config

---
## TODO - bug fix
- PyMilvus Socket operation on non-socket (issue 778)
- PyMilvus connection pool is not useful (ref: grpc issue 20985)
- Debug yesterday's CI hangs bug (issue 12075)
- Debug Distributed CI hangs (issue 11915)
- Debug DN 1000% CPU in CI
- [DONE] Debug Load collection failed after compact and create index (issue 12146 pr 12204)

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

---
## TODO - pymilvus operation
- [DONE] `hello_milvus.py`, pr 818
- [WIP] PyMilvus sig meeting enhancement agenda

---
## TODO - Communicating
- Milvus doesn't handle partition description now (issue 8668)

## Tracking - Unmerged PR
- 11423
- [DONE] 12283
- [DONE] 818
- [DONE] 12204

## Timeline
**11.26 Fri.**
- [DONE] Debug Insert data fails when etcd pod recovered running status after been killed (issue 10171)
**11.25 Thi.**
- [DONE] The search results are inconsistent before and after compaction(issue 12241)
- [DONE] Make DN Ut coverage to 90% (issue 7684, 8058, pr 12283)

**11.24 Wed.**
- [DONE] DN GC collection release unexpected flowgraph (issue 12249, pr 12258)

**11.23 Tue.**

**11.22 Mon.**
- [DONE] `hello_milvus.py`, pr 818
- [DONE] Debug Load collection failed after compact and create index (issue 12146 pr 12204)
