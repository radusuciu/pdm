# Changelog

All notable changes to this project will be documented in this file.

## [unreleased]

### Bug Fixes

- Chdir to BASE_DIR
- S/groups/group/ in deprecated description
- Invoke pip with `--isolated`
- Typo: s/filie/file (#833)
- A bug that dep with extras can't be updated (#1167)
- Merge the Script and Description field from listing (#1151)
- Use platform standard directories for all PDM directories (#1161)
- Only trust parsing result when all are static
- Duplicate usage shown on CLI parsing error (#1170)
- Use normal streamhandler for logging (#1185)
- Read the correct PDM_RESOLVE_MAX_ROUNDS env variable (#1181)
- Fix resolve requirements with extras (#1187)
- Check if the host pip is compatible with the project python (#1196)
- Avoid circular imports
- Fix unbound local name
- Update unearth to fix package install issue for private pypi
- Respect `--prerelease` in the install script
- Fix run env overriding pep582 (#1211)
- Removing package shouldn't break TOML (#1222)
- Write lockfile before post_lock hook (#1225)
- Suppress errors when cache dir isn't accessible (#1229)
- Don't save python path for venv commands (#1231)
- Env_file variables do not override existing (#1239)
- Fix locking sort bug (#1257)
- Support conda in environment detection (#1254)
- Don't expand secrets in [metadata.files] (#1259)
- Try `python` executable first (#1260)
- Crashes when executing pdm show for an sdist (#1277)
- TypeError when publishing a package with non-ascii in metadata
- Use description field from PEP 621 as summary (#1275)
- Try the read the lock file even if the version is incompatible (#1278)
- Use absolute instead of resolve
- A test failure due to bug fix
- Set minimum version for `packaging` dependency (#1295)
- Prefer compatible packages (#1302)
- Remove dependance on network for several tests (#1297)
- Store dependencies by name and version (#1308)
- Work on FIPS 140-2 Enabled Systems (#1313)
- Bug of missing hashes (#1339)
- Warning about failure to parse project files (#1341)
- Ignore invalid values of `data-requires-python` (#1340)
- Editables not installed. Close #1344
- Don't create virtualenv when switching python versions
- Show summary if all are up-to-date
- Reduce unncessary package download for certain commands (#1374)
- Fix a crash issue when depending on editable packages with extras (#1403)
- Pass `pypi.[ca,client]_cert[s]` to install step of builders (#1405)
- Do not save python path under non-interactive mode (#1410)
- Restrict importlib-metadata version (#1417)
- Update version checker to show self update command (#1408)
- Update the hint for keyring installation
- Use new setuptools (#1428)
- Fix the support for relative paths from outside the project (#1432)
- Correctly overrive the command
- Update the completion script for the new --check flag
- Use pypi importlib_metadata on python < 3.10 (#1467)
- Don't override default handling of SIGINT
- Make `sitecustomize.py` respect the `PDM_PROJECT_MAX_DEPTH` environment variable. Resolves #1413. (#1480)
- Python_version comparison in environment markers (#1486)
- No need to write setup.py anymore
- Do not add local package to lockfile (#1481)
- Bump the lockfile version to 4.1
- Handle "sh" and "dash" in print_pep582_command (#1502) (#1511)
- Test against the latest findpython (#1518)
- Improve the error report for resolution (#1519)
- Make the pdm sessions identical
- Test failures and upgrade unearth
- Fix minimum version requirement for tomlkit (#1539)
- Fallback to pdm.pep517 for unknown custom build backend (#1546)
- Egg segment for local dependency (#1552)
- Strip the local part when building a specifier for comparison (#1566)
- Exclude `packaging 22.0` to avoid breakage (#1568)
- Matching problem of packages in lockfile (#1570)
- Write the version statically in wheel
- Correctly mark a symlink as file to remove (#1581)
- Remove unused object
- Exclude site-packages for symlinks of the python executable
- Logging for fetching hashes
- Fix an uninstallation error on Windows (#1605)
- Hide spinner output for build resolver
- Fix the way of expanding command
- Fix linter error
- Deduplicate lists when running pdm import (#1627)
- Fix the wildcards in requirement specifiers (#1632)
- Proper display for extra Pypi indexes config (#1622)
- Correct the hash key for requirements (#1648)
- Load pypi sources from project config (#1651)
- Set VIRTUAL_ENV in pdm run (#1652)
- Try a second source for the packaging version in case importlib metadata failed (#1656)
- Eliminate the importlib.resources warnings (#1661)
- Allow force re-creating venv in project (#1666)
- Import editable requirements into dev dependencies (#1676)
- Prefer built distributions (#1697)
- Don't crash when trying to update the shebang in a binary script (#1710)
- Resolution failure with nested relative path deps (#1712)
- A local packages finding issue
- Fix a bug of show command not showing metadata of current project (#1740)
- In project conda venv activate without argument (#1735)
- Improve the error message when encountering an invalid requirement (#1766)

### Bugfix

- Fix the unstable uninstallation error (#851)
- Update the candidate identifier if the requirement has no name (#902)
- Unquote path in req url (#1075)

### Docs

- Use Highcharts for the benchmark plot (#803)
- Multiple versions (#1126)

### Documentation

- Mention editable mode installation
- Fix some typos
- Add comment about PATH in PyCharm
- Recommended way to install head version
- Add note about setting a HOME in CI
- Add multi-stage Dockerfile example
- Improve namespace packages detection instructions
- Improve VSCode integration examples
- Fix typo in news/487.bugfix.md
- Replace some `-s` occurrences with `-G` for group
- Clarify the use of `-d` without `-G` (#806)
- Add neovim setup documenation (#899)
- Add notes about using Pylance/Pyright (#967)
- PDM logo use cdn (#984)
- Add notes about using jupyter in vsc (#988)
- Add notes about using jupyter in VSCode #848 (#1020)
- 📝 Fix typo in `pip install pdm` description (#1061)
- Fix URL requirement example with "Dependency specification" (#1081)
- Fix typos (#1088)
- Add example for `find_links`
- Update about using lower Python versions
- Improve the docs about dependencies
- Add CLI reference doc
- Use asciiart as the program description
- Restructure the docs about project metadata and build configuration
- Fix typos and improve a little
- Update contributing guide
- Multiple fixes
- Fix a couple documentation typos (#1172)
- Changed behavior
- Add sticky navigation
- Add sponsors graph
- Add anchor link to the sponsor svg
- Update the copyright year
- Pip.conf is not read anymore (#1197)
- Pdm.toml -> .pdm.toml (#1213)
- Add docs for niche in entrypoint name
- Five different of caches (#1227)
- Add packaging status to readme and doc/index
- Update configuration.md (#1262)
- Recommend v2 of github action
- Mention the plugin in VSCode usage
- Fix docs about dynamic version
- #1357 Add missing editable install dependency group criteria (#1358)
- Add working with version control section (#1373)
- Fix zh-CN README typo (#1387)
- Update the contributing guide
- Fix a broken link in CONTRIBUTING.md (#1449)
- Reflect the changes
- Mention the requirement to import from setup.py
- Fix venv.with_pip syntax error (#1512)
- Clarify the behavior of includes (#1532)
- Add pdm expansions in header
- Don't show expansion if not initialized
- Fix typo in help output of update command (#1615)
- Fix configuration typo for `venv.in_project` (#1617)
- Fixed misplaced backtick (#1633)
- Update default value (#1636)
- Add umami analytics
- Improve contributing docs (#1713)
- Install via asdf-vm (#1725)
- Add pyright/eglot config for emacs (#1721)

### Feat

- Add `minimum` save strategy (#752)
- Add support for Conda environments (#749)

### Feature

- Cache command: (list/remove)
- Prerelease option for add and update (#779)
- Support resolution overriding (#801)
- Signals for init, install, lock (#802)
- Pdm lock --refresh (#812)
- Pdm install --check (#813)
- Remember the last selection in "pdm use" (#852)
- Support pre and post scripts (#898)
- Configurable global project path (#986)
- Complete lifecycle signals and documentation (#1147)

### Features

- Better UI for cache clear command
- Support showing individual fields in pdm show
- Use tomllib on Python 3.11 (#1072)
- Replace halo, click, and termcolor with rich (#1091)
- Use `unearth` as the backend to find and download packages (#1096)
- New command: pdm publish (#1107)
- Added composite tasks support (#1117)
- Add option to skip hooks (#1127)
- Support setup.py import (#1137)
- Forbid editable depenencies in project table (#1140)
- Update pdm-pep517 to 1.0 (#1153)
- Fetch the candidate hashes concurrently (#1154)
- Remove the compatible support for pdm legacy metadata (#1157)
- Yarn-like root scripts fallback (#1159)
- Added a post_use hook (#1163)
- Add back color functions for backword-compatibility
- Add `--no-keep` option to sync command (#1191)
- Pdm venv integration (#1193)
- Make lockfile contain urls instead of filenames (#1203)
- Get link from URLs stored with the lock file (#1204)
- Site-wide configuration (#1205)
- Support pwsh (PowerShell Core) (#1217)
- Reference other groups in optional dependencies (#1242)
- Remove dependency of pip (#1268)
- Introduce `pypi.ca_certs` config entry (#1267)
- Add pdm export to available pre-commit hooks (#1279)
- Deprecate top-level imports (#1282)
- Add config for client cert and key for PyPI (#1292)
- Add an override option to the env_file script option (#1299)
- Switch to src layout (#1317)
- Delay the trigger of post_lock in add and update command (#1320)
- Introduce `ca_certs` / `--ca-certs` to `pdm publish` repos (#1395)
- Add venv.prompt config to allow customizing prompt when venv is activated (#1390)
- Remove top level imports (#1404)
- New command group 'self' (#1406)
- Allow pdm init to receive a python version (#1421)
- Remove deprecated config names (#1422)
- Add a default requires-python on import (#1426)
- Use pdm to resolve and install build requirements (#1429)
- Prompt for credentials and/or keyring when publishing (#1430)
- Customizable theme colors (#1452)
- Write useful informations for github action (#1453)
- Set field as dynamic if variable exists in req
- Add `--check` flag to `pdm lock` (#1460)
- Option to ship pip when creating a venv (#1463)
- Enhance the pdm list command (#1469)
- Pdm lock --check pre-commit hook (#1475)
- Beautify the build error (#1501)
- Rename the resolution.overrides table (#1503)
- Remove backend specific code to support multiple backends (#1506)
- Replace pep517 with pyproject-hooks (#1528)
- Add an optional `{args[:defaults]}` placeholder for script arguments (#1533)
- Add pdm-backend to the supported backends
- Make it possible to override the task runner
- Update installer to 0.6.0 (#1550)
- Remove usages of __file__ to support pdm in a zipapp (#1567)
- Expose pytest fixtures and helpers for pdm plugins (#1594)
- Support multiple indexes in config (#1597)
- Add `@generated` comment (#1612)
- Support implicit python script execution (#1628)
- Ignore remembered selection in pdm init (#1673)

### JSONFileCache

- Replace .has_key() with __contains__() (#1209)

### Miscellaneous Tasks

- Remove remaining artifacts from #1127 (#1152)
- Added a tox.ini file for easier local testing against all Python versions (#1160)
- Remove click from test deps
- Reword the changelog fragments, add `break` entry type
- Change the project description (#1174)
- Update unearth version to 0.4.1 (#1186)
- Better logging when running pep 517
- Add error hint for non-PEP 517 package failure
- Update the links to the docs
- Pre-commit autoupdate (#1198)
- Update lockfile to version 4.0
- Release v2.0.0b2
- Upgrade GitHub Actions (#1206)
- Pyupgrade --py37-plus (#1208)
- Update news fragment
- Rename the news
- Update unearth version
- Release 2.0.0
- Release 2.0.1
- Release 2.0.2
- Detect available python versions for integration (#1249)
- Release 2.0.3
- Multiple minor improvements
- Release 2.1.0
- Release 2.1.1
- Release 2.1.2
- Release 2.1.3
- Release 2.1.4
- Release 2.1.5
- Replace deprecated `set-output` command with `GITHUB_OUTPUT` file (#1434)
- Fix typo in documentation link id (#1436)
- Add release note for #1469
- Release 2.2.0
- Release 2.2.1
- Change the python version to download (#1490)
- Remove benchmark code and page
- Update doc dependencies
- Release 2.3.0
- Add trackgit badge
- Update the lower bound for findpython
- Release 2.3.1
- Update deps unearth and packaging (#1555)
- Release 2.3.2
- Release 2.3.3
- Ignore coverage warnings (#1582)
- Release 2.3.4
- Release 2.4.0
- Correct some cli typos (#1618)
- Fix some wording
- Release 2.4.1
- Fix pre-commit hooks
- Release 2.4.2
- Release 2.4.3
- Update findpython to 0.2.4 (#1696)
- Release 2.4.4
- Release 2.4.5
- Lint with Ruff (#1715)
- Release 2.4.6
- Correct the checksum of install script, closing #1737
- Release 2.4.7
- Release 2.4.8
- Release 2.4.9

### Performance

- Speed up the resolution with lazy find_matches (#1098)

### Pyre

- Name has type `str` but is used as type `None` (#1336)

### Refactor

- Remove the global state
- Remove the reference of 'stream' singleton
- Unify the code about selecting interpreter
- Split the build() into smaller pieces
- Switch to importlib.metadata.Distribution
- Extract environment related code from Candidate (#920)
- Project files (#1499)

### Styling

- Enhance group formatting in messages (fixes #1329) (#1342)

### Bugfix

- Change the is_subset check logic

### Ci

- Configure codecov

<!-- generated by git-cliff -->
