# Week 10.11 - 10.17

## Todo - Review

1. Knowhere compilation review.

2. Arrow compilation review.

3. PyMilvus tf/pytorch review.

4. PyMilvus typing review.

### Not in schedule
**10.11 Mon.**

- Reviewed delete implementation (8050)

----------------------------

### Arrow compilation review
**10.11 Mon.**

- Figuring out what's this PR and why do we need it. a + b needs in memory arrow

- Gave Guan suggestions on how to make PR

----------------------------

### Knowhere compilation review
**10.12 Tue.**

- Review on centOS

**10.11 Mon.**

- I reviewed the codes again, despite some tiny problems, it's ready to merge.

- Before merging, Shen needs to squash all commit messages,
and I need to double check on **Ubuntu18.04 and CentOS7**.

- Found bug in build.sh under index/ `-u` config, konwhere had never built and run unit tests.

- Tested knowhere on Ubuntu18.04 from a clean environment without/with OpenBLAS

    - `./build.sh -u` passed

    - `./test_knowhere` ut passed

- Tested Milvus on Ubuntu18.04 from a clean environment without/with OpenBLAS

    - `make all` passed

    - `make test-cpp` passed

- Build unit tests in knowhere failed for the first time

    `CMAKE_INSTALL_LIBDIR` is in `GNUInstallDirs` module, need to include the latter before
    using the former.

## Todo - Create

1. Sum up 7313 problems and sulotions.

2. Design DataNode flush task scheduler.

3. Write PyMilvus contributing doc.

4. Refactor PyMilvus error handler.
