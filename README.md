# 7주차 RAG Chatbot (Ollama + LangChain + Chroma)

한성대학교 학사공지 PDF를 검색해서 답하는 RAG 챗봇입니다.

## 구성
- step1_ollama.py: Ollama(gemma3:4b) 모델 호출
- step2_retrieval.py: PDF 로드, Chunking, Embedding, Chroma 검색
- step3_basic_rag.py: 검색 결과를 프롬프트에 넣는 기본 RAG
- step4_chat_rag.py: 이전 질문을 반영하는 대화형 RAG
- app.py: Streamlit 챗봇 UI

## 실행 환경
- Google Colab (T4 GPU)
- Ollama gemma3:4b
- 임베딩: sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2

## 실행 방법
1. `6w/data/` 폴더에 공지 PDF(`공지*.pdf`)를 넣고, 이 파일들은 `7w/` 폴더에 둡니다.
2. `ollama pull gemma3:4b`
3. `pip install -r requirements.txt`
4. `python step1_ollama.py` → `step2` → `step3` → `step4`
5. `streamlit run app.py`

## 참고 및 협업
- 1차 결과물: [tjwogus0309-code/hw](https://github.com/tjwogus0309-code/hw)
- 위 결과물을 검토하고 피드백한 뒤 직접 수정한 버전입니다.
- 주요 수정 사항: (직접 실행하며 바꾼 내용을 여기에 적기)
