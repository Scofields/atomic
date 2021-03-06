## 1.19 (2017-08-17)
    Add configuration compliance scan to "atomic scan"
    Atomic/backends/_docker.py: Correct NoneType error (BZ #1481967)
    Atomic/backends/_docker.py: Correct run flow
    Atomic/containers.py: Add NAME field to container list
    Atomic/install.py: Don't write the install data if the install fails
    Atomic/mount.py: Fix duplication with fq image name (BZ #1480325)
    Atomic/scan.py: Add rootfs to self.mount_paths BZ:1461788
    Atomic/systemcontainers.py: Set prefix to "/" if None
    Atomic/trust.py: Fix str/byte encoding for Python3
    Atomic/trust.py: Python3 throws an exception
    Fix Python3 issues for F26
    Fix multiple images filters
    Fix the _mark_used function to identify image as being used
    Honor --gnupghome on push
    Introduction of ContainersStorage backend
    Remove commissaire integration
    help: add '-t' argument to groff call to preprocess tables
    images: include the backend in list --json
    images: show the virtual size for system containers
    syscontainers: by default disable copy to the host with --user
    syscontainers: by default don't install rpm on AH
    syscontainers: cleanup on Ctrl-C
    syscontainers: drop import via libarchive
    syscontainers: fix default template for systemd
    syscontainers: fix reading image id in run_once
    syscontainers: introduce CONF_DIRECTORY
    syscontainers: make sure we can delete dirs/files with --user
    syscontainers: on error delete temporary copied files
    syscontainers: print what files are copied to the host
    syscontainers: refactor a duplicated variable
    syscontainers: remove self.user condition for extract
    syscontainers: store the size of an OCI layer
    syscontainers: support PIDFILE with bwrap-oci
    uninstall: inhibit UNINSTALL if there are running containers
    util: allow to override gomtree|bwrap_oci|runc|skopeo paths
## 1.18 (2017-06-1)
    Add integrations tests for atomic_dbus_client.py
    Add test_images_list.sh
    Allow mount/unmount without active dockerd
    Atomic/backends/_docker.py: Error prevention with atomic run
    Atomic/backends/_docker.py: Fix uninstall
    Atomic/containers.py: Always return json when requested
    Atomic/containers.py: quiet supersedes json
    Atomic/rpm_host_install: rename the RPM to the container name
    Atomic/rpm_host_install: replace rpmbuild with rpmwriter module
    Atomic/rpmwriter.py: new module for writing an RPM file
    Atomic/syscontainers.py: Supress Error output
    Atomic/tag.py: Fix tag to work with dockerd, invalid images BZ #1454656
    Atomic/util.py: Add logic to install lookup for shortnames
    Atomic/util.py: Add no_proxy
    Atomic/util.py: Check install against FQ name
    Atomic/util.py: decode registries information to utf-8
    Do not strip port for insecure check
    Fix container/image filters
    Fix mount for ostree backends.  Needed to make sure the cmd
    Fix tagged images not being displayed
    Fix test_tag.sh
    Incorporate registries parsing tool
    Merge pull request #978 from jlebon/pr/rhci-resize-root
    Prefix RPM labels with atomic.
    Re-pulling image error should exit 0
    Refactor system container tests
    Replace tarfile with tar on ostree import case
    add manpage for help command
    atomic.conf: fix syntax error of the YAML format
    atomic: Fix silent failure from AssertionError
    bug: Escape %config in rpm_host_install.py
    correct parameter name for InstallData
    dbus: Anonymous pushes should not fail on auth
    docker,uninstall: correct cmd manipulation
    help: prefer help file over label
    implement `install --storage=docker --system-package=yes`
    mount: create context manager for {Docker,OSTree}Mount
    mount: use system containers storage when possible
    refactor: move {un,}install_rpm to rpm_host_install
    resolves #993 fixes file bind mounts
    rpm_host_install: don't dupe files from /etc
    rpm_host_install: let build_rpm return installed files
    syscontainers: add function for mounting from the storage
    syscontainers: add new test image
    syscontainers: do not commit special files
    syscontainers: do not fail if the file already exist on the host
    syscontainers: do not overwrite main error message
    syscontainers: drop support for OSTree < 2016.8
    syscontainers: ensure the parent directory exists on file copy
    syscontainers: honor ATOMIC_OSTREE_REPO also in user mode
    syscontainers: introduce EXEC_STARTPRE and EXEC_STOPPOST
    syscontainers: introduce containers storage
    syscontainers: introduce variable PIDFILE
    syscontainers: prune layers from the storage
    syscontainers: support detached mode for the default config file
    syscontainers: support detached runC containers
    syscontainers: support rename of directories
    syscontainers: use storage for oneshot containers
    syscontainers: use the correct manifest to read the image id
    syscontainers: use the correct path for the storage on Atomic Host
## 1.17 (2017-04-20)
    Allow anonymous push
    Always use fq names for dest image
    dbus: Lots of fixes
    Atomic/install.py: Record installs for later use
    Signing
    Fix registries.d/*.yaml config lookup
    Fix “fqdn” computation in RegistryInspect
    Honor proxy usage
    Makefile: add new rule test-suite
    Only compute util.Decompose(expanded_image_name) once
    Simplify registries.d/*.yaml config lookup
    Update (atomic sign) for the updated sigstore layout
    atomic.d/openscap: Improve openscap scans
    backends: add tag_image method
    bash: add autocompletion for images tag
    docs: document images tag
    image: add new subcommand tag
    install: add --system-package
    Improve Atomic Install
        Lots of improvements in system containers
        syscontainer: support rpm installs
	syscontainers: Add run once logic to install
    syscontainers: fix containers list --json
    syscontainers: use --systemd-cgroup with runC
    systemcontainers: fill default values when using oneshot
    util: Don't try to create directories at module import time

## 1.16 (2017-02-22)
    Fix uninstall bug: BZ 1425495
    add --lvsize option to atomic storage modify
    Account for API Changes in docker-py-2
    Suppress STDOUT of lower level commands e.g. vgreduce, wipefs.
    Fix Stop Regression: BZ #1422448
    Enable dbus install, stop.
    Allow for async scans via dbus
    syscontainers: allow delete by image id
    syscontainers: support @sha256: format for image listing
    Fix FQ Name for SystemContainers

## 1.15 (2017-01-17)
    update default trust policy file
    Validate reg input to trust add cmd
    Atomic/objects/image.py: Fix verify for v1
    Atomic/verify.py: Fix dbus implementation of image verify
    main: Don't catch all AttributeErrors
    storage: Process arguments in set_args, not __init__
    images, containers: do lowercase comparison for filter values
    images: apply filters before any output
    containers: --json exports image_id
    Refactor atomic stop
    Add keywords to completions

## 1.14 (2017-01-02)
    update: refactor into non-base verbs
    Atomic storage reset does not work on docker-latest
    Fixes for documentation
    syscontainers: unlink temporary file if substitution fails
    syscontainers: simplify substitution of variables
    Add --all to images delete
    tests: replace sed with a python script
    syscontainers: prune the ostree repo with images prune
    syscontainers: allow delete multiple images by ID
    syscontainers: use the image id from the raw manifest
    syscontainers: use system checkout as import tmp directory
    syscontainers: fix tarfile import with no RepoTags
    syscontainers: generate an UUID at installation time
    syscontainers: update honor --force
    Refactor containers verb
    Atomic/diff.py: Fix options bug
    Unify and refactor atomic verify
    fix get auth from docker.io
    redhat-ci: make testsuites required
    push: prompt user/pass lowercase
    Atomic/diff.py: Use go-mtree for file comparisons
    run: add --detach and only add -t if in a TTY
    dbus: fix Install() and Run() signatures
    pull: support dockertar for docker backend
    Atomic/top.py: Fix options handling in top
    generate: default storage for mounts
    Add fedora25_cloud target for vagrant
    Atomic Info Unittests
    Refactor images
    The HELP label by default should be "help"
    atomic_dbus: keep the name until the process exits
    Add substitutions for Opt variables
    Minor fix to delete
    Atomic/mount.py: Re-Add _clean_temp_container_by_path (BZ 1397839)
    test_util.py: adapt for newer sepolicies
    syscontainers: add rollback
    backends: has image|container return objects
    syscontainers: fix installation
    backends: add skeleton for ostree backend
    syscontainers: allow to specify what image to pull
    syscontainers: get_containers accept what containers to inspect
    Add refactoring structure
    Atomic/mount.py: shutil.rmtree input must be dir
    Use centos for all test images
    syscontainers: output better json errors
    atomic diff: Add ability to compare metadata
    syscontainers: environment variable detection
    Add  SYSTEMD_IGNORE_CHROOT=1 to environment of SPCs
    The HELP label by default should be "help"
    make vagrant-check: Run tests with vagrant

## 1.13 (2016-12-13)
Refactor verbs:
	containers
	update
	verify
	images
backends: has image|container return objects
Add  SYSTEMD_IGNORE_CHROOT=1 to environment of SPCs
Atomic diff: Use go-mtree for file comparisons
syscontainers:
	Lots of Bug Fixes
	simplify substitution of variables
	add rollback
Signing:
	push - use credentials in skopeo copy
	pull: support dockertar for docker backend
	fix get auth from docker.io
	prompt user/pass lowercase

Dbus Bindings:

## 1.13 (2016-10-24)
Add --storage option to image-related commands
syscontainers: Fix docker: and dockertar: installs
Atomic/images.py: Enable filter for dangling.
Add atomic trust verb
Add support for image signing
Add support for overlay2 driver
Allow pull from registry not in docker conf
Add dbus support for atomic stop
Add dbus support for atomic install/uninstall
Add dbus support for atomic run
Add dbus support for atomic pull
Add dbus support for atomic top.
Remove primary commands and move to images subcommand
    atomic help
    atomic info
    atomic verify
    atomic version
Introduce registry inspect methods

## 1.12 (2016-9-7)
Fixes for syscontainers
Add atomic images generate to generate mtree meta data
Fix up atomic with overlay backend
Add atomic sign to allow simple signing of images
Add atomic pull support for signatures

## 1.11 (2016-8-9)
Add support for system containers
Add support for managing storage
Add support for atomic ps
Improve dbus interfaces
Improvements to atomic scan

## 1.10 (2016-5-25)
Improve Error Handling
- Unify error messages for no docker daemon (BZ #1300187)

Add atomic storage command
- Modify docker-storage-setup to reset storage
- Move atomic migrate to atomic storage
atomic diff improvements
- Improve docs and output messages for diff
atomic scan improvements
- Allow specification of rootfs
- Implement generic scanning in Atomic
- Do standard compliance scan without CVEs using openscap
atomic install|run
- Set PWD environment if not currently set
- Fix handling of unicode names
- Fix shell expansion on commands.
atomic hosts unlock
- Remove r/o bind mount on atomic host /usr. Replace it with writable overlay filesystem.
Support for system containers
- Add install/uninstall/update/images --system command
- Use OSTree to store layers and do containers checkouts
- Store system containers on ostree in /var/lib/containers/atomic/
- Use Skopeo to retrieve manifest and layers
- atomic pull --storage
Allow atomic command to run as non root for certain commands

## 1.9 (2016-2-22)
Use Skopeo for remote inspection
Use docker.AutoVersionClient to avoid API version mismatch
atomic: harden shell invocations
Use the async API from openscap-daemon to perform CVE scans if possible
Atomic/run.py: Add security implications messages based on RUN label
Atomic/help.py: Display man-like help for an image

## 1.8 (2015-12-10)
Add `atomic top`
Fix lean in `atomic diff`

## 1.7 (2015-11-13)
Add `atomic migrate`
Add `atomic host deploy`

## 1.6 (2015-10-22)
Support python3

## 1.5 (2015-09-29)
Add `atomic scan`

## 1.4 (2015-09-1)
Add `atomic push --satellite`
Change upload to push

## 1.3 (2015-09-1)
Add `atomic mount`

## 1.2 (2015-08-14)
Add `atomic install display` option
Add `atomic -v` option

## 1.1 (2015-01-14)
Add `atomic verify`

## 1.0 (2015-01-14)
Initial Version
