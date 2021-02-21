<template>
    <div class="col-lg-12">
        <div class="card">
            <div class="card-body">
                <h5 class="card-title">Looking for a cool password?!</h5>
                <div class="col-lg-8 m-auto">
                    <div class="input-group">
                        <input type="text" class="form-control" name="txt-pass" id="txt-pass" readonly v-model="password">
                        <div class="input-group-append">
                            <button class="btn btn-outline-secondary" type="button" @click="copyPassword"><i class="fas fa-copy"></i></button>
                            <button class="btn btn-outline-secondary" type="button" @click="getNewPassword"><i class="fas fa-redo"></i></button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="text-center">
            <a href="https://github.com/santhoshjanan/simplepasswordapi"><i class="fab fa-github"></i></a>
            <a href="https://github.com/santhoshjanan/simplepasswordclient"><i class="fab fa-github"></i></a>
        </div>
    </div>
</template>

<script>
import axios from "axios"

export default {
    name: 'GeneratePassword',
    data(){
        return {
                password: 'no-password'
            }
    },
    mounted(){
        this.getNewPassword()
    },
    methods: {
        getNewPassword(){
            axios.get('http://localhost')
            .then(response => {this.password = response.data.password});
        },

        copyPassword(){
            document.getElementById('txt-pass').select();
            document.execCommand("copy");
        }
    }
    

}
</script>


<style scoped>

</style>
