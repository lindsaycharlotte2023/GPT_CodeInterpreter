# Chainlit Project

Chainlit is an AI-driven project designed to carry out various tasks. It is built on a plugin architecture that can easily extend new features.

## Project Features

- **Plugin Architecture**: Chainlit uses a flexible and extensible plugin architecture. Each plugin is a folder containing `functions.py` and `config.json` files, defining the functionality and configuration of the plugin.

- **Function Manager**: The function manager is responsible for parsing and calling the functions defined in the `functions.py` file of each plugin.

- **AI Driven**: Chainlit leverages the power of AI to understand and generate human language, enabling it to handle a variety of tasks.

## Current Plugins

1. **General Plugin**: This plugin provides the functionality of displaying and uploading images.

2. **Python Interpreter Plugin**: This plugin includes a Python executor for running Python code, which is very useful for tasks such as data analysis and table processing.

3. **Vue Plugin**: Currently under development, this plugin is designed to work with Vue projects, automating the entire Vue project modification through the chat interface.

## Plugin Structure and Usage

Each plugin is a directory in the 'plugins' folder. The directory name is the name of the plugin. Each plugin directory contains at least two files:

1. `functions.py`: This file contains the functions provided by the plugin. Each function should be a top-level function (i.e., not a method of a class or an inner function), and should be named in a way that reflects its functionality. Functions can be synchronous or asynchronous.

2. `config.json`: This file contains the configuration of the plugin. It is a JSON file with a required field: `enabled`. If `enabled` is set to `true`, the functions of the plugin will be imported and available for use. If `enabled` is set to `false`, the functions of the plugin will not be imported.

To use a plugin, make sure it is enabled in its `config.json` file. Once enabled, the functions provided by the plugin will be automatically imported when the script runs. The AI assistant will be able to call these functions in the conversation.

## Creating Plugins

To create a plugin, follow these steps:

1. Create a new directory in the 'plugins' folder. The directory name will be the name of the plugin.

2. In the new directory, create a file named `functions.py`. In this file, define the functions you want the plugin to provide. Each function should be a top-level function and should be named in a way that reflects its functionality.

3. In the same directory, create a file named `config.json`. In this file, add the following JSON:

```json
{
    "enabled": true
}
```

This will enable the plugin by default. If you want to disable the plugin, you can change `true` to `false`.

## Running the Project

To run this project, you need to follow these steps:

1. First, you need to create a `.env` file in the root directory of the project. You can do this by copying the `.env.example` file.

2. In the `.env` file, you need to provide your OpenAI API key. This should be a string, like `OPENAI_API_KEY=your_api_key_here`. Please replace `your_api_key_here` with your actual OpenAI API key.

3. Still in the `.env` file, you need to set the base URL for the OpenAI API. This should be a string, like `OPENAI_API_BASE=https://api.openai.com/v1`.

4. After saving the `.env` file, you need to install Chainlit. You can do this with pip: `pip install chainlit`.

5. Once Chainlit is installed, you can run the project with the following command: `chainlit run app.py -w`.

## Use Replit to deploy

## Step 1: Deploy to Repl.it

Click the button below to deploy this project to Repl.it:

[![Run on Repl.it](https://replit.com/badge/github/boyueluzhipeng/GPT_CodeInterpreter)](https://replit.com/new/github/boyueluzhipeng/GPT_CodeInterpreter)

Once you've clicked the button, the project repository will be cloned into a new Repl.it workspace.

## Step 2: Install Dependencies

After the project has been cloned, you need to install the necessary dependencies. To do this, open the Shell terminal in Repl.it, and run the following command:

```bash
pip install -r requirements.txt
```

This will install all the Python packages listed in the `requirements.txt` file.

## Step 3: Configure Environment Variables

Next, you need to set up the environment variables. In the Shell terminal, run the following command:

```bash
cp .env.example .env
```

This command copies the contents of the `.env.example` file into a new file named `.env`.

## Step 4: Add Secrets

Then, go to the 'Secrets' section in Repl.it (usually on the left sidebar), and select 'Edit as JSON'. Copy and paste the following JSON content:

```json
{
  "OPENAI_API_KEY": "your_api_key",
  "OPENAI_API_BASE": "https://api.openai.com/v1"
}
```

Replace `"your_api_key"` with your actual OpenAI API key.

## Step 5: Run the Project

Now, you're ready to run the project. Click the 'Run' button at the top of the Repl.it interface.

## Step 6: Access the Web Interface

Once the project is running, find your public URL in the 'Webview' section. You can use this URL to access the GPT Code Interpreter in your web browser.

And that's it! You've successfully deployed the GPT Code Interpreter on Repl.it. If you encounter any issues, please refer to the Repl.it documentation or raise an issue on the project's GitHub page.

## Contributing

Contributions are welcome! Please read the contribution guide to learn how to contribute to this project.

## License

This project is licensed under the terms of the MIT license.