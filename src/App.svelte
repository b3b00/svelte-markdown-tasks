<script lang="ts">

	import TaskRenderer from "./TaskRenderer.svelte";
	import SvelteMarkdown from "svelte-markdown";


	// let content:string = `
	// - [ ] todo
	// - [X] done
	// - [ ] nested tasks
	// 	- [X] sub task #1
	// 	- [ ] sub task #2
	// 	- [X] sub task #3

	// `

	let content = `**toto**
- [ ] todo
- [X] done
- [X] **formated task**
- [ ] nested tasks
    - [X] sub task #1
    - [ ] sub task #2
    - [X] sub task #3		
`;
	
	
</script>

<SvelteMarkdown renderers={{listitem: TaskRenderer	}} source={content} />


