<template>
  <div class="p-0">
    <div class="p-0 bg-dark text-light">
      <div class="container-fluid">
        <div class="row">
          <div class="col-md-12">
            <h4 class=""><u><b>Node Info</b></u></h4>
          </div>
        </div>
      </div>
    </div>
    <div class="p-0">
      <div class="container-fluid">
        <div class="row">
          <div class="col-md-12">
            <div class="card">
              <div class="card-header"> Etherbase Address</div>
              <div class="card-body">
                <blockquote class="blockquote mb-0">
                  <p>{{gethnode.data.coinbaseAddress}}</p>
                </blockquote>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="m-0 p-2" style="">
      <div class="container-fluid">
        <div class="row">
          <div class="col-md-4" style="">
            <h5 class="" style="" contenteditable="true">Sync Info</h5>
            <div class="table-responsive">
              <table class="table">
                <thead>
                  <tr></tr>
                </thead>
                <tbody>
                  <tr>
                    <td>currentBlock</td>
                    <td>{{gethnode.data.syncInfo.currentBlock}}</td>
                  </tr>
                  <tr>
                    <td>highestBlock</td>
                    <td>{{gethnode.data.syncInfo.highestBlock}}</td>
                  </tr>
                  <tr>
                    <td>knownStates</td>
                    <td>{{gethnode.data.syncInfo.knownStates}}</td>
                  </tr>
                  <tr>
                    <td>pulledStates</td>
                    <td>{{gethnode.data.syncInfo.pulledStates}}</td>
                  </tr>
                  <tr>
                    <td>startingBlock</td>
                    <td>{{gethnode.data.syncInfo.startingBlock}}</td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>
          <div class="col-md-4" style="">
            <h5 class="" style="">Last Block Info</h5>
            <div class="table-responsive">
              <table class="table">
                <thead>
                  <tr></tr>
                </thead>
                <tbody>
                  <tr>
                    <td>hash</td>
                    <td>{{gethnode.data.lastBlockInfo.hash}}</td>
                  </tr>
                  <tr>
                    <td>timestamp</td>
                    <td>{{gethnode.data.lastBlockInfo.timestamp}}</td>
                  </tr>
                  <tr>
                    <td>difficulty</td>
                    <td>{{gethnode.data.lastBlockInfo.difficulty}}</td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>
          <div class="col-md-4" style="">
            <h5 class="">Accounts</h5>
            <div class="table-responsive">
              <table class="table">
                <thead>
                  <tr>
                    <th>Account</th>
                    <th>Balance</th>
                  </tr>
                </thead>
                <tbody>
                  <tr v-for="balance in gethnode.data.balances" v-bind:key="balance.account">
                    <td>{{balance.account}}</td>
                    <td>{{balance.balance}}</td>
                  </tr>
                </tbody>
              </table>
            </div>
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
      gethnode: null
    }
  },
  mounted () {
    axios
      .get('http://localhost/node-info')
      .then(response => (this.gethnode = response))
  }
})
</script>
