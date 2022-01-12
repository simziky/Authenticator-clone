<template>
  <div class="wallet-main">

    <div class="wallet-banner">INTEGRATE WALLET</div>
          <div class="gallery-heading"><h1>Choose your wallet</h1></div>
    <div class="wallet-gallery">
              
                <div v-for="item in image_items" :key="item"  class="wallet-gallery-inner" @click="log">
                     <router-link :to=" `/connect?title=${item.title}`"  class="wallet-link"> 
                     
                      <img  :src="item.image_path"  alt="" />
                        <h4>{{item.title}} </h4> 
                        </router-link>
                </div>
        </div>

  </div>
</template>

<script>
export default {

    methods:{
     
    },


    data(){
      return{
        image_items:[

          {
            image_path : require("@/assets/img/rainbow.jpg"),
                title: "Rainbow",
          },
          {
            image_path : require("@/assets/img/ronin.png"),
                title: "Ronin Wallet",
          },
           {
            image_path : require("@/assets/img/icontex.png"),
                title: "Icontex",
          },
          {
            image_path : require("@/assets/img/trust.png"),
                title: "Trust Wallet",
          },
         
          {
            image_path : require("@/assets/img/ledger.png"),
                title: "Ledger Wallet",
          },
          {
            image_path : require("@/assets/img/metamask.jpg"),
                title: "MetaMask",
          },
          {
            image_path : require("@/assets/img/walletconnect.jpg"),
                title: "WalletConnect",
          },
          {
            image_path : require("@/assets/img/gnosis.png"),
                title: "Gnosis Safe",
          },
          {
            image_path : require("@/assets/img/binance.png"),
                title: "Binance",
          },
          {
            image_path : require("@/assets/img/defi.png"),
                title: "DeFI Wallet",
          },
          {
            image_path : require("@/assets/img/harmony.jpg"),
                title: "Harmony Wallet",
          },
          {
            image_path : require("@/assets/img/solaris.jpg"),
                title: "Solaris",
          },
          {
            image_path : require("@/assets/img/keplr.jpg"),
                title: "Keplr Wallet",
          },
          {
            image_path : require("@/assets/img/pillar.png"),
                title: "Pillar",
          },
          {
            image_path : require("@/assets/img/imtoken.jpg"),
                title: "imToken",
          },
          {
            image_path : require("@/assets/img/onto.jpeg"),
                title: "ONTO",
          },
          {
            image_path : require("@/assets/img/coinbase.png"),
                title: "Coinbase",
          },
          {
            image_path : require("@/assets/img/fortmatic.jpg"),
                title: "Fortmatic",
          },
          {
            image_path : require("@/assets/img/samourai.png"),
                title: "Samourai",
          },
          {
            image_path : require("@/assets/img/tokenpocket.jpg"),
                title: "TokenPocket",
          },
          {
            image_path : require("@/assets/img/mathwallet.png"),
                title: "MathWallet",
          },
          {
            image_path : require("@/assets/img/bitpay.jpg"),
                title: "BitPay",
          },
          {
            image_path : require("@/assets/img/ledgerlive.jpg"),
                title: "Ledger Live",
          },
          {
            image_path : require("@/assets/img/authereum.png"),
                title: "Authereum",
          },
          {
            image_path : require("@/assets/img/avalanche.png"),
                title: "Avalanche",
          },
          {
            image_path : require("@/assets/img/terra.png"),
                title: "Terra Wallet",
          },
          {
            image_path : require("@/assets/img/matic.jpg"),
                title: "Matic Wallet",
          },
          {
            image_path : require("@/assets/img/dharma.jpg"),
                title: "Dharma",
          },
          {
            image_path : require("@/assets/img/inch.png"),
                title: "1inch Wallet",
          },
          {
            image_path : require("@/assets/img/huobi.jpg"),
                title: "Huobi Wallet",
          },
          {
            image_path : require("@/assets/img/eidoo.png"),
                title: "eidoo",
          },
          {
            image_path : require("@/assets/img/mykey.jpg"),
                title: "MYKEY",
          },
          {
            image_path : require("@/assets/img/loopring.jpg"),
                title: "Loopring",
          },
          {
            image_path : require("@/assets/img/trustvault.jpg"),
                title: "TrustVault",
          },
          {
            image_path : require("@/assets/img/atomic.png"),
                title: "Atomic",
          },
          {
            image_path : require("@/assets/img/coin98.jpg"),
                title: "Coin98",
          },
          {
            image_path : require("@/assets/img/coolwallet.png"),
                title: "CoolWallet S",
          },
          {
            image_path : require("@/assets/img/alice.png"),
                title: "Alice",
          },
          {
            image_path : require("@/assets/img/alpha.jpg"),
                title: "AlphaWallet",
          },
          {
            image_path : require("@/assets/img/dcent.png"),
                title: "D'cent",
          },
          {
            image_path : require("@/assets/img/zelcore.png"),
                title: "ZelCore",
          },
          {
            image_path : require("@/assets/img/nash.png"),
                title: "Nash",
          },
          {
            image_path : require("@/assets/img/cybavo.png"),
                title: "CYBAVO",
          },
          {
            image_path : require("@/assets/img/coinomi.png"),
                title: "Coinomi",
          },
          {
            image_path : require("@/assets/img/gridplus.png"),
                title: "GridPlus",
          },
          {
            image_path : require("@/assets/img/tokenary.jpg"),
                title: "Tokenary",
          },
          {
            image_path : require("@/assets/img/torus.png"),
                title: "Torus",
          },
          {
            image_path : require("@/assets/img/spatium.jpeg"),
                title: "Spatium",
          },
          {
            image_path : require("@/assets/img/safepal.png"),
                title: "SafePal",
          },
          {
            image_path : require("@/assets/img/infinito.png"),
                title: "Infinito",
          },
          {
            image_path : require("@/assets/img/infinity.jpg"),
                title: "Infinity Wallet",
          },
          {
            image_path : require("@/assets/img/ownbit.jpg"),
                title: "Ownbit",
          },
          {
            image_path : require("@/assets/img/easypocket.jpg"),
                title: "EasyPocket",
          },
          {
            image_path : require("@/assets/img/bridge.jpg"),
                title: "Bridge Wallet",
          },
          {
            image_path : require("@/assets/img/sparkpoint.jpg"),
                title: "SparkPoint",
          },
          {
            image_path : require("@/assets/img/viawallet.jpg"),
                title: "ViaWallet",
          },
          {
            image_path : require("@/assets/img/bitkeep.jpg"),
                title: "BitKeep",
          },
          {
            image_path : require("@/assets/img/vision.jpg"),
                title: "Vision",
          },
          {
            image_path : require("@/assets/img/peakdefi.jpg"),
                title: "PEAKDEFI",
          },
          {
            image_path : require("@/assets/img/unstoppable.jpg"),
                title: "Unstoppable",
          },
          {
            image_path : require("@/assets/img/halodefi.jpg"),
                title: "HaloDefi Wallet",
          },
          {
            image_path : require("@/assets/img/dok.png"),
                title: "Dok Wallet",
          },
          {
            image_path : require("@/assets/img/midas.png"),
                title: "Midas Wallet",
          },
          {
            image_path : require("@/assets/img/ellipal.jpg"),
                title: "Ellipal",
          },
          {
            image_path : require("@/assets/img/kyberswap.jpg"),
                title: "KyberSwap",
          },
          {
            image_path : require("@/assets/img/atoken.jpg"),
                title: "AToken Wallet",
          },
          {
            image_path : require("@/assets/img/tonguewallet.jpg"),
                title: "Tongue Wallet",
          },
          {
            image_path : require("@/assets/img/keyringpro.jpg"),
                title: "KEYRING PRO",
          },
          {
            image_path : require("@/assets/img/talken.jpg"),
                title: "Talken Wallet",
          },
          {
            image_path : require("@/assets/img/xinfin.png"),
                title: "Xinfin XDC",
          },
          {
            image_path : require("@/assets/img/rwallet.png"),
                title: "RWallet",
          },
          {
            image_path : require("@/assets/img/plasmapay.jpg"),
                title: "PlasmaPay",
          },
          {
            image_path : require("@/assets/img/o3wallet.jpg"),
                title: "O3Wallet",
          },
          {
            image_path : require("@/assets/img/jade.jpg"),
                title: "Jade Wallet",
          },
          {
            image_path : require("@/assets/img/guarda.jpg"),
                title: "Guarda Wallet",
          },
          {
            image_path : require("@/assets/img/defiant.jpg"),
                title: "Defiant",
          },
          {
            image_path : require("@/assets/img/trustee.jpg"),
                title: "Trustee Wallet",
          },
          {
            image_path : require("@/assets/img/coinus.jpg"),
                title: "CoinUs",
          },
          {
            image_path : require("@/assets/img/cmorq.png"),
                title: "cmorq",
          },
          {
            image_path : require("@/assets/img/valora.jpg"),
                title: "Valora",
          },
          {
            image_path : require("@/assets/img/quiverx.png"),
                title: "QuiverX",
          },
          {
            image_path : require("@/assets/img/celo.png"),
                title: "Celo Wallet",
          },
          {
            image_path : require("@/assets/img/cleo.jpg"),
                title: "Cleo",
          },
          {
            image_path : require("@/assets/img/atari.png"),
                title: "Atari Wallet",
          },
          {
            image_path : require("@/assets/img/daedalus.png"),
                title: "Daedalus Wallet",
          },
          {
            image_path : require("@/assets/img/mobox.png"),
                title: "Mobox",
          },
          {
            image_path : require("@/assets/img/neoline.jpg"),
                title: "Neoline",
          },
          {
            image_path : require("@/assets/img/revolut.png"),
                title: "Revolut Wallet",
          },
          {
            image_path : require("@/assets/img/xdefi.png"),
                title: "XDefi",
          },
          {
            image_path : require("@/assets/img/callisto.png"),
                title: "Callisto Wallet",
          },

        ]

      }
    }

}
</script>

<style>

</style>