# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is "Gourmet-Genie", a single-page web application that helps users create refined, gourmet recipes from available ingredients. The entire application is contained in a single HTML file with embedded CSS and JavaScript.

## Architecture

### Single-File Structure
- **index.html**: Contains the complete application (HTML markup, CSS styles, JavaScript logic)
- **prompt.md**: Contains the original German requirements/specification for the application

### Core Components

The application is built around the `GourmetGenie` JavaScript class (`index.html:644-996`) with these main responsibilities:

1. **API Key Management** (`index.html:658-707`): Extracts DeepSeek API key from URL parameters and manages authentication status
2. **Recipe Generation** (`index.html:713-772`): Creates prompts and calls the DeepSeek API to generate gourmet recipes
3. **UI Management** (`index.html:811-990`): Handles displaying recipe cards, detailed views, and loading states

### Key Features

- **Ingredient Input**: Users enter available ingredients in a textarea
- **Recipe Suggestions**: Generates 3 gourmet recipe suggestions using DeepSeek AI
- **Recipe Details**: Shows full recipe with ingredients, steps, cooking tips, and shopping list for missing ingredients
- **Responsive Design**: Apple-inspired UI that works on desktop and mobile

## Development Commands

Since this is a single HTML file application, there are no build commands, test runners, or package managers. Development is straightforward:

1. **Run locally**: Open `index.html` in a web browser
2. **Test with API**: Add `?apikey=your-deepseek-api-key` to the URL
3. **No build process**: All code is self-contained in the HTML file

## API Integration

The app integrates with DeepSeek's chat completion API:
- **Endpoint**: `https://api.deepseek.com/v1/chat/completions`
- **Model**: `deepseek-chat`
- **Authentication**: Bearer token via API key URL parameter
- **Response handling**: Parses JSON recipe data from AI responses (`index.html:774-809`)

## UI Architecture

The interface uses a card-based layout with these main sections:
- **Header**: App branding and tagline
- **API Status**: Shows API key status and setup instructions
- **Ingredients Input**: Textarea for user ingredient entry
- **Recipe Grid**: Displays generated recipe suggestions
- **Recipe Detail**: Full recipe view with ingredients, steps, and tips

The styling follows Apple's design language with glassmorphism effects, smooth animations, and a clean color palette.

## File Structure Note

This is intentionally a single-file application for easy deployment and sharing. All dependencies (CSS animations, JavaScript logic, API calls) are self-contained within `index.html`.