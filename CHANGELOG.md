# Changelog

## v0.3.2

- Added support for named params for prepared queries in batches and started raising an explanatory error message if named params are used in simple queries in batches.
- Added `Xandra.run/3` to execute a function with a single Xandra connection checked out from the pool.

## v0.3.1

- Made statement re-preparing happen on the same connection.

## v0.3.0

- Renamed `Xandra.Connection.Error` to `Xandra.ConnectionError`.
- Added support for clustering with random load balancing strategy.
- Fixed the error message for ping failures.
- Fixed a bug where the TCP socket would not be closed in case of failures during connect.

## v0.2.0

- Added support for compression of protocol data (see documentation for the `Xandra` module).
- Added support for the `:serial_consistency` option in `Xandra.execute(!)/3,4`.
- Added support for the `:timestamp` option in `Xandra.execute(!)/4` when executing simple or prepared queries.
- Fixed a bug when repreparing queries that got stale in the cache.