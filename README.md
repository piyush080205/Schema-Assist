```markdown
# Schema Assist 🤖📊

**Schema Assist** is an intelligent Data Dictionary Agent that bridges the gap between complex relational databases and natural language. It empowers business users, analysts, and data scientists to explore large datasets—like the Olist Brazilian E‑Commerce dataset—without writing SQL. By combining an LLM/NLP engine with an automatically maintained metadata layer, the agent translates plain‑English questions into executable queries and instantly renders interactive **Plotly** visualizations.

---

## 🚀 Overview

Data exploration is often gatekept by technical complexity. Business users struggle to interpret large relational databases without SQL or visualization expertise. Manual data dictionary maintenance is slow, creating a disconnect between raw data and actionable insights.

**Schema Assist** turns static data into a conversational partner. Ask questions like *“Show me monthly order trends”* or *“What’s the average delivery time?”* and get real‑time answers with rich, interactive charts—all within a chat interface (Slack, web app, or Jupyter/Colab).

---

## ✨ Key Features

- **Natural language querying** – No SQL required.
- **Automated data dictionary** – Schema descriptions and relationships are maintained automatically.
- **LLM‑powered intent understanding** – Uses Cohere Command + Embed models to parse user questions.
- **Real‑time Plotly visualizations** – Bar charts, line charts, scatter plots, maps, heatmaps, and more.
- **Multi‑turn conversations** – Drill down, filter, and explore through follow‑up questions.
- **Metadata‑driven & scalable** – Designed to handle large datasets (e.g., 100k+ orders).
- **Chat‑integrated** – Deployable in Slack, web apps, or interactive notebooks like Colab.
- **Instant insights** – Summaries, trends, correlations, and geographic distributions on demand.

---

## 🧠 Architecture

```
User Query → NLP Understanding → Data Retrieval → Plotly Generation → Chat Response
```

**Components:**
1. **LLM/NLP Engine** – Interprets user intent (e.g., “Show me monthly order trends”) using Cohere models.
2. **Metadata Layer** – Stores data dictionary with column descriptions, relationships, and sample values.
3. **Query Generator** – Translates natural language into SQL or DataFrame queries.
4. **Plotly Visualizer** – Creates interactive charts (bar, line, scatter, map, etc.).
5. **Chat Interface** – Web app (React), Slack bot, or Jupyter/Colab widget.

---

## 🛠️ Tech Stack

| Layer       | Tools & Technologies |
|-------------|----------------------|
| **Frontend**| React, Plotly, Chart.js |
| **Backend** | Python, FastAPI, PostgreSQL, SQLAlchemy |
| **LLM**     | Cohere Command, Cohere Embed |
| **Vector Store** | FAISS (Facebook AI Similarity Search) |
| **Notebook**| Google Colab / Kaggle |
| **Dataset** | [Brazilian E‑Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) |

---

## 📁 Dataset

We use the **Olist Brazilian E‑Commerce** dataset, which contains:
- ~100k orders from 2016–2018
- Customers, sellers, products, reviews, geolocation, and payments
- Multiple interconnected tables (orders, customers, products, etc.)

The agent’s metadata layer captures all table schemas, relationships, and sample rows to enable accurate query generation.

---

## 🔧 Setup & Run in Google Colab

Follow these steps to try Schema Assist in Colab:

### 1. Open a new Colab notebook

### 2. Install dependencies
```python
!pip install langchain cohere plotly pandas sqlalchemy faiss-cpu
```

### 3. Clone the repository (if available)
```python
!git clone https://github.com/your-repo/Schema-Assist.git
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
