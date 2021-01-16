<template>
    <table>
        <tr>
            <th></th>
            <th> Strongly disagree <br><br> 1 </th>
            <th> <br><br><br> 2 </th>
            <th> Disagree <br><br><br> 3 </th>
            <th> <br><br><br> 4 </th>
            <th> Neither agree nor disagree <br> 5 </th>
            <th> <br><br><br> 6 </th>
            <th> Agree <br><br><br> 7 </th>
            <th> <br><br><br> 8 </th>
            <th> Strongly agree <br><br> 9 </th>
        </tr>
        <tr class="row">
            <td><span>The teacher allowed us to pursue our own interests</span>
            <span class="icon has-text-danger" title="Please answer this question"><i class="fas fa-exclamation-circle"></i></span>
        </td>
        <td style="width: 70px;"><label class="radio"><input type="radio" name="36" value="1"></label></td>
        <td style="width: 70px;"><label class="radio"><input type="radio" name="36" value="2"></label></td>
        <td style="width: 70px;"><label class="radio"><input type="radio" name="36" value="3"></label></td>
        <td style="width: 70px;"><label class="radio"><input type="radio" name="36" value="4"></label></td>
        <td style="width: 70px;"><label class="radio"><input type="radio" name="36" value="5"></label></td>
        <td style="width: 70px;"><label class="radio"><input type="radio" name="36" value="6"></label></td>
        <td style="width: 70px;"><label class="radio"><input type="radio" name="36" value="7"></label></td>
        <td style="width: 70px;"><label class="radio"><input type="radio" name="36" value="8"></label></td>
        <td style="width: 70px;"><label class="radio"><input type="radio" name="36" value="9"></label></td>
        </tr>
        <tr class="row">
            <td><span>Students were encouraged to openly express ideas</span>
            <span class="icon has-text-danger" title="Please answer this question"><i class="fas fa-exclamation-circle"></i></span>
        </td>
        <td style="width: 70px;"><label class="radio"><input type="radio" name="37" value="1"></label></td>
        <td style="width: 70px;"><label class="radio"><input type="radio" name="37" value="2"></label></td>
        <td style="width: 70px;"><label class="radio"><input type="radio" name="37" value="3"></label></td>
        <td style="width: 70px;"><label class="radio"><input type="radio" name="37" value="4"></label></td>
        <td style="width: 70px;"><label class="radio"><input type="radio" name="37" value="5"></label></td>
        <td style="width: 70px;"><label class="radio"><input type="radio" name="37" value="6"></label></td>
        <td style="width: 70px;"><label class="radio"><input type="radio" name="37" value="7"></label></td>
        <td style="width: 70px;"><label class="radio"><input type="radio" name="37" value="8"></label></td>
        <td style="width: 70px;"><label class="radio"><input type="radio" name="37" value="9"></label></td>
        </tr>
    </table>
</template>

<script>
export default {
  name: 'SurveyTable'
}
</script>

<style scoped>
    table td:first-child {
        border-right: solid #dbdbdb 1px;
    }

    table th:first-child {
        border-right: solid #dbdbdb 1px;
    }

    th {
        background-color: #fff;
        text-align: center !important;
    }

    td{
        border-top: 1px solid #dbdbdb;
        border-bottom: 1px solid #dbdbdb;
    }

    tr:nth-child(odd) {
        background-color: #ececec;
    }

    tr:hover {
        background-color: #ececec;
    }
</style>
