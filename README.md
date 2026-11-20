# toolchain-mirror

Unmodified upstream toolchain releases, repacked so Bazel unpacks them faster. Bazel decodes xz on a single thread; zstd archives of the same tar unpack several times faster.

Each release says where its files came from, how they were repacked and their checksums. The archives are published once and never rebuilt: another zstd version may pack the same tar into different bytes, and builds pin the SHA-256.

The software in each release keeps its own licence, included in the release.
