<template>
    <div class="event-card d-flex justify-content-between">
        <div class="hover-ef">

        </div>
        <div class="text text-start">
            <i class="fa-solid fa-location-dot"></i><p>{{location}}</p>
            <h6>{{event}}</h6>
        </div>
        <div class="date-ticket">
            <h1>{{day}}</h1>
            <p>{{month}}</p>
            <button class="primary-btn small">Get ticket</button>
        </div>
    </div>
</template>

<script>
export default {
    props:{
        location: String,
        event: String,
        day: Number,
        month: String,
    }
}
</script>

<style scoped lang="scss">
.event-card{
    background: var(--main-bg-light);
    padding: 1.5rem;
    cursor: pointer;
    border-radius: 0.5rem;
    position: relative;
    overflow: hidden;
    &:hover{
        background: var(--white);
        box-shadow: 0 1rem 2rem rgba(0,0,0,0.1);
        .hover-ef{
            display: block;
        }
    }

    .hover-ef{
        position: absolute;
        left: 0;
        top: 0;
        min-height: 100%;
        width: 4px;
        background-color: var(--jungle-green);
        display: none;
    }
    .text{
        padding-top: 0.5rem;
        i{
            float: left;
            padding-right: 0.5rem;
            padding-top: 0.1rem;
            color: var(--gray);
        }
        p{
            font-size: 0.9rem;
            color: var(--gray);
        }
        h6{
            font-weight: bold;
        }
    }

    .date-ticket{
        h1{
            font-weight: normal;
            color: var(--jungle-green);
            margin: 0;
        }
        p{
            text-transform: uppercase;
            font-weight: 600;
            margin: 0.2rem;
        }
    }
}
</style>
