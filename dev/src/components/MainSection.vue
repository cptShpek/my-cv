<template>

    <div>

        <table>
            <tr>
                <td><img src="./img/photo.png" width="200"></td>
                <td>
                    <h1>Ihor Shapovalov</h1>
                    <table>
                        <tr>
                            <td>Date of birth</td>
                            <td>-</td>
                            <td>03 jan 1997</td>
                        </tr>
                        <tr>
                            <td>City</td>
                            <td>-</td>
                            <td>Kyiv</td>
                        </tr>
                        <tr>
                            <td>Contact</td>
                            <td>-</td>
                            <td>+380500545013</td>
                        </tr>
                        <tr>
                            <td>E-mail</td>
                            <td>-</td>
                            <td>tarzansh1397@gmail.com</td>
                        </tr>
                    </table>
                </td>
            </tr>
        </table>
        
    </div>

</template>

<script>
export default {
    name:'MainSection'
}
</script>

<style scoped>
    .main{
        display: flex;
        justify-content: space-between;
    }
    h1 + table{
        border-style: dotted;
        background-color: bisque;
    }
</style>