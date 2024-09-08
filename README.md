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
const CampgroundSchema = new mongoose.Schema({
  title: String,
  price: String,
  description: String,
  location: String,
});
```

3. Create seed data to test with Mongodb. Use information from external files and loop through them to create Sample data.

```javascript
const sample = (array) => {
  return array[Math.floor(Math.random() * array.length)];
};

const seedDB = async () => {
  await Campground.deleteMany({});
  for (let i = 0; i < 50; i++) {
    const random1000 = Math.floor(Math.random() * 1000);
    const camp = new Campground({
      title: `${sample(descriptors)} ${sample(places)}`,
      location: `${cities[random1000].city}, ${cities[random1000].state}`,
    });
    await camp.save();
  }
};
```
