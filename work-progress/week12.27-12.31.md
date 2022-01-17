# Week 12.27 - 12.31

---
## TODO - bug fix
- PyMilvus Socket operation on non-socket (issue 778)

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

5. 推进 BaseKV enhancement #11313

## Tracking - Unmerged PR
- 11423
- mark 1.x API as deprecated
    - PyMilvus connection pool is not useful (ref: grpc issue 20985)

## Timeline - InProgress
- Ut with thirdparty services should be restricted inside the config rootPath scope
- load raise error: The specified key does not exist (issue 13250)
    Not reproducing lately
- Debug: Flush hangs at e2e test after deleting datacoord or rootcoord pod kill chaos (issue 14300)
- [] Read `Seek` procedure in Milvus, locate possible reason why stuck
    If pulsar healthy:
        1. deadlock
        2. usage problem
        3. other
    If pulsar not healthy:
        1. Why stuck forever rather than raising an error
- [] Try reproducing this localy or on kubenetes

## Timeline - DONE
[12-30] RootCoord gets the binlog paths is incomplete when call BuildIndex (issue 14620, pr14632)
[12-30] DN will release a DataSyncSevice twice, cause watch channel event hanging (issue 14602) (pr 14631 by zhenshan)
[12-29] Debug: Flush hangs at e2e test after deleting datacoord or rootcoord pod kill chaos (issue 14300)
    Stuck at seek??
[12-28] Review: Add hellomilvus in jupyter notebook pr 848
[12-28] Review: 14418
[12-28] Help cyd compile faiss distance
[12-27] Insert slow 12701: making some progress
