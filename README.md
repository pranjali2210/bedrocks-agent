# 🤖 Bedrock Agent — wallE

An AWS Bedrock-powered conversational shopping agent with personalized product recommendations, cart management, and DynamoDB persistence.

---

## 📋 Table of Contents

- [Agent Details](#agent-details)
- [Action Groups](#action-groups)
- [Chatbot Demo](#chatbot-demo)
- [Cart Table (DynamoDB)](#cart-table-dynamodb)

---

## Agent Details

<img width="1034" height="766" alt="Image" src="https://github.com/user-attachments/assets/44eccf9c-0bc9-4430-8690-ea7da59335ab" />

---

## Action Groups

The agent has **4 action groups**, all currently enabled:

| Name | State | Last Updated |
|------|-------|--------------|
| `addItemToCart` | ✅ Enabled | March 05, 2026, 22:01 (UTC+05:30) |
| `getCart` | ✅ Enabled | March 05, 2026, 22:00 (UTC+05:30) |
| `personalizeItems` | ✅ Enabled | March 06, 2026, 19:38 (UTC+05:30) |
| `productbot` | ✅ Enabled | March 06, 2026, 13:56 (UTC+05:30) |

![Action Groups](assets/action-groups.png)

> **Note:** Memory (*New*) allows the agent to retain conversational context across sessions. Currently disabled for this agent.

---

## Chatbot Demo

The agent handles natural language shopping requests — recommending products, adding to cart, and cross-selling based on user behavior.

### Example Conversation

**Turn 1 — Product Discovery**

> 👤 *"I want to buy a gift for my mother"*
>
> 🤖 Here are some gift ideas for your mother:
> 1. Heartfelt rose - Romantic Heartfelt rose
> 2. Cherished hat - Trendy Cherished hat
>
> Would you like to add any of these to your cart?

![Chatbot Turn 1](assets/chatbot-1.png)

---

**Turn 2 — Add to Cart + Cross-sell**

> 👤 *"yes 2nd one"*
>
> 🤖 Please provide your email to use as your user ID.

> 👤 *"67@qwer"*
>
> 🤖 Other customers also bought this along with the Cherished hat:
> 1. Heartfelt rose - Romantic Heartfelt rose
>
> Would you like to add it to your cart as well?

> 👤 *"yes"*

![Chatbot Turn 2](assets/chatbot-2.png)

---

## Cart Table (DynamoDB)

The agent persists cart data to a **DynamoDB table**. After the conversation above, the table reflects the added items:

**Table:** `product-chatbot-Cart-1EI9RPV2UQ827`

| user_id | product_name |
|---------|--------------|
| mm@123 | Cherished cologne |
| 67@qwer | Cherished hat |
| 67@qwer | Heartfelt rose |
| 123@mm | Celebratory necklace |
| 123@mm | Joyous cologne |

> Scan result: **5 items returned · 5 scanned · 100% efficiency · 2 RCUs consumed**

![Cart Table](assets/cart-table.png)
