<template>
   <div class="ui vertical stripe segment">
    <div class="ui text container">
      <div v-for="note in notes">
		<h3 class="ui header">{{ note.title }}</h3>
		<p>{{ note.full }} </p>
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

let app = Firebase.initializeApp(config, "detail");
let db = app.database();
let notesRef = db.ref('articles');

export default {
  name: 'list',
  firebase() {
  	return { notes: notesRef.orderByChild("link").equalTo(this.$route.params.id) }
  }
}
</script>