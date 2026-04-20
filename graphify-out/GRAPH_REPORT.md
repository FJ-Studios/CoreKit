# Graph Report - /Users/jeoffrey/Documents/Workspaces/shiki/packages/CoreKit  (2026-04-19)

## Corpus Check
- 21 files · ~8,173 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 221 nodes · 389 edges · 14 communities detected
- Extraction: 72% EXTRACTED · 28% INFERRED · 0% AMBIGUOUS · INFERRED: 108 edges (avg confidence: 0.8)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- [[_COMMUNITY_Community 0|Community 0]]
- [[_COMMUNITY_Community 1|Community 1]]
- [[_COMMUNITY_Community 2|Community 2]]
- [[_COMMUNITY_Community 3|Community 3]]
- [[_COMMUNITY_Community 4|Community 4]]
- [[_COMMUNITY_Community 5|Community 5]]
- [[_COMMUNITY_Community 6|Community 6]]
- [[_COMMUNITY_Community 7|Community 7]]
- [[_COMMUNITY_Community 8|Community 8]]
- [[_COMMUNITY_Community 9|Community 9]]
- [[_COMMUNITY_Community 10|Community 10]]
- [[_COMMUNITY_Community 11|Community 11]]
- [[_COMMUNITY_Community 12|Community 12]]
- [[_COMMUNITY_Community 13|Community 13]]

## God Nodes (most connected - your core abstractions)
1. `ContainerTests` - 25 edges
2. `Container` - 23 edges
3. `Resolve` - 21 edges
4. `ResolveTests` - 12 edges
5. `CacheRepositoryTests` - 12 edges
6. `CacheRepository` - 11 edges
7. `String` - 11 edges
8. `CacheRepositoryError` - 10 edges
9. `TestModel` - 9 edges
10. `StubAssembly` - 9 edges

## Surprising Connections (you probably didn't know these)
- `CacheRepositoryTests` --inherits--> `XCTestCase`  [EXTRACTED]
  /Users/jeoffrey/Documents/Workspaces/shiki/packages/CoreKit/Tests/CoreKitTests/CacheRepositoryTests.swift →   _Bridges community 0 → community 2_
- `TestModel` --inherits--> `Equatable`  [EXTRACTED]
  /Users/jeoffrey/Documents/Workspaces/shiki/packages/CoreKit/Tests/CoreKitTests/CacheRepositoryTests.swift →   _Bridges community 2 → community 6_
- `TestModel` --inherits--> `Sendable`  [EXTRACTED]
  /Users/jeoffrey/Documents/Workspaces/shiki/packages/CoreKit/Tests/CoreKitTests/CacheRepositoryTests.swift →   _Bridges community 2 → community 3_
- `InterfaceType` --inherits--> `Equatable`  [EXTRACTED]
  /Users/jeoffrey/Documents/Workspaces/shiki/packages/CoreKit/Sources/CoreKit/Utilities/NetworkStatus.swift →   _Bridges community 6 → community 4_
- `Container` --inherits--> `Sendable`  [EXTRACTED]
  /Users/jeoffrey/Documents/Workspaces/shiki/packages/CoreKit/Sources/CoreKit/DI/Container.swift →   _Bridges community 3 → community 1_

## Communities

### Community 0 - "Community 0"
Cohesion: 0.1
Nodes (6): ContainerTests, StubAssembly, DIAssembly, Resolve, ResolveTests, XCTestCase

### Community 1 - "Community 1"
Cohesion: 0.08
Nodes (14): Container, ContainerError, circularDependency, invalidRegistration, notRegistered, resolutionFailed, Registration, RegistrationProtocol (+6 more)

### Community 2 - "Community 2"
Cohesion: 0.14
Nodes (10): CacheContainerModel, CacheRepository, CacheRepositoryProtocol, InvalidateTime, inTime, never, CacheRepositoryTests, TestModel (+2 more)

### Community 3 - "Community 3"
Cohesion: 0.08
Nodes (17): AppIdentity, AppLog, DebugAddress, CacheRepositoryError, cannotCreateCache, decodedError, deleteError, encodedError (+9 more)

### Community 4 - "Community 4"
Cohesion: 0.13
Nodes (9): InterfaceType, cellular, ethernet, localhost, unknown, wifi, NetworkStatus, NetworkStatusStorage (+1 more)

### Community 5 - "Community 5"
Cohesion: 0.2
Nodes (7): Data, Date, DateFormatter, ISO8601DateFormatter, JSONDecoder, pocketbaseDateDecoder(), Dictionary

### Community 6 - "Community 6"
Cohesion: 0.23
Nodes (5): AnyObject, BaseCoordinator, Coordinator, Equatable, Identifiable

### Community 7 - "Community 7"
Cohesion: 0.17
Nodes (11): CodingKeys, body, invalideTime, modelType, readCount, timestamp, CodingKey, DIEnvironment (+3 more)

### Community 8 - "Community 8"
Cohesion: 0.38
Nodes (1): String

### Community 9 - "Community 9"
Cohesion: 0.33
Nodes (2): ResolveOptional, ResolveWeak

### Community 10 - "Community 10"
Cohesion: 0.33
Nodes (1): View

### Community 11 - "Community 11"
Cohesion: 0.67
Nodes (2): DIAssembly, Resolver

### Community 12 - "Community 12"
Cohesion: 1.0
Nodes (1): Encodable

### Community 13 - "Community 13"
Cohesion: 1.0
Nodes (0): 

## Knowledge Gaps
- **29 isolated node(s):** `invalidRegistration`, `transient`, `cached`, `weak`, `production` (+24 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **Thin community `Community 12`** (2 nodes): `Encodable`, `Encodable+Extensions.swift`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.
- **Thin community `Community 13`** (1 nodes): `Package.swift`
  Too small to be a meaningful cluster - may be noise or needs more connections extracted.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `Container` connect `Community 1` to `Community 0`, `Community 2`, `Community 3`?**
  _High betweenness centrality (0.409) - this node is a cross-community bridge._
- **Why does `InterfaceType` connect `Community 4` to `Community 3`, `Community 6`?**
  _High betweenness centrality (0.157) - this node is a cross-community bridge._
- **Are the 6 inferred relationships involving `Container` (e.g. with `.setUp()` and `.testParentContainerFallback()`) actually correct?**
  _`Container` has 6 INFERRED edges - model-reasoned connections that need verification._
- **Are the 18 inferred relationships involving `Resolve` (e.g. with `.testDIConfigureWithAssemblies()` and `.testRegisterAndResolve()`) actually correct?**
  _`Resolve` has 18 INFERRED edges - model-reasoned connections that need verification._
- **What connects `invalidRegistration`, `transient`, `cached` to the rest of the system?**
  _29 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `Community 0` be split into smaller, more focused modules?**
  _Cohesion score 0.1 - nodes in this community are weakly interconnected._
- **Should `Community 1` be split into smaller, more focused modules?**
  _Cohesion score 0.08 - nodes in this community are weakly interconnected._