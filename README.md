# Spring to Helidon AI Converter (Contextual)

This project provides an application to convert Maven-based Spring Boot projects into Helidon MP projects.

The application leverages OpenAI APIs for communication with LLMs and is compatible with OpenAI models such as `gpt-4o-mini` and `gpt-4o`.

## How It Works

The project provides a prompt and a set of callback functions or tools to the LLM to get and write back project files. The LLM must be clever enough to process the project this way. Better the model, better the result. The best results achieved with `gpt-4o`. `gpt-4o-mini` gives acceptable results too.

## Usage

### 1. Build the Project
Ensure you have Java 21 or higher and Maven installed.

```bash
mvn package
```

### 2. Configure the Application

Edit the `./config/converter.properties` file to set the following:
- `project-root`: Path to the source Spring Boot project.
- `destination-root`: Path to save the converted Helidon project.
- `model.api-key`: Your OpenAI API key.

### 3. Run the Application

```bash
java -jar target/converter-1.0-SNAPSHOT.jar ./config
```

## Configuration

You can customize the prompt sent to the model by editing `config/prompt.txt` file.
