<template>
  <div class="hello">
    <div class="py-3 text-center" style="">
      <div class="container">
        <div class="row">
          <div class="col-md-12">
            <form class="form-inline">
              <div class="input-group w-100">
                <input type="text" class="form-control form-control-sm" placeholder="Contract Address">
                <div class="input-group-append"><button class="btn btn-primary" type="button">Get Info</button></div>
              </div>
            </form>
          </div>
        </div>
      </div>
      <div class="container">
        <div class="row">
          <div class="col-lg-4 col-md-6 p-4">
            <h4><b>Name (symbol)</b><br></h4>
            <p>{{contract.data.name}} ({{contract.data.symbol}})</p>
          </div>
          <div class="col-lg-4 col-md-6 p-4">
            <h4>Current Balance</h4>
            <p>{{contract.data.balanceOfTokens}}</p>
          </div>
          <div class="col-lg-4 col-md-6 p-4">
            <h4>Total Supply</h4>
            <p>{{contract.data.totalSupply}}</p>
          </div>
          <div class="col-lg-4 col-md-6 p-4">
            <h4>Decimals</h4>
            <p>{{contract.data.decimals}}</p>
          </div>
          <div class="col-lg-4 col-md-6 p-4">
            <h4> <b>Contract Address</b></h4>
            <p>{{contract.data.address}}</p>
          </div>
          <div class="col-lg-4 col-md-6 p-4">
            <h4>Owner Address</h4>
            <p>{{contract.data.owner}}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default ({

  data () {
    return {
      contract: null
    }
  },
  mounted () {
    axios
      .get('http://localhost/basic-info')
      .then(response => (this.contract = response))
  }
})
</script>
