<template>
 	<section class="section section--last">
		<div class="container container--left">
            <div class="section__body">
				<div class="form__wrap">
                    <div class="form__back">
                        <img src="/img/back-form.jpg" alt="">
					</div>
					<div class="form__main">
						<h2 class="h2 form__title">
							<span class="red">принять</span> участие
						</h2>
                        <form class="form__form" @submit.prevent="submit">
                        
                            <div class="form__field">
								
								<input  class="form__input" type="text"
                                placeholder="Ваши имя и фамилия"
                                v-model="v$.form.firstName.$model"
                                @blur="v$.form.firstName.$touch()">
                                <label class="form__label">
                                    Ваши имя и фамилия
                                </label>
                                <div class="form__error" v-if="v$.form.firstName.$error">
                                    <span v-if="!v$.form.firstName.required.$response">Обязательное поле. </span>
                                    <span v-if="!v$.form.firstName.name_validation.$response">Допустимое имя содержит только буквы и пробелы.</span>
                                </div>   
                                              
							</div>


                            <div class="form__field">
                                
                                <input class="form__input" type="text"
                                placeholder="Компания"
                                v-model="v$.form.company.$model">

                                <label class="form__label">Компания</label>

                                <div class="form__error" v-if="v$.form.company.$error">
                                    <span v-if="!v$.form.company.required.$response">Обязательное поле. </span>
                                </div>            
							</div>

                            <div class="form__field">
                                
                                <input class="form__input" placeholder="E-mail" type="email" 
                                v-model="v$.form.email.$model" 
                                @blur="v$.form.email.$touch()">

                                <label class="form__label">E-mail</label>

                                <div class="form__error" v-if="v$.form.email.$error">
                                    <span v-if="!v$.form.email.required.$response">Обязательное поле. </span>
                                    <span v-if="!v$.form.email.email.$response" class="error">Введите корректный email. </span>
                                </div> 
            
							</div>

                            <div class="form__field">
                                
                                <input class="form__input" placeholder="Телефон" type="text" 
                                v-model="v$.form.phone.$model" 
                                @blur="v$.form.phone.$touch()">

                                <label class="form__label">Телефон</label>

                               <div class="form__error" v-if="v$.form.phone.$error">
                                    <span v-if="!v$.form.phone.required.$response">Обязательное поле. </span>
                                    <span v-if="!v$.form.phone.phone_validation.$response">Введите корректный номер</span>
                                </div>  
            
							</div>

                            <div class="form__btn">
								<button type="submit"  class="btn btn--default btn--big">
                                    <span class="btn__text">
									    Зарегистрироваться
                                    </span>
								</button>
							</div>

                        </form>

                         <div class="form-ok" :class="{ active: submitStateClass }">
                            <div class="form-ok__title">
                                Спасибо!
                            </div>
                            <div class="form-ok__text">
                                Ваше сообщение отправлено.
                            </div>
                        </div>
                    </div>

					<div class="form__img">
                        <img src="/img/form.jpg" alt="">
					</div>
				</div>
			</div>
		</div>
	
	</section>
</template>

<script>

    import useVuelidate from '@vuelidate/core'
    import { required, email, minLength, sameAs } from '@vuelidate/validators'


    export function validName(name) {

        let validNamePattern = new RegExp("^[a-zA-Za-яA-z ]+$");
        console.log(validNamePattern.test(name))

        if (validNamePattern.test(name)){
            return true;
        }

        return false;
    }

    export function validPhone(phone) {

        let phoneExp = /^((8|\+7)[\- ]?)?(\(?\d{3}\)?[\- ]?)?[\d\- ]{7,10}$/;
        let validPhonePattern = new RegExp(phoneExp);

        if (validPhonePattern.test(phone)){
            return true;
        }

        return false;
    }


    export default {

    setup () {
        return { v$: useVuelidate() }
    },

    data() {
        return {
        form: {
            submitStateClass: false,
            firstName: '',
            company: '',
            email: '',
            phone: ''
            }
        }
    },

    validations() {
            return {
                
                form: {
                    firstName: { 
                    required, name_validation: {
                            $validator: validName,
                            $message: 'Неверное имя. Допустимое имя содержит только буквы и пробелы.'
                        } 
                    },
                    company: { required },
                    email: { required, email },
                    phone: { 
                    required, phone_validation: {
                            $validator: validPhone,
                            $message: 'Введите корректный номер'
                        } 
                    },
                },
            }
        },
        methods: {
            submitState() {
                this.submitStateClass = !this.submitStateClass;  
            },
            submit() {
                this.v$.$touch();
                if (this.v$.$invalid) {
                   
                } else {
                    this.submitState();
                    
                }
            }
        }
    }
</script>



