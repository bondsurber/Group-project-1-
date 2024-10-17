# Mist 4610 Group Project 1
## GROUP 1: Spotify Database

## Team Name: 
4610Fa24Group1 

## Team Members:

1. Louis Miranda [@louismiranda](https://github.com/louismiranda)
2. Bond Surber [@bondsurber](https://www.github.com/bondsurber)
3. Sidd Kawatra [@](https://www.github.com/RileyDoggett)

## Problem Description:

The task at hand is to model and build a relational database for the digital music streaming platform: Spotify. Spotify offers a few subscription plans for its users, millions of songs from different artists, and curated playlists made by either users or Spotify-themselves; therefore, the main entities in the model are SubscriptionPlan, User, Playlist, Song, Artist, and Advertisement. We are interested in accurately modeling these relationships, generating sample data, and populating the entities and their attributes with this sample data. Furthermore, we are interested in performing functioning queries on this data so that they may provide us with valuable business insight into both users and artists who utilize the platform, and the playlists and ads that Spotify operates. 

## Data Model

Explanation of data model: 

Our model is based on the structure of Spotify. The 'SubscriptionPlan' entity is representative of the select number of premium plans (Individual Premium, Family Premium, Student Premium, or Free) that Spotify offers for its users; this table tracks the type of subscription plan and their respective prices. Within each subscription plan, there are many users, and this is represented by the one-to-many relationship we have placed between the 'SubscriptionPlan' and 'User' entities. 

The 'User' entity keeps track of a Spotify user's username, age, country, and more. This entity branches off into 2 relationships: a one-to-many relationship with the 'Playlist' entity and a many-to-many relationship with the 'Song' entity. The one-to-many relationship with 'Playlist' showcases how Spotify users can have many playlists. (The many-to-many relationship between 'User' and 'Song' will be explained further down below) 

The 'Playlist' entity keeps track of a playlist's name and creation date, and whether it was created by Spotify or a user. Each playlist on Spotify can have many songs, and each song can be on several playlists, which is represented through the many-to-many relationship we placed between the 'Playlist' and 'Song' entities.

The 'Song' entity can be thought of as the core of our data model because it includes 4 many-to-many relationships between the 'User', 'Playlist', 'Artist', and 'Advertisement' entities. In Spotify, users can interact with many songs through several means, such as liking or sharing a song, and each song can have many of these interactions with different users, which is represented through the many-to-many relationship that 'User' has with 'Song', as previously mentioned. 

