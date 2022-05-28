<template>
    <div class="blocca" :class="domanda == '1' ? 'visible' : '' ">
        <div class="container">
            <div class="popup">
                <h1>Domanda</h1>
                <h4>Ciao come stai?</h4>
                <button class="si">Si</button>
                <button class="no">No</button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Domande',
    props: {
        domanda: String
    },
}
</script>

<style lang="scss" scoped>
.blocca{
    display: none;
    position: absolute;
    top: -60px;
    left: 0;
    margin: 0;
    width: 100%;
    height: 100vh;

    .container{
        width: 600px;
        height: 400px;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        background-color: cadetblue;
        border: 1px solid blue;
        padding: 30px;

        .popup{
            text-align: center;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);

            h1{
                margin: 10px;
            }

            h4{
                margin: 40px;
            }

            .si, .no{
                padding: 20px;
                margin: 20px;
                border: none;
                cursor: pointer;

                &:hover{
                    scale: 1.1;
                }

                &:active{
                    border: 2px solid black;
                }
            }

            .si{
                background-color: lime;
            }

            .no{
                background-color: red;
            }
        }
    }
}

.visible{
    display: block;
}
</style>