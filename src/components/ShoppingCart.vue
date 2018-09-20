<script>
import { mapState, mapMutations, mapGetters } from "vuex"
import CartLine from "./ShoppingCartLine"

export default {
    components: { CartLine },
    computed: {
        ...mapState({ lines: state => state.cart.lines }),
        ...mapGetters({ totalPrice: "cart/totalPrice" })
    },
    methods: {}
}
</script>
