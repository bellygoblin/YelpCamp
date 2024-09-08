# Udemy Course Project: Yelp Camp

## Domains Covered

- HTML
- CSS
- Javascript
- Node.js
- Express
- Mongoose
- EJS
- Mongodb

## Project Configuration Notes

1. Built a base Express App project using Node.js. Included EJS and Mongoose modules for page template rendering and Mongodb interfacing.
2. Set up a 'models' directory to build out Mongodb Schema

```javascript
const CampgroundSchema = new Schema({
  title: String,
  price: String,
  description: String,
  location: String,
});
```
