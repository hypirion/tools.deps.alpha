Changelog
===========

* 0.5.410 on Mar 16, 2018
  * TDEPS-54 add -Sdeps and -A support to -Spom
  * TDEPS-55 fix -Spom for xml file with comment before root node
  * TDEPS-40 clean up log dependencies
  * Update to tools.gitlibs 0.2.64
* 0.5.398 on Feb 22, 2018
  * Update dependency versions to latest
* 0.5.393 on Feb 21, 2018
  * Change call to clojure -Senv to -Sdescribe
* 0.5.388 on Feb 20, 2018
  * Better error if cache dir can't be created
  * API additions and refactoring
* 0.5.373 on Feb 10, 2018 
  * Add tools.deps.alpha/lib-location method
  * Load all extensions in tools.deps.alpha
  * Add support in make-classpath for skipping classpath and lib writing
* 0.5.351 on Feb 2, 2018 
  * Alias support for main, jvm opts, and generic aliases
  * TDEPS-38 Fix issues with merging non-maps at top-level
  * Automatically add src/main/clojure as a source path in pom manifest reader
* 0.5.342 on Jan 23, 2018
  * TDEPS-19 Add support for command line deps config data
  * Add print-tree script
  * Fix bug with git deps with :deps/root
* 0.5.323 on Jan 18, 2018
  * Remove stray debug print in -Spom
  * Fix source paths in pom manifest reader
* 0.5.317 on Jan 18, 2018
  * TDEPS-24 Major changes to expansion and version resolution
  * TDEPS-32 git extension should use :deps/root if specified
  * Change error handling to dump stack on unexpected exception
  * Add pom file reader for local and git deps
  * TDEPS-34 Emit exclusions and classifiers in pom gen
  * Tighten git sha comparison rules
* 0.4.295 on Jan 10, 2018
  * Disallow prefix sha in git coord
  * TDEPS-28 - -Spom - now supports -R and -C aliases (for top-level deps)
  * TDEPS-18 - Internal refactoring for script arg handling
* 0.4.277 on Jan 8, 2018
  * Add code for resolve-tags command
  * Git deps now use :sha and :tag rather than :rev
  * TDEPS-27 - pom gen reported warning when run on Java 9
  * Less confusing errors when a git dep has no deps.edn
* 0.3.260 on Jan 4, 2018
  * TDEPS-25 - pom gen will now sync repositories
  * Update to latest version of gitlibs
* 0.3.254 on Jan 3, 2018
  * Refactored gitlibs out into library
* 0.3.231 on Dec 21, 2017
  * Insert deps config at front of config chain rather than back
  * Make deps manifest reader tolerant of missing deps.edn in project
* 0.3.225 on Dec 21, 2017
  * Fix bug in cache dir configuration
* 0.3.220 on Dec 20, 2017
  * Added support for git deps - see docs for details
  * Print warnings and messages to stderr rather than stdout
* 0.2.196 on Dec 7, 2017
  * Local deps should use full deps file chain, not just project deps
  * Change default clojars url back
* 0.2.190 on Dec 2, 2017
  * Change default clojars url to use the CDN
  * Fix bug in :local/root for jar manifests
* 0.2.183 on Nov 8, 2017
  * Improve error handling when switching on coordinate and manifest types
  * Close pom reader before writing during pom gen sync
* 0.2.173 on Oct 31, 2017
  * TDEPS-14 - Canonicalize lib symbol format
* 0.2.167 on Oct 26, 2017
  * Add s3 Maven repo support
* 0.2.162 on Oct 24, 2017
  * Add pom gen/sync
* 0.2.155 on Oct 6, 2017
  * Overhaul provider extensions
  * Implement local provider deps project support
* 0.2.130 on Sep 21, 2017
  * Always treat libs-file as stale
* 0.2.122 on Sep 21, 2017
  * Ignore reserved "deps" namespace when dispatching on coord type
  * Avoid duplicating cache logic in makecp
* 0.2.116 on Sep 20, 2017
  * New strategy for coordinate specification and dispatch
* 0.1.108 on Sep 19, 2017
  * Remove -P classpath overrides option handling
* 0.1.103 on Sep 19, 2017
  * Bug fixes for :paths and :extra-paths
* 0.1.85 on Sep 15, 2017
  * TDEPS-11 - Lift provider attributes up to top-level with namespace qualifiers
  * Use platform-specific character when creating classpaths
  * Add top-level :paths and make-classpath :extra-paths
* 0.1.78 on Sep 12, 2017
  * TDEPS-10 - Change makecp to take a list of config files to be merged left to right rather than just a user and project level file. Changed args to be named rather than positional to help with script evolution.
* 0.1.73 on Aug 31, 2017
  * Combine user and project deps.edn with `merge-with merge` rather than `merge`
* 0.1.68 on Aug 25, 2017
  * Top dep coords take priority over transitive deps
* 0.1.62 on Aug 24, 2017
  * Omit scope and optional attributes on expanded Maven deps
  * Handle exclusions in resolve-deps
* 0.1.56 on Aug 22, 2017
  * Add specs
  * Add provider-specific version comparison
  * Add Maven version comparison
  * Report exclusions in Maven coords
* 0.1.40 on Aug 14, 2017
  * makecp now takes an initial argument that is the system deps file to avoid all implicit dirs
* 0.1.35 on Aug 14, 2017
  * Load prototype :file provider in addition to the :mvn provider
  * clj script has been deprecated and moved to the brew-install repo (but is still here for the moment)
* 0.1.29 on Aug 1, 2017
  * Modify clj script to check whether ~/.clojure/clj.props has changed and if so, re-run install-clj
  * TDEPS-2 Overhauled makecp error handling
  * Make rlwrap usage dependent on availability
  * Rename deptools.cp to clj.cp
* 0.1.14 on Jul 24, 2017
  * Initial release
