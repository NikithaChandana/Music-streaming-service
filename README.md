# Database Management System for Music Streaming Service

## Project Overview
This project aims to design and implement a **Database Management System (DBMS) for a Music Streaming Service**. The system efficiently manages user profiles, tracks, streaming history, and payment transactions while enabling robust data analysis for business and user insights.

## Team Members:
- Nikitha Chandana 
- Prathyusha Murala 
- Shashank Guda 
- Vishnu Charugundla

## Problem Statement
Our goal is to develop a scalable and efficient DBMS that addresses the following challenges:
1. **User Data Management**: Handling millions of users, including profile management, authentication, and subscription tracking.
2. **Track Data Management**: Storing metadata for millions of tracks, including artist, album, genre, popularity, and streaming statistics.
3. **Streaming History**: Recording user listening history to analyze trends and user behavior.
4. **Payments/Transactions**: Tracking subscription payments, renewals, and customer retention patterns.

## Proposed Solution
To address these challenges, we propose the following:

### **User Profile Management**
- Users table to store usernames, emails, hashed passwords, and subscription details.
- Secure authentication for user login and registration.

### **Track Data Management**
- **Tracks Table**: Stores metadata (title, artist, album, genre, release date, duration, popularity, streaming statistics).
- **Albums and Artists Tables**: Maintains relationships between albums, artists, and tracks.
- **Genres Table**: Classifies tracks by genre.

### **Streaming History**
- **User Activities Table**: Logs user actions, including session times and activity timestamps.
- **Listening History Table**: Tracks the history of songs listened to by each user.

### **Payments/Transactions**
- **Subscriptions Table**: Stores user subscription details, including type, renewal dates, and payment history.
- **Transactions Table**: Records payment transactions, timestamps, amounts, and statuses.

## **Database Schema (Key Entities & Attributes)**

### **Users Table**
- UserID (Primary Key)
- Full Name
- Username
- Email
- Password (Hashed & Salted)
- Date of Birth
- State (Assumption: All users are US-based)
- Subscription Type

### **Tracks Table**
- TrackID (Primary Key)
- ArtistID (Foreign Key)
- AlbumID (Foreign Key)
- GenreID (Foreign Key)
- Title
- Duration
- Release Date
- Genre
- Language

### **Albums Table**
- AlbumID (Primary Key)
- Title
- Release Date
- ArtistID (Foreign Key)

### **Artists Table**
- ArtistID (Primary Key)
- Artist Name
- Full Name
- Country

### **Genre Table**
- GenreID (Primary Key)
- Genre Name
- Description

### **User Activity Table**
- ListeningID (Primary Key)
- UserID (Foreign Key)
- TrackID (Foreign Key)
- AlbumID (Foreign Key)
- SessionID
- Session Duration
- Session_Start_Timestamp
- Session_End_Timestamp

## **Business & Data Analytics (Work in Progress)**

### **User Insights**
- Identify top **tracks, artists, albums, genres, and languages** based on a given frequency (daily, weekly, monthly, yearly).
- Analyze **app usage time** based on streaming history.

### **Artist Insights**
- Determine popular **tracks, albums, and genres** based on state-wise user data.
- Analyze **user demographics (age, gender, location)** for targeted marketing.
- Identify **optimal times to release new tracks/albums** based on peak user activity.

### **Business Insights**
- Identify **top artists** in a given state to assess market value for sponsorship deals.
- Determine **user conversion rates** and analyze patterns of subscription renewals and cancellations.

## **Assumptions**
- If a user starts a song, they listen to it entirely.
- All users are located in the US.

## **Future Enhancements**
- Implement AI-driven **recommendation algorithms** for personalized music suggestions.
- Expand the database to support **multi-country users and localized music content**.
- Integrate real-time **user engagement tracking** to improve music recommendations.

## **Conclusion**
This DBMS serves as the foundation for a scalable music streaming service, providing structured data management for users, artists, and stakeholders. The system ensures data integrity, user privacy, and valuable business insights through analytical tools and predictive modeling.
