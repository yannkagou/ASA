<template>
  <main>
    <div class="modal-body">
      <div class="title">Faites un don</div>

      <form class="profile-form" @submit.prevent="saveAppointmentForm">
        <div class="form-items">
          <div class="form-group">
            <label class="input-label">Votre Nom</label>
            <input
              class="email"
              type="text"
              v-model="appointmentform.name"
              placeholder="Nom..."
              required
            />
          </div>
          <div class="form-group">
            <label class="input-label">Votre Email</label>
            <input
              class="email"
              type="email"
              v-model="appointmentform.email"
              placeholder="Email..."
              required
            />
          </div>
        </div>

        <div class="form-items">
          <div class="form-group">
            <label class="input-label">Numero de telephone</label>
            <input
              class="email"
              type="text"
              v-model="appointmentform.tel"
              placeholder="Tel avec 237 (pas de +)..."
              required
            />
          </div>
          <div class="form-group">
            <label class="input-label">Adresse</label>
            <input
              class="email"
              type="text"
              v-model="appointmentform.address"
              placeholder="Adresse..."
              required
            />
          </div>
        </div>

        <div class="form-items">
          <div class="form-group">
            <label class="input-label">Ville</label>
            <input
              class="email"
              type="text"
              v-model="appointmentform.town"
              placeholder="Votre ville..."
              required
            />
          </div>
          <div class="form-group">
            <label class="input-label">Option</label>
            <select
              class="email"
              v-model="appointmentform.option"
              placeholder="Choisir votre option..."
              required
            >
              <option value="dons">dons</option>
              <option value="subventions">subventions</option>
            </select>
          </div>
        </div>

        <div class="form-items2">
          <label class="input-label">Montant</label>
          <input class="email" v-model="amount" type="number" required />
        </div>

        <div class="form-items2">
          <label class="input-label">Un Message</label>
          <textarea
            class="email"
            v-model="appointmentform.message"
            rows="4"
            cols="50"
            placeholder="Entrez un message..."
            required
          ></textarea>
        </div>

        <div class="footer2">
          <button class="cancel" @click="cancelAppointmentForm">Annuler</button>
          <div class="footer-left">
            <button @click="saveAppointmentForm" class="submit" type="submit">Envoyer</button>
          </div>
        </div>
      </form>
    </div>
  </main>
</template>

<script setup>
import { ref, reactive } from 'vue'

let appointmentform = reactive({
  name: '',
  email: '',
  tel: '',
  address: '',
  town: '',
  option: '',
  message: ''
})

let amount = ref(0)

async function saveAppointmentForm() {
  window.location.href =
    'https://api.monetbil.com/widget/v2.1/VaB3haeYIao9zm8KrhQKwxFaoQ3ITQ8W/?amount=' + amount.value
}
</script>
