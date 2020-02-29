<template>
    <div class="container first pt">
        <div class="row">
            <form name="login_form" @submit.prevent="withCredentials">
                <div class="panel panel-default center-block" id="registrer">
                    <div class="panel-heading">
                        <h3 class="panel-title">Registre</h3>
                    </div>

                    <div class="panel-body">
                        <div class="form-group">
                            <div id="ic" style="display:none;" class="alert alert-danger" role="alert">
                                <span class="glyphicon glyphicon-exclamation-sign" aria-hidden="true"></span>
                                <span class="sr-only">Error:</span>
                                Indentifiants incorrects
                            </div>
                            <input type="email" name="email" v-model="model.email" required placeholder="Email"
                                   autofocus class="form-control">
                        </div>
                        <div class="form-group">
                            <input type="password" name="password" v-model="model.password" required placeholder="Mot de passe"
                                   class="form-control">
                        </div>
                    </div>

                    <div class="panel-footer">
                        <a :href="'register'">S'inscrire</a>
                        <button type="submit" class="btn btn-primary pull-right">Se connecter</button>
                    </div>
                </div>
            </form>
        </div>
    </div>
</template>