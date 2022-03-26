<script>
	import { Swiper, SwiperSlide } from 'swiper/svelte';
	import { Autoplay, EffectCube, Navigation, Pagination } from "swiper";
	import 'swiper/css'
	import 'swiper/css/effect-cube'
	import 'swiper/css/pagination'
	import 'swiper/css/navigation'

	const pagination = {
		clickable: true,
		renderBullet: function (_, className) {
			return '<span class="' + className + '"></span>';
		},
	};
</script>

<main>
	<Swiper
		{pagination}
		navigation={true}
		modules={[Autoplay, EffectCube, Navigation, Pagination]}
		class="stories"
		spaceBetween={0}
		slidesPerView={1}
		effect={"cube"}
		cubeEffect={{
			shadow: false
		}}
		autoplay={{
			delay: 5000,
			disableOnInteraction: false,
  }}
	>
		<SwiperSlide><img class="story" src="https://i.pinimg.com/originals/09/a8/76/09a876a502006380101f3f072421d4b3.jpg" alt="instagram story"/></SwiperSlide>
		<SwiperSlide><img class="story" src="https://i.pinimg.com/originals/09/a8/76/09a876a502006380101f3f072421d4b3.jpg" alt="instagram story"/></SwiperSlide>
		<SwiperSlide><img class="story" src="https://i.pinimg.com/originals/09/a8/76/09a876a502006380101f3f072421d4b3.jpg" alt="instagram story"/></SwiperSlide>
		<SwiperSlide><img class="story" src="https://i.pinimg.com/originals/09/a8/76/09a876a502006380101f3f072421d4b3.jpg" alt="instagram story"/></SwiperSlide>
	</Swiper>
</main>

<style>
	.story {
		border-radius: 0.5em;
		width: 100%;
	}
</style>
