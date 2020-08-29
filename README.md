# Why not use create-react-app?

When it comes to creating React projects, most people very naturally reach for create-react-app. There's nothing wrong with that. create-react-app is very handy and I use it often when I just need a React project and don't really care how many dependencies it installs. But, at times, I need something minimal. At those times I don't need the App.test.js file or the image assets.

For such situations, I find create-react-app unnecessary. Creating a project and setting it up yourself gives you more control over its dependencies.

# Webpack alternative

I thought of reading the Webpack documentation and manually setting up a React project. But looking at the Webpack docs, it seemed it would take some time before I can understand how to set everything up. That's when I came across Parcel js. It's supposed to be zero-config and easy to get started with.

I tried it and it was quick work. Creating a project and installing dependencies to looking at the result on localhost - took just 5 steps.

# 1. Create a project

The first step is to create a project. Go to your console or command line and create a new directory and cd into that directory.
We need a package.json file before we can install any dependencies. Let's create that as well.
The -y flag will answer yes to all questions and create a package.json file with the default options. Now we can install our dependencies.

# 2. Install dependencies

We are going to need Parcel js and Babel plugins as dev dependencies along with React packages.
These are all the dependencies we need to get started with a React project.

# 3. Babel config and scripts

Those babel plugins will need to be added in a .babelrc.json file. Babel explains very well the difference between .babelrc.json, babel.rc and when to use either of them.

At this stage, your folder structure should look something like this.
I've already added the babel config file and added the presets.
Next, we need to add a start script in package.json.
We need to tell Parcel the file it would need to render. The --open flag tells Parcel to open localhost in the default browser on your system. If you don't need Parcel to do this, leave this flag out. You can still open localhost:1234 in your browser of choice. The default port Parcel uses is 1234.

# 4. Write code

Although we created the start script, we don't have an HTML file nor have we written any React code. Let's do that now. First we will create the HTML file, write some React code in App.js and then render the component to the DOM in the entry file index.js.
Here is a look at the folder structure after adding the code files. Except the HTML file, I kept the other code files in the src folder:

# 5. Start Parcel

We already wrote the start script in the second step. Let's run the project.
If you put the --open flag in the start script, then it should have opened in the default browser for your system. Otherwise, just open a browser of your choice and go to localhost:1234.

# Wrapping up

Even without create-react-app or the Parcel equivalent, create-react-app-parcel, you can make a minimal React app. If your project needs more complexity, more libraries, or a different folder structure, you can add that to the existing code.

If you've always used Webpack, give Parcel a try. It is super quick to set up and doesn't need many configurations.
