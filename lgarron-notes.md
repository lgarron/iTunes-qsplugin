# iTunes-qsPlugin Notes

Lucas Garron
July 20, 2012

## Reveal in Playlist...
- We only care about a single song in the fist pane. Make sure sane behaviour (i.e. no crashing) happens for multiple songs or playlists in the first pane.
- Third pane should offer playlists containing the song in the first pane.
  - Right-arrowing could be conceivably be convenient, but it's probably better to disable that and only allow a list of playlists to be filtered. (Doesn't seem possible? The "Move To" action doesn't prevent the QS interface from letting you try to move into a file instead of a folder.)
  - The default selection in the third pane should be the playlist of the direct object, if there is one. It woul dbe nice if this were possible without rearranging the results (that way, playlists ni the third pane always appear in order).
- An action to get the playlists of a song in the first pane (there has to be a good name for this).
- Use song IDs when possible, since some titles are identical
- Resolve proxies
- It's possible to cache playlist contents, but that's undesirable because the contents could be changing quickly (also, unnecessary memory use).
- Is there a good way to handle multiple occurences of a song in a playlist?
- "Reveal Item" for a song navved in from a playlist should probably reveal in the playlist (same as playing).
- Application Action for "Reveal Currently Playing Song"
- Document new actions.
- Garbage collection?
- Reversed action: Playlist > Add Track...
- Feature: Drag-drop a song on a playlist selected in first pane to append.
- Bug: Enable/Disable tracks toggles each track in a playlist. If a track is in a playlist an even number of times, there is no net effect on it.
- If still using, scripting bridge, make sure to use playlist ID instead of name.
- Issue: "Reveal in Playlist" opens iTunes to find valid indirect objects.
- Alternate actions:
  - Play > Reveal (should reveal in playlist if navved from playlist)

- Song-Playlist combination that doesn't work (although it works with other playlists, including other smart playlists): Test Drive (Waltz v0.1) (Reveal in Playlist…)  Movie Music Playlist [First guess: Mismatch between iTunes' persistent ID for the playlist and the one stored in the catalog?]