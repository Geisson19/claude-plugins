# Claude Code Plugins Marketplace

Personal plugins for Claude Code.

## Installation

```bash
/plugin marketplace add YOUR_GITHUB_USERNAME/claude-plugins
```

Then install individual plugins:

```bash
/plugin install insights-mode@geisson-plugins
```

## Available Plugins

### insights-mode

Explains architecture decisions, trade-offs, and patterns while writing complete code. No TODOs—just mentorship alongside shipping.

**Features:**
- `★ Insight` blocks explaining pattern choices and trade-offs
- Complete, production-ready code (no homework)
- Tuned for NestJS, Flutter, TypeScript, Prisma stack
- Covers DDD patterns, state management, type design, performance considerations

**Example output:**

```typescript
@Injectable()
export class TransactionService {
  // ... complete implementation
}
```

```
★ Insight ─────────────────────────────────────
Using interactive transaction because we need to read balance mid-transaction.
Trade-off: holds locks slightly longer on both wallet rows.
───────────────────────────────────────────────
```

## Adding More Plugins

1. Create folder in `plugins/your-plugin-name/`
2. Add `.claude-plugin/plugin.json` manifest
3. Add hooks, commands, or agents
4. Update `marketplace.json` to include the plugin
5. Push to GitHub

## License

MIT
