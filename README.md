# 🤖 Schema Assist

> Conversational Data Dictionary Agent for Relational Databases  
> Ask questions in plain English. Get SQL + interactive charts instantly.

---

## 📌 What is Schema Assist?

Schema Assist transforms complex relational databases into a conversational analytics experience.

Instead of writing SQL, users can ask:

- “Show monthly order trends”
- “What’s the average delivery time?”
- “Top 5 cities by revenue?”

The system interprets intent, generates queries, and returns interactive charts powered by Plotly.

---

## 🎯 Why This Matters

Business users often struggle with:
- Writing SQL
- Understanding schema relationships
- Maintaining data dictionaries
- Creating meaningful visualizations

Schema Assist solves this by combining:
- LLM-powered intent parsing  
- Auto-maintained metadata layer  
- Dynamic query generation  
- Real-time visualization  

---

## ⚙️ How It Works

```text
User Query
    ↓
Intent Understanding (LLM)
    ↓
Metadata-Aware Query Generation
    ↓
Database Execution
    ↓
Interactive Plotly Visualization
```

---

## 🧠 Core Architecture

### 1️⃣ LLM/NLP Engine  
Uses Cohere models for intent detection and embedding similarity.

### 2️⃣ Metadata Layer  
Auto-maintained schema descriptions, relationships, and sample values.

### 3️⃣ Query Generator  
Translates natural language → SQL or Pandas queries.

### 4️⃣ Visualization Engine  
Interactive charts using Plotly (line, bar, scatter, map, heatmap).

### 5️⃣ Interface Layer  
Deployable via:
- React Web App  
- Slack Bot  
- Jupyter / Colab  

---

## 🛠 Tech Stack

| Layer | Technology |
|-------|------------|
| Backend | Python, FastAPI, SQLAlchemy |
| Database | PostgreSQL |
| LLM | Cohere Command + Embed |
| Vector Search | FAISS |
| Visualization | Plotly |
| Frontend | React |
| Notebook Support | Google Colab |

---

## 📊 Dataset Used

**Brazilian E-Commerce Public Dataset by Olist**

- ~100k orders (2016–2018)
- Customers, sellers, products, payments, reviews
- Multi-table relational structure

Perfect for testing metadata-driven query generation.

---

## 🚀 Run in Google Colab

### Install dependencies

```python
!pip install langchain cohere plotly pandas sqlalchemy faiss-cpu
```

---

### 3. Clone the repository (if available)
```python
!git clone https://github.com/piyush080205/Schema-Assist.git
%cd schema-assist
```

## 💬 Usage Examples

| User Query | Bot Response |
|------------|--------------|
| *“What columns are in the orders table?”* | Displays table schema with descriptions + sample data |
| *“What’s the average delivery time?”* | “Average delivery time is 12.3 days” + histogram |
| *“Show me order distribution by state”* | Interactive Plotly map of Brazil with bubble sizes |
| *“How have sales trended over time?”* | Plotly line chart with monthly order totals + forecast |
| *“Is there a relationship between price and review score?”* | Plotly scatter plot with trend line |

---

## 🎯 Demo Scenario

1. **Ask**: “What’s in the dataset?” → Agent returns summary of tables and key columns.  
2. **Follow‑up**: “Show me top 5 product categories by sales” → Bar chart of top categories.  
3. **Drill down**: “Now filter to just 2018” → Updates chart with 2018 data.  
4. **Explore**: “Map of customer locations for electronics” → Geographic map of electronics orders.  
5. **Analyze**: “Correlation between freight cost and review score” → Scatter plot + trend line.

---


## 👥 Team

**Team Elite**  
HackFest 2.0 – Round I

---

## 📄 License

This project is licensed under the MIT License.

---

## 🙌 Acknowledgments

- [Olist](https://olist.com/) for the public Brazilian E‑Commerce dataset
- [Cohere](https://cohere.com/) for the LLM and embedding APIs
- [Plotly](https://plotly.com/) for beautiful interactive charts

```
