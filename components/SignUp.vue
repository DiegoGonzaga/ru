<template>
  <div class="container alert alert-primary">
    <b-form>
      <b-form-group label="Name" label-for="txt_name">
        <b-form-input id="txt_name"></b-form-input>
      </b-form-group>

      <b-form-group label="Birthday" label-for="txt_birth">
        <b-form-input id="txt_birth" type="date"></b-form-input>
      </b-form-group>

      <b-form-group label="Email" label-for="txt_email">
        <b-form-input id="txt_email" type="email"></b-form-input>
      </b-form-group>

      <b-button variant="btn btn-info btn-block">Sign Up</b-button>
    </b-form>
  </div>
</template>