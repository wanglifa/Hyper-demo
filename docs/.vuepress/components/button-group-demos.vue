<template>
    <div class="contentWrapper">
        <div class="componentsMessage">
            <hy-button-group>
                <hy-button icon="left">上一页</hy-button>
                <hy-button>更多</hy-button>
                <hy-button icon="right" icon-postition="right">下一页</hy-button>
            </hy-button-group>
            <hy-spread >
                <pre v-if="showCode"><code>{{content}}</code></pre>
            </hy-spread>
        </div>
        <div class="dispalyCode" @click="showCode=!showCode">▼ <span>显示代码</span></div>
    </div>
</template>

<script>
    import ButtonGroup from '../../../src/ButtonGroup.vue'
    import Button from '../../../src/Button.vue'
    import Spread from '../../../src/Spread.vue'

    export default {
        components:{
            'hy-button-group': ButtonGroup,
            'hy-button':Button,
            'hy-spread':Spread
        },
        data(){
            return {
                content:
`
<hy-button-group>
    <hy-button icon="left">上一页</hy-button>
    <hy-button>更多</hy-button>
    <hy-button icon="right" icon-postition="right">下一页</hy-button>
</hy-button-group>`.trim(),
                showCode:false
            }
        }
    }
</script>

<style lang="scss" scoped>
@import './main.scss';
</style>
