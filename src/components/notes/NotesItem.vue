<template>
    <div class="notes-item">
        <h3>{{note.title}}</h3>
        <span>{{note.date}}</span>
        <p>{{note.descr}}</p>
        <div class="notes-item-controls">
            <a href="#" class="btn" @click.prevent="$emit('changeNote', note.id)">
                <img src="@\assets\img\edit.svg" alt="">{{words.editbtn[lang]}}
            </a>
            <a href="#" class="btn" @click.prevent="$emit('deleteNote'), note.id">
                <img src="@\assets\img\del.svg" alt="">{{words.deledit[lang]}}
            </a>
        </div>
    </div>
</template>

<script>
    export default {
        inject: ['words'],
        props: ['note','lang'],
    }
</script>

<style>

</style>