# AI - a commandline ChatGPT client in BASH with conversation/completion support

## Features:

* **Interactive chat sessions** with the `gpt-3.5-turbo` API endpoint (aka ChatGPT)

* **Multiline input**

* **Markdown support for replies** (requires [glow](https://github.com/charmbracelet/glow#installation))

* **One shot Q&A** with optional follow-up conversation

* **Data piping support** (sending file contents to ChatGPT)

* **Full conversation support**:
  
  * locally store unlimited conversations (in JSON format)
  
  * quick resume last conversation
  
  * delete/resume any stored conversation
  
  * conversation messages replay on resume
  
  * store current and start new conversation (reset history) during interactive sessions
  
  * Automatic conversation topic identification and update

## Full command line options (`ai -h`):

###### Start a new interactive conversation:

`ai`

###### One shot Q&A (exit after reply):

`ai "how many planets are there in the solar system?"`

###### Force an interactive conversation (continue interacting after reply):

`ai -i "what is the fastest animal on earth?"`

###### Submit data as part of the question:

`cat file.txt | ai can you summarize the contents of this file?`

###### List saved conversations:

`ai -l`

###### Continue last conversation:

`ai -c`

###### Continue specific conversation:

`ai -c [conversation_id]`

###### Delete a conversation:

`ai -d [conversation_id]`

###### Delete all conversations:

`rm "/root/conversations.json"`

## Example usage:

[![asciicast](https://asciinema.org/a/566887.svg)](https://asciinema.org/a/566887)

## Installation:

###### Prerequisites:

* Install [glow](https://github.com/charmbracelet/glow#installation) for Markdown rendering support in your terminal

* `jq` (e.g. `apt install jq`)

* `curl` (e.g. `apt install curl`)

Install the script by either cloning this repository or directly downloading to your `$PATH`, e.g.:

```shell
curl "https://raw.githubusercontent.com/nitefood/ai-bash-gpt/master/ai" > /usr/bin/ai && chmod 0755 /usr/bin/ai
```
