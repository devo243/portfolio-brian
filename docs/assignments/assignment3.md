---
title: Assignment 3
layout: doc
---

# Assignment 3

## Pitch

artBook is a social media dedicated for fans of any topic (games, TV Series, Books, Youtubers, Streamers, etc.) that want to share their own fanart or drawings about the topic and check out new content related to it. Compared to other social media, either the content is image-based but it is hard to compile all the art of a specific topic, or the content is specific to the topic, but art is not the main type of content and such it is not as prioritized.

Thus, artBook is designed to give easier access to fanart content, by creating communities that gather such content in one place and the content itself is only image-based. artBook achieves this goal by the concept of Community where content is aggregated through these communities and not through a global feed. In addition, through Image Posting the only content that is shown to users is in image form and so fanart/drawings are prioritized in this medium. Hence, artBook is determined to be a simple, quick, and easy way to engage and share fanart content to the fans.

---

## Concepts

#### Community[User, Item]

**Purpose**

Users can join groups dedicated to a certain topic

**Operation Principle**

A user joins a community to check out items related to a certain topic made by other users, and add their own items.

**State**

    community: One ID
    title: community -> One String
    description: community -> One String
    numMembers: community -> One Integer
    items: community -> Set Items
    members: community -> Set Users

**Actions**

    join(member: User, community: ID):
        if member not in community.members:
            community.members += member
            community.numMembers += 1

    leave(member: User, community: ID):
        if member in community.members:
            community.members -= member
            community.numMembers -= 1

    addItem(item: Item, community: ID):
        community.items += item
    
    deleteItem(item: Item, community: ID):
        if item in community.items:
            community.items -= item

    lookItems(community: ID, out items: Items):
        return community.items

#### Image Posting[User, Image]

**Purpose**

Users can post images for other users

**Operation Principle**

An user makes a post and other users see the post

**State**

    posts: Set IDs
    content: posts -> One Image
    creator: posts -> One User

**Actions**

    addPost(im: Image, creator: User)
        create new post:= new ID
        posts += post
        post.content := im
        post.creator := creator

    deletePost(post:ID)
        posts -= post
        post.content := None
        post.creator := None

#### Favoriting[Item, User]

**Purpose**

Gives the user a way to express support for an item they liked and saved the item

**Operation Principle**

A user sees an item that they like and so they favorite the item to save it in the platform

**State**

    numFavorites: Item -> One Integer
    favorites: user -> set Items

**Actions**

    favorite(user: User, item: Item):
        item.numFavorites += 1
        user.favorites += item

    unfavorite(user: User, item: Item):
        if item in user.favorites:
            user.favorites -= item
            item.numFavorites -= 1

#### Featuring[Item]

**Purpose**

To promote a certain item to multiple users so more users see the item

**Operation Principle**

After an item has gained enough attention from some users, it gets promoted to other users to see

**State**

    attention: One Integer
    promoted: Set Items
    minimumAttention: One Integer

**Actions**

    promote(item: Item, promoted: Items, attention: Integer, out featured: Items):
        if item not in promoted:
            if attention >= minimumAttention:
                promoted += item
        
        return featured
    
    depromote(item: Item, promoted: Items, attention: Integer, out featured: Items):
        if item in promoted:
            if attention < minimumAttention:
                promoted -= item

        return featured

#### Sessioning[User]

**Purpose**

To initiate a session in the platform

**Operation Principle**

A user starts a session in the platform and can interact with the platform

**State**

    session: One User
    active: user -> One Boolean

**Action**

    startSession(user: User, out session: User):
        user.active := True
        return user

    endSession():
        if user.active:
            user.active := False

#### Authenticating[User]

**Purpose**

To authenticate that the person is in fact a corresponding user in the platform

**Operation Principle**

A person gives a password and a name to get access to a user in the platform with the same name and password

**State**

    users: Set Users
    name: user -> One String
    password: user -> One String

**Actions**

    authenticate(name: String, password: String, out user: User):
        for user in users:
            if user.name == name and user.password == password:
                return user

    register(name: String, password: String):
        if name not in user.name for all user in users:
            user := new User
            user.name := name
            user.password := password
            users += user

---

## Synchronizations

---

## Wireframe

---

## Tradeoffs








