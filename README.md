# Playlist Management System

This C++ program provides a simple command-line interface to manage a playlist. You can add, delete, display songs, save the playlist to a file, and load the playlist from a file.

## Features

- **Add a Song**: Add a new song to the playlist.
- **Delete a Song**: Remove a song from the playlist by its serial number.
- **Delete Playlist**: Remove all songs from the playlist.
- **Display Playlist**: Show the current playlist with song indices.
- **Save to File**: Save the playlist to a file.
- **Load from File**: Load songs from a file into the playlist.

## Classes

### `Player`
Represents a single song in the playlist, with pointers to previous and next songs.

#### Attributes:
- `int ind`: Serial number of the song.
- `string song`: Name of the song.
- `Player* prev`: Pointer to the previous song.
- `Player* next`: Pointer to the next song.

### `Playlist`
Manages the list of `Player` objects, providing functionalities to manipulate and display the playlist.

#### Methods:
- `int getNum() const`: Returns the number of songs in the playlist.
- `Player* getHead() const`: Returns the head (first song) of the playlist.
- `void addSong(const string& newSong)`: Adds a new song to the playlist.
- `void deleteSong(int n)`: Deletes a song at the specified index.
- `void deletePlaylist()`: Deletes all songs in the playlist.
- `int displayPlaylist()`: Displays the entire playlist.
- `void saveToFile(const string& filename)`: Saves the playlist to a file.
- `void loadFromFile(const string& filename)`: Loads songs from a file into the playlist.

## Compilation

To compile the program, use a C++ compiler like `g++`:

```bash
g++ -o playlist_manager main.cpp
