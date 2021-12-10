# Week 12.06 - 12.10

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
- 12710

## Timeline - InProgress
[12.01 Wed.] PyMilvus seperate orm and Milvus client, and mark them as dup.
[12.06 Tue.] Debug distributed CI stuck

## Timeline - DONE
[12.09 Thi.] Debug Auto compaction sometimes runs slowly (issue 13045)
[12.09 Thi.] Debug Length of search result is wrong for test case "test_compact_and_index" (issue 12441)

[12.08 Wed.] Optimize compilation for Arrow
[12.07 Tue.] Debug The actual number of entities inserted is inconsistent with the server num_entities issue 12512
[12.06 Mon.] Finish pymilvus get commit from a certain version.
[12.06 Mon.]The serach result is incorrect when compact is applied to segment outside the time-travel range (issue 12450, pr 12710)
