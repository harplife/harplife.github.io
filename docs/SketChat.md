# Online Chat n Sketch

[Repository](https://github.com/harplife/sket-chat)

Web Application where users can join a public/private room to chat and sketch together.

## Design

picture here

## General Functions

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

## Detailed Functions

- [ ] Basic Drawing Tools and Functions (Shape, Size, Color)
  - [x] Toggle Erase (selectedColor, choiceColor, eraseColor)
- [ ] Initial Sketch Sync on join

## Thoughts, Notes, Issues

- Need to get a list of drawing tools (ellipses, rects, line, etc)
- I don't think server needs to be aware when changes are made, it only needs to emit the data the client sends. For example, when a user changes pen color, server doesn't need to be aware of the fact - it only emits what it receives. I can't yet have a clear idea of when the server should keep track of changes.
- Initial Sketch Sync may be more difficult than previously thought. It's easier with normal chat, since messages can be saved to DB and then called when a user joins. However, with sketch, saving all sketch actions and then calling it may be too much. But alas, we shall try.

## Reference

- Socket.io `.emit()` cheatsheet [link](https://socket.io/docs/v3/emit-cheatsheet/)
