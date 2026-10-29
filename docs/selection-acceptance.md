# Concrete collective selection

`staging.vxii.test.selection` supplies a bare Region instantiator and ordinary classifiers for
the lexical families realm `earth:PhysicalEnvironment`, attribute
`agency:Appropriateness`, identity `geography:Continental` and role `agency:Participant`.
The concrete role root `imod:Reference` adds a second independent role family.
There is deliberately no instantiator for a complete predicate-qualified Region expression.

The canonical suite requests a qualified collective, discovers or reuses its native Region
cohort, attributes missing family knowledge to those same members, and checks the resulting
virtual selection. Random classifications are allowed: expected member IDs are derived from
the committed native members' actual predicates. No assertion assumes a particular random
category assignment or member count.

The initial route covers collective subjects and agents. This fixture exercises subjects;
it does not establish support for event or relationship discovery lifecycles.

| Canonical action | Guarantee asserted |
| --- | --- |
| `select_realm` | Fresh discovery/classification produces a valid realm-filtered view; repeating the request creates no native observation or contextualization. |
| `select_attribute` | Attribute classification updates existing native member IDs and retains geometry; selection matches the resulting predicates. |
| `select_identity` | Identity classification uses the same native substantial cohort, without partitioning cohorts by identity predicate. |
| `select_role` | Role classification follows the same member/update/selection contract. |
| `select_two_role_families` | Participant and Reference remain separate role families, both apply conjunctively, and repeated selection performs no native work. Reference is a concrete lexical root and must include itself. |
| `select_multiple_families` | All four requested predicates apply conjunctively to one cohort; repeated selection performs no native work. A zero-member intersection is valid. |
| `select_deterministic_four_families` | Fixed Appropriate/Patient/Terrestrial/African outputs through the existing permit-gated classifier; verifies committed membership, at least four actual classifier invocations, stable native state and no repeated invocation on replay. Geometry/cardinality are not seeded. |
| `select_known_different` | Concrete `any Terrestrial` first classifies every member as Terrestrial. Requesting Aquatic afterward returns a successful empty view and does not reclassify existing knowledge. |
| `selected_model_input` | An ordinary count model consumes the predicate-qualified collective through its local `selected` alias. Recover its actual committed input receipt, check the input selection, and compare a numeric output cell with that input's member count. |
| `select_partial_support` | Seed native discovery over the western half, then request selection over the complete region. The result must have complete native support and consistent selected membership; the earlier native producer must remain present. |
| `select_subtype` | Classify a synthetic estuarine cohort, then select its Aquatic supertype. The nonempty selection must reuse the same members without classification or instantiation. Coordinates are only support for this explicit synthetic category fixture. |
| `select_empty_native` | A genuine permit-gated native contextualizer generates zero members and must finish with real successful INSTANTIATION provenance. Its invocation evidence, zero-member result and repeat are checked. An Agent supplies geometry so no Region context becomes an incidental native member. |
| `select_missing_classifier` | Missing required classification fails rather than returning an exhaustive empty selection; native state stays unchanged. |
| `select_family_rollback` | The failing second classifier must observe an earlier concrete family on its actual member. Positive in-memory invocation evidence plus unchanged native state demonstrates non-vacuous rollback; retry in the same context must work. |
| `select_consumer_rollback` | An ordinary model validates its actual selected input and deliberately fails. Positive consumer invocation evidence plus unchanged native state proves rollback; a normal retry recovers the actual input receipt. |
| `select_explicit_observer` | Use the actual persisted Agent in the request and inspection scope, replay its selection after JSON transport, and reject replay with that observer absent from the inspection scope. |
| `classify_without_focus` | Explicit Agent geometry with no singular focus supports fresh concrete classification, repeat no-op and already-known different-value no-op. Fresh EXISTING audits preserve the actual member identities and known values. |
| `select_native_operation_dependency` | Use explicit request geometry and an actual selected Agent with no singular Region focus. Check the returned support against that observer's geometry. A native Stream producer first executes a direct collective Region CLASSIFICATION dependency. A permit-gated function verifies actual earlier member invocations and their staged attributions before normal object emission. Select the one deterministic Patient Stream, replay its original IDs, and prove reuse with explicit identical support performs no new native work. |
| `select_native_operation_rollback` | A failing ordinary consumer must have consumed the selected Stream after Region classification, ordered Stream discovery and its own classification. Positive order/discovery/member counters plus unchanged committed native state prove non-vacuous rollback of native observations, members, classifications and execution history against the prepared catalogs and an existing singular Region context; retry must succeed. |

`inspector.selectioncheck(context, view, {{each ...}})` checks native source completion,
certified semantic content and selected observer, then independently enumerates committed cohort
members within the request geometry. Every member must have concrete knowledge for each
requested family. The expected selected ID set uses Reasoner subtype matching for every requested
predicate. It must equal the receipt, Runtime enumeration and returned count. Member identities,
meanings and geometry must agree with the native graph. A persisted qualified producer fails
the assertion: only the native source observation is produced.

Every direct and nested `selectioncheck` requires a version-3 receipt, the current
`semantic-content-v2` static-content identity, and a successfully revalidated scoped
`semantic-dependency-v1` witness. The witness covers the actual admitted producers,
selected computations and bound inputs, all native members (including excluded members),
classifier/characterization provenance, and observer/context semantics. Opaque or missing
execution footprints remain UNKNOWN. A process-local generation and owner session fence
active plans; neither establishes durable semantic identity.

Identical content and relevant authority proofs can survive a Reasoner restart; changed
content requires normal revalidation even if a numeric counter repeats. Older receipts and
recorded observations remain readable, but inspection never stamps or upgrades their proof.
An unrelated mutable authority does not block a selection whose complete dependency signature
is proven independent. A relevant provider with no stable version/snapshot returns
REVALIDATION_REQUIRED: cached identity answers or historical membership do not establish
current exhaustive completeness. Refreshing/retracting mutable provider answers is not
implemented by this receipt protocol. Failure to certify does not disable the provider or
remove historical observations.

Canonical selection assertions check these guards through the normal inspector/query paths.
They do not themselves restart a Reasoner or exercise every configured authority capability;
actual restart and affected-authority acceptance evidence must be recorded separately.
`inspector.nativesnapshot`/`nativeunchanged` compare committed native observations, cohorts,
membership, attribution and contextualization provenance. Submission/resolution bookkeeping
may change. This differs from `classificationnoop`, which requires a fresh successful
classification audit with EXISTING-only results.

Concept arguments use k.Actors semantic literals. The inspector retains legacy strings for
compatibility; model-local aliases and Observable production requirements are not semantic
matching inputs. Previously compiled actors with static String method signatures must be
recompiled after updating the Services libraries.

`inspector.selectioninput(context, consumer, "selected")` reads the canonical committed
consumer's captured local-input receipt, rather than issuing an independent query after the
consumer ran. Runtime validates the recovered view before `selectioncheck` checks its semantic
and native graph invariants. `cellcheck` reads one finite numeric cell through the existing
export traversal and compares it in double precision. The count is a small exact integer, so
this case uses zero tolerance. This one-cell assertion does not claim a complete raster scan.

The deterministic empty/failure functions require `inspector.fixtures` in an actual native
testcase-owned context. They cannot be enabled by production parameters, metadata flags or
remote callers. `clearfixtures` revokes the permit; scope/testcase cleanup also revokes it.
Invocation counters survive the deliberate transaction rollback as in-memory evidence only.
No fixture manufactures a successful activity or completion receipt.

`selection_native_dependency` uses existing `earth:Stream`, `earth:Region`,
`agency:Appropriateness` and `agency:Participant` concepts. Its Stream instantiator declares
`observing agency:Appropriateness of each earth:Region` directly, rather than converting this
collective operation into a quality of a singular category-bearing context. A selected concrete
Agent is selected explicitly, and the positive case supplies explicit geometry without a singular focus. Occupied Agent geometry is not a PERCEIVES capability, so this fixture does not test inherited perception geometry. The COUNT consumer rollback case supplies a small individual Region context before its baseline, as required for a quality consumer.

The gated `klab.tests.fixtures.classify(result=...)` returns a normal concrete classifier result
and records the actual member's logical identity and invocation ordinal privately. The normal
classifier executor must validate and stage that result. `discoverafter(members=..., family=...)`
then uses an ordinary Runtime native query and member enumeration. It requires complete native
discovery, a nonempty member set, a prior recorded invocation for every same member, and the
concrete family now visible in each member's projected semantics. Only then does it emit one
object through `Data.Builder.object`. `classification`, `ordered` and `discovery` counters are
execution evidence, not commit counts or generated provenance. The output identity is derived
from the real scope, target and supplied geometry; a failed normal object builder is not counted
as successful discovery. All functions use the same private native-testcase permit.

`inspector.selectionreplay(context, view)` serializes `Observation.forTransport(view)` as JSON,
decodes an Observation, and submits that QUERY_ID request to the normal Runtime query path.
It compares the durable receipt (all fields except historical numeric generation), source IDs, selected IDs, member enumeration and returned
count, and requires committed native state to stay unchanged. The realm case checks fresh and
reused views; the ordinary consumer case checks its persisted input receipt; the explicit
observer case checks eligible replay and wrong-observer rejection.

Execution evidence and remaining gaps must be recorded with the final candidate. Merely adding
these cases does not establish acceptance. Minimal missing-fragment execution and replay
require explicit executed evidence; do not infer them from compilation or semantic checks.

Catalogs retain their existing independent durable lifecycle. The native-operation rollback case creates its singular Region context first, which already populates the Region catalog. It prepares only the empty Stream catalog through the permit-gated preparecatalog helper before taking the strict snapshot. The helper deliberately rejects a populated catalog; the Region catalog is not an empty-catalog baseline. Catalog preparation creates no observation or discovery completion; unknown discovery remains incomplete. The positive native producer case performs no catalog setup and exercises normal catalog creation.

## Scope, audit and failure oracles

Bare collective discovery remains an independent root and clears a supplied singular focus.
The preseed/reuse cases (`select_attribute`, `select_identity`, `select_role`,
`select_known_different` and `select_subtype`) therefore use the same unfocused scope,
explicit geometry and explicitly absent observer for discovery, classification and selection.
`select_partial_support` uses that same scope for western discovery and full-support completion;
it checks complete output geometry and retention of the western member IDs and their geometry.
`select_realm` separately covers a focused qualified request and focused repeated reuse.
Completion evidence from another focus or observer is not interchangeable.

`inspector.classificationcheckfor(context, before, {{requested}}, {{family}})` distinguishes
the concrete requested predicate from its lexical family. It requires an actual mutation of
existing member identities and one matching successful audit, including the exact requested
predicate. The concrete `any Terrestrial` classification case exercises this verb with requested `Terrestrial` and family `PhysicalEnvironment`. Selection instead invokes family-root operations, then applies the requested concrete predicates in the final view filter: its attribute/identity/role cases therefore use `classificationcheck(..., family)` and verify the actual family request in the audit. A concrete final filter does not make the executed family operation a concrete request.

Failure cases use `inspector.failed(observation)`: a non-null, empty, unassigned response with
finite zero coverage and an error notification. `present` checks only non-null capture and is
not a failure oracle. Null responses and successful zero-member QUERY_ID selections fail the
failure assertion. Fixture counters, `nativeunchanged` and retry checks remain independent
requirements for non-vacuous rollback.

These corrected scope and oracle assertions require a fresh live canonical run. Their source
presence alone is not acceptance evidence.


Qualified predicate clauses inside a characterization bearer are grouped as one inherent
operand when serialized. This prevents a later family from reparsing the intended bearer as
additional roles on its Region. Plain/simple decorated bearers and raw grammar remain
unchanged. The existing semantic compiler configuration revision includes
`qualified-inherent-grouping-v1` so source-identical captures using the former encoding
are rejected and rebuilt; this does not change closure policy or fingerprint schema.


The fixed-predicate fixture uses `staging.vxii.test.selection_deterministic` and requires `inspector.fixtures(ctx)` from an actual owned native testcase. It does not alter production generator policy. A historical applicability rejection lacked its exact predicate/target; passing deterministic transaction and exhaustive semantic reconstruction do not retrospectively establish its cause.
