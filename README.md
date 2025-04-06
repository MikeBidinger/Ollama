# Ollama

Ollama is a tool that allows you to run large language models (LLM's) locally on your own computer.
It provides a simple way to download, run, and interact with models like LLaMA, Mistral, or other open-source LLM's without relying on cloud-based services.

For more information visit their [webpage](https://ollama.com) or their [GitHub repository](https://github.com/ollama/ollama).

## Install Ollama

Before we are able to run Ollama models, we first need to download and install Ollama.
It can be downloaded from their [download webpage](https://ollama.com/download).
Once downloaded, install the Ollama application.
To make sure the installation was successful and Ollama is running, we can check this be executing the following command in the CLI:

```bash
ollama
```

The returned result should look something like:

```result
Usage:
  ollama [flags]
  ollama [command]

Available Commands:
  serve       Start ollama
  create      Create a model from a Modelfile
  show        Show information for a model
  run         Run a model
  stop        Stop a running model
  pull        Pull a model from a registry
  push        Push a model to a registry
  list        List models
  ps          List running models
  cp          Copy a model
  rm          Remove a model
  help        Help about any command

Flags:
  -h, --help      help for ollama
  -v, --version   Show version information

Use "ollama [command] --help" for more information about a command.
```

## Pull Models

To be able to use a Ollama model, we first need to pull it.
We're able to have multiple models, but only one model can be used at a time.
To pull a specific model, executing the following command in the CLI:

```bash
ollama pull qwen2.5-coder:1.5b
```

## Show Available Models

All the available models are listed on the [library webpage](https://ollama.com/library) and in the [GitHub README](https://github.com/ollama/ollama/blob/main/README.md#model-library).
To view all the pulled models, use the following command in the CLI:

```bash
ollama list
```

> Be aware that how bigger the size of a model (more parameters), the more RAM should be available to run the model.

## Run Models

Once the model is pulled, it can be run to interact with it.
Use the following command in the CLI to run the model:

```bash
ollama run qwen2.5-coder:1.5b
```

> When the model is not yet pulled, this command will also pull is before it will run.

Now you can enter a message to get an answer of the model.
You can exit the active model by entering `/bye`.
