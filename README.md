# AI - a commandline ChatGPT client in BASH with conversation/completion and image generation support

## Features:

* **Interactive chat sessions** with the `gpt-3.5-turbo` API endpoint (aka ChatGPT)

* **Multiline input**

* **Image generation support:**
  
  * image preview grid rendered directly in the terminal
  
  * generate up to 10 images at a time
  
  * automatic URL shortening
  
  * optionally save images and prompt to local disk

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

###### One shot Q&A (will ask you to continue interacting, otherwise quit after answer):

`ai "how many planets are there in the solar system?"`

###### Generate one or more images (default 1, max 10):

`ai -i [num] "a cute cat"`

###### Submit data as part of the question:

`cat file.txt | ai can you summarize the contents of this file?`

###### List saved conversations:

`ai -l`

###### Continue last conversation:

`ai -c`

###### Continue specific conversation:

`ai -c <conversation_id>`

###### Delete a specific conversation:

`ai -d <conversation_id>`

###### Delete selected conversations:

`ai -d <conversation_id_start>-<conversation_id_end>`

###### Delete all conversations:

`rm "/root/conversations.json"`

## Usage examples:

##### (Interaction and conversation resuming)

[![asciicast](https://asciinema.org/a/572784.svg)](https://asciinema.org/a/572784)

##### (Image generation)

[![asciicast](https://asciinema.org/a/572785.svg)](https://asciinema.org/a/572785)

##### (Input piping to stdin)

[![asciicast](https://asciinema.org/a/572786.svg)](https://asciinema.org/a/572786)

## Installation:

###### Prerequisites:

* Install jq, curl, imagemagick, catimg
  
  * for e.g. Ubuntu: `apt -y install jq curl imagemagick catimg`

* Install [glow](https://github.com/charmbracelet/glow#installation) for Markdown rendering support in your terminal

###### Script download:

Install the script by either cloning this repository or directly downloading to your `$PATH`, e.g.:

```shell
curl "https://raw.githubusercontent.com/nitefood/ai-bash-gpt/master/ai" > /usr/bin/ai && chmod 0755 /usr/bin/ai
```
