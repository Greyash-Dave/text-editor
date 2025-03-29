
# Simple Rust Text Editor (Hecto Clone)

This is a practice project implementing a simple text editor in Rust, following the excellent Hecto tutorial by Philipp Flenker: [https://www.flenker.blog/hecto/](https://www.flenker.blog/hecto/).

## Features

* **File Handling:**
    * Create and open files.
    * Save files (`Ctrl+S`).
    * Save as functionality.
* **Basic Text Editing:**
    * Insert characters.
    * Delete characters.
    * Insert newlines.
    * move caret.
* **Terminal UI:**
    * Status bar displaying file information.
    * Message bar for user feedback.
    * Command bar for save as.
* **Quit Confirmation:**
    * Requires `Ctrl+Q` to be pressed three times if the file has unsaved changes.
* **Resize handling**

## Usage

1.  **Clone the repository:**

    ```bash
    git clone <repository_url>
    cd <repository_directory>
    ```

2.  **Build the project:**

    ```bash
    cargo build --release
    ```

3.  **Run the editor:**

    ```bash
    ./target/release/your_editor_name <filename>
    ```

    * Replace `<your_editor_name>` with the name of your executable.
    * replace `<filename>` with the name of the file you want to open or create.

## Key Bindings

* `Ctrl+S`: Save the current file.
* `Ctrl+Q`: Quit the editor (requires three presses if the file is modified).
* arrow keys: move the caret.
* Page up/down: move the view up and down a page.
* Home: move to start of line.
* End: move to end of line.

## Code Structure

The project is organized into the following modules:

* `editor`: Contains the main `Editor` struct and its logic.
* `command`: Defines the commands that the editor can handle.
* `commandbar`: implements command bar.
* `documentstatus`: Implements document status structure.
* `line`: Implements line structure.
* `messagebar`: Implements message bar.
* `position`: Defines the position struct.
* `size`: Defines the size struct.
* `statusbar`: Implements status bar.
* `terminal`: Handles terminal interactions using `crossterm`.
* `uicomponent`: defines the UIComponent trait.
* `view`: Manages the text view and scrolling.
* `buffer`: manages the document buffer.
* `fileinfo`: mananges file information.

## Dependencies

* `crossterm`: For terminal manipulation.

## Notes

* This is a practice project and may not have all the features of a full-fledged text editor.
* The project closely follows the Hecto tutorial, with some minor modifications.
* Error handling is basic.
* This editor is designed to be used in a terminal.
