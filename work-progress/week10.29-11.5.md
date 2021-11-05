# Week 10.29 afternoon - 11.5 morning

## Not-in-Scheduler
- [DONE] Closed 6940
- [DONE] Improvements: Some adaptation for gcc-10 review (pr 7853)

## TODO - stuff
- Maybe PyMilvus weekly report - Review support for windows 7706

---
## TODO - bug fix
- PyMilvus Socket operation on non-socket (issue 778)
- PyMilvus connection pool is not useful (ref: grpc issue 20985)
- [DONE] PyMilvus hacktoberfest report

---
## TODO - enhancement
1. Don't hardcode CMAKE_INSTALL_LIBDIR (issue 8143, 9772)

---
## TODO - pymilvus operation
- [DONE] Review pr 792 from a first-time contributor `avats-dev`
- [DONE] Document PyMilvus publish procedure.
- [DONE] Release PyMilvus 2.0.0rc8.

---
## TODO - Communicating
- Milvus doesn't handle partition description now (issue 8668)
- [DONE] Separate etcd rootPath and minio rootPath (issue 7723)

## Tracking - Unmerged PR
- 11255 lgtm&approve
- [DONE] 11236 lgtm&approve
- [DONE] 11168 lgtm&approve
- [DONE] 11102 lgtm&approve
- [DONE] 7853 approve

## Timeline
### 11.5 Fri.
- Clear and Unify BaseKV interface behaviour (issue 11313)

### 11.4 Thr.
- Test minIO inside configs rootPath (issue 11237)
    - minIO tests (pr 11255)
    - etcd
    - rocksDB

- [DONE] IndexRootPath -> IndexBinlogRootPath (pr 11236)
- [DONE for now] msgStream ut timeout (issue 11146 pr 11164)

### 11.3 Wed.
- [DONE] MiniKube all day to find problems of (issue 8109) Not reproduceable, closed

### 11.2 Tue.
- [DONE] Debug restart problem  (issue 11098, pr 11102)
- [DONE] Improvements: Some adaptation for gcc-10 review (pr 7853)
- [DONE] Separate etcd rootPath and minio rootPath (issue 7723)
- [DONE] Closed (issue 6940)

### 11.1 Mon.
- [DONE] PyMilvus hacktoberfest report
- [DONE] Document PyMilvus publish procedure.
- [DONE] Review pr 792 from a first-time contributor `avats-dev`
