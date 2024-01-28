<script>
import Header from "./lib/Header.svelte";
import VideoItem from "./lib/VideoItem.svelte";

const blurays = [
    {
        id: 'b1',
        title: 'The Avengers',
        subtitle: 'Some assembly required.',
        cast: 'Robert Downey Jr, Chris Evans, Scarlett Johansson',
        imageUrl: 'https://image.tmdb.org/t/p/w600_and_h900_bestv2/RYMX2wcKCBAr24UyPD7xwmjaTn.jpg',
        description: 'When an unexpected enemy emerges and threatens global safety and security, Nick Fury, director of the international peacekeeping agency known as S.H.I.E.L.D., finds himself in need of a team to pull the world back from the brink of disaster. Spanning the globe, a daring recruitment effort begins!'
    },
    {
        id: 'b2',
        title: 'Batman',
        subtitle: 'Justice is always darkest before the dawn.',
        cast: 'Michael Keaton, Jack Nicholson, Kim Basinger'        ,
        imageUrl: 'https://image.tmdb.org/t/p/w600_and_h900_bestv2/cij4dd21v2Rk2YtUQbV5kW69WB2.jpg',
        description: 'Batman must face his most ruthless nemesis when a deformed madman calling himself "The Joker" seizes control of Gotham\'s criminal underworld.'
    }
]
</script>

<style>
    #blurays {
        margin-top: 5rem;
    }
</style>

<Header />

<section id="blurays">
    {#each blurays as bluray}
        <VideoItem
                title={bluray.title}
                subtitle={bluray.subtitle}
                cast={bluray.cast}
                imageUrl={bluray.imageUrl}
                description={bluray.description.substring(0, 120) + '...'}/>
    {/each}
</section>
