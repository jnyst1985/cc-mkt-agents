# Marketing Agent Suite for Claude Code

A powerful collection of 4 specialized AI marketing agents that analyze your existing content, ask intelligent questions, and produce data-driven marketing assets without assumptions or fabrication.

## 🚀 Quick Start

### Installation

1. Install Claude Code if you haven't already:
```bash
# Installation instructions at claude.ai/code
```

2. Copy all `.md` agent files to your Claude Code agents directory:
```bash
~/.claude/agents/
```

3. Verify installation:
```bash
claude-code list-agents
```

You should see all 4 marketing agents + orchestrator listed.

## 📋 Core Marketing Agents

### The 4 Production-Ready Agents

| Agent | Purpose | Key Output |
|-------|---------|------------|
| `product-marketing-strategist` | Product positioning & messaging architecture | Comprehensive positioning documents with personas |
| `ux-microcopy-specialist` | Interface copy & error message optimization | Complete microcopy systems with accessibility |
| `landing-page-optimizer` | High-converting landing page creation | Full landing pages with A/B test variations |
| `conversion-copywriter` | Multi-channel nurture sequences | Email, SMS, WhatsApp sequences with triggers |
| `marketing-agent-orchestrator` | Helps select the right agent & workflow | Agent recommendations and project plans |

### Core Operating Principles

All agents:
- **Discover context** - Automatically scan your project files
- **Read everything** - Analyze existing documentation and data
- **Ask for specifics** - Request real metrics and testimonials
- **Never fabricate** - No made-up numbers or fake social proof
- **Flag gaps** - Clearly indicate what information is needed

## 💡 How The Agents Work

### The 4-Step Process

#### Step 1: Discovery
```bash
# Each agent automatically runs:
glob **/*.{md,txt,json,csv,html}  # Finds all relevant files
```

#### Step 2: Analysis
- Reads product documentation
- Reviews existing campaigns
- Analyzes performance data
- Identifies available assets

#### Step 3: Clarification
```
Agent: "I found your product-overview.md. To create optimal positioning, I need:
1. Your exact pricing model (not estimates)
2. Three customer testimonials with quantifiable results
3. Your primary differentiator vs [Competitor A]
Please provide actual data."
```

#### Step 4: Generation
- Uses only verified information
- Incorporates your specific data
- Flags any missing elements
- Never invents content

## 🎯 Primary Use Cases

### Use Case 1: Complete Product Launch

**Step-by-Step Process:**

```bash
# 1. Define positioning and messaging
claude-code run product-marketing-strategist
# → Analyzes market, asks for differentiators
# → Output: positioning-[product]-v1.md

# 2. Create high-converting landing page
claude-code run landing-page-optimizer
# → Reads positioning, asks for social proof
# → Output: landing-page-[product]-v1.md

# 3. Build nurture sequences
claude-code run conversion-copywriter
# → References previous outputs, asks for metrics
# → Output: email-sequence-[product]-v1.md

# 4. Optimize product interface
claude-code run ux-microcopy-specialist
# → Uses positioning, asks for user data
# → Output: microcopy-[product]-v1.md
```

### Use Case 2: Fix Conversion Problems

```bash
# 1. Optimize landing page
claude-code run landing-page-optimizer
# → Asks for current conversion rate, testimonials
# → Output: landing-page-optimized-v1.md

# 2. Create recovery sequences
claude-code run conversion-copywriter
# → Asks for abandonment reasons, channels
# → Output: recovery-sequence-v1.md
```

### Use Case 3: Reduce Support Tickets

```bash
# Run microcopy specialist
claude-code run ux-microcopy-specialist
# → Analyzes support tickets
# → Asks for error frequencies, character limits
# → Output: microcopy-errors-v1.md
```

### Use Case 4: Repositioning

```bash
# Start with strategy
claude-code run product-marketing-strategist
# → Analyzes competitors
# → Asks for differentiation, win/loss data
# → Output: positioning-new-v1.md
```

## 📁 Optimal File Organization

### Recommended Structure

```
/marketing-project
  /research
    product-overview.md         # Product capabilities
    competitor-analysis.md      # Competitive landscape
    customer-interviews.txt     # Voice of customer
    market-research.md         # Industry insights
    
  /data
    conversion-metrics.csv     # Current performance
    email-performance.json     # Campaign metrics
    support-tickets.csv        # User pain points
    test-results.md           # A/B test history
    
  /assets
    testimonials.md           # Real customer quotes
    case-studies.md           # Success stories
    customer-logos/           # Logo files with permission
    
  /outputs
    positioning-v1.md         # Agent-generated
    landing-page-v1.md        # Agent-generated
    email-sequence-v1.md      # Agent-generated
    microcopy-v1.md          # Agent-generated
```

### Naming Conventions

**Your input files:**
```
[type]-[description].[ext]
product-overview.md
customer-testimonials.md
conversion-metrics.csv
```

**Agent output files:**
```
[type]-[project]-v[version].md
positioning-acme-v1.md
landing-page-acme-v2.md
email-sequence-launch-v1.md
microcopy-checkout-v1.md
```

## 🔄 Multi-Agent Workflows

### Sequential Workflow: Product Launch

```mermaid
positioning → landing page → email sequence → interface copy
```

1. **Start with Strategy**
   ```bash
   claude-code run product-marketing-strategist
   ```
   - Establishes positioning
   - Defines messaging pillars
   - Creates personas

2. **Create Landing Page**
   ```bash
   claude-code run landing-page-optimizer
   # Reference: positioning-v1.md
   ```
   - Uses positioning for consistency
   - Implements conversion psychology
   - Generates A/B tests

3. **Build Sequences**
   ```bash
   claude-code run conversion-copywriter
   # Reference: positioning-v1.md, landing-page-v1.md
   ```
   - Maintains message consistency
   - Multi-channel orchestration
   - Behavioral triggers

4. **Optimize Interface**
   ```bash
   claude-code run ux-microcopy-specialist
   # Reference: positioning-v1.md
   ```
   - Aligns with brand voice
   - Reduces friction
   - Improves clarity

### Parallel Workflow

After positioning is complete, run simultaneously:
```bash
# Terminal 1
claude-code run landing-page-optimizer

# Terminal 2
claude-code run conversion-copywriter

# Terminal 3
claude-code run ux-microcopy-specialist
```

## 📊 Data Requirements by Agent

### Product Marketing Strategist
**You Provide:**
- Product documentation
- Market research
- Competitor information

**Agent Asks For:**
- Exact pricing model
- Customer testimonials with metrics
- Specific differentiators
- Win/loss reasons
- Target customer titles

### Landing Page Optimizer
**You Provide:**
- Product description
- Target audience
- Conversion goals

**Agent Asks For:**
- Current conversion rate
- 5-10 customer testimonials
- Customer logos (with permission)
- Case studies with results
- Trust signals (awards, badges)
- Any real urgency factors

### Conversion Copywriter
**You Provide:**
- Product information
- Customer journey
- Available channels

**Agent Asks For:**
- Email performance metrics
- Sales cycle length
- Compliance requirements
- Channel opt-in rates
- Top objections from sales
- Behavioral triggers available

### UX Microcopy Specialist
**You Provide:**
- Interface descriptions
- User flows
- Current copy

**Agent Asks For:**
- Support ticket data
- Character limits per element
- Task completion rates
- Error frequencies
- User research findings
- Technical constraints

## 🤖 Example Agent Interactions

### Product Marketing Strategist
```
"I've analyzed your files and found product features in product-overview.md.
To create optimal positioning, I need to clarify:

1. What's your pricing? (e.g., Starter: $49/mo, Pro: $149/mo)
2. Can you provide 3 customer success stories with specific metrics?
3. Which 3 competitors do you most often lose deals to?
4. What capability do you have that competitors genuinely don't?

Please provide actual data, not estimates."
```

### Landing Page Optimizer
```
"I found your positioning doc. For a high-converting page, I need:

1. Current conversion rate? (e.g., 2.3%)
2. 5 testimonials with full name, company, and specific results?
3. 10 customer logos you have permission to display?
4. Any legitimate urgency (real deadline, limited seats)?

Only real, verified information will be used."
```

### Conversion Copywriter
```
"I've reviewed your email-performance.json. To optimize sequences:

1. What's your average sales cycle? (e.g., 21 days)
2. Which channels are customers opted into?
3. Top 3 objections from your sales team?
4. What behavioral triggers can your system track?

I need actual metrics, not projections."
```

### UX Microcopy Specialist
```
"I analyzed 200 support tickets about password errors. I need:

1. Character limits for error messages?
2. What are the actual password requirements?
3. Current task completion rate for sign-up?
4. Most common user errors from your data?

Please provide real constraints and metrics."
```

## ⚠️ What Agents Will NOT Do

### Never:
- ❌ Make up testimonials or quotes
- ❌ Invent statistics or metrics
- ❌ Create fake urgency
- ❌ Generate placeholder content
- ❌ Assume pricing
- ❌ Fabricate case studies
- ❌ Use stock photos as customers
- ❌ Make unverifiable claims

### Always:
- ✅ Use data from your files
- ✅ Ask for missing information
- ✅ Flag gaps in data
- ✅ Request permission for assets
- ✅ Verify compliance needs
- ✅ Mark sections needing data
- ✅ Maintain accuracy
- ✅ Respect truth in marketing

## 🐛 Troubleshooting

| Problem | Solution |
|---------|----------|
| "Can't find context" | Ensure files are in project directory with clear names |
| "Too many questions" | Prepare data files before running agents |
| "Generic output" | Provide specific examples and real data |
| "Agents not connecting" | Use consistent file naming: [type]-[project]-v[X].md |
| "No social proof" | Gather real testimonials before running |
| "Weak urgency" | Only use legitimate deadlines, not fake scarcity |

## 📈 Success Metrics

| Agent Output | Track This | Target |
|--------------|------------|---------|
| Positioning document | Sales adoption rate, win rate | +20% win rate |
| Landing pages | Conversion rate, bounce rate | +50% conversion |
| Email sequences | Open rate, click rate, conversions | +25% engagement |
| Microcopy | Support tickets, task completion | -30% tickets |

## 🚦 Quick Decision Guide

```
Need clear positioning?
→ product-marketing-strategist

Have positioning, need landing page?
→ landing-page-optimizer

Need to nurture leads?
→ conversion-copywriter

Users confused or stuck?
→ ux-microcopy-specialist

Not sure where to start?
→ marketing-agent-orchestrator
```

## ✅ Project Checklist

### Before Starting
- [ ] Gather product documentation
- [ ] Collect real testimonials
- [ ] Export performance metrics
- [ ] Document competitors
- [ ] Prepare brand guidelines

### During Execution
- [ ] Run orchestrator first for guidance
- [ ] Start with positioning if new project
- [ ] Provide real data when asked
- [ ] Save outputs with version numbers
- [ ] Reference previous outputs

### After Completion
- [ ] Review all outputs for consistency
- [ ] Verify all claims are factual
- [ ] Set up metric tracking
- [ ] Plan iteration based on results

## 💡 Best Practices

### 1. Data First
Always have ready:
- Real conversion rates
- Actual testimonials
- True performance metrics
- Verified case studies

### 2. Sequential Building
- Positioning → Landing Pages → Sequences → Microcopy
- Each builds on the previous

### 3. Version Control
```
positioning-v1.md → Initial
positioning-v2.md → Market feedback
positioning-v3.md → Competitive update
```

### 4. Consistency
Each agent should reference:
```
"Using positioning from positioning-v1.md..."
```

## 🤝 Team Usage

### Marketing Managers
- Use orchestrator for planning
- Ensure data accuracy
- Review outputs
- Track ROI

### Copywriters
- Provide real examples
- Refine agent outputs
- Add creative polish
- Maintain voice

### Product Marketers
- Supply positioning inputs
- Verify claims
- Provide insights
- Validate messaging

### Data Analysts
- Export clean metrics
- Track performance
- Feed results back
- Measure impact

---

**Version**: 3.0.0  
**Last Updated**: January 2024  
**Agents**: 4 Core + 1 Orchestrator  
**Principle**: Real Data → Smart Questions → Honest Output

Transform your marketing with AI precision, built on truth and powered by your actual data.