# ARTimeSkyline

This is a modified version of Mark Hampton's [ARTimeNAB.jl](https://github.com/markNZed/ARTimeNAB.jl)
anomaly detection algorithm which was used and published to achieve the top
rank on the Numenta anomaly benchmark ([NAB](https://github.com/numenta/NAB))
scoreboard in Feb 2022.  Please see [ARTimeNAB](https://github.com/markNZed/ARTimeNAB.jl)
for the full details on the origins, inspiration and acknowledgements relating
to the algorithm.

The version here is modified in the following ways to ensure it can be run in
a real time fashion with [Skyline](https://github.com/earthgecko/skyline):

- The algorithm function accepts all required parameters as being passed as
  kwargs rather than hardcoded and defaults to the original values.  This allows
  for tuning the parameters to values suited to data set and testing.
- The function also validates some parameters and modifies them to even numbers
  if required so that no errors are encountered at runtime due to uneven windows,
  etc.

That is it.
