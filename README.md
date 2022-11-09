# Go-DB-Comparison
a comparison of a few sql packages. 
Database/sql, Sqlx, Sqlc and GORM

`example` directory contains basic code for performing the same actions using the various packages.

`benchmarks` directory contains code for benchmarking all 4 packages. 
You can run the benchmarks by executing the command 
```
$ go test -run=XXX -bench=.
```

below a result from the running of the benchmark
```
================================== BENCHMARKING 1 RECORDS ====================================== 
goos: linux
goarch: amd64
pkg: github.com/rexfordnyrk/go-db-comparison/benchmarks
cpu: Intel(R) Core(TM) i7-8550U CPU @ 1.80GHz
Benchmark/database/sql_limit:1_-8                  11128            105370 ns/op
Benchmark/sqlx_limit:1_-8                          10000            111365 ns/op
Benchmark/sqlc_limit:1_-8                          10000            108700 ns/op
Benchmark/gorm_limit:1_-8                          16742             70535 ns/op
================================================================================================
================================== BENCHMARKING 10 RECORDS ====================================== 
Benchmark/database/sql_limit:10_-8                  9727            108236 ns/op
Benchmark/sqlx_limit:10_-8                          9043            116293 ns/op
Benchmark/sqlc_limit:10_-8                         10000            113071 ns/op
Benchmark/gorm_limit:10_-8                         16965             75148 ns/op
================================================================================================
================================== BENCHMARKING 100 RECORDS ====================================== 
Benchmark/database/sql_limit:100_-8                10000            107338 ns/op
Benchmark/sqlx_limit:100_-8                        10000            114617 ns/op
Benchmark/sqlc_limit:100_-8                        10000            114440 ns/op
Benchmark/gorm_limit:100_-8                        16810             71593 ns/op
================================================================================================
================================== BENCHMARKING 1000 RECORDS ====================================== 
Benchmark/database/sql_limit:1000_-8               10000            111443 ns/op
Benchmark/sqlx_limit:1000_-8                        9792            111644 ns/op
Benchmark/sqlc_limit:1000_-8                       10000            114245 ns/op
Benchmark/gorm_limit:1000_-8                       16417             71042 ns/op
================================================================================================
================================== BENCHMARKING 10000 RECORDS ====================================== 
Benchmark/database/sql_limit:10000_-8              10000            106227 ns/op
Benchmark/sqlx_limit:10000_-8                       9711            111548 ns/op
Benchmark/sqlc_limit:10000_-8                      10000            113653 ns/op
Benchmark/gorm_limit:10000_-8                      16928             74733 ns/op
================================================================================================
================================== BENCHMARKING 15000 RECORDS ====================================== 
Benchmark/database/sql_limit:15000_-8              11377            108174 ns/op
Benchmark/sqlx_limit:15000_-8                      10000            110007 ns/op
Benchmark/sqlc_limit:15000_-8                       9697            107933 ns/op
Benchmark/gorm_limit:15000_-8                      16348             73725 ns/op
===================================================================================================
PASS
ok      github.com/rexfordnyrk/go-db-comparison/benchmarks      33.163s

```