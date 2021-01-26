# Projects

List of all personal projects

TODO: put this on my github [homepage](https://github.com/harplife/harplife.github.io). Personal projects as portfolio. TIL stuff should be on here too, maybe more as individual article.

## Online Chat n Sketch

[Repository](https://github.com/harplife/sket-chat)

Web Application where users can join a public/private room to chat and sketch together.

### Design

picture here

### General Functions

- [x] Web Server (w/ Node.js http)
- [x] Web Socket (w/ Socket.io)
- [x] Sketch (w/ p5.js)
- [x] Chat (w/ Socket.io)
- [ ] User Login (DB)
- [ ] User OAuth Login (Kakao, Naver, Google, etc.)
- [ ] Guest handling (Cookie, Session, Temporary sign-in)
- [ ] Rooms
- [ ] User Data Persistence
- [ ] Room Data Persistence
- [ ] Export Sketch

### Detailed Functions

- [ ] Basic Drawing Tools and Functions (Shape, Size, Color)
  - [x] Toggle Erase (selectedColor, choiceColor, eraseColor)
- [ ] Initial Sketch Sync on join

### Thoughts, Notes, Issues

- Need to get a list of drawing tools (ellipses, rects, line, etc)
- I don't think server needs to be aware when changes are made, it only needs to emit the data the client sends. For example, when a user changes pen color, server doesn't need to be aware of the fact - it only emits what it receives. I can't yet have a clear idea of when the server should keep track of changes.
- Initial Sketch Sync may be more difficult than previously thought. It's easier with normal chat, since messages can be saved to DB and then called when a user joins. However, with sketch, saving all sketch actions and then calling it may be too much. But alas, we shall try.

### Reference

- Socket.io `.emit()` cheatsheet [link](https://socket.io/docs/v3/emit-cheatsheet/)

## Image Manipulation on Multiple Images

[Repository](https://github.com/harplife/image_view)

Desktop Application where user can browse local images in a grid-like fashion, with a bit of image manipulation.

For example,

- user can select "grey" and all images will be shown in grey-scale.
- user can select "complementary" and all the images will be shown in colors that are complement to the original colors.
- blur
- rain drops
- sort by dominant color
- sort by aspect

### Functions

- [ ] Web Application (w/ Node.js http)
- [ ] Grid Layout
- [ ] Image Preload with Promise
- [ ] Image Manipulation
- [ ] Scroll & Load

### Thoughts, Notes, Issues

- I've tried two grid systems, and each of them have some kind of flaws.
- Loading all images at once causes issues.
- Scroll & Load seems to break one of the grid system. Perhaps it's best to query list of images, preload grid system with image size, and then load images with promise.

## Online Ear Training

Web Application where user can train their ears.

This is an imitation of Technical Ear Training class at Webster.

Trainee will try to find the difference between the original sound clip and the manipulated sound clip.

### Functions

- [ ] Web Application (w/ Node.js http)

## Online Recipe Keeping

Web Application where user can record and view their recipes.

This one's for Kaity.

We'll do this simply with Flask and SQLite, and make it distributable with PyInstaller.

### Functions

- [ ] Web Application (w/ Flask)

## Audio Data Analyzer

Web Application where a user can analyze a sound file.

Analyze sound file as whole, as clips, or as real-time.

### Functions

### Thoughts, Notes, Issues

- I need to look back on the elements of audio, and see what can be useful visual information.

## Audiovisual Representation

My dream project. Visualize music through art/or images.

### Functions

### Thoughts, Notes, Issues

- Once done, this will be implemented to the image viewer project.