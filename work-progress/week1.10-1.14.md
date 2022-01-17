# Week 1.10 - 1.14

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
- 15102 (flowgraphManager)
- 11423 (memoryKV)
- mark 1.x API as deprecated
    - PyMilvus connection pool is not useful (ref: grpc issue 20985)

## TODO - bug
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


## Timeline - InProgress
- Tracking this issue 12741
- Bump numpy from 1.19.5 to 1.21.0 in /tests/python_client

## Timeline - DONE
- [DONE] Track issue: proxy ut panic 15105
