<script>
  import { Map, Marker } from '@beyonk/svelte-mapbox'
  let mapComponent

	function onClick() {
    mapComponent.flyTo({center:[-118.260830,34.082288]})
	}
</script>

<Map accessToken="pk.eyJ1IjoiY29ubm9yYnJvd24iLCJhIjoiY2xjczJzYXNuMGx6NDN2bjR2aXAzOWY0ZyJ9.7-sM-0G8TGnHv8VW8dpcTA"
	style="mapbox://styles/mapbox/outdoors-v11"
  zoom=11
  center={[-71.224518,42.213995]}
  bind:this={mapComponent} 
  on:click={onClick}
>
	 <Marker lat=42.301941 lng=-71.285433 label="Whole Foods" />,
</Map>