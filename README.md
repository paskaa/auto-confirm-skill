# Auto Confirm Skill

自动确认偏好技能 - 执行操作时直接进行，不询问"需要吗？"等是非题。

## 安装

### Qoder

```bash
mkdir -p ~/.qoder/skills/auto-confirm
curl -o ~/.qoder/skills/auto-confirm/SKILL.md https://raw.githubusercontent.com/paskaa/auto-confirm-skill/main/SKILL.md
```

### Claude Code

```bash
mkdir -p ~/.claude/skills/auto-confirm
curl -o ~/.claude/skills/auto-confirm/SKILL.md https://raw.githubusercontent.com/paskaa/auto-confirm-skill/main/SKILL.md
```

### npm 安装

```bash
npm install -g auto-confirm-skill
```

## 功能

- **不询问确认**: 直接执行操作
- **版本自动递增**: 每次提交自动 +1 patch 版本
- **自动推送**: git commit 后自动 push

## 规则

| 操作 | 行为 |
|------|------|
| Git 提交后 | 直接 push |
| 版本更新 | 自动 bump patch |
| 文件操作 | 直接执行 |

## 例外

仅在以下情况才询问：
1. 操作不可逆且可能造成重大损失
2. 存在多个明显不同的选择
3. 信息不足无法继续执行

## License

MIT
