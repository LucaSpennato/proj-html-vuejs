<template>
  <section>
    <div class="container">
        <div class="row justify-content-between">
            <div class="row col-9 m-auto justify-content-between">
                <div class="col-4">
                    Enjoy the low price. We are tracking any intention of privacy.
                </div>
                <div class="col-4 text-capitalize text-end">
                    &copy; 2020 NEXGEN is proudly powered by <a href="#">Codings.</a>
                </div>
            </div>
            <div class="col-1 text-end">
                <a href="#headTopSection"><i class="bi bi-arrow-up-short"></i></a>
            </div>

        </div>
    </div>
  </section>
</template>

<script>
export default {
    name: 'BottomSection',
}
</script>

<style lang="scss" scoped>
    @import '../../scss/style.scss';
    section{
        background-color: black;
        padding: 1rem;
        color: $CcPumice;
        font-size: .7rem;
        a{
            color: $CcBluelagoon;
            text-decoration: none;
        }
        i{
            padding: .1rem .3rem;
            color: black;
            border-radius: 50%;
            font-size: 1.5rem;
            background-color: $McShark;
        }
    }
</style>