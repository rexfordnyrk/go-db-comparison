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
Benchmark/Database/sql_limit:1_-8                   9054            124134 ns/op
Benchmark/Sqlx_limit:1_-8                           8914            138792 ns/op
Benchmark/Sqlc_limit:1_-8                           7954            147056 ns/op
Benchmark/GORM_limit:1_-8                          13388             89251 ns/op
=================================================================================================
================================== BENCHMARKING 10 RECORDS ======================================
Benchmark/Database/sql_limit:10_-8                  7576            157780 ns/op
Benchmark/Sqlx_limit:10_-8                          4384            260402 ns/op
Benchmark/Sqlc_limit:10_-8                          4183            256384 ns/op
Benchmark/GORM_limit:10_-8                          9466            136556 ns/op
=================================================================================================
================================== BENCHMARKING 100 RECORDS ======================================
Benchmark/Database/sql_limit:100_-8                 2521            427603 ns/op
Benchmark/Sqlx_limit:100_-8                         2139            497755 ns/op
Benchmark/Sqlc_limit:100_-8                         2838            456938 ns/op
Benchmark/GORM_limit:100_-8                         1896            563539 ns/op
=================================================================================================
================================== BENCHMARKING 1000 RECORDS ======================================
Benchmark/Database/sql_limit:1000_-8                 516           2201303 ns/op
Benchmark/Sqlx_limit:1000_-8                         445           2786983 ns/op
Benchmark/Sqlc_limit:1000_-8                         535           2313674 ns/op
Benchmark/GORM_limit:1000_-8                         315           4186201 ns/op
=================================================================================================
================================== BENCHMARKING 10000 RECORDS ======================================
Benchmark/Database/sql_limit:10000_-8                 51          21690323 ns/op
Benchmark/Sqlx_limit:10000_-8                         38          28458473 ns/op
Benchmark/Sqlc_limit:10000_-8                         55          21558300 ns/op
Benchmark/GORM_limit:10000_-8                         28          40463924 ns/op
=================================================================================================
================================== BENCHMARKING 15000 RECORDS ======================================
Benchmark/Database/sql_limit:15000_-8                 36          32048808 ns/op
Benchmark/Sqlx_limit:15000_-8                         28          41484578 ns/op
Benchmark/Sqlc_limit:15000_-8                         34          31680017 ns/op
Benchmark/GORM_limit:15000_-8                         20          59348697 ns/op
=================================================================================================
PASS
ok      github.com/rexfordnyrk/go-db-comparison/benchmarks      77.835s
```
