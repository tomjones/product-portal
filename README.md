# Product Portal

Single page inventory manager for client seeking a solution to manage their warehouse organization. 

Current functionality: 
* check in a product with name, lot number, weight (kg), and shelf location
* update product warehouse shelf location
* check out product 
* get a generated barcode and print for product


## Deployment

To deploy this project run these commands at the top level:

```bash
  bundle istall
  rails db:migrate
  rails db:seed
```
Run these commands at the client folder level:
```bash
  npm install
```
Once you have downloaded all the necessary gems and packages, at the top level run this command to start server:
```bash
  rails s
```
Then run this command at the client folder level:
```bash
  npm start
```
There is a Procfile included with this project to run the backend and frontend simultaneously once all packages and gems have been installed: 
```bash
  foreman start -f Procfile.dev
```


## Demo

[Video](https://youtu.be/pe7siYFoc2w)


## Included Libraries

 - [Serializer](https://github.com/rails-api/active_model_serializers)
 - [Bootstrap for React](https://react-bootstrap.github.io/)
 - [DataTable from react-data-table-component](https://www.npmjs.com/package/react-data-table-component)
 - [Barcode from react-barcode](https://www.npmjs.com/package/react-barcode)
 - [useReactToPrint from react-to-print](https://www.npmjs.com/package/react-to-print)
 - [icons from FontAwesome](https://fontawesome.com/icons)


sudo service postgresql start

step by step, i hope this makes sense bc i am finishing up my lunch break now!
add the new object with part number and description to unileverPartNumbers array in client/src/products_table.js
delete the files that are currently in the public folder (should include a folder called static and some pngs and a few other files)
in terminal cd into the client folder. from the terminal in the client folder, run command npm run build which will dump the compiled code into client/build folder
move the content of the client/build folder to the public folder
cd out of the client folder and back to the top level of the application. run rails s in the terminal, this starts up the rails server using the generated code from the public folder and you should be able to see your changes live
should be good to deploy!