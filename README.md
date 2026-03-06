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

<img width="1006" height="638" alt="Image" src="https://github.com/user-attachments/assets/6e2f1372-4c23-4d3f-95da-99535e073572" />

---

## Chatbot Demo

The agent handles natural language shopping requests — recommending products, adding to cart, and cross-selling based on user behavior.

<img width="655" height="610" alt="Image" src="https://github.com/user-attachments/assets/4135238a-ff1e-475b-ac93-73eb0a0ae459" />

<img width="655" height="554" alt="Image" src="https://github.com/user-attachments/assets/a1851a50-0f73-4b19-bfbf-3d5cd102731e" />

---

## Cart Table (DynamoDB)

The agent persists cart data to a **DynamoDB table**. After the conversation above, the table reflects the added items:

<img width="1522" height="767" alt="Image" src="https://github.com/user-attachments/assets/fcee70be-7b75-41ee-9b79-149fb9ba9fac" />

![Cart Table](assets/cart-table.png)
