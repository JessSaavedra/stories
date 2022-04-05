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
		<SwiperSlide><img class="story" src="https://user-images.githubusercontent.com/7197057/160722373-57da3478-3fac-4774-a4a9-9f4660638c8e.png" alt="instagram story"/></SwiperSlide>
		<SwiperSlide><img class="story" src="https://user-images.githubusercontent.com/7197057/160722371-637eb18b-2db2-4433-9094-791ede9951af.png" alt="instagram story"/></SwiperSlide>
		<SwiperSlide><img class="story" src="https://user-images.githubusercontent.com/7197057/160722370-8da95358-3867-4e5c-a6f2-5675265ab5fe.png" alt="instagram story"/></SwiperSlide>
		<SwiperSlide><img class="story" src="https://user-images.githubusercontent.com/7197057/160722365-5b7fbb46-85e7-4ff4-ad81-a36d494431dd.png" alt="instagram story"/></SwiperSlide>
		<SwiperSlide><img class="story" src="https://user-images.githubusercontent.com/7197057/161784353-b131f998-535b-4d6b-b51c-8c12610e24fc.png" alt="instagram story"/></SwiperSlide>
		<SwiperSlide><img class="story" src="https://user-images.githubusercontent.com/7197057/161784358-ed1069d8-b02b-404f-9409-b53396a40d1b.png" alt="instagram story"/></SwiperSlide>
		<SwiperSlide><img class="story" src="https://user-images.githubusercontent.com/7197057/161784367-76603bc6-8674-4b78-b1c3-b89af1980594.png" alt="instagram story"/></SwiperSlide>
	</Swiper>
</main>

<style>
	.story {
		border-radius: 0.5em;
		width: 100%;
	}
</style>
