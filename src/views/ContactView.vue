<script setup>
import Title from '../components/utils/Title.vue'
</script>
<template>
  <div class="form-content">
    <div class="form-title">
      <Title title="Contato" msg="Utilize o formulário para entrar em contato"></Title>
    </div>
    <div v-if="errors.length">
      <b>Por favor, corrija o(s) seguinte(s) erro(s):</b>
      <p id="error" v-for="error in errors">{{ error }}</p>
    </div>

    <div v-if="responses">
      <p id="success" v-for="response in responses">{{ response }}</p>
    </div>

    <input type="email" v-model="form.email" placeholder="E-mail" @keyup="clear" />
    <input type="text" v-model="form.subject" placeholder="Assunto" @keyup="clear" />
    <textarea v-model="form.message" placeholder="Mensagem" @keyup="clear" />
    <button @click="submit" v-if="!loading">Enviar</button>
    <p v-if="loading">Carregando...</p>
  </div>
</template>

<style>
.form-title {
  margin: 2rem 0;
}

.form-content {
  display: flex;
  flex-direction: column;
  gap: 6px;
}

input[type=text],
input[type=email],
textarea {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  display: inline-block;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
  font-family: Inter,
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    Oxygen,
    Ubuntu,
    Cantarell,
    'Fira Sans',
    'Droid Sans',
    'Helvetica Neue',
    sans-serif;
}

button {
  width: 100%;
  background-color: hsl(197, 100%, 50%);
  color: white;
  padding: 14px 20px;
  margin: 8px 0;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: hsl(197, 100%, 50%, 25%);
}

#error {
  color: red;
}

#success {
  width: 100%;
  background-color: hsl(197, 100%, 50%);
  color: white;
  padding: 14px 20px;
  margin: 8px 0;
  border: none;
  border-radius: 4px;
}
</style>

<script>
export default {
  data() {
    return {
      errors: [],
      loading: false,
      form: {
        email: '',
        subject: '',
        message: ''
      }
    }
  },
  methods: {
    clear() {
      this.errors = [];
      this.responses = [];
    },
    submit(e) {
      this.loading = true;

      setTimeout(() => {
        if (this.form.name && this.form.subject && this.form.message) {
          return true;
        }

        this.errors = [];
        this.responses = [];

        var emailSchema = /\S+@\S+\.\S+/;

        if (!this.form.email || !emailSchema.test(this.form.email)) {
          this.errors.push('Digite um email válido.');
        }
        if (!this.form.subject) {
          this.errors.push('Digite um assunto.');
        }
        if (!this.form.message) {
          this.errors.push('Digite uma mensagem.');
        }

        if((this.errors.length == 0)){
          this.responses.push('Mensagem enviada com sucesso');
          console.log(responses)
        }
      }, 2000 )

      setTimeout(() => {
        this.loading = false
      }, 2000);

    }
  }
}
</script>