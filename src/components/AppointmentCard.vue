<template>
  <div class="popup-form">
    <div class="popup-form-content">
      <button class="close-button" @click="cancelAppointmentForm">
        <i class="fa-solid fa-x"></i>
      </button>
      <div class="modal-body">
        <div class="title">Enregistrez Vous</div>

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
                <option value="inscription_personne">Inscription personne</option>
                <option value="inscription_famille">Inscription famille</option>
                <option value="adhesion_personne">Adhésion personne</option>
                <!-- <option value="adhesion_enfants">Adhésion enfants</option> -->
                <option value="dons">dons</option>
              </select>
            </div>
          </div>

          <div class="form-items2" v-if="appointmentform.option == 'dons'">
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
    </div>
  </div>
</template>

<script setup>
import { ref, reactive } from 'vue'
// import axios from 'axios'

defineProps({
  showAppointment: Boolean
})
const emits = defineEmits(['showAppointmentPopup'])

const cancelAppointmentForm = () => {
  emits('showAppointmentPopup')
}

// let showAppointment = ref(false)

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

// function showAppointmentPopup() {
//     showAppointment.value = !showAppointment.value
// }

async function saveAppointmentForm() {
  if (appointmentform.option == 'inscription_personne') {
    cancelAppointmentForm()
    // window.location.href = 'https://nokash.co/pay-now/dl-663b97e7938f61715181'
    window.location.href = 'https://nokash.co/pay-now/dl-663ba312cd82f1715184'
  } else if (appointmentform.option == 'inscription_famille') {
    cancelAppointmentForm()
    window.location.href = 'https://nokash.co/pay-now/dl-663ba312cd82f1715184'
  } else if (appointmentform.option == 'adhesion_personne') {
    cancelAppointmentForm()
    window.location.href = 'https://nokash.co/pay-now/dl-663d2adcc7aca1715284'
  } else if (appointmentform.option == 'dons') {
    /* else if (appointmentform.option == 'adhesion_enfants') {
    cancelAppointmentForm()
    window.location.href = 'https://nokash.co/pay-now/dl-663d2b56a819c1715284'
  } */
    cancelAppointmentForm()
    window.location.href = 'https://nokash.co/pay-now/dl-664fa72dea5aa1716496'
  }
}
</script>

<style>
.popup-form {
  position: fixed;
  overflow-y: scroll;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  width: 100%;
  /* height: 100%; */
  background-color: rgba(0, 0, 0, 0.5);
  padding: 20px;
  z-index: 9999;
  display: flex;
  justify-content: center;
  align-items: center;
}
.popup-form-content {
  width: 95%;
  margin: auto;
  background-color: #fff;
  border-radius: 8px;
  padding: 0px 16px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
  position: relative;
}
.popup-form-content .close-button {
  display: block;
  position: absolute;
  width: 48px;
  height: 48px;
  border-radius: 50%;
  border: none;
  background: rgb(255, 255, 255);
  box-shadow: rgba(39, 40, 51, 0.16) 0px 8px 16px;
  top: -16px;
  right: -16px;
  outline: var(--primary);
}

.modal-body {
  display: flex;
  flex-direction: column;
}
.modal-body .title {
  font-size: 20px;
  font-weight: bold;
  display: flex;
  justify-content: center;
  align-items: center;
  color: rgba(0, 0, 0, 0.85);
  border-bottom: 1px solid #eee;
  margin-bottom: 40px;
  padding-top: 5px;
}

.modal-body .profile-form {
  margin-top: 25px;
  display: flex;
  flex-direction: column;
  width: 95%;
  margin: 0 auto;
  min-height: 0;
  text-align: left;
  padding: 0;
  color: #000;
  font-size: 14px;
  line-height: 1.5715;
  list-style: none;
  box-shadow: none;
}
.modal-body .profile-form .form-items {
  display: block;
  margin-bottom: 20px;
}
.modal-body .profile-form .form-items .form-group {
  width: 100%;
  display: flex;
  flex-direction: column;
}
.input-label {
  padding-bottom: 5px;
  color: rgba(0, 0, 0, 0.85);
  font-size: 12px;
  margin-bottom: 5px;
}
.input-label::after {
  display: inline-block;
  margin-right: 4px;
  margin-left: 2px;
  color: #ff4d4f;
  font-size: 14px;
  line-height: 1;
  content: '*';
}
.email {
  line-height: 1;
  padding: 15px;
  border-radius: 14px;
  border: 1px solid #ccc;
}
.email:hover {
  border-color: var(--primary-hover);
  border-right-width: 1px !important;
}
textarea:hover {
  border-color: var(--primary-hover) !important;
}

.email:focus {
  border-color: var(--primary-hover);
  box-shadow: 0 0 0 2px var(--primary-hover);
  border-right-width: 1px !important;
  outline: 0;
}

.modal-body .profile-form .form-items2 {
  display: flex;
  flex-direction: column;
  margin-bottom: 30px;
}
.modal-body .profile-form .form-items2 input {
  width: 100%;
}

.cancel {
  line-height: 1;
  display: inline-block;
  font-weight: 400;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s cubic-bezier(0.645, 0.045, 0.355, 1);
  height: 50x;
  padding: 15px 15px;
  font-size: 12px;
  border-radius: 12px;
  background: #fff;
  min-width: 20px;
  border: 1px solid var(--primary);
  color: var(--primary);
  margin-right: 5px;
  outline: 0;
}
.submit {
  line-height: 1;
  display: inline-block;
  font-weight: 400;
  text-align: center;
  cursor: pointer;
  transition: all 0.3s cubic-bezier(0.645, 0.045, 0.355, 1);
  height: 50px;
  padding: 15px 15px;
  font-size: 12px;
  border-radius: 12px;
  background: var(--primary);
  min-width: 20px;
  border: 1px solid var(--primary);
  color: #fff;
  outline: 0;
}
.cancel:focus {
  outline: 0;
}
.submit:focus {
  outline: 0;
}

.footer2 {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 20px;
}
</style>
