# AI - a commandline ChatGPT client in BASH with conversation/completion support

---

## Features:

* **Interactive chat sessions** with the `gpt-3.5-turbo` API endpoint (aka ChatGPT)

* **Multiline input**

* **Markdown support for replies** (requires [glow](https://github.com/charmbracelet/glow#installation) or [mdless](https://github.com/ttscoff/mdless#installation))

* **One shot Q&A** with optional follow-up conversation

* **STDIN piping** (sending file contents to ChatGPT)

* **Full conversation support**:
  
  * locally store unlimited conversations (in JSON format)
  
  * quick resume last conversation
  
  * delete/resume any stored conversation
  
  * conversation messages replay on resume
  
  * store current and start new conversation (reset history) during interactive sessions
  
  * Automatic conversation topic identification and update

---

## Full command line options (`ai -h`):

```shell
Start a new interactive conversation:
  ai
One shot Q&A (exit after reply):
  ai "what is love?"
Force an interactive conversation (continue interacting after reply):
  ai -i "what are you?"
Submit data as part of the question:
  cat file.txt | ai can you summarize the contents of this file?
List saved conversations:
  ai -l
Continue last conversation:
  ai -c
Continue specific conversation:
  ai -c [conversation_id]
Delete a conversation:
  ai -d <conversation_id>
Delete all conversations:
  rm "conversations.json"
```

---

## Example usage:

[![asciicast](https://asciinema.org/a/skNoeQlIH3Y1LBce5Q4EeRVjx.png)](https://asciinema.org/a/skNoeQlIH3Y1LBce5Q4EeRVjx)


