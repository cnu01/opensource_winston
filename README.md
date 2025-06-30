# Contribution Summary: Winston File Transport Permissions

## Project Chosen

**Project:** [winstonjs/winston](https://github.com/winstonjs/winston)

**Why this project?**
- Winston is one of the most popular and widely used logging libraries in the Node.js ecosystem.
- It is a well-established open source project with a large user base and active community.
- Contributing to Winston provides an opportunity to make a meaningful impact for many developers and organizations.

## Issue Addressed

**Issue:** [Feature Request: Change default permissions for file transport (#2026)](https://github.com/winstonjs/winston/issues/2026)

**Summary:**
- The request was to allow users to control the file permissions (`mode`) and ownership (`uid`, `gid`) for log files and directories created by Winston's File transport.
- This is important for security and operational flexibility, especially in production environments where log files need specific access controls.

## Pull Request

**Submitted PR:** [feat(file-transport): add mode, uid, and gid options for file and directory creation #2557](https://github.com/winstonjs/winston/pull/2557)

## Solution Overview

- Added support for `mode`, `uid`, and `gid` options to the File transport.
- Updated the File transport implementation to use these options when creating log files and directories.
- Added/updated tests to verify that the file mode is set as expected (with consideration for system umask).
- Updated documentation to describe the new options and their usage.
- Manually tested `uid`/`gid` options by running as root and verifying file ownership.

## Testing

- All automated tests pass locally (`npm test`).
- Manual script was used to verify `uid`/`gid` functionality.
- The solution is robust and production-ready.

## PR Reference

For full details and code review, see the submitted PR:
[https://github.com/winstonjs/winston/pull/2557](https://github.com/winstonjs/winston/pull/2557) 