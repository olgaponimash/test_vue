<script setup>
	import Menu from './components/Menu.vue'
	import Speakers from './components/Speakers.vue'
	import Form from './components/Form.vue'
</script>	

<script >
	export default {
	data() {
		return {
		ref: null
		};
	},
	methods: {
		handleClick() {
		this.$refs.targetRef.scrollIntoView({ behavior: 'smooth' });
		}
	}
	};
</script>

<template>
	<svg style="display: none;">
    	<defs>
			<!--width="17" height="14" viewBox="0 0 17 14"-->
			<g id="svg-right">
				<path d="M9 1L15.2415 7.04944L9 13.0989"  stroke-width="1.5"/>
				<path d="M0 7.25H14.5"  stroke-width="1.5" stroke-linejoin="round"/>			
			</g>

			

			<!--width="17" height="14" viewBox="0 0 17 14"-->
			<g id="svg-left">
				<path d="M8 1L1.75854 7.04944L8 13.0989" stroke-width="1.5"/>
				<path d="M17 7.25H2.5" stroke-width="1.5" stroke-linejoin="round"/>
			</g>

			<!--width="24" height="24" viewBox="0 0 24 24"-->
			<g id="svg-twitter">
				<g clip-path="url(#clip0_1707_601)">
				<path d="M24 4.55899C23.1167 4.9504 22.1689 5.21585 21.1731 5.33436C22.1899 4.72546 22.9682 3.75966 23.3371 2.61236C22.3833 3.17625 21.3305 3.5857 20.2087 3.80766C19.3104 2.84934 18.0326 2.25244 16.6154 2.25244C13.8964 2.25244 11.6918 4.45703 11.6918 7.17452C11.6918 7.55993 11.7353 7.93636 11.8193 8.29632C7.72807 8.09083 4.10026 6.13071 1.67222 3.15224C1.24779 3.87813 1.00634 4.72393 1.00634 5.62679C1.00634 7.33499 1.87618 8.8422 3.19595 9.72401C2.38908 9.69703 1.63022 9.47507 0.965866 9.10613V9.16762C0.965866 11.5522 2.66355 13.5423 4.91461 13.9952C4.50218 14.1062 4.06728 14.1677 3.61736 14.1677C3.29944 14.1677 2.99199 14.1362 2.69053 14.0762C3.3174 16.0333 5.13508 17.4566 7.28869 17.4956C5.6045 18.8153 3.48089 19.5997 1.17434 19.5997C0.776924 19.5997 0.385473 19.5757 6.10352e-05 19.5322C2.17916 20.9315 4.76618 21.7473 7.54666 21.7473C16.6034 21.7473 21.554 14.2457 21.554 7.73993L21.5375 7.10256C22.5048 6.41264 23.3417 5.54581 24 4.55899Z" />
				</g>
				<defs>
				<clipPath id="clip0_1707_601">
				<rect width="24" height="24" fill="white"/>
				</clipPath>
				</defs>		
			</g>

			<!--width="24" height="24" viewBox="0 0 24 24"-->
			<g id="svg-linkedin">
				<g clip-path="url(#clip0_1707_607)">
				<path d="M24 14.5937V23.4666H18.856V15.1879C18.856 13.1082 18.112 11.6889 16.2501 11.6889C14.8287 11.6889 13.9828 12.6454 13.6107 13.5707C13.475 13.9015 13.4401 14.3619 13.4401 14.8249V23.4666H8.29438C8.29438 23.4666 8.36368 9.44522 8.29438 7.99249H13.4396V10.1859C13.4291 10.2023 13.4156 10.22 13.4058 10.2359H13.4396V10.1859C14.1232 9.13302 15.344 7.62897 18.0766 7.62897C21.462 7.62891 24 9.84061 24 14.5937ZM2.91175 0.533203C1.15141 0.533203 0 1.68785 0 3.20624C0 4.69155 1.1181 5.88124 2.84345 5.88124H2.87782C4.67225 5.88124 5.78823 4.69177 5.78823 3.20624C5.75442 1.68785 4.67225 0.533203 2.91175 0.533203ZM0.30561 23.4666H5.44936V7.99249H0.30561V23.4666Z"/>
				</g>
				<defs>
				<clipPath id="clip0_1707_607">
				<rect width="24" height="24" fill="white"/>
				</clipPath>
				</defs>	
			</g>

			<!--width="13" height="24" viewBox="0 0 13 24"-->
			<g id="svg-facebook">
			    <path d="M12.487 0.0049936L9.37474 0C5.87822 0 3.61861 2.31828 3.61861 5.90643V8.62969H0.489373C0.21897 8.62969 0 8.84891 0 9.11932V13.065C0 13.3354 0.219219 13.5544 0.489373 13.5544H3.61861V23.5106C3.61861 23.781 3.83758 24 4.10799 24H8.19075C8.46116 24 8.68013 23.7808 8.68013 23.5106V13.5544H12.3389C12.6093 13.5544 12.8283 13.3354 12.8283 13.065L12.8298 9.11932C12.8298 8.98948 12.7781 8.86514 12.6865 8.77326C12.5949 8.68138 12.47 8.62969 12.3402 8.62969H8.68013V6.32115C8.68013 5.21157 8.94454 4.64829 10.3899 4.64829L12.4865 4.64755C12.7567 4.64755 12.9756 4.42833 12.9756 4.15817V0.494367C12.9756 0.224462 12.7569 0.00549296 12.487 0.0049936Z"/>
			</g>

			<!--width="24" height="18" viewBox="0 0 24 18"-->
			<g id="svg-youtube">
    			<path d="M23.0645 2.0046C22.1982 0.974765 20.5987 0.554688 17.5441 0.554688H6.45569C3.33112 0.554688 1.70454 1.00186 0.841471 2.09828C0 3.16728 0 4.74238 0 6.92235V11.0774C0 15.3007 0.9984 17.445 6.45569 17.445H17.5442C20.1931 17.445 21.661 17.0743 22.6106 16.1655C23.5845 15.2335 24 13.7118 24 11.0774V6.92235C24 4.62338 23.9349 3.039 23.0645 2.0046ZM15.4081 9.5735L10.3729 12.2051C10.2603 12.2639 10.1372 12.2931 10.0143 12.2931C9.87507 12.2931 9.73618 12.2556 9.61316 12.1811C9.38152 12.0408 9.24008 11.7897 9.24008 11.5189V6.27265C9.24008 6.0023 9.38113 5.75146 9.61231 5.61102C9.84356 5.47058 10.1312 5.46098 10.3711 5.58563L15.4063 8.20024C15.6625 8.33324 15.8234 8.59771 15.8237 8.88625C15.8241 9.17502 15.6639 9.43988 15.4081 9.5735Z" />
			</g>

			<!--width="24" height="24" viewBox="0 0 24 24"-->
			<g id="svg-instagram">
    			<path d="M23.0939 0.906398C22.4897 0.302041 21.7657 0 20.9222 0H3.07826C2.23447 0 1.51064 0.302151 0.906288 0.906398C0.302041 1.51048 0 2.23442 0 3.07804V20.9218C0 21.7653 0.301987 22.4894 0.906288 23.0935C1.51064 23.6977 2.23464 24 3.07826 24H20.922C21.7653 24 22.4896 23.6977 23.0938 23.0935C23.6981 22.4894 23.9999 21.7653 23.9999 20.9218V3.07804C23.9998 2.23425 23.6981 1.5107 23.0939 0.906398ZM8.61745 8.64832C9.56008 7.737 10.6929 7.28112 12.0159 7.28112C13.349 7.28112 14.487 7.737 15.4298 8.64832C16.3727 9.55981 16.8438 10.6615 16.8438 11.9531C16.8438 13.2446 16.3727 14.3463 15.4298 15.2575C14.487 16.1692 13.3494 16.625 12.0159 16.625C10.693 16.625 9.56025 16.1688 8.61745 15.2575C7.67461 14.3462 7.20324 13.2446 7.20324 11.9531C7.20324 10.6615 7.67461 9.55986 8.61745 8.64832ZM21.2816 20.2814C21.2816 20.5521 21.1875 20.7785 21.0002 20.9609C20.8123 21.1432 20.5887 21.2343 20.3281 21.2343H3.62521C3.35442 21.2343 3.12768 21.1432 2.94555 20.9609C2.76314 20.7789 2.67202 20.5521 2.67202 20.2814V10.1561H4.87508C4.66684 10.8124 4.56269 11.4948 4.56269 12.203C4.56269 14.2034 5.29177 15.9089 6.7501 17.3206C8.20858 18.7318 9.96375 19.4377 12.0158 19.4377C13.37 19.4377 14.6199 19.1147 15.7661 18.4689C16.912 17.8227 17.8176 16.9453 18.4848 15.8359C19.1515 14.7264 19.4849 13.5154 19.4849 12.203C19.4849 11.4949 19.3803 10.8126 19.1721 10.1561H21.2817V20.2815H21.2816V20.2814ZM21.2816 6.32793C21.2816 6.63002 21.1774 6.88527 20.9687 7.09357C20.7605 7.30202 20.5054 7.40611 20.2032 7.40611H17.4845C17.1826 7.40611 16.9271 7.30197 16.7189 7.09357C16.5106 6.88527 16.4065 6.63002 16.4065 6.32793V3.75004C16.4065 3.45834 16.5106 3.20578 16.7189 2.99217C16.9272 2.77868 17.1826 2.6718 17.4845 2.6718H20.2032C20.5054 2.6718 20.7606 2.77863 20.9687 2.99217C21.1774 3.20578 21.2816 3.45834 21.2816 3.75004V6.32793Z"/>
			</g>
		</defs>
	</svg>
  	<header class="header container">
		<div class="header__main">
			<a href="" class="logo">
				<img src="/img/logo-main.png" alt="">
			</a>
			 <Menu/>
		</div>
		<div class="header__btn">
			<button @click="handleClick" class="btn btn--default" >
				<span class="btn__text hidden-mobile">принять участие</span> 
				<span class="btn__text hidden-desktop">участвовать</span> 
			</button>
		</div>
    </header>
	<div class="banner">
		<div class="banner__img">
			<img src="/img/banner.jpg" alt="">
		</div>
		<div class="banner__wrap">
			<div class="container container--big">
				<div class="banner__main">
					<h1 class="h1 banner__title">
						<span class="red extrabold block">
							ДИЗАЙН
						</span>
						
						КОНФЕРЕНЦИЯ
					</h1>
					<div class="banner__text">
						Главное событие в дизайне и архитектуре
					</div>
					<div class="banner__btn">
						<button @click="handleClick"  class="btn btn--out-white">
							<span class="btn__text">
								принять участие
							</span>
						</button>
					</div>
				</div>
				<div class="banner__info">
					<div class="banner__info-body">
						<div class="banner__info-date">
							7-9 апреля 2019
						</div>
						<div class="banner__info-text">
							Культурный центр «ЗИЛ»
						</div>
					</div>
					<div class="banner__info-logo">
						<img src="/img/logo.png" alt="">
					</div>
				</div>
			</div>
		</div>
		
	</div>
   

	<section class="section">
		<div class="container container--big">
			<h2 class="h2 section__title section__title--mini">
				<span class="section__title-text"><span class="red">Опыт</span> практиков</span>
			</h2>
			<div class="section__body">
				<div class="section__text section__text--small">
					Узнайте, как эффективно работать и зарабатывать
					в сфере дизайна, визуализации, проектирования
					и строительства
				</div>

				<div class="about">
					<div class="about__img">
						<img src="/img/about.jpg" alt="">
					</div>
					<div class="about__body">
						<h3 class="h3 about__title">
							<span class="white-mobile">О чем</span> <span class="red">молчат</span> дизайн-эксперты?
						</h3>

						<div class="about__text">
							Спикеры поделятся практическими знаниями,
							особенностями подхода, секретами и фишками. 
						</div>

						<div class="about__atten">
							Каждый найдет свое.
						</div>
					</div>
				</div>
			</div>
		</div>
	
	</section>

	<Speakers  />
	<div ref="targetRef">
		<Form  />
	</div>
</template>
