# Redwood JS Blog Example 1 - Part 2

The commands documented below came from the
[RedwoodJS Tutorial](https://redwoodjs.com/docs/tutorial/foreword)
webpage.

This repo contains the tutorial from chapter 5 to the afterword
and the forward to intermission is in
[redwood-blog-1](https://github.com/carltonj2000/redwood-blog-1)
repo.

```bash
git clone https://github.com/redwoodjs/redwood-tutorial
cd redwood-tutorial
yarn install
yarn rw prisma migrate dev
yarn rw dev
yarn rw storybook
yarn rw test
# creating comments
yarn rw g component Comment
yarn rw storybook
yarn rw test
yarn rw g cell Comments
# update schema.prisma
yarn rw prisma migrate dev
yarn rw g sdl Comment --no-crud
yarn rw console
```

Once in the javascript rw cli type the following:

```javascript
db.comment.findMany()
db.comment.findMany({ where: {postId: 1}})
db.comment.create({ data: { name: 'Peter', body: 'I also like leaving comments', postId: 2 } })
.exit
```
