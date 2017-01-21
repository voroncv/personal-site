<template>
   <div class="ui vertical stripe segment">
    <div class="ui text container">
    <h4 class="ui horizontal header divider"><a>Articles</a></h4>
      <div v-for="note in notes">
		<h3 class="ui header">{{ note.title }}</h3>
		<p>{{ note.little }} </p>
		<router-link class="ui large button" :to="note.link">Read More</router-link>
		<br /><br />
      </div>
    </div>
  </div>
</template>

<script>

import * as Firebase from "firebase";

let config = {
	apiKey: "AIzaSyDrloO354xkhHebheZIuPKsb5Y4t8XUjiQ",
    authDomain: "mysite-356cc.firebaseapp.com",
    databaseURL: "https://mysite-356cc.firebaseio.com",
    storageBucket: "mysite-356cc.appspot.com",
    messagingSenderId: "326201181084"
}

let app = Firebase.initializeApp(config);
let db = app.database();
let notesRef = db.ref('articles');

export default {
  name: 'list',
  firebase: {
  	notes: notesRef
  }
}
</script>