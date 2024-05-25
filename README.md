# This is where we start documenting

### MAY 24

#### WE learn about the use of module bundler (webpack),Let's setup webpack

- npm init -y
- npm install webpack webpack-cli --save-dev
- npm install --save lodash

Those are need to preinstall before working any futher

- import every file to index.js file (like other js file , css file , image, text ,svg)
- npx webpack ( to execute / run )
- create webpack.config.js file
  - ADD this in webpack.config.js
[
const path = require('path');

module.exports = {
entry: './src/index.js',
output: {
filename: 'main.js',
path: path.resolve(\_\_dirname, 'dist'),
},
};
]

- npx webpack --config webpack.config.js
- add this in package.json { "build": "webpack" }
- npm run build to make bundle insted of using npx webpack --config

#### Configuring for adding style and image to bundler

- npm install --save-dev css-loader ts-loader

- add webpack.config.js "

      module.exports = {module: {
      rules: [
       {
      test: /\.css$/,
       use: [
      { loader: 'style-loader' },
       {
      loader: 'css-loader',
     options: {
      modules: true,
     },
      },
     { loader: 'sass-loader' },

             {
                  test: /\.(png|svg|jpg|jpeg|gif)$/i,
                  type:'asset/resource',
                },

          ],
        },
      ],

  },
  };

"
