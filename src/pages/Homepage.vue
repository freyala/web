<template>
  <main>
    <section id="section-1">
      <div class="diagonal-1">
        <div style="background: url('/images/SVG/homepage-bg-top.svg') no-repeat top right;">
          <div class="container mx-auto pt-32 flex flex-wrap">
            <div class="w-full lg:w-1/2 pt-48 pb-24">
              <h2 class="text-2xl lg:text-5xl font-thin pr-24">
                A fast and low-cost token built on the <span
                  class="font-semibold text-primary-alt">Harmony Blockchain</span>.
              </h2>

              <br>

              <p class="text-xl lg:text-4xl font-thin my-8">
                <span class="font-semibold">GameFi Crossing ($XYA)</span> is an HRC-20 token centered around integrating
                cryptocurrency in the form of gamified NFTs and decentralized applications.
              </p>

              <br>
              <router-link :to="{ name: 'get-xya' }">
                <button
                    class="uppercase bg-gradient-to-r from-primary to-secondary py-4 px-8 rounded-md text-white text-lg lg:text-xl text-semibold">
                  Ways to get XYA
                </button>
              </router-link>
            </div>
            <div class="w-full">
              <a class="flex" href="#section-2">
                <img class="w-16 mx-auto" src="/images/SVG/go-down.svg" alt="Scroll down">
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="section-2" class="mt-20">
      <div class="diagonal-2 pt-20">
        <div class="container mx-auto flex flex-wrap">
          <div class="w-full lg:w-1/2 ml-auto">
            <p class="text-2xl lg:text-5xl font-thin lg:pr-8">
              Creating a <span class="font-semibold text-primary-alt">beginner-friendly</span> means of using crypto.
            </p>
            <br>
            <p class="text-2xl lg:text-4xl font-thin my-8">
              The idea behind this project is to create a beginner-friendly means of using crypto with the power of
              low-cost and fast transactions on the Harmony blockchain.
              <br>
              <br>
              To start, we have launched an interactive app to enter the GameFi Crossing world.
            </p>
          </div>
        </div>
        <div class="relative flex flex-wrap bg-black lg:bg-transparent mt-12 lg:mt-0">
          <div class="container mx-auto pt-12 lg:pt-96">
            <div class="w-full lg:w-1/2 lg:pr-12">
              <p class="text-3xl lg:text-5xl font-thin my-8 text-white">
                Go to battle with your <span class="font-semibold text-primary-alt">Harmons!</span>
              </p>
              <br>
              <p class="text-2xl lg:text-4xl font-thin my-8 text-white">
                The core part of this ecosystem is CryptIDs, which are effectively monster collectible NFTs that players
                can purchase, trade and battle others with.
              </p>
            </div>
          </div>

          <div class="w-full lg:w-1/2 lg:absolute bottom-0 right-0">
            <img src="/images/PNG/harmons.png" alt="Harmons">
          </div>
        </div>

        <div class="container ml-auto flex flex-wrap mt-8 lg:mt-32 px-8 lg:px-24 py-12 bg-white rounded-l-3xl">
          <p class="text-3xl lg:text-5xl font-thin w-full">
            <span class="font-semibold text-primary-alt">GameFi Crossing</span> by the numbers:
          </p>

          <div class="w-full lg:w-1/2 lg:w-1/4 mt-12 text-center">
            <p class="text-3xl lg:text-5xl font-bold text-primary-alt">
              {{
                $store.getters.loadingPrice ? 'Fetching...' : $store.getters.tokenSupply.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",")
              }}
            </p>
            <p class="text-xl lg:text-3xl uppercase">
              Total token supply
            </p>
            <br>
            <hr>
            <br>
            <p class="text-3xl lg:text-5xl font-bold text-primary-alt">
              {{
                $store.getters.loadingPrice ? 'Fetching...' : $store.getters.graveyard.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",")
              }}
            </p>
            <p class="text-xl lg:text-3xl uppercase">
              Tokens burnt
            </p>
            <br>
            <hr>
            <br>
            <p class="text-3xl lg:text-5xl font-bold text-primary-alt">
              $ {{ $store.getters.loadingPrice ? 'Fetching...' : parseFloat($store.getters.price).toFixed(3) }}
            </p>
            <p class="text-xl lg:text-3xl uppercase">
              Current price
            </p>
          </div>

          <div class="w-full lg:w-3/4 mt-12 lg:pl-20">
            <ul class="text-xl lg:text-3xl font-thin">
              <li>150M - In-game rewards</li>
              <li>52M - Upcoming partnerships, farming and casino</li>
              <li>21M - Community projects, events, hackathons and bounties</li>
              <li>15M - Initial coin offering</li>
              <li>4.5M - Development fund</li>
              <li>2.5M - Seed fund investors (span over a year)</li>
              <li>1M - Faucet fund</li>
            </ul>
          </div>

          <div class="w-full lg:w-1/4 mt-12">
            <div class="flex">
              <img class="my-auto w-20 inline" src="/images/SVG/arrow-right.svg" alt="Arrow right">
              <span class="uppercase ml-4 text-2xl font-semibold text-primary-alt">
                <router-link :to="{ name: 'chart' }">
                  See live chart
                </router-link>
              </span>
            </div>
          </div>
          <div class="w-full lg:w-3/4 mt-12 pl-20">
            <!--            <div class="flex">-->
            <!--              <img class="my-auto w-20 inline" src="/images/SVG/arrow-right.svg" alt="Arrow right">-->
            <!--              <span class="uppercase ml-4 text-2xl font-semibold text-primary-alt">-->
            <!--                More on GameFi Crossing tokenomics-->
            <!--              </span>-->
            <!--            </div>-->
          </div>
        </div>

        <div class="container mx-auto py-24 flex flex-wrap">
          <p class="w-full text-3xl lg:text-5xl text-white text-center">
            <span class="font-semibold text-primary-alt">
              Get XYA
            </span>
            from these DEXes built on the Harmony Blockchain:
          </p>

          <div class="w-full lg:w-1/3 flex flex-wrap mt-16">
            <div class="flex w-full">
              <img class="h-24 xl:h-48 mx-auto" src="/images/SVG/viperswap.svg" alt="Viperswap">
            </div>
            <div class="flex mt-8 mx-auto">
              <a href="https://viperswap.one/#/swap?outputCurrency=0x9b68bf4bf89c115c721105eaf6bd5164afcc51e4"
                 target="_blank">
                <img class="my-auto w-10 xl:w-20 inline" src="/images/SVG/arrow-right-white.svg" alt="Arrow right">
                <span class="uppercase ml-4 text-2xl font-semibold text-primary-alt">
                  Viperswap
                </span>
              </a>
            </div>
          </div>
          <div class="w-full lg:w-1/3 flex flex-wrap mt-16">
            <div class="flex w-full">
              <img class="h-24 xl:h-48 mx-auto" src="/images/SVG/dfk.png" alt="Defi Kingdoms">
            </div>
            <div class="flex mt-8 mx-auto">
              <a href="https://game.defikingdoms.com/#/" target="_blank">
                <img class="my-auto w-10 xl:w-20 inline" src="/images/SVG/arrow-right-white.svg" alt="Arrow right">
                <span class="uppercase ml-4 text-2xl font-semibold text-primary-alt">
                  Defi Kingdoms
                </span>
              </a>
            </div>
          </div>
          <div class="w-full lg:w-1/3 flex flex-wrap mt-16">
            <div class="flex w-full">
              <img class="h-24 xl:h-48 mx-auto" src="/images/SVG/lootswap.svg" alt="Lootswap">
            </div>
            <div class="flex mt-8 mx-auto">
              <a href="https://lootswap.finance/#/swap?outputCurrency=0x9b68bf4bf89c115c721105eaf6bd5164afcc51e4"
                 target="_blank">
                <img class="my-auto w-10 xl:w-20 inline" src="/images/SVG/arrow-right-white.svg" alt="Arrow right">
                <span class="uppercase ml-4 text-2xl font-semibold text-primary-alt">
                  Lootswap
                </span>
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="mt-12" id="section-i-2">
      <div class="container mx-auto py-12 lg:py-24">
        <div class="w-full xl:w-3/4">
          <p class="text-2xl lg:text-5xl font-extralight">
            What is GameFi Crossing <span class="font-semibold text-primary-alt">(XYA)</span> ?
          </p>

          <br>
          <br>

          <p class="text-xl lg:text-4xl font-extralight">
            GameFi Crossing ($XYA) is an HRC-20 token built on the Harmony blockchain.
            <br>
            <br>
            The idea behind this project is to create a beginner-friendly means of using crypto with the power of
            low-cost and fast transactions on the Harmony blockchain.
            <br>
            <br>
            The core part of this ecosystem is CryptIDs, which are effectively monster collectible NFTs that players can
            purchase, trade and battle others with.
          </p>
        </div>
        <div class="w-1/4"></div>
      </div>

      <div class="w-full h-2 bg-gradient-to-r from-primary to-secondary"></div>
    </section>

    <section id="section-i-3" class="bg-black pb-12 lg:pb-24">
      <div class="container mx-auto flex flex-wrap py-12 lg:py-24">
        <p class="text-white w-full font-extralight text-3xl lg:text-5xl">
          GameFi Crossing <span class="font-semibold text-primary-alt">Tokenomics</span>
        </p>

        <div class="w-full lg:w-3/4 mt-12 lg:pr-20">
          <ul class="text-xl lg:text-3xl text-white font-extralight">
            <li>150M - In-game rewards</li>
            <li>52M - Upcoming partnerships, farming and casino</li>
            <li>21M - Community projects, events, hackathons and bounties</li>
            <li>15M - Initial coin offering</li>
            <li>4.5M - Development fund</li>
            <li>2.5M - Seed fund investors (span over a year)</li>
            <li>1M - Faucet fund</li>
          </ul>
        </div>
        <div class="w-full lg:w-1/4 mt-12">
          <hr class="border-primary-alt">
          <br>
          <br>

          <p class="text-xl lg:text-2xl font-extralight text-primary-alt">
            Please note that the figures mentioned are subject to change depending on future burns.
            <br>
            <br>
            XYA is also non-mintable, meaning that there is a hard cap.
          </p>

          <br>
          <br>
          <hr class="border-primary-alt">
        </div>

        <div class="w-full flex flex-wrap mt-20 text-center">
          <div class="w-full lg:w-1/2 mb-4 lg:mb-0">
            <p class="text-3xl lg:text-6xl font-bold text-primary-alt">
              {{
                $store.getters.loadingPrice ? 'Fetching...' : $store.getters.tokenSupply.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",")
              }}
            </p>
            <p class="text-xl lg:text-3xl uppercase text-white mt-8">
              Total token supply
            </p>
          </div>
          <div class="w-full lg:w-1/2 mb-4 lg:mb-">
            <p class="text-3xl lg:text-6xl font-bold text-primary-alt">
              {{
                $store.getters.loadingPrice ? 'Fetching...' : $store.getters.currentSupply.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",")
              }}
            </p>
            <p class="text-xl lg:text-3xl uppercase text-white mt-8">
              Circulating token supply
            </p>
          </div>
          <div class="w-full lg:w-1/2 mb-4 lg:mb-0">
            <p class="text-3xl lg:text-6xl font-bold text-primary-alt">
              {{
                $store.getters.loadingPrice ? 'Fetching...' : $store.getters.graveyard.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",")
              }}
            </p>
            <p class="text-xl lg:text-3xl uppercase text-white mt-8">
              Tokens burnt
            </p>
          </div>
          <div class="w-full lg:w-1/2 mb-4 lg:mb-0">
            <p class="text-3xl lg:text-6xl font-bold text-primary-alt">
              $ {{ $store.getters.loadingPrice ? 'Fetching...' : parseFloat($store.getters.price).toFixed(3) }}
            </p>
            <p class="text-xl lg:text-3xl uppercase text-white mt-8">
              Current price
            </p>
          </div>
        </div>

        <div class="w-full my-auto text-center mt-12">
          <p class="text-white text-2xl">
            <span class="text-primary-alt cursor-pointer"
                  v-clipboard:copy="'0x9b68BF4bF89c115c721105eaf6BD5164aFcc51E4'">Contract address:</span> <br
              class="block lg:hidden"> <span
              style="word-break: break-all" class="cursor-pointer"
              v-clipboard:copy="'0x9b68BF4bF89c115c721105eaf6BD5164aFcc51E4'">0x9b68BF4bF89c115c721105eaf6BD5164aFcc51E4</span>
            <img src="/images/SVG/copy.svg" alt="Copy" class="inline pl-2 w-8">
          </p>
        </div>

      </div>

      <div
          class="container mx-auto flex flex-wrap p-8 lg:p-12 rounded-3xl bg-gradient-to-r from-primary to-secondary my-12">
        <div class="w-full lg:w-4/5 mx-auto text-center">
          <p class="text-5xl text-white font-extralight">
            Stay <span class="font-semibold">connected</span> and updated:
          </p>
          <br>
          <p class="text-2xl text-white font-extralight">
            The community is active on several different social media platforms, with Discord being the recommended and
            active place to stay updated and interact with the community.
          </p>
        </div>

        <div class="w-full mx-auto text-center">
          <div class="flex flex-wrap">
            <div class="w-full lg:w-1/4 flex flex-wrap mt-8 lg:mt-16 mb-8">
              <img class="h-12 lg:h-24 mx-auto mb-8" src="/images/SVG/discord.svg" alt="Discord">
              <div class="w-full">
                <a href="https://discord.gg/tKtr9GgzA6" target="_blank">
                  <img class="my-auto w-20 inline" src="/images/SVG/arrow-right-white.svg" alt="Arrow right">
                  <span class="uppercase ml-4 text-2xl font-semibold text-white">
                    Discord
                  </span>
                </a>
              </div>
            </div>
            <div class="w-full lg:w-1/4 flex flex-wrap mt-8 lg:mt-16 mb-8">
              <img class="h-12 lg:h-24 mx-auto mb-8" src="/images/SVG/twitter.svg" alt="Discord">
              <div class="w-full">
                <a href="https://twitter.com/gameficrossing" target="_blank">
                  <img class="my-auto w-20 inline" src="/images/SVG/arrow-right-white.svg" alt="Arrow right">
                  <span class="uppercase ml-4 text-2xl font-semibold text-white">
                    Twitter
                  </span>
                </a>
              </div>
            </div>
            <div class="w-full lg:w-1/4 flex flex-wrap mt-8 lg:mt-16 mb-8">
              <img class="h-12 lg:h-24 mx-auto mb-8" src="/images/SVG/telegram.svg" alt="Discord">
              <div class="w-full">
                <a href="https://t.me/gameficrossing" target="_blank">
                  <img class="my-auto w-20 inline" src="/images/SVG/arrow-right-white.svg" alt="Arrow right">
                  <span class="uppercase ml-4 text-2xl font-semibold text-white">
                    Telegram
                  </span>
                </a>
              </div>
            </div>
            <div class="w-full lg:w-1/4 flex flex-wrap mt-8 lg:mt-16 mb-8">
              <img class="h-12 lg:h-24 mx-auto mb-8" src="/images/SVG/reddit.svg" alt="Discord">
              <div class="w-full">
                <a href="https://www.reddit.com/r/XYA_Official/" target="_blank">
                  <img class="my-auto w-20 inline" src="/images/SVG/arrow-right-white.svg" alt="Arrow right">
                  <span class="uppercase ml-4 text-2xl font-semibold text-white">
                    Reddit
                  </span>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="mt-12" id="section-t-2">
      <div class="container mx-auto py-12 lg:py-24">
        <div class="w-full xl:w-3/4">
          <p class="text-2xl lg:text-5xl font-extralight">
            Team work makes the <span class="font-semibold text-primary-alt">dream</span> work.
          </p>

          <br>
          <br>

          <p class="text-2xl lg:text-4xl font-extralight">
            Behind GameFi Crossing is a handful of talented and committed individuals who contribute collaboratively and
            seamlessly to drive the project to success.
          </p>
        </div>
        <div class="w-1/4"></div>
      </div>

    </section>

    <section id="section-t-3" class="bg-black py-24 my-24">
      <div
          class="container mx-auto flex flex-wrap p-8 lg:p-12 rounded-3xl bg-gradient-to-r from-primary to-secondary my-12">
        <div class="w-full lg:w-4/5 mx-auto text-center">
          <p class="text-5xl text-white font-extralight">
            Say hello to us on <span class="font-semibold">Discord</span>!
          </p>
          <br>
          <p class="text-2xl text-white font-extralight lg:pr-32">
            You can find the team active on Discord. Feel free to pop in to chat or ask any questions about GameFi Crossing.
          </p>
        </div>

        <div class="w-full lg:w-1/3 mx-auto text-center">
          <div class="flex flex-wrap">
            <img class="w-32 mx-auto my-8" src="/images/SVG/discord.svg" alt="Discord">
            <div class="w-full">
              <a href="https://discord.gg/tKtr9GgzA6" target="_blank">
                <img class="my-auto w-20 inline" src="/images/SVG/arrow-right-white.svg" alt="Arrow right">
                <span class="uppercase ml-4 text-2xl font-semibold text-white">
                  Discord
                </span>
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="section-t-4" class="py-24">
      <div class="container mx-auto">
        <p class="text-3xl lg:text-7xl text-primary-alt font-semibold text-center">
          CryptIDs
        </p>

        <p class="text-2xl lg:text-5xl font-extralight mt-4 lg:mt-8 text-center">
          Stake. Unlock. Upgrade. Challenge.
        </p>

        <p class="text-xl lg:text-3xl w-full lg:w-4/5 mx-auto font-extralight mt-8 text-center">
          CryptIDs, also known as ‘Harmons’, are monster collectible NFTs created with distinctive properties, giving
          each one a unique combination of stats and abilities (hence different strengths and weaknesses). Some Harmons
          are simply stronger and more valuable.
        </p>

        <div class="flex flex-wrap my-12 lg:my-24 relative">
          <div class="w-full lg:w-1/2 opacity-20 lg:opacity-100 absolute top-0 left-0 lg:relative">
            <img src="/images/PNG/harmon-board-bg.png" alt="Harmons on board" style="max-width: 640px;">
          </div>
          <div class="z-10 w-full lg:w-1/2 text-center lg:text-left">
            <p class="text-3xl lg:text-5xl text-primary-alt font-semibold">
              Stake <span class="font-extralight"> & </span> Unlock
            </p>

            <br>

            <p class="text-2xl lg:text-3xl font-extralight">
              Users can slowly unlock more Harmons tokens by staking XYA, playing minigames and more upcoming ways.
              These tokens can be used to open booster packs containing a small number of monsters tentatively named
              Harmons.
            </p>

            <br>
            <br>

            <p class="text-3xl lg:text-5xl text-primary-alt font-semibold">
              Upgrade <span class="font-extralight"> your Harmons </span>
            </p>

            <br>

            <p class="text-2xl lg:text-3xl font-extralight">
              All Harmons will have their own unique forms and the following rarities: Common, Rare and
              Epic. Players will be able to upgrade their Harmons to the next rarity level by merging the same
              base creature multiple times. Some Harmons will have an extra rarity: Legendary.
              <br>
              <br>
              Legendary variants are limited to a certain group of Harmons and are relatively difficult to
              collect, with them being substantially more difficult to obtain or craft.
            </p>

            <br>
            <br>

            <p class="text-3xl lg:text-5xl text-primary-alt font-semibold">
              Challenge <span class="font-extralight"> others and battle your Harmons </span>
            </p>

            <br>

            <p class="text-2xl lg:text-3xl font-extralight">
              Once you build up a valiant army of Harmons, you can battle others. Matchmaking is done based on the
              rarity of your NFTS. This means that someone with all legendary Harmons will never go against someone with
              purely common Harmons.
            </p>

            <br>
            <br>

            <div class="border-l-8 border-primary-alt pl-10">
              <p class="text-2xl text-primary-alt">
                A detailed game document for CryptIDs will be released soon. More precise information will be provided
                about mechanics, Harmons, gameplay and other features.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="section-r-2" style="background: url('/images/PNG/road.png') no-repeat left bottom">
      <div class="container mx-auto py-12 lg:py-24">
        <div class="w-full xl:w-3/4">
          <p class="text-2xl lg:text-5xl font-extralight">
            What’s planned for GameFi Crossing in <span class="font-semibold text-primary-alt">2022</span> ?
          </p>

          <br>
          <br>

          <p class="text-2xl lg:text-4xl font-extralight">
            Below is the current roadmap for GameFi Crossing planned for the first half of 2022. This list is subject to change and may be
            updated with updates and/or future milestones.
          </p>

          <br>
          <br>

        </div>

        <div class="timeline-container">
          <div class="timeline font-extralight">
            <div class="container cnt-finished right">
              <div class="content">
                <h2 class="text-2xl lg:text-4xl">CryptoPigs Tamagotchi</h2>
                <br>
                <p>
                  CryptoPigs are NFTs on the Harmony blockchain integrated into the GameFi Crossing ecosystem, featuring a tamagotchi minigame with token rewards. There are 5000 piggies in total, each with four to seven randomly generated attributes. The tamagotchi game requires users to take care of their piggies to earn COINKx.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="w-full bg-gradient-to-r from-primary to-secondary">
        <div class="container mx-auto flex">
          <div class="w-3/4 mx-auto flex flex-wrap py-4">
            <div class="w-full lg:w-2/5 text-center lg:text-right my-auto">
              <p class="text-3xl text-white font-extralight">Current</p>
            </div>
            <div class="w-full lg:w-1/5 text-center my-auto">
              <img class="h-24 mx-auto" src="/images/SVG/loading-working-on.svg" alt="Currently working on logo">
            </div>
            <div class="w-full lg:w-2/5 text-center lg:text-left my-auto">
              <p class="text-3xl text-white font-semibold">XYA emitting plots</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="section-r-3" class="bg-black pb-24 mb-24">
      <div class="timeline-container text-white">
        <div class="timeline">
          <div class="container left">
            <div class="content">
              <h2 class="text-2xl md:text-4xl">Discord Bot Revamp</h2>
              <br>
              <p>
                Being able to interact with the blockchain on Discord has become so much more powerful and easy. Sir Reginald is now equipped with new features for convenience, community interaction and more. Old redundant commands are removed as well.
              </p>
            </div>
          </div>
          <div class="container right">
            <div class="content">
              <h2 class="text-2xl md:text-4xl">Community NFT Listings</h2>
              <br>
              <p>
                Dingos are added to the GameFi Crossing NFT Marketplace as the first community project collection that users will be able to buy, sell and bid for using our platform. Other community projects partnered with GameFi Crossing will slowly be added.
              </p>
            </div>
          </div>
          <div class="container left">
            <div class="content">
              <h2 class="text-2xl md:text-4xl">Plots marketplace</h2>
              <br>
              <p>
                Buy, sell and bid for plots in the NFT Marketplace with supported tokens in the GameFi Crossing ecosystem. Be able to view the unique attribute values and neighborhood of each plot being sold before purchasing.
              </p>
            </div>
          </div>
          <div class="container right">
            <div class="content">
              <h2 class="text-2xl md:text-4xl">Cross-Project Plots</h2>
              <br>
              <p>
                Integration from other projects in Harmony that partner up with GameFi Crossing are added to plots of land, which are accessible in the GameFi Crossing World App. These offer special and exclusive buffs, use cases and more. Stake NFTs in plots of land to boost the emission of XYA. Certain NFTs from other projects will also have this staking feature, offering their own benefits when staked to a plot.
              </p>
            </div>
          </div>
          <div class="container left">
            <div class="content">
              <h2 class="text-2xl md:text-4xl">Tamagotchi Decorations</h2>
              <br>
              <p>
                Decorations are available to purchase in bulk using ONE/COINKx. There are predefined slots for decorations, with specific tags and types that can be assigned to a slot. Decorations also offer bonuses such as improving the COINKx multiplier for a CryptoPig.
              </p>
            </div>
          </div>
          <div class="container right">
            <div class="content">
              <h2 class="text-2xl md:text-4xl">CryptoPigs Minigames</h2>
              <br>
              <p>
                A unique assortment of traditional minigames involving CryptoPigs allows players to gain experience points, enabling them to level up and rank on a global leaderboard.
              </p>
            </div>
          </div>
          <div class="container left">
            <div class="content">
              <h2 class="text-2xl md:text-4xl">Mobile UI Revamp</h2>
              <br>
              <p>
                The GameFi Crossing website will be re-designed especially to fit the specifications of mobile devices, as well as make it easier to navigate. Full mobile support and integration are also included in this revamp.
              </p>
            </div>
          </div>
          <div class="container right">
            <div class="content">
              <h2 class="text-2xl md:text-4xl">Desktop UI Revamp</h2>
              <br>
              <p>
                An entire website revamp to match the overall aesthetic of GameFi Crossing, serving as a proper introduction to our project, story and more. It will feature an automated MetaMask setup, in-world chart, beginners tutorial and a proper documentational wiki of all the ins and outs of GameFi Crossing.
              </p>
            </div>
          </div>
          <div class="container left">
            <div class="content">
              <h2 class="text-2xl md:text-4xl">The Frey Boss Battles</h2>
              <br>
              <p>
                Bosses are randomly generated NFTs (similar to the Frey) with varying rewards and difficulty. Boss battles feature card-based combat with traditional turn-based RPG mechanics. Each Frey attribute and type will have unique attack, defense and ability cards
              </p>
            </div>
          </div>
          <div class="container right">
            <div class="content">
              <h2 class="text-2xl md:text-4xl">CryptIDs Beta</h2>
              <br>
              <p>
                Users will be able to stake XYA-ONE LP tokens to generate tokens for CryptIDs, introducing a stake-to-play system. The beta release will be a version of CryptIDs with initial monsters to test features and quality of life (QOL) changes. Multiple game modes may be added, as well as special events for exclusive prizes and Harmons.
              </p>
            </div>
          </div>
          <div class="container left">
            <div class="content">
              <h2 class="text-2xl md:text-4xl">CryptoPigs PVP</h2>
              <br>
              <p>
                Pig versus pig. The main CryptoPigs PvP game has rock-paper-scissors mechanics with 5 elements, allowing players to bet with and earn rewards by winning matches.
              </p>
            </div>
          </div>
          <div class="container right">
            <div class="content">
              <h2 class="text-2xl md:text-4xl">CryptoPigs Breeding</h2>
              <br>
              <p>
                Breeding is a mechanic for CryptoPigs where NFTs can breed to create Gen 1 offspring with unique appearances and traits, as well as possible mutations.
              </p>
            </div>
          </div>
        </div>
      </div>

      <div
          class="container mx-auto flex flex-wrap p-8 lg:p-12 rounded-3xl bg-gradient-to-r from-primary to-secondary my-12">
        <div class="w-full lg:w-4/5 mx-auto text-center">
          <p class="text-5xl text-white font-extralight">
            Stay <span class="font-semibold">connected</span> and updated:
          </p>
          <br>
          <p class="text-2xl text-white font-extralight">
            The community is active on several different social media platforms, with Discord being the recommended and
            active place to stay updated and interact with the community.
          </p>
        </div>

        <div class="w-full mx-auto text-center">
          <div class="flex flex-wrap">
            <div class="w-full lg:w-1/4 flex flex-wrap mt-8 lg:mt-16 mb-8">
              <img class="h-12 lg:h-24 mx-auto mb-8" src="/images/SVG/discord.svg" alt="Discord">
              <div class="w-full">
                <a href="https://discord.gg/tKtr9GgzA6" target="_blank">
                  <img class="my-auto w-20 inline" src="/images/SVG/arrow-right-white.svg" alt="Arrow right">
                  <span class="uppercase ml-4 text-2xl font-semibold text-white">
                    Discord
                  </span>
                </a>
              </div>
            </div>
            <div class="w-full lg:w-1/4 flex flex-wrap mt-8 lg:mt-16 mb-8">
              <img class="h-12 lg:h-24 mx-auto mb-8" src="/images/SVG/twitter.svg" alt="Discord">
              <div class="w-full">
                <a href="https://twitter.com/gameficrossing" target="_blank">
                  <img class="my-auto w-20 inline" src="/images/SVG/arrow-right-white.svg" alt="Arrow right">
                  <span class="uppercase ml-4 text-2xl font-semibold text-white">
                    Twitter
                  </span>
                </a>
              </div>
            </div>
            <div class="w-full lg:w-1/4 flex flex-wrap mt-8 lg:mt-16 mb-8">
              <img class="h-12 lg:h-24 mx-auto mb-8" src="/images/SVG/telegram.svg" alt="Discord">
              <div class="w-full">
                <a href="https://t.me/gameficrossing" target="_blank">
                  <img class="my-auto w-20 inline" src="/images/SVG/arrow-right-white.svg" alt="Arrow right">
                  <span class="uppercase ml-4 text-2xl font-semibold text-white">
                    Telegram
                  </span>
                </a>
              </div>
            </div>
            <div class="w-full lg:w-1/4 flex flex-wrap mt-8 lg:mt-16 mb-8">
              <img class="h-12 lg:h-24 mx-auto mb-8" src="/images/SVG/reddit.svg" alt="Discord">
              <div class="w-full">
                <a href="https://www.reddit.com/r/XYA_Official/" target="_blank">
                  <img class="my-auto w-20 inline" src="/images/SVG/arrow-right-white.svg" alt="Arrow right">
                  <span class="uppercase ml-4 text-2xl font-semibold text-white">
                    Reddit
                  </span>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  name: 'Homepage'
}
</script>