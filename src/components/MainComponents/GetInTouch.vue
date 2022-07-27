<template>
  <section id="get-touch">
    <div class="container flex-center">
        <div class="row col-10">
            <div class="col-7 infos">
                    <h6 class="text-uppercase">
                        send a message
                    </h6>
                    <h1 class="fw-bold py-4">
                        get in
                        <span>touch</span>
                    </h1>
                    <p>
                        We will responde to your message as soon as possible.
                    </p>
                </div>
        </div>
    </div>
  </section>
</template>

<script>
export default {
    name: 'GetInTouch',
}
</script>

<style lang="scss">
    @import '../../scss/style.scss';

    #get-touch{
        padding: 7rem;
        .infos{
            h1{
                text-transform: capitalize;
            }
            span{
                @include companyStyledWord;
            }
            h6{
                color: $CcBluelagoon;
                font-size: .8rem;
            }
            p{
                color: $CcPumice;
            }
        }
    }

</style>