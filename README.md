TRPG_Keeper

User create log to share TRPG game experience or some information since it might need long waiting before the next part of the game to happen.

Process:
1. Use or start new game title
2. Use or start new avatar
3. Post text on the main section under the title with avatar’s name and user’s id
4. If current title is comment-friendly, there will be a section for the uses to discuss



User Schema:{
    Id (primary key): number
    Password: string
    AvatarsId[]: number[]
}

Avatar Schema{
    Id (primary key): number
    Name: string
    User: number
    Description: string
    TitlesId: number[]
    PostsId: number[]
}

Post Schema{
    Id (primary key): number
    TitleId: number
    Author: number (userid)
    Text: string
    isComment: boolean
}


Title Schema{
    Id (primary key): number
    Name (unique): string
    AvatarsId: number[]
    PostsId: number[]
    commentFriendly: boolean
}
