# 🧠 MediBot – Ask the Book!

MediBot is an intelligent question-answering chatbot that extracts and answers queries using information from the **Gale Encyclopedia of Medicine (2nd Edition)**. It uses state-of-the-art embeddings, vector databases, and large language models to generate contextually relevant answers backed by the book.

---

## 📘 Source Book

**The Gale Encyclopedia of Medicine – 2nd Edition**  
- Publisher: Gale Group  
- ISBN: 0-7876-5489-2  
- This encyclopedia includes ~1,700 full-length articles on medical disorders, conditions, tests, treatments, and more.  
- Layperson-friendly language, medically reviewed, and comprehensive.

---

## 🛠️ Tech Stack

| Component        | Tech Used                              |
|------------------|-----------------------------------------|
| Language Model   | HuggingFace Inference API (Mistral-7B)  |
| Embeddings       | `sentence-transformers/all-MiniLM-L6-v2` |
| Vector Database  | FAISS                                   |
| UI Framework     | Streamlit                               |
| Orchestration    | LangChain                               |
| Format           | Python                                  |

---

## 📁 Project Structure

```
├── data/                          # Folder to store PDFs
├── vectorstore/                  # FAISS vector store files
├── main_embedding.py             # Load, chunk, embed PDFs
├── query_console.py              # Run queries in console
├── app.py                        # Streamlit-based chatbot UI
├── .env                          # HuggingFace token
└── README.md
```

---

## ⚙️ Setup & Run

### 1. Clone the repository

```bash
git clone https://github.com/your-username/medibot.git
cd medibot
```

### 2. Install requirements

```bash
pip install -r requirements.txt
```

### 3. Add your HuggingFace API token

Create a `.env` file in the root directory:

```env
HF_TOKEN=your_huggingface_token_here
```

### 4. Add PDF book

Place the medical encyclopedia PDF inside the `data/` folder.

### 5. Generate Embeddings

```bash
python main_embedding.py
```

### 6. Test Console Q&A

```bash
python query_console.py
```

### 7. Run Streamlit App

```bash
streamlit run app.py
```

---

## 💬 Example Use Cases

- **"What is the treatment for calcium deficiency?"**
- **"List symptoms of Campylobacteriosis."**
- **"Can caffeine affect sleep patterns?"**

MediBot will search the medical encyclopedia and answer directly using the source context.

---

## ⚠️ Disclaimer

> This chatbot is for educational and informational use only. It is not intended to replace professional medical advice, diagnosis, or treatment.

---

## 📬 Contact

For any questions or suggestions, please contact (mailto:anantshiva9@gmail.com).
