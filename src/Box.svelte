<main>
    <div class="box">
        <slot></slot>
    </div>
</main>

<style>
    .box {
        text-align: center;
        position: absolute;
        top: 60%;
        left: 50%;
        transform: translate(-50%, -60%);
    }
</style>
