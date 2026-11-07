# Tentative query acceptance inputs

Baseline: klab.staging.vxii master baa9717f8c118501b77a6460e4c885bdf456a7cd, verified against GitHub.
These definitions are not automatically run by the canonical testcase. No live submission occurred.

`staging.vxii.test.queries` contains one setup observation and three named query definitions.
In a fresh disposable context, submit `rectangle`, then observe `geography:Elevation in m` within it,
using the existing staging model namespace/project. Wait for successful commit with complete numeric
storage before any query. The rectangle is the same 500 m by 400 m / 100 m grid used by the existing
`storage_views` k.Actors test. A singular Region query is deliberately absent: runtime's detached
substantial query route supports enumerable collectives, not singular identity reuse.

| Definition | Prerequisite | Expected result after setup | New contextualization |
| --- | --- | --- | --- |
| `rectangle` | Fresh disposable context | One substantial observation with definition identity; setup may resolve dependencies | Yes, setup only |
| `elevation_native` | Committed full Elevation storage | Nonempty detached ID-0 view, requested m semantics, full requested coverage; source IDs identify existing committed Elevation | None |
| `elevation_mm` | Same source | Detached ID-0 view in mm; source identity unchanged; lazy values equal m values times 1000, preserving missingness | None |
| `elevation_west` | Same source | Detached ID-0 view over the western 200 m by 400 m; full coverage of this smaller request, using existing source storage | None |

ID 0 denotes a detached view, not preservation of the native observation's numeric ID. Source IDs
in IM_QUERY_SOURCE_IDS express reuse. Exact generated Elevation values are not asserted. A query
before setup must not resolve missing coverage; an empty result is different from a failed resolution.
These are tentative acceptance expectations, not observed live results. Partial *discovery* completion
for classification needs successful native collective producer activities; a Region acknowledgment
or merely a registered collective is not sufficient setup. This namespace does not invent such a setup.

## Existing testcase integration and gaps

The canonical `testcases/klab/staging/vxii/testsuite.kactors` already uses inspector.viable,
contains, scancheck, celltext and unitcheck. `scancheck(ctx, view, "D2_XY", 1, 8)` and the
D2_YX / D2_XInvY variants accept detached quality views. `unitcheck(ctx, elevation, "mm", 1000, 0)`
expects the committed numeric source, so use it on setup Elevation, not the mm query view.
No existing inspector assertion certifies exact classified member IDs or zero classifier invocations.

The shared observation builder and Modeler support classified `define query` symbols and preserve
the namespace/name. Parsing, semantic validation and builder ID-0 conversion were tested in an
isolated small OWL environment. This is not full worldview/project ingestion or live runtime execution.
The current core.context.submit verb accepts semantics, identity Urn, geometry or a definition map;
it does not directly accept a KimSymbolDefinition or retrieve one from a bare string. Its `query`
verb is a typed graph selector, not the detached observation-query submission route. Therefore
named-query submission through k.Actors still needs a verified definition-to-submission path before
these names can be wired into the testcase. No runner, inspector extension or Maven goal was added.

After that path is supplied, use the table as the setup/submission/assertion mapping; keep each
scenario in a fresh testcase-owned context. Publication and any live acceptance require approval.
