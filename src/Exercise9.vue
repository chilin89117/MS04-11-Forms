<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
        <form v-if="!submitted">
          <appNames v-model.lazy="user.names"></appNames>

          <div class="form-group">
            <label for="email">Email:</label>
            <input type="email" id="email" class="form-control" v-model.lazy="user.email">
          </div>

          <div class="form-group">
            <label for="pwd">Password:</label>
            <input type="password" id="pwd" class="form-control" v-model.lazy="user.password">
          </div>

          <div class="form-group">
            <label for="radios">Save to Database?</label>
            <div id="radios" class="form-control">
              <label for="rdyes">
                <input type="radio" id="rdyes" value="true" v-model="saveToDB">&nbsp;Yes&nbsp;&nbsp;&nbsp;&nbsp;
              </label>
              <label for="rdno">
                <input type="radio" id="rdno" value="false" v-model="saveToDB">&nbsp;No
              </label>
            </div>
          </div>

          <button class="btn btn-success" @click.prevent="submitted=true">Submit</button>
        </form>
      </div>
    </div>
    <hr>

    <div class="row">
      <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
        <div class="panel panel-primary" v-if="submitted">
          <div class="panel-heading">Your Data</div>
          <div class="panel-body">
            <p>Full Name: {{user.names.fname + ' ' + user.names.lname}}</p>
            <p>Email: {{user.email}}</p>
            <p>Password: {{user.password}}</p>
            <p>Store in Database?: {{saveToDB}}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import Names from './Names.vue'

  export default {
    data() {
      return {
        user: {
          names: {
            fname: '',
            lname: '',
          },
          email: '',
          password: '',
        },
        saveToDB: false,
        submitted: false,
      };
    },
    components: {
      appNames: Names,
    },
  };
</script>
