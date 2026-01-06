# Poem Analysis App

An AI/LLM application that analyzes poetry and generates a report paper.

## Project Overview

This application will:
1. Accept a markdown file containing a poem as input
2. Analyze the poem using LangChain and an LLM
3. Generate a structured academic paper about the poem
4. Output the paper in a readable format

## Prerequisites

- Python 3.8+
- OpenAI API key (or alternative LLM provider)
- Basic understanding of Python and markdown

## Task Breakdown

### Phase 1: Environment Setup

**Goal**: Get your development environment ready

- [ ] Create a new Python virtual environment
- [ ] Install required packages: `langchain`
- [ ] Set up project directory structure:

### Phase 2: File Loading

**Goal**: Learn to use LangChain's document loaders

**Key Concepts**: Document loaders, TextLoader, UnstructuredMarkdownLoader

**Tasks**:
- [ ] Import the appropriate LangChain document loader
- [ ] Write a function to load the markdown file
- [ ] Extract the poem text from the loaded document
- [ ] Handle file reading errors gracefully

**LangChain Components to Learn**:
- `langchain.document_loaders.TextLoader`
- `langchain.document_loaders.UnstructuredMarkdownLoader`

### Phase 3: Prompt Engineering

**Goal**: Create effective prompts for poem analysis

**Key Concepts**: Prompt templates, few-shot learning, structured outputs

**Tasks**:
- [ ] Design a prompt template for poem analysis
- [ ] Include instructions for analyzing:
  - Literary devices (metaphor, simile, imagery, etc.)
  - Themes and meanings
  - Structure and form
  - Tone and mood
  - Historical/cultural context
- [ ] Create a template for the paper structure
- [ ] Use `PromptTemplate` or `ChatPromptTemplate` from LangChain

**LangChain Components to Learn**:
- `langchain.prompts.PromptTemplate`
- `langchain.prompts.ChatPromptTemplate`

### Phase 4: LLM Integration

**Goal**: Connect to an LLM and make basic calls

**Key Concepts**: LLM initialization, chat models, API integration

**Tasks**:
- [ ] Initialize your chosen LLM (e.g., OpenAI's GPT-4)
- [ ] Configure temperature and other parameters
- [ ] Test a simple poem analysis call
- [ ] Handle API errors and rate limits

**LangChain Components to Learn**:
- `langchain_openai.ChatOpenAI`
- Understanding model parameters (temperature, max_tokens, etc.)

### Phase 5: Chain Construction

**Goal**: Build a LangChain chain to orchestrate the analysis

**Key Concepts**: Chains, LLMChain, sequential chains

**Tasks**:
- [ ] Create a chain that combines your prompt and LLM
- [ ] Build a simple LLMChain for initial analysis
- [ ] Consider using SequentialChain for multi-step analysis:
  1. Initial reading and summary
  2. Literary device identification
  3. Theme analysis
  4. Paper writing
- [ ] Test the chain with a sample poem

**LangChain Components to Learn**:
- `langchain.chains.LLMChain`
- `langchain.chains.SequentialChain`
- `langchain.chains.SimpleSequentialChain`

### Phase 6: Output Formatting

**Goal**: Structure the generated paper properly

**Key Concepts**: Output parsers, structured outputs

**Tasks**:
- [ ] Define the expected paper structure (introduction, body paragraphs, conclusion)
- [ ] Use output parsers to ensure consistent formatting
- [ ] Consider using Pydantic for structured output validation
- [ ] Format the output as markdown or plain text

**LangChain Components to Learn**:
- `langchain.output_parsers.StructuredOutputParser`
- `langchain.output_parsers.PydanticOutputParser`

### Phase 7: Memory (Optional Advanced Feature)

**Goal**: Add conversation memory for iterative refinement

**Key Concepts**: Conversation memory, chat history

**Tasks**:
- [ ] Implement ConversationBufferMemory
- [ ] Allow users to ask follow-up questions about the analysis
- [ ] Enable iterative refinement of the paper

**LangChain Components to Learn**:
- `langchain.memory.ConversationBufferMemory`
- `langchain.memory.ConversationSummaryMemory`

### Phase 8: Testing and Refinement

**Goal**: Validate your application works correctly

**Tasks**:
- [ ] Test with multiple poems of different styles
- [ ] Verify the quality of generated papers
- [ ] Adjust prompts and parameters for better results
- [ ] Add error handling for edge cases
- [ ] Create sample poems in the `poems/` directory

### Phase 9: Enhancement Ideas (Optional)

Once the basic app works, consider adding:

- [ ] CLI interface with argument parsing
- [ ] Support for multiple file formats (txt, pdf)
- [ ] Comparison of multiple poems
- [ ] Citation generation for references
- [ ] Export to PDF or DOCX
- [ ] Web interface with Streamlit or Gradio
- [ ] Vector store for storing analyzed poems
- [ ] RAG (Retrieval Augmented Generation) for literary context

## Success Criteria

You'll know you've succeeded when:
- Your app successfully loads a poem from a markdown file
- It generates a coherent, well-structured academic paper
- The analysis includes literary devices, themes, and interpretations
- The output is saved in a readable format
- You understand how each LangChain component works
