<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
        <form>
          <h1>File a Complaint</h1>
          <hr>
          <div class="form-group">
            <label for="email">Email</label>
            <input type="text" id="email" class="form-control" v-model="email" autofocus>
          </div>

          <div class="form-group">
            <label for="password">Password</label>
            <input type="password" id="password" class="form-control">
          </div>

          <div class="form-group">
            <label for="age">Age</label>
            <input type="number"
                   id="age"
                  class="form-control">
          </div>

          <div class="form-group">
            <label for="message">Message</label>
            <!-- Interpolation between <textarea>{{ test }}</textarea> doesn't work!-->
            <textarea id="message"
                      rows="5"
                      class="form-control"></textarea>
          </div>

          <div class="checkbox">
            <label for="sendmail">
              <input type="checkbox"
                     id="sendmail"
                     value="SendMail"> Send Mail
            </label>
            <label for="sendInfomail">
              <input type="checkbox"
                     id="sendInfomail"
                     value="SendInfoMail"> Send Infomail
            </label>
          </div>

          <div class="radio">
            <label for="male">
              <input type="radio"
                     id="male"
                     value="Male"> Male
            </label>
            <label for="female">
              <input type="radio"
                     id="female"
                     value="Female"> Female
            </label>
          </div>

          <div class="form-group">
            <label for="priority">Priority</label>
            <select id="priority"
                    class="form-control">
              <option></option>
            </select>
          </div>
          <hr>

          <button class="btn btn-primary">Submit</button>
        </form>
      </div>
    </div>
    <hr>

    <div class="row">
      <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
        <div class="panel panel-default">
          <div class="panel-heading">
            <h4>Your Data</h4>
          </div>
          <div class="panel-body">
            <p>Email: {{email}}</p>
            <p>Password:</p>
            <p>Age:</p>
            <p>Message: </p>
            <p><strong>Send Mail?</strong></p>
            <ul>
              <li></li>
            </ul>
            <p>Gender:</p>
            <p>Priority:</p>
            <p>Switched:</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        email: '',
      };
    },
  };
</script>

<style>

</style>
