# LoadRunner VuGen Project Analysis

## Project Summary
This repository contains a **Micro Focus LoadRunner VuGen (Virtual User Generator)** script template for web performance testing. It represents a foundational structure for HTTP/HTML protocol testing scripts.

## Technical Details

### Project Type
- **Tool**: LoadRunner VuGen 2023.1
- **Protocol**: Web - HTTP/HTML
- **Language**: C
- **Locale**: English (India)

### Architecture Pattern
The project follows LoadRunner's standard **three-phase execution model**:

1. **vuser_init.c**: Initialization phase (executed once per virtual user)
2. **Action.c**: Main action phase (executed repeatedly based on iteration settings)  
3. **vuser_end.c**: Cleanup phase (executed once per virtual user)

### Key Components

#### Core Script Files
- `Action.c` - Contains the main business logic transactions
- `vuser_init.c` - Handles setup, authentication, and initialization
- `vuser_end.c` - Performs cleanup and logout operations
- `globals.h` - Global variables and API includes

#### Configuration Files
- `default.cfg` - Runtime settings (iterations, think time, logging)
- `default.usp` - User script properties and run logic definition
- `mWebHttpHtml2.usr` - Script metadata and project settings

#### VuGen Metadata
- `ScriptUploadMetadata.xml` - VuGen project structure definition
- `Bookmarks.xml` - Development bookmarks (empty)
- `Breakpoints.xml` - Debug breakpoints (empty)
- `UserTasks.xml` - User task definitions

#### Custom Components
- `lrw_custom_body.h` - Custom HTTP request body sections
- `custom_body_variables.txt` - Documentation for body variables

### Current State
- **Template Status**: Basic/empty template
- **Implementation**: All functions contain only `return 0;` statements
- **Ready for**: Extension with actual web requests and business logic

### Configuration Highlights
- **Iterations**: 1 (single run)
- **Think Time**: Disabled (NOTHINK)
- **Transactions**: Automatic transaction handling enabled
- **Logging**: Brief logging enabled
- **Web Recorder**: Version 8
- **Connection Pool**: Unlimited connections

### Use Cases
This template is suitable for:
- Web application performance testing
- HTTP/HTTPS API testing
- Load testing scenarios
- Stress testing web services
- Performance regression testing

### Extension Points
To make this functional, developers would typically:
1. Add web_url() or web_custom_request() calls in Action.c
2. Implement authentication logic in vuser_init.c
3. Add parameterization for test data variation
4. Configure correlation for dynamic values
5. Add transaction boundaries for performance measurement
6. Implement proper error handling and validation

### Development Environment
- Compatible with LoadRunner VuGen 2023.1 and later
- Requires LoadRunner development license
- Can be executed on LoadRunner Controller for load testing
- Supports integration with LoadRunner Analysis for results analysis

This structure provides a solid foundation for building comprehensive web performance testing scenarios while following LoadRunner best practices and conventions.