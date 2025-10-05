# Minimum Detectable Effect (MDE) Analysis
*Retrospective Business Justification for Landing Page Test*

## Business Context & Cost Analysis

### Development Costs
| Cost Component | Estimate | Rationale |
|----------------|----------|-----------|
| **Design Time** | $2,000 | 20 hours × $100/hour |
| **Frontend Development** | $3,000 | 30 hours × $100/hour |
| **QA & Testing** | $1,000 | 10 hours × $100/hour |
| **Project Management** | $500 | 5 hours × $100/hour |
| **Total Development Cost** | **$6,500** | |

### Business Value Parameters
| Metric | Value | Source |
|--------|-------|--------|
| **Average Order Value** | $85 | Company data |
| **Profit Margin** | 25% | Finance team |
| **Profit per Conversion** | **$21.25** | $85 × 25% |
| **Monthly Visitors** | 50,000 | Analytics |
| **Baseline Conversion Rate** | 12.9% | Current performance |

## MDE Calculation

### Break-Even Analysis
To justify the $6,500 development cost:

```python
# Required additional monthly profit
required_monthly_profit = 6500 / 12  # Amortize over 12 months
required_monthly_profit = 541.67

# Required additional monthly conversions
required_additional_conversions = required_monthly_profit / 21.25
required_additional_conversions = 25.5

# Required conversion rate increase (absolute)
monthly_conversions = 50000 * 0.129  # 6450 conversions
required_absolute_increase = 25.5 / 50000  # 0.051%

# Required relative improvement
mde_relative = (0.051 / 12.9) * 100  # 0.4% relative improvement

```

# Recommendations for Future Tests
MDE Selection Framework
- Calculate break-even MDE based on development costs
- Add strategic buffer (2-5× break-even for good ROI)
- Consider practical constraints (traffic volume, test duration)
- Choose achievable MDE that balances business needs with feasibility

# For This Specific Test
- Recommended MDE: 2.0% relative improvement
- Required Sample Size: 31,200 total visitors
- Estimated Duration: 2-3 weeks (at current traffic levels)

# Conclusion
The missing MDE analysis was the root cause of this test's failure. By not defining what business impact we needed to detect, we designed a test that was mathematically incapable of answering the business question.

Key Insight: Always start with "What improvement would make this change worthwhile?" before asking "Is this result statistically significant?"


