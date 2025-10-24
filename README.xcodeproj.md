See `xcode/MLX.xcodeproj`.

# Cmlx

This is set up to build roughly how Package.swift builds.

- Look at Project -> Cmlx -> Build Phases
- remove all Project headers
- remove all Copy Bundle Resources
- remove any files that should not be built from the Target membership, e.g the items in `exclude`

Public headers are in `include-framework` and this is managed by tools/update-mlx

Settings, including header search paths are in xcode/xcconfig.

# MLX, etc.

These are just normal frameworks that link to Cmlx and others as needed.  The source files are all swift and there are no special settings needed.
