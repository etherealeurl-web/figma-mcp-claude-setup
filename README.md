# 🎨 Figma MCP Claude Setup

Configuration guide and automation scripts for connecting Figma MCP server to Claude Code and generating code from Figma designs.

## 📋 Overview

This repository contains everything you need to connect Figma to Claude Code via the **Model Context Protocol (MCP)**, enabling you to generate code directly from your Figma designs.

## ✨ Features

✓ Generate code from selected Figma frames  
✓ Extract design context (variables, components, layout)  
✓ Retrieve Make resources  
✓ Keep design system components consistent  
✓ No desktop app installation required (remote server)  

## 🚀 Quick Start for Claude Code

### Step 1: Add Figma MCP Server

Open your terminal and run:

```bash
claude mcp add --transport http figma https://mcp.figma.com/mcp
```

### Step 2: Access MCP Management in Claude

In Claude Code, type:

```
/mcp
```

### Step 3: Select and Authenticate Figma

- Select `figma` from the list
- - Choose `Authenticate`
  - - Click "Allow Access" to authorize Figma integration
   
    - ### Step 4: Verify Connection
   
    - Type `/mcp` again and you should see:
   
    - ```
      Authentication successful. Connected to figma
      ```

      ## 📱 Alternative Setup for Other Editors

      ### VS Code Setup

      1. Use shortcut `⌘ Shift P` then select:
      2.    - `MCP: Open User Configuration` (for global access)
            -    - OR `MCP: Open Workspace Folder MCP Configuration` (for this workspace only)
             
                 - 2. Paste configuration in `mcp.json`:
                  
                   3. ```json
                      {
                        "inputs": [],
                        "servers": {
                          "figma": {
                            "url": "https://mcp.figma.com/mcp",
                            "type": "http"
                          }
                        }
                      }
                      ```

                      3. Click "Start" and "Allow Access"
                     
                      4. ### Cursor Setup
                     
                      5. 1. Click the Figma MCP server deep link
                         2. 2. Click "Install"
                            3. 3. Click "Connect" to begin authentication
                              
                               4. ## 🔧 Configuration Files
                              
                               5. - **Global config**: `~/.claude.json`
                                  - - **Project config**: `/Users/[username]/Documents/MCP/Claude/.mcp.json`
                                   
                                    - ## 💡 How to Use
                                   
                                    - 1. **Copy your Figma design link** from a frame or layer
                                      2. 2. **In Claude Code**, describe what you want: "Generate code for this design" + paste the Figma URL
                                         3. 3. Claude extracts the node-id and provides design context automatically
                                           
                                            4. ## 📚 Resources
                                           
                                            5. - [Figma MCP Server Documentation](https://developers.figma.com/docs/figma-mcp-server/)
                                               - - [Model Context Protocol](https://modelcontextprotocol.io/)
                                                 - - [Claude Documentation](https://claude.ai/docs)
                                                  
                                                   - ## ⚙️ MCP Capabilities
                                                  
                                                   - With the Figma MCP server enabled, you can:
                                                  
                                                   - - **Generate code from selected frames**: Select a Figma frame and turn it into code
                                                     - - **Extract design context**: Pull in variables, components, and layout data directly
                                                       - - **Retrieve Make resources**: Gather code resources from Make files
                                                         - - **Code Connect integration**: Keep your generated code consistent with your codebase
                                                          
                                                           - ## 🔐 Authentication
                                                          
                                                           - The remote server requires OAuth authentication through Figma. Once set up, you get seamless access to your Figma data without needing to install Figma's desktop app.
                                                          
                                                           - ## 📝 Best Practices
                                                          
                                                           - 1. **Structure your Figma file logically** with clear component organization
                                                             2. 2. **Use descriptive frame names** for better code generation
                                                                3. 3. **Write detailed prompts** to guide the AI generation
                                                                   4. 4. **Set up custom rules** for consistent output
                                                                     
                                                                      5. ## 🐛 Troubleshooting
                                                                     
                                                                      6. ### Connection Issues
                                                                     
                                                                      7. If connection fails, verify:
                                                                      8. - Claude Code is up to date
                                                                         - - Figma authentication is complete
                                                                           - - Your Figma account has proper permissions
                                                                            
                                                                             - ### MCP Not Found
                                                                            
                                                                             - Ensure you've:
                                                                             - - Installed Claude Code CLI tools
                                                                               - - Run the `claude mcp add` command
                                                                                 - - Restarted Claude Code after setup
                                                                                  
                                                                                   - ## 📄 License
                                                                                  
                                                                                   - MIT License - Feel free to use and modify
                                                                                  
                                                                                   - ## 🤝 Contributing
                                                                                  
                                                                                   - Contributions welcome! Please feel free to submit issues and pull requests.
                                                                                  
                                                                                   - ---

                                                                                   **Setup Time**: ~2 minutes
                                                                                   **No installation required**: Uses remote server
                                                                                   **Full integration**: Works seamlessly with Claude Code
