<template>
    <div class="center">
        <div>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ad aliquid architecto atque beatae, cumque
            deserunt, dolor dolorem eius eos est fugiat harum id labore laborum magnam molestiae necessitatibus
            neque nesciunt nulla, numquam odit officia perspiciatis provident quaerat quas qui quibusdam quidem quos
            sit soluta suscipit temporibus unde voluptatem. Cum dolorem quod recusandae soluta tempore! A, at
            cupiditate deleniti eaque eos excepturi iste itaque neque porro quasi rem vel, voluptas? Aut
            consequuntur delectus earum eos ex facere fuga fugiat harum in ipsam iste labore, laudantium magnam
            molestias optio quibusdam quis recusandae, sapiente tempora veniam? Ad dolore facilis fugiat, laboriosam
            magnam necessitatibus nobis porro sed voluptate voluptates! Ad adipisci aliquid animi assumenda
            consequatur dolorem dolorum error eum, fugit hic inventore nam necessitatibus nihil omnis praesentium
            quo rem, saepe sint vitae voluptates. Ex inventore libero molestias quo veritatis. Cupiditate, enim
            explicabo harum minus officiis quo ratione tenetur? Amet facilis recusandae rem veritatis voluptates.
        </div>
    </div>
</template>

<script>
</script>

<style lang="scss" scoped>
    .center {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        z-index: -1;

        div {
            padding-top: 5rem;
            max-width: 400px;
        }
    }

    @media screen and (max-width: 550px) {
        .center {
            padding: 0 30px;
        }
    }
</style>
