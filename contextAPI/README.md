# Context

Co ntext provides a way to pass data through the component tree without having to pass props down manually at every level.

In a typical React application, data is passed top-down (parent to child) via props, but such usage can be cumbersome for certain types of props (e.g. locale preference, UI theme) that are required by many components within an application. Context provides a way to share values like these between components without having to explicitly pass a prop through every level of the tree.

When to Use Context Before You Use Context API

React.createContext Context.Provider Class.contextType Context.Consumer Context.displayName Examples

# When to use /not use it

Things that belong in a context is data that is considered global like a user or a cart etc. So let’s try to list the different reasons for using a Context:

data needed in many places , data that needs to be used by many components like a theme, user or a cart
pass props through many components , sometimes it’s better to use composition over context when you want to pass a props value through many components
