<template>
  <div class="row">
    <div class="col-sm-6">
      <div class="form-group">
        <label for="fname">First Name:</label>
        <input type="text" id="fname" class="form-control" autofocus
               @input="value.fname=$event.target.value">
      </div>
    </div>
    <div class="col-sm-6">
      <div class="form-group">
        <label for="lname">Last Name:</label>
        <input type="text" id="lname" class="form-control"
               @input="value.lname=$event.target.value">
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      value: Object,
    },
  };
</script>
