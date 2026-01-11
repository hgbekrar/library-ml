# Unit 1 

## What is an agent ?
definition : An AI agent is a system that leverages an AI model to interact with its environment in order to achieve a user-defined objective. It *combines* resonning, planning and the execution of actions (usually using external tools) to fullfil tasks.

### What is an agent composed of ?
* Brain (AI Model, reasoning, choosing best options)
* Body (capabilities and tools)


### What AI Model are used for agents ?
* **Large Language Models** (LLM) which inputs&outputs **Text** such as : 
* * *ChatGPT* from *OpenAI*
  * *Gemini* from *Google*
  * *Llama* from *Meta*
> But other types of models are available such as **Vision Language Models** (VLM) that take **Images/Videos** as inputs.

### How agents execute actions ?
* the answer is : they use (external) **Tools** to execute **Actions**


## What are LLMs ?
definition : An AI model that is very good at both **understanding and generating human language**. This model was trained on a vast amount of text, allowing it to learn patterns, *structure* and meaning *in language* (*pretraining* is an **unsupervised learning**). It generally contains many milions of parameters. They are built on a **Transformer** architecture (a neural network architecture from deep learning based on the **Attention** algorithm)

### How they can get good at **understanding and generating human language** ?
answer : transformers
### What is a Transformer ?
there are 3 types of Transformers : 
* An Encoder : takes text as input and outputs a dense representation (**embedding**) of this text
* A Decoder : takes a sequence of tokens and outputs the next most probable token, **one at a time**
* Seq2Seq (sequence to sequence / Encoder-Decoder) : combines a encoder to transform the text into a *context-representation* then uses a decoder to output the next token.

> LLMs are typically composed of a decoder-based model with bilions of parameters

> The underlying principle of an LLM is to predict the next token given a sequence of previous tokens.

### What is a token ?
*unit of information* an LLM works with. For efficiency tokens aren't whole words.

### Does each LLM model has the same token list / "vocabulary"?
No

### Are there special tokens ?
Yes, for example EOS Tokens (End Of Sequence Tokens). (they vary across the LLM providers)

### What roles play EOS in Text Generation ?
When the LLM predicts an EOS, it terminates the prediction of the model.


### How works one single loop in Text Generation ?
> Indeed, LLMs are called **autoregressive**, while not generating an EOS, they keep calling themselves again and again. An output from one loop is used as an input for the next loop.
* the sequence of text is **tokenized**, then the model makes the tokens in a representation space that captures meaning of the words.
* decoding the sequence to output the most probable next token (can be done in different ways)

### How can I use LLMs ?
* locally (on your computer)
* use a cloud / API

#### What resources do you need to run a model on your computer ?
#### What is a cloud/api ?
* a cloud is a set of servers hosted by a company
* an API (*application programming interface*) is an **interface** (like a gate), send queries and get responses to connect to the physical servers (*cloud*)
#### how works an API call ?
* url = the endpoint
* payload = the order / prompt 
* an API key = your "ID Card"

## What are tools ?
* A tool is a **function** given to the LLM. This function should fulfill a clear objective.
* A good tool should be a tool that complements the power of an LLM.
* Moreover the knowledge of an LLM consists of its training data, so to give him **up-to date** information, tools are necessary.
* A tool should contain : a textual description of what the function does, a callable (something to perform an action), arguments (to write inputs)
### What is a Chat Templates ?
### What is a system prompt ?
> system_message = "behave like this = Agent behavior, here are your tools = Agent tools has access to, what you have to do ..."
> JSON Format messages ?
### How do tools work ?
### How do we give tools to an LLM ?
#### 1st Strategy to solve this problem - Plain text description
**use the system prompt to give a clear and precise description of the tools the LLM has access to.**
we have to tell exactly 
* what the tool does 
* what exactly it takes an input
#### 2nd - Class in Python
* create a class (parameters including a callable function)
* and a decorator (@tool) which computes the string for the LLM automatically given that you are in the same format imposed by the decorator and that you provide a call with required inputs for the class
#### 3rd - MCP
*Model Context Protocol* 

standardizes the usage of tools by LLMs

## Agent Workflows - thought, action, observation cycle
definition :
* Thought : the LLM decides what is the next step
* Action : The Agent calls external tools with the right parameters
* Observation : The model *reflects on the response from the tool*

> the guidelines and rules are generally embedded in the system prompt : system_message = "... use thought-action-observation cycle, descriptions... ..."

