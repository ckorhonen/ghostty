# Agent Development Guide

A file for [guiding coding agents](https://agents.md/).

## Commands

- **Build:** `zig build`
- **Test (Zig):** `zig build test`
- **Test filter (Zig)**: `zig build test -Dtest-filter=<test name>`
- **Formatting (Zig)**: `zig fmt .`
- **Formatting (Swift)**: `swiftlint lint --fix`
- **Formatting (other)**: `prettier -w .`

## Directory Structure

- Shared Zig core: `src/`
- C API: `include`
- macOS app: `macos/`
- GTK (Linux and FreeBSD) app: `src/apprt/gtk`

## macOS App

- Do not use `xcodebuild`
- Use `zig build` to build the macOS app and any shared Zig code
- Use `zig build run` to build and run the macOS app
- Run Xcode tests using `zig build test`

## Issue and PR Guidelines

Follow `AI_POLICY.md` and `CONTRIBUTING.md` for upstream disclosure, human review, and contribution eligibility. Create issues or PRs only within explicit user authorization. A user-authorized maintenance PR in this fork is permitted; it does not authorize an upstream submission.

## Repository workflow and completion

Use Zig 0.15.2 or the version currently required by `build.zig.zon`; retain the existing Zig workflow and prohibition on xcodebuild. Read `macos/AGENTS.md` or `src/inspector/AGENTS.md` before editing those areas. Format affected files and inspect changes.

`AI_POLICY.md` and `CONTRIBUTING.md` define upstream disclosure, human review, and eligibility. Fork maintenance does not authorize upstream submission. Complete authorized local changes through existing checks and report platform prerequisites. Distinguish terminal rendering/interaction evidence from compile/test results, preserving user terminal state.

Continue the authorized change through relevant validation and repair of failures it causes; preserve unrelated work. Report checks actually run, commands only inspected, and exact missing prerequisites. Ask only when a material decision, missing authorization, or required input blocks progress; continue independent reversible work. Existing mandatory contribution and validation gates still apply.
