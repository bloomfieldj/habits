<script>
	const date = new Date();

	const habits = [
		{
			name: 'Jonathon',
			slow: true,
			meditate: true,
			journal: true,
			vegetables: true,
			water: true,
			exercise: true
		}
	];
</script>

<h1>Habits</h1>
<h2>
	{new Intl.DateTimeFormat('en-us', {
		weekday: 'long',
		year: 'numeric',
		month: 'long',
		day: 'numeric'
	}).format(date)}
</h2>
<p>Tap and hold each habit to mark them as complete.</p>
<table>
	<thead>
		<tr>
			<td> Name </td>
			<td> Slow Start</td>
			<td> Meditate</td>
			<td> Journal</td>
			<td> Exercise</td>
			<td> Vegetables</td>
			<td> Water</td>
		</tr>
	</thead>
	<tbody>
		{#each habits as habit}
			<tr>
				<td>
					<h3>{habit.name}</h3>
				</td>
				<td>
					<label><input type="checkbox" bind:checked={habit.slow} />Slow Start</label>
				</td>
				<td>
					<label><input type="checkbox" bind:checked={habit.meditate} />Meditate</label>
				</td>
				<td>
					<label><input type="checkbox" bind:checked={habit.journal} />Journal</label>
				</td>
				<td>
					<label><input type="checkbox" bind:checked={habit.exercise} />Exercise</label>
				</td>
				<td>
					<label><input type="checkbox" bind:checked={habit.vegetables} />Vegetables</label>
				</td>
				<td>
					<label><input type="checkbox" bind:checked={habit.water} />Water</label>
				</td>
			</tr>
		{/each}
	</tbody>
</table>
