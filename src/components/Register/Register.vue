<template>
  <div class="register">
        <form action="" data-toggle="validator" id="contact_form">
            <div class="row">
                <div class="form-group col-xl-6">
                    <label for="email">Email:</label>
                    <input type="email" class="form-control" id="email" name="email" />
                </div>
                <div class="form-group col-xl-6">
                    <label for="pwd">Password:</label>
                    <input type="password" class="form-control" id="pwd" name="password" @input="password_check" v-model="pass">
                    <nav class="check-pwd">
                        <ul>
                            <li class="check-pwd__item" :class="{ 'check-pwd__item--green' : length }"><i class="fa fa-circle-o" aria-hidden="true"></i>8 - 15 characters</li>
                            <li class="check-pwd__item" :class="{ 'check-pwd__item--green' : has_number }"><i class="fa fa-circle-o" aria-hidden="true"></i>1 or more numbers</li>
                            <li class="check-pwd__item" :class="{ 'check-pwd__item--green' : has_lowCase }"><i class="fa fa-circle-o" aria-hidden="true"></i>1 or more lower case letters</li>
                            <li class="check-pwd__item" :class="{ 'check-pwd__item--green' : has_upCase }"><i class="fa fa-circle-o" aria-hidden="true"></i>1 or more upper case letters</li>
                            <li class="check-pwd__item" :class="{ 'check-pwd__item--green' : has_special }"><i class="fa fa-circle-o" aria-hidden="true"></i>1 or more special characters ($@&!%)</li>
                        </ul>
                    </nav>
                </div>
            </div>
            <div class="register__valid-msg" :class="{'show': check_all && show_msg}">
                <h3 class="d-flex register__valid-msg__title">
                    <i class="fa fa-check-circle" aria-hidden="true"></i>
                    <span>Registration Successful</span>
                </h3>
                <p class="d-flex register__valid-msg__synapsis">
                    <i class="fa fa-caret-right" aria-hidden="true"></i>
                    <span>
                        Thank you for registering for our event with XM. You will receive an email shortly with confirmation of your registration.
                    </span>
                </p>
            </div>
            <div class="register__submit row">
                <button type="button" class="submit btn" :class="{'disabled':!check_all}" id="submit-button" @click="ShowMassage">register now</button>
            </div>
        </form>

        <p class="register__sublink1 ta-c">Don’t have an account? <a href="#" title="button">Create one here</a> and register for the event</p>

        <p class="register__sublink2 ta-c">Terms and Conditions apply*. To read the full T&Cs, <a href="#" title="button">click here.</a></p>
    </div>
</template>

<script>
export default {
    name: 'CRegister',

    data(){
        return{
            pass:       '',
            check_all: null,
            has_number:    false,
            has_lowCase: false,
            has_upCase: false,
            has_special:   false,
            length:false,
            show_msg:false,
        }
    },

    

    methods: {

        password_check() {
            this.check_all = /^(?=.*\d)(?=.*[a-z])(?=.*[A-Z])(?=.*[@%!])[0-9a-zA-Z@%!]{8,}$/.test(this.pass);
            this.has_number    = /\d/.test(this.pass);
            this.has_lowCase = /[a-z]/.test(this.pass);
            this.has_upCase = /[A-Z]/.test(this.pass);
            this.has_special   = /[!@#$%^&*+=._-]/.test(this.pass);
            this.length   = /^[0-9a-zA-Z@%!]{8,15}$/.test(this.pass);
        },

        ShowMassage(){
            this.show_msg = !this.show_msg;
        }
    }

}
</script>
