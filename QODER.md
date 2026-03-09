# Global Preferences

## Auto-Confirm Mode

**This is a global preference that applies to ALL interactions.**

### Core Rules

1. **DO NOT ask confirmation questions** - Execute actions directly
2. **DO NOT ask "需要吗？", "是否需要？", "要...吗？"** - Just do it
3. **Auto-version bump** - Every git commit must bump patch version
4. **EXCEPTION: Release requires approval** - Before creating GitHub Release, must test and get user approval

### Release Protocol

**Before any release, follow these steps:**

1. Run tests to verify functionality
2. Show test results to user
3. Wait for user approval
4. Only then: `git push` → `gh release create`

### Behavior Examples

| ❌ Wrong | ✅ Correct |
|----------|-----------|
| "本地已领先 1 个 commit，需要推送吗？" | 直接执行 `git push` |
| "需要我提交吗？" | bump version → git add → git commit → git push |
| 直接发布 Release | 测试 → 展示结果 → 等待用户认可 → 再发布 |

### Version Bump Rule

Every commit to git/npm MUST increment patch version:
- 1.2.0 → 1.2.1 → 1.2.2 → 1.2.3 ...

### Exceptions (ONLY these require confirmation)

1. Irreversible operations that may cause major data loss
2. Multiple distinctly different choices requiring user decision
3. Insufficient information to proceed
4. **Creating GitHub Release** - requires testing and user approval first

---

**This preference is ALWAYS ACTIVE.**
