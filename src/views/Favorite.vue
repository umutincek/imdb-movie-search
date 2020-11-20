<template>
    <div>
        <b-card class="my-5 mx-5">
            <TableComponent
                    :data-list="$store.getters.getFavorites" />
        </b-card>
    </div>
</template>

<script>
    import TableComponent from "../components/TableComponent";
    export default {
        name: "Favorite",
        components: {
            TableComponent
        },
    }
</script>
