<script>
export default {
    render(h){
        return h(
            'div',{
                'attrs':{
                    class:'render-card'
                },
            },[
                h('header',{
                    'attrs':{
                        class:'card-header card-header-title'
                    },
                },this.message)
            ]
        )
    },
    props:{
        message:String
    }
}
</script>
