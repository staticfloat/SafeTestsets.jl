# SafeTestsets.jl

`@safetestset` puts `@testset` into a module.

You can use it by
```julia
using SafeTestsets
@safetestset "Benchmark Tests" begin include("benchmark_tests.jl") end
```
which makes a new module whose name is generated by `gensym()`, or
```julia
using SafeTestsets
@safetestset BenchmarkTests = "Benchmark Tests" begin include("benchmark_tests.jl") end
```
which makes a module named `BenchmarkTests`.
