# TOKEN-Spatialmythos: Royalice Density Manipulation Unit

## What is this?
This project is a unique integration between a quantum-inspired spatial simulation (Royalice) and multiple LLMs (Claude, Gemini, ChatGPT, Grok, Kimi). It creates a **bridge between simulated spatial physics and LLM APIs**, using "waveform channel communication" and token-based access control tied to spatial coordinates and RAM allocation.

## Key Features

1. **Waveform-Channel LLM Communication**
   - Sends messages to LLMs over simulated "waveform channels"
   - Locked to spatial coordinates from the density manipulation simulation
   - Allocates RAM buffers tied to coordinate magnitudes

2. **Token-Based Access Control**
   - Permissions: Read/Write/Delete/Execute/Full
   - Tokens have origin spatial coordinates
   - Expiration time for temporary permissions

3. **Multi-Model Support**
   - Claude (Anthropic API)
   - Gemini (Google Cloud API)
   - ChatGPT (OpenAI API)
   - Grok (X.AI API)
   - Kimi (Moonshot API)

4. **Terminal Interface**
   - `send [endpoint] [message]` sends message to single LLM
   - `broadcast [message]` sends message to all LLMs simultaneously
   - `status` shows current network/waveform lock status
   - `messages` shows all received messages

5. **Spatial Simulation Integration**
   - Simulates particle field/density manipulation
   - Hawking radiation calculations
   - Hash space representation of system state

## How to Use

### Basic Setup
1. Clone the repo: `git clone https://github.com/JlovesYouGit/TOKEN-Spatialmythos.git`
2. Build: `dotnet build`
3. Run: `dotnet run`

### API Key Configuration
Set these environment variables to use real APIs (otherwise demo mode):
- `ANTHROPIC_API_KEY` for Claude
- `GOOGLE_API_KEY` for Gemini
- `OPENAI_API_KEY` for ChatGPT
- `XAI_API_KEY` for Grok
- `MOONSHOT_API_KEY` for Kimi

### Using the Interactive Terminal
When you run the simulation, you'll automatically enter interactive terminal mode after initialization:
```
> send claude Hello! What can you do?
[Bridge-Waveform] Claude: Starting API discovery...
[Claude] [response text here]

> broadcast What is a quantum?
Calling all endpoints...
[Claude] [response]
[Gemini] [response]
[Grok] [response]
[ChatGPT] [response]
[Kimi] [response]
```

## Benefits for LLM Use

1. **Multi-Model Coordination**
   - Run same query across all 5 LLMs at once
   - Compare responses side by side
   - Broadcast system prompts to all models

2. **Spatial Context Awareness**
   - All messages are tagged with a spatial coordinate from the simulation
   - Coordinates are sent to the LLMs
   - Can use this for spatial/3D reasoning prompts

3. **Token Permission System**
   - Fine-grained control over what models can do
   - Temporal access control via expiration times
   - Coordinate-bound permission tokens

4. **RAM-Backed Storage Access**
   - Each LLM endpoint has its own RAM buffer tied to spatial coordinate
   - Storage slots for data persistence
   - Access controlled via permission tokens

## Architecture Overview
```
[Royalice Simulation] → [Extract Coordinate] → [Lock Waveform/RAM] → [Send Token] → [LLM API Call]
```

- **EndpointBridge**: Manages individual LLM connections
- **MacRouteManager**: Routes messages/tokens across channels
- **CommunicationChannel**: Simulated network channel between endpoints
- **WaveformPacket**: Data structure for waveform-based message passing

## Project Structure
- `Royalice.cs`: Main codebase (simulation, endpoints, communication)
- `visualizer/`: Web-based simulation visualizer
- `Royalice.csproj`: .NET 8 project configuration

## Contributing
Pull requests are welcome!

## License
TBD

