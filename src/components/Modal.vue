<template>
    <div id="backdrop">
        <div class="modal">
            <p>Modal Content</p>
        </div>
    </div>
</template>


<style>
    .modal{
        width: 400px;
        padding: 10px;
        margin: 100px;
        background-color: white;
        border-radius:10px;
    }
    .backdrop{
        top: 0px;
        position: fixed;
        background: rgba(0, 0, 0, 0.5);
        width: 100%;
        height: 100%;
    }
</style>