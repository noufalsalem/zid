<template>
<div>
    <h1> {{crdMsg}} </h1>
</div>

<div class="container payContainer">
    <div class="row">
        <div class="col-xs-12 col-md-6 col-md-offset-4">
            <div class="panel panel-default">
                <div class="panel-heading">
                    <div class="row">
                        <div class="inlineimage"> 
                        <img class="img-responsive images" src="https://cdn0.iconfinder.com/data/icons/credit-card-debit-card-payment-PNG/128/Mastercard-Curved.png"> 
                        <img class="img-responsive images" src="https://cdn0.iconfinder.com/data/icons/credit-card-debit-card-payment-PNG/128/Visa-Curved.png"> 
                        <img class="img-responsive images" src="https://cdn0.iconfinder.com/data/icons/credit-card-debit-card-payment-PNG/128/American-Express-Curved.png"> 
                        <img class="img-responsive images" src="https://cdn0.iconfinder.com/data/icons/credit-card-debit-card-payment-PNG/128/Paypal-Curved.png"> 
                    </div>
                </div>
            </div>
        <div class="panel-body">
            <form role="form">
                <div class="row">
                    <div class="col-xs-12">
                        <div class="form-group"> <label>CARD NUMBER</label>
                            <div class="input-group"> 
                                <input type="tel" class="form-control" 
                                min-length="19" maxlength="19" placeholder="Valid Card Number" /> 
                                <span class="input-group-addon">
                                <span class="fa fa-credit-card">
                                </span> </span> 
                            </div>
                        </div>
                    </div>
                </div>
<div class="row">
    <div class="col-xs-7 col-md-7">
        <div class="form-group"> <label><span class="hidden-xs">EXPIRATION</span>
        <span class="visible-xs-inline">EXP</span> DATE</label> <input type="tel" class="form-control" 
        maxlength="5" placeholder="MM / YY" />
        </div>
    </div>
    <div class="col-xs-5 col-md-5 pull-right">
        <div class="form-group"> <label>CV CODE</label> 
        <!--v-model cvCode from @Options is not recognized (test change)-->
        <input type="password" class="form-control" placeholder="CVC" 
        v-model="cvCode" 
        min-length="3" maxlength="4" /> 
        </div>
    </div>
</div>
        <div class="row">
            <div class="col-xs-12">
                <div class="form-group"> <label>CARD HOLDER</label> 
                <!--v-model cardHolder from @Options is not recognized (test change)-->
                <input type="text" class="form-control" placeholder="Card Owner Name"
                v-model="cardHolder" 
                min-length="4" maxlength="25"/> 
                </div>
            </div>
        </div>
    </form>
</div>
    <div class="panel-footer">
        <div class="row">
            <div class="col-xs-12"> <button class="btn btn-success btn-lg btn-block" @click="submitForm">
            Confirm Payment</button> 
            </div>
        </div> 
        <br>
        <div class="row">
            <div class="col-xs-12"> <button class="btn btn-danger btn-lg btn-block" type="reset">
            Cancel</button> 
            </div>
        </div>
    </div>

            </div>
        </div>
    </div>
</div>
  
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
//below is importing for vuelidate
import useValidate from '@vuelidate/core'
import { required } from '@vuelidate/validators'

@Options({
  props: {
    crdMsg: String,
    //everything in data method is new addition to test
    data() {
        return {
            v$: useValidate(),
            cardHolder: String,
            cvCode: 0
        }
    }
  }
})


export default class CreditPage extends Vue {
  crdMsg!: string;
    
    //everything until the end of submitForm is a new addition to test
    validations() {
        return {
            cardHolder: { required },
            cvCode: { required }
        }
    }
    submitForm() {
        // this.v$.$validate(); // V$ DOES NOT EXIST ON TYPE CREDITPAGE ERROR. NEED PROPTYPE?
        alert('Form Success');
    }
  }

</script>

<style scoped>
@import url("http://cdn.dcodes.net/2/payment_icons/dc_payment_icons.css");
@import url("https://maxcdn.bootstrapcdn.com/bootstrap/3.3.0/css/bootstrap.min.css");

h1 {
    margin: 40px 0 0;
}

.payContainer {
    margin-left: 20px;
    margin-top: 40px;
}
.inlineimage {
    max-width:470px;
    margin-right: 8px;
    margin-left: 10px
}
.images {
    display: inline-block;
    max-width: 98%;
    height: auto;
    width: 22%;
    margin: 1%;
    left:20px;
    text-align: center
}
</style>
