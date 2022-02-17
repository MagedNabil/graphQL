#
Authentication EndPoints
mutation register {
    createUser(userData: {
        username: "sleem",
        password: "1234545",
        firstName: "hamada",
        lastName: "sleem",
        age: 12
    }) {
        firstName
        lastName
        age
    }
}

mutation login {
    loginUser(username: "sleem", password: "1234545") {
        token
        error
    }
}


#
Posts EndPoints
mutation createPost {
    postCreate(token: "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiI2MjA5Y2ZkMzQyZTMxODcwZWMzMDczZDYiLCJpYXQiOjE2NDQ4MTAyMjV9.zLGXl7VrhKYtgmFVWXs7PxhFosKhyh3ccC-cDuU4O6k",
        content: "my Second Post")
}
mutation updateSinglePost {
    postUpdate(token: "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiI2MjA5Y2ZkMzQyZTMxODcwZWMzMDczZDYiLCJpYXQiOjE2NDQ4MTAyMjV9.zLGXl7VrhKYtgmFVWXs7PxhFosKhyh3ccC-cDuU4O6k",
        content: "new Post Content", postId: "620a6821eacf0f804b6f255d") {
        content
        user {
            firstName
            age
            lastName
        }
        error
    }
}
mutation deleteSinglePost {
    postDelete(token: "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiI2MjA5Y2ZkMzQyZTMxODcwZWMzMDczZDYiLCJpYXQiOjE2NDQ4MTAyMjV9.zLGXl7VrhKYtgmFVWXs7PxhFosKhyh3ccC-cDuU4O6k",
        postId: "620a6821eacf0f804b6f255dx")
}
query getMyPosts {
    getMyPosts(token: "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiI2MjA5Y2ZkMzQyZTMxODcwZWMzMDczZDYiLCJpYXQiOjE2NDQ4MTAyMjV9.zLGXl7VrhKYtgmFVWXs7PxhFosKhyh3ccC-cDuU4O6k") {
        content
        user {
            age
        }

    }
}
query getAllPosts {
    getAllPosts {
        content
        user {
            firstName
            lastName
            age
        }
        comments {
            content
        }
    }
}#
Comments
mutation createComment {
    commentCreate(token: "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiI2MjA5Y2ZkMzQyZTMxODcwZWMzMDczZDYiLCJpYXQiOjE2NDQ4MTAyMjV9.zLGXl7VrhKYtgmFVWXs7PxhFosKhyh3ccC-cDuU4O6k", postId: "620a6f525472f96c096d97c7", content: "Second Post Comment")
}
query getAllCommentsForPost {
    getPostComments(postId: "620a6f525472f96c096d97c7x") {
        error
        content
    }
}