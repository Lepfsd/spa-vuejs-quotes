<template>
    <div>
        <form>
            <div class="row">
                    <div class="col-xs-12 col-md-6">
                        <div class="form-group">
                                <label>Quote</label>
                                <textarea class="form-control" rows="3" v-model="quote"></textarea>      
                        </div>
                        <div class="form-group">
                                <button class="btn btn-primary" @click.prevent="createNew">add quote</button>      
                        </div>   
                    </div>  
                
            </div>
        </form> 
    </div>
</template>
<script>
export default {
  data: function(){
      return {
          quote: ''
      };
  },
  methods: {
      createNew(){
          this.$emit('quoteAdded', this.quote);
          this.quote = '';
      }
  }
}
</script>

<style>

</style>


