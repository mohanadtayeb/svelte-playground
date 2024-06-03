

<script lang="ts">
import "./app.css";

import Button from "$lib/components/ui/button/button.svelte";
import Input from "$lib/components/ui/input/input.svelte";
import "tailwindcss/tailwind.css";

let inputValue: any;
let numbersArr = [{
  num: 0,
  color: "bg-red-500",
  id: 'num_0',

},
{
  num: 1,
  color: "bg-blue-500",
  id: 'num_1',
}
,
{
  num: 2,
  color: "bg-green-500",
  id: 'num_2',
}
,
{
  num: 3,
  color: "bg-yellow-500",
  id: 'num_3',
}
,
{
  num: 4,
  color: "bg-purple-500",
  id: 'num_4',
}
,
{
  num: 5,
  color: "bg-cyan-500",
  id: 'num_5',
}
,
{
  num: 6,
  color: "bg-orange-500",
  id: 'num_6',
}
,
{
  num: 7,
  color: "bg-indigo-500",
  id: 'num_7',
}
,
{
  num: 8,
  color: "bg-pink-500",
  id: 'num_8',
}
,
{
  num: 9,
  color: "bg-teal-500",
  id: 'num_9',
}
]

function handleClick() {

  
  
}

function handleEqual() {
  console.log("equal")
}

function handleNumber(e: any) {
inputValue = inputValue + e.target.innerText;
console.log(inputValue)
}


</script>



<main>
  <div class="container w-fit mt-10 border-2 p-5 rounded-xl">
    <Input placeholder="1234..." bind:value={inputValue} class="mb-4" id="txt-field" on:click ={handleClick}  ></Input>
  <div class="inline-grid gap-4  grid-cols-3 grid-rows-3 grid-flow-row-dense">
    {#each numbersArr as number}
      <Button class={`${number.color} center`} id={number.id} on:click={handleNumber}>
      {number.num}
      </Button>
    {/each}
    <Button class="bg-gray-500 center col-span-2" id="equal"> 
      =
      </Button>
  </div>
</div>


</main>


<style>
  
</style>