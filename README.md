# Proactive Agent Enhanced 🦞

[![Version](https://img.shields.io/badge/version-3.1.0-blue.svg)](https://github.com/yaoge/proactive-agent-enhanced)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![OpenClaw](https://img.shields.io/badge/OpenClaw-Skill-orange.svg)](https://openclaw.ai)

Transform AI agents from task-followers into proactive partners that anticipate needs and continuously improve.

## 🎯 What This Skill Does

**Proactive Agent Enhanced** brings Claude Code's innovative features to OpenClaw:

- 🧠 **Session Memory Compaction** - Unlimited conversation length
- ⚡ **Hooks Lifecycle System** - Fine-grained control over agent behavior
- 📝 **WAL Protocol** - State persistence across interruptions
- 🗂️ **Three-Tier Memory** - Global, Project, and Local memory layers
- 🤖 **Auto Memory Extraction** - Automatic learning capture
- 💓 **Heartbeat System** - Proactive behavior every 30 minutes

## 🚀 Quick Start

### Installation

```bash
# Install via OpenClaw
openclaw skill install proactive-agent-enhanced

# Or manually
cp proactive-agent-enhanced.skill ~/.openclaw/skills/
```

### Activation

Simply tell your agent:

```
"Enable enhanced mode"
```

Or create the config file:

```bash
touch ~/.openclaw/ENHANCED_MODE.config
```

### Verification

```bash
openclaw status
# Look for: Enhanced Mode: Active
```

## 📖 Core Features

### 1. Session Memory Compaction

Never lose context in long conversations. Automatically compresses memory at 75% usage.

```
Context: 78% → Compacting → Continuing seamlessly
```

### 2. Hooks System

12 events, 4 executor types for complete control:

```json
{
  "hooks": {
    "SessionStart": [{ "type": "command", "command": "load-context" }],
    "PreToolUse": [{ "type": "agent", "agentId": "validator" }],
    "SessionEnd": [{ "type": "prompt", "prompt": "Extract learnings" }]
  }
}
```

### 3. WAL Protocol

Write-Ahead Logging ensures state persistence:

```
Critical Info → Write to Disk → Respond to User
```

### 4. Three-Tier Memory

```
Global (~/.openclaw/) → Project (./.openclaw/) → Local (./.openclaw-local/)
```

### 5. Auto Memory

Automatically extracts 6 types of memories:
- ERROR - Command failures
- LEARNING - User corrections
- DECISION - Key choices
- PATTERN - Recurring workflows
- PREFERENCE - User habits
- REFERENCE - Important resources

### 6. Heartbeat

Proactive checks every 30 minutes:
- Active behavior tracking
- Security scanning
- Self-healing
- Memory management
- Surprise generation

## 📚 Documentation

- [SKILL.md](SKILL.md) - Complete skill documentation
- [references/session-memory.md](references/session-memory.md) - Memory compaction
- [references/hooks-system.md](references/hooks-system.md) - Hooks configuration
- [references/wal-protocol.md](references/wal-protocol.md) - WAL protocol
- [references/memory-architecture.md](references/memory-architecture.md) - Memory tiers
- [references/auto-memory.md](references/auto-memory.md) - Auto extraction
- [references/heartbeat.md](references/heartbeat.md) - Heartbeat system
- [references/EXAMPLES.md](references/EXAMPLES.md) - Usage examples

## 🔧 Scripts

- `scripts/check_context.py` - Check context usage
- `scripts/init_enhanced_mode.py` - Initialize enhanced mode
- `scripts/heartbeat_check.py` - Run heartbeat checks

## 🛠️ Requirements

- OpenClaw >= 2026.3.28
- Python >= 3.10

## 🗺️ Roadmap

- [x] Phase 1: Foundation (Session Memory, Hooks, Heartbeat)
- [x] Phase 2: Enhanced Mode (Long-term memory, Proactive thinking)
- [ ] Phase 3: Local Embeddings (Ollama integration)
- [ ] Phase 4: Autonomous Crons (Self-scheduled tasks)
- [ ] Phase 5: Proactive Surprise (Automated delights)

## 🤝 Contributing

Contributions welcome! Please read our [Contributing Guide](CONTRIBUTING.md).

## 📄 License

MIT License - see [LICENSE](LICENSE) file.

## 🙏 Acknowledgments

- Built for [OpenClaw](https://openclaw.ai)
- Created by 耀哥 (Yaoge) with ❤️

## 📞 Support

- Issues: [GitHub Issues](https://github.com/yaoge/proactive-agent-enhanced/issues)
- Discussions: [GitHub Discussions](https://github.com/yaoge/proactive-agent-enhanced/discussions)
- OpenClaw: [Documentation](https://docs.openclaw.ai)

---

**Transform your agent. Evolve toward Jarvis.** 🦞✨
