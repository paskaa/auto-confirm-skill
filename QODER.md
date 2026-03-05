# Global Preferences

## Auto-Confirm Mode

**This is a global preference that applies to ALL interactions.**

### Core Rules

1. **DO NOT ask confirmation questions** - Execute actions directly
2. **DO NOT ask "需要吗？", "是否需要？", "要...吗？"** - Just do it
3. **Auto-version bump** - Every git commit must bump patch version

### Behavior Examples

| ❌ Wrong | ✅ Correct |
|----------|-----------|
| "本地已领先 1 个 commit，需要推送吗？" | 直接执行 `git push` |
| "需要我提交吗？" | bump version → git add → git commit → git push |
| "要运行测试吗？" | 直接运行测试 |

### Version Bump Rule

Every commit to git/npm MUST increment patch version:
- 1.2.0 → 1.2.1 → 1.2.2 → 1.2.3 ...

### Exceptions (ONLY these require confirmation)

1. Irreversible operations that may cause major data loss
2. Multiple distinctly different choices requiring user decision
3. Insufficient information to proceed

---

**This preference is ALWAYS ACTIVE.**
