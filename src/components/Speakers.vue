
<script>
// If you are using PurgeCSS, make sure to whitelist the carousel CSS classes
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'
import { defineComponent } from 'vue'


export default defineComponent({
  name: 'Breakpoints',
  components: {
    Carousel,
    Slide,
    Navigation,
  },
  data: () => ({
	slides : [
		{id: 1,url: 'img/p2.jpg', name:'Светлана', fio:'Котлукова', text:'Маркетолог, руководитель PR-агентства<br> для дизайнеров «АрхДиалог»'}, 
		{id: 2, 
		url: 'img/p1.jpg',
		name:'Станислав', fio:'Орехов', text:'Дизайнер, визуализатор,<br> руководитель студии<br> d-e-s-i-g-n.ru'}, 
		{id: 3,url: 'img/p3.jpg', name:'Максим', fio:'Вересов', text:'Архитектор, строитель, руководитель компании деревянного строительства'}, 
		{id: 4, url: 'img/p4.jpg',name:'Андрей', fio:'Вересов', text:'Дизайнер, визуализатор, руководитель студии '}
	],
    settings: {
      itemsToShow: 1,
      snapAlign: 'center',
    },
    
    breakpoints: {
      560: {
        itemsToShow: 2,
        snapAlign: 'center',
      },
      768: {
        itemsToShow: 3.5,
        snapAlign: 'center',
      },
   
      1024: {
        itemsToShow: 3,
        snapAlign: 'start',
      },
    },
  })
})


</script>


<template>
	<section class="section section--big">
		<div class="container container--left container--slider">
			<h2 class="h2 section__title">
				<span class="section__title-text">спикеры</span>
			</h2>
			<div class="section__body">
				<div class="item__mobile">
					<div class="item__mobile-wrap">
						<div class="item" v-for="slide in slides" :key="slide.id">
							<div class="item__img">
								<img :src='slide.url'>
							</div>
							<div class="item__name">
								{{slide.name}}
								<span class="red item__fio">
									{{slide.fio}}
								</span>
							</div>
							<div class="item__text" v-html='slide.text'>
								
							</div>
						</div>
					</div>
				</div>
				<Carousel v-bind="settings" :breakpoints="breakpoints">
					<slide v-for="slide in slides" :key="slide.id">
						<div class="item">
							<div class="item__img">
								<img :src='slide.url'>
							</div>
							<div class="item__name">
								{{slide.name}}
								<span class="red item__fio">
									{{slide.fio}}
								</span>
							</div>
							<div class="item__text" v-html='slide.text'>
								
							</div>
						</div>
					</Slide>

					<template #addons>
						<navigation>
							<template #next>
								<svg width="17" height="14" viewBox="0 0 17 14" class="svg-icon"><use xlink:href="#svg-right"></use></svg>
							</template>
							<template #prev>
								<svg width="17" height="14" viewBox="0 0 17 14" class="svg-icon"><use xlink:href="#svg-left"></use></svg>
							</template>
						</navigation>
					</template>
				</Carousel>
			</div>
		</div>
	
	</section>

</template>

<style>

	.carousel {
		margin-left: -11px;
		margin-top: 5px;
		padding-bottom: 84px;
	}

	.carousel__viewport {
		overflow: visible;
	}

	.carousel__slide {
		padding: 0 12px;
		align-items: flex-start;
	}

	.carousel__prev:hover, .carousel__next:hover {
		background-color: #DA353B;
	}
	
	.carousel__prev--disabled {
		pointer-events: none;
	}

	.carousel__next--disabled {
		pointer-events: none;
	}

	.carousel__next {
		right: 16px;
	}

    .carousel__prev {
		right: 79px;
    	left: initial;
	}

	.carousel__prev .svg-icon use, .carousel__next .svg-icon use {
		stroke: #DA353B;
		fill: transparent;
		transition: stroke 0.3s ease;
	}

	.carousel__prev:hover .svg-icon use, .carousel__next:hover .svg-icon use {
		stroke: #fff;
	}

	.carousel__prev, .carousel__next {
		width: 43px;
		height: 43px;
		border: 2px solid #DA353B;
		display: flex;
		align-items: center;
		justify-content: center;
		bottom: 0;
		top: initial;
		transform: translateY(0);
		margin: 0;
		transition: background-color 0.3s ease;
	}

	@media(max-width: 560px ) {
		.carousel {
			display: none;
		}
	}
</style>
