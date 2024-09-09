## Abomination - Folia fork

<img src="https://raw.githubusercontent.com/xymb-endcrystalme/Abomination/dev/logo.webp" width="150px" height="150px" style="margin-top: 20px;"/>


### Warning:

If you're using `.mca`, going `abomination`<->`folia`<->`other forks` won't be a problem.

If you're using `.linear` be careful - other forks support only `.linear v1`.
Abomination reads both `.linear v1` and `.linear v2`, but writes only `.linear v2`.
If you want to go back to a fork that supports only `.linear v1` don't use Abomination until those forks update. Or you're willing to convert all chunks back to `.linear v1`.

### Philosophy:

- Stability over novelity - will lag a few weeks behind new versions for stability reasons
- 100% compatible by default - all plugin-breaking options are opt-in
- **Aggresive** optional performance patches - for those who need as many players as possible
- Less patches is better - all performance patches have measurable impact
- Increased security - packet firewall to minimise the risk of coord exploits
- Bug bounty for coord exploits and dupes
- Some gameplay patches - because why not
- Documentation for every option

### Support:<br/>
[![Discord](<https://img.shields.io/badge/Abomination-Discord-blue>)](https://discord.gg/qwcq5WJka3) [![GitHub Issues](<https://img.shields.io/badge/GitHub-Issues-blue>)](https://github.com/xymb-endcrystalme/Abomination/issues) [![E-Mail](<https://img.shields.io/badge/Email-blue>)](mailto:xymb@endcrystal.me)

### Progress:

| Task           | Progress | Ready |
|----------------|---------------|---------------|
| Linear Region File Format v2 - base implementation | 100% | ✅
| Linear Region File Format v2 - config changes | 0% | ❌
| Linear Region File Format v2 - handle features | 10% | ❌
| Linear Region File Format v2 - handle features unit test | 0% | ❌
| Linear Region File Format v2 - limit amount of threads | 0% | ❌
| Linear Region File Format v2 - save memory | 0% | ❌
| Linear Region File Format v2 - crash on unknown features | 0% | ❌
| Linear v2 feature - world/entity/poi in a single region file | 0% | ❌
| Packet firewall port from SecurityKaiiju 1.19.4 | 100% | ✅
| NBT deduplication on chunk write | 100% | ✅
| NBT deduplication on chunk read | 100% | ✅
| NBT deduplication - Linear v2 feature | 0% | ❌
| NBT deduplication - Thresholds | 0% | ❌
| NBT deduplication - reverting | 100% | ✅
| Exploit: Fix overstacked items | 0% | ❌
| Exploit: Fix oversized shulkers | 0% | ❌
| Networking: Remove those unnecessary entity move packets | 100% | ✅


[//]: <> (fixOverstackedItems)
[//]: <> (fixOversizedShulkerBoxes)


### TODO:

TODO

### Docs:

TODO

### Compile:
```
./gradlew applyPatches
./gradlew createReobfBundlerJar
```

Afterwards you'll find your jar in `build/libs`.

### Unit tests:
```
./gradlew :abomination-server:test --tests "abomination.*"
```