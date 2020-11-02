<template>
    <div class="card">
        <img :src="require('~/assets/' + thumbnail)" alt="thumbnail" class="image" />
        <div class="card-content">
            <div class="title">
                <span class="text">
                    {{title}}
                </span>
                <div v-if="tags.length > 0" class="tag-box">
                    <div v-for="(tag, i) in tags" :key="i" class="tag">
                        <span>{{tag}}</span>
                    </div>
                </div>
            </div>
            <div v-if="description != undefined" class="description">
                {{description}}
            </div>
            <div  v-if="infomations != undefined" class="infomations">
                <table>
                    <tr v-for="(infomation, i) in infomations" :key="i">
                        <td class="title">{{infomation.title}}</td>
                        <td>{{infomation.data}}</td>
                    </tr>
                </table>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ["thumbnail", "title", "tags", "description","infomations"]
}
</script>

<style scoped>
.card{
    background: #ffffff;
    width: 420px;
}
.image{
    background: #6F7C8C;
}
.card-content{
    padding: 20px;
}
.title{
    display: flex;
}
.text{
    font-size: 16px;
    color: #0F2540;
    font-weight: 700;
}
.tag-box{
    display: flex;
    margin-left: 10px;
}
.tag{
    margin-left: 10px;
    height: 24px;
    line-height: 20px;
    background: #C9E1EC;
    border: 1px solid #3A8FB7;
    border-radius: 2px;
    padding: 0 8px 0 8px;
}
.tag span{
    font-size: 12px;
    color: #3A8FB7;
}
.description{
    color: #0F2540;
    font-size: 14px;
    margin-top: 16px;
}
.infomations{
    margin-top: 12px;
}
.infomations td{
    font-size: 12px;
    color: #6F7C8C;
}
.infomations .title{
    width: 130px;
}
</style>