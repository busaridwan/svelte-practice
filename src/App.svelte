<script>
	import FeedbackForm from "./components/FeedbackForm.svelte";
	import FeedbackList from "./components/FeedbackList.svelte";
	import FeedbackStats from "./components/FeedbackStats.svelte";
// 	let feedback = [
//   {
//     id: 1,
//     rating: 10,
//     text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. consequuntur vel vitae commodi alias voluptatem est voluptatum ipsa quae.',
//   },
//   {
//     id: 2,
//     rating: 9,
//     text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. consequuntur vel vitae commodi alias voluptatem est voluptatum ipsa quae.',
//   },
//   {
//     id: 3,
//     rating: 8,
//     text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. consequuntur vel vitae commodi alias voluptatem est voluptatum ipsa quae.',
//   },
// ]
// const deleteFeedback = (e) => {
// 	console.log(e.detail);
// 	const itemId = e.detail;
// 	feedback = feedback.filter((item) => item.id != itemId);
// }
// $: count = feedback.length;
// $: average = feedback.reduce((a, {rating}) => a + rating, 0) / feedback.length;

</script>

<main class="container">
	<FeedbackForm />
	<FeedbackStats />
	<!-- <FeedbackStats {count} {average} /> -->
	<!-- <FeedbackList feedback={feedback}/> -->
	<FeedbackList />
	<!-- <FeedbackList {feedback} on:delete-feedback={deleteFeedback}/> -->
	<!-- Count: {count}
	Average: {average} -->

</main>