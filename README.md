# 白细胞突围 / Immune Rush — Vibe Lab submission

This repository is the exported Android Gradle project, not the editable Unity source.
Unity 6000.6.6f1; IL2CPP; ARM64 only; package com.immunerush.vr; target/compile SDK 36.
Unity bundled NDK 27.2.12479018, Gradle 9.3.1, Java 17 compatibility, CMake 3.22.1.

IL2CPP has been precompiled locally. buildIl2Cpp is disabled without replacing its original task body.
Run :launcher:assembleRelease with the Android SDK environment configured. The platform handles Unity installation paths.
.vibelab-prebuilt.json records native binaries and metadata hashes.

Validation (2026-11-16):
- Unity export succeeded with zero build errors.
- Forced IL2CPP build succeeded.
- Release APK built before and after removing IL2CPP sources.
- Final build reports buildIl2Cpp SKIPPED.
- All 16 APK native-library hashes match before/after cleanup.
- ELF64 AArch64 and ZIP alignment checked.
- Nine native libraries have 16 KB alignment warnings; 16 KB device compatibility is NOT claimed.
- Unity 6 APK has not yet been tested on a connected headset.
- Cloud build has not been executed. Local success does not guarantee cloud success.
- Source migration retains PICO Integration 3.4.0; embedded SDK bake-name GetInstanceID call adapted to GetEntityId for Unity 6.6.

Publish this repository to GitHub and submit its URL plus the full 40-character commit ID.
No signing keys, APKs, local.properties, or IL2CPP compiler sources are included.

Update 2026-11-17: identity panel now reads 保持活力，拾取营养补给 / 躲避血栓障碍，消灭病毒. Re-exported and forced-precompiled IL2CPP; both release builds passed, all 16 native-library hashes match before/after cleanup, and the new text was verified in global-metadata.dat. Nine 16 KB alignment warnings remain.
