# Changelog

## 0.3.0 - 2024-07-03

### Changes

- Vector Database backend now uses OpenSearch instead of Milvus. This will give us many more options with managing metadata from the ingested documents as well as strong RBAC features.
- install scripts should be a little more intuitive to use now.
- Loader page has been merged into Collection Management.
- The production version of Concierge now runs entirely in Docker, this should limit the number of issues relating to Python configurations.
- The user no longer needs to download the repository from GitHub to install Concierge, it is now done via the PyPI package manager.
- Default port set to 15130

### Added

- `delete_index` command
- `documents` command
- `list_indices` command
- `delete_document` command
- Ability to view documents in collection
- Ability to delete documents from collection
- Ability to set web app port in environment variables

## 0.2.0 - 2024-05-15

### Changes

- Web GUI ported from Streamlit to Shiny for Python: we have found Shiny to be much more robust, especially with handling long tasks such as ingesting documents.
- `launch.py` and `install.py` improved to (hopefully) work on more Operating Systems.

### Added

- Theme selector for Web GUI

## 0.1.3 - 2024-03-14

### Added

- `launch.py` script to make starting Concierge simpler.
- Collaborator Guide to clarify our internal policy on handling branches and versioning.

## 0.1.0 2024-03-06

Initial Data Concierge MVP release for public testing.

### Features

- `install.py` helper to ensure correct configuration
- Ability to ingest PDF documents and web pages into a Milvus vector database
- Ability to retrieve documents from the database that match the user's prompt
- Ability to answer the user's prompt using the retrieved documents as the context and Ollama to generate the response
- Streamlit powered Web UI
- CLI scripts also available


