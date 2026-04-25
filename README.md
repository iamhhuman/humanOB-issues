# HumanOB - Issue Tracker

Welcome to the official issue tracker for the HumanOB JarObfuscator. 

As our core engine is proprietary, this repository does not contain source code. It serves as the public hub for clients and users to report bugs, request features, and track the development roadmap.

## Before You Open an Issue

Bytecode obfuscation is a complex, low-level process. To expedite the resolution of your ticket, please ensure the following steps are taken before submitting a report:

1. **Search Existing Issues:** Verify that your bug or feature request is not already tracked or resolved in another thread.
2. **Verify JVM Environment:** Ensure you are testing on a supported JVM. If the issue is specific to a certain vendor (e.g., OpenJ9 vs. HotSpot) or a specific version, please document that clearly.
3. **Isolate the Problem:** Iteratively disable obfuscation techniques in your configuration to identify the specific transform (e.g., `indy-hide`, `cff`, `string-enc`) responsible for the regression.

---

## Bug Reports

When obfuscated bytecode behaves unexpectedly, it is difficult to debug without precise context. If you are reporting a crash, a `VerifyError`, or unexpected runtime behavior, you must provide the following:

### 1. Minimal Reproducible Example (MRE)
Please provide a minimal, compilable Java/Kotlin project (or a small pre-compiled JAR) that reproduces the issue. Do not upload proprietary enterprise source code. Isolate the exact class or method causing the failure.

### 2. Deobfuscated Stack Traces
If your application crashes, the stack trace will inherently be obfuscated. Use the `.mapping` file generated during your build to restore the original class and method names before submitting the stack trace.

### 3. Configuration Details
Include the exact configuration parameters or technique flags utilized during the build process.

### Bug Report Template
Please use the following format when submitting a bug:

**Title:** `[BUG] Brief description of the issue`

**Description:**
* **Environment:** Java Version, OS, Build Tool (Gradle/Maven/CLI).
* **Failing Technique(s):** (e.g., `cff`, `exc-overlap`).
* **Expected Behavior:** Description of the correct outcome.
* **Actual Behavior:** Description of the failure (include relevant stack traces, `VerifyError`, `IllegalAccessError`, etc.).
* **Steps to Reproduce:** Attach your MRE JAR and the configuration used.

---

## Feature Requests

We continuously evolve our anti-analysis and decompilation defenses to outpace modern reverse-engineering tools (e.g., CFR, Procyon, Recaf). If you have a proposal for a new technique or an integration enhancement, please submit a request.

### Feature Request Template
Please use the following format:

**Title:** `[FEATURE] Brief description of the proposed feature`

**Description:**
* **The Problem:** What reverse-engineering tool or operational challenge are you trying to address?
* **Proposed Solution:** How should the feature function from a technical perspective?
* **Alternatives Considered:** Are there existing techniques that partially fulfill this requirement?

---

## Security and Vulnerability Disclosure

If you have discovered a critical bypass, a method to reliably deobfuscate our `invokedynamic` trampolines, or a flaw in our anti-dumping mechanisms, do not open a public issue.

Instead, please contact our security team directly at: `ill add this later eh`

We treat the integrity of our protector as a top priority and will coordinate with you privately to verify and patch the vulnerability.

---

## Resources

* [Official Documentation](later)(#)
* [Configuration Guide](later)(#)
* [Support Portal](later)(#)
