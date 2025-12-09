<template>
    <div class="input-wrapper">
        <input min="0" type="number" @input="changeAmount($event.target.value)"placeholder="Введите число" />
        <button @click="convert()">Конвертировать</button>
        <button @click="favourite()" className="fav-button">В избранное</button>
    </div>
</template>

<script>
    export default {
        props:{
            changeAmount: {
                type: Function,
                required: true
            },
            convert: {
                type: Function,
                required: true
            },
            favourite: {
                type: Function,
                required: true
            }
        },

    }
</script>

<style scoped>
.input-wrapper {
    display: flex;
    flex-direction: column;
    align-items: center; /* центровка по горизонтали */
    gap: 15px; /* расстояние между инпутом и кнопкой */
}

input{
    outline: none;
    width: 500px;
    font-size: 1.2em;  
    border-radius: 3px;
    border: 0;
    padding: 10px 15px;
    background: #fafafa;
    color: #333;
}

button {
    padding: 15px 20px;
    color: #fff;
    text-transform: uppercase;
    cursor: pointer;
    background: #1A032d;
    border: 0;
    border-radius: 3px;
}

button.fav-button {
    margin-left: 20px;
}

</style>

