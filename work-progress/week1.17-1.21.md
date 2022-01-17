# Week 12.27 - 12.31

---
## TODO - bug fix

---
## TODO - enhancement [AFTER GA]
1. Clear and Unify BaseKV interface behaviour (issue 11313)
    - Fix memoryKV load and basetable (pr 11423)
2. Test minIO inside configs rootPath (issue 11237)
    - minIO tests (pr 11255)
    - etcd
    - rocksDB
3. Milvus doesn't handle partition description now (issue 8668)
4. 推进 BaseKV enhancement #11313

## Tracking - Unmerged PR
- 11423 (memoryKV) [AFTER GA]

## TODO - Bug
- Debug: Flush hangs at e2e test after deleting datacoord or rootcoord pod kill chaos (issue 14300)
    The producers didn't recover properly

## Timeline - In Progress
## Timeline - DONE
**PyMilvus:**
2. Meetings on how to solve issue: losing requirements version range (issue 850, pr 863 by DragonDriver)

1. Bugs fixes**
- Connect get TypeError: __init__() missing 1 required positional argument: 'message' (issue 15236, pr 866)
- Test cases fail reporting `'GrpcHandler' object has no attribute 'wait_for_loading_partitions_complete'`
(issue 15235, pr 867, pr15244)
