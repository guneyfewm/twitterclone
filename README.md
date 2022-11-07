# React Twitter Clone
## Made With Redux Toolkit Bootstrap and React Router
## Preview
![twitter](https://user-images.githubusercontent.com/116850173/200340896-74105c2f-3d89-491a-84fc-dd1a0eb78cc5.gif)


## Sign Up Page
![image](https://user-images.githubusercontent.com/116850173/200341742-57a1eed4-83f0-4853-8e60-7aa498eee3c7.png)
All the values you type gets stored in local storage. You can either fill in the details or press continue witout signing up 
<br>
(if you don't sign up the application will store a default username and handle).

## Home
![image](https://user-images.githubusercontent.com/116850173/200343587-c2ce9ee5-e605-45da-af77-8c0ea696ee10.png)
You can upload images and text messages.
<br> When you click on the Tweet button it takes the refs values and uploads them into local storage using newPost() reducer from our "features/TwitterAppSlice" app slice.
<br>
<br>Down below we map our posts state to show our tweets using useSelector() and .map()<br> 
(Our "posts" state has an inital state of localstorage["Tweets"] so that when we refresh the page we don't lose our tweets)

## Explore
![image](https://user-images.githubusercontent.com/116850173/200345467-a4ccf90f-e179-4d71-adc0-bfc0cdd29115.png)

We have 6 different hashtags here each of them are different states and have different new post and delete post reducers.
And they get stored in different parts of local storage.

## Deleting a post
![image](https://user-images.githubusercontent.com/116850173/200346167-8e4a7778-fe8a-4f4f-8faf-48ded46fb6f0.png)
By clicking the X button you simply dispatch a deletePost() reducer and use the filter method on our state with the condition of post.id != action.payload
<br> This makes it so that whenever you click a delete button it sends the id of that post to the reducer function and returns the state without the post of that id

## Bookmarking
### Bookmark Button
![image](https://user-images.githubusercontent.com/116850173/200347781-cf781234-c20e-44f8-a1d5-70c4c37d8d84.png)
### Bookmark Page
![image](https://user-images.githubusercontent.com/116850173/200347213-2d491acb-56b2-466a-b2c8-c3ed0eb3f9c5.png)
You can bookmark tweets by clicking the pin button next to them. All the bookmarked tweets will be stored in localstorage and will be displayed in the bookmark page.
You can delete bookmarks by clicking the x button next to them.
## Profile Page
![image](https://user-images.githubusercontent.com/116850173/200348180-346b7ae5-ada7-4528-bc03-96033fde12dd.png)
You can change your username,handle and profile picture in this section.
<br> All of them will be stored in local storage aswell.
