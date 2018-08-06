<template>
  <v-container fluid grid-list-lg style="margin-bottom: 1.5em">
    <v-layout row wrap>
      
      <v-flex xs12>
        <v-card color="blue-grey darken-2" class="white--text">
          <v-card-title primary-title>
            <div class="headline">Air</div>
          </v-card-title>
          <v-card-actions>
            <v-btn dark color="orange" v-on:click="emitAirBookEvent">Book now</v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>
      
      <v-flex xs12>
        <v-card color="cyan darken-2" class="white--text">
          <v-card-title primary-title>
            <div class="headline">Hotel</div>
          </v-card-title>
          <v-card-actions>
            <v-btn color="orange" dark v-on:click="emitHotelBookEvent">Book now</v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>
      
      
      <v-flex xs12>
        <v-card color="purple darken-2" class="white--text">
          <v-card-title primary-title>
            <div class="headline">Car</div>
          </v-card-title>
          <v-card-actions>
            <v-btn color="orange" dark v-on:click="emitCarBookEvent">Book now</v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>
    
    </v-layout>
  </v-container>
</template>
<script>
  export default {
    name: 'home',
    components: {},
    data: function () {
      return {
        airBook: {
          "common": {
            "app": {
              "appVersion": "1.2",
              "appName": "TripAssist",
              "appBuild": "3"
            },
            "id": "457dfa2b-f34e-4799-b281-15e4b62372a7-999",
            "user": {
              "loyaltyProgramMember": "YES",
              "tenantId": "tmc1",
              "userId": "d964d047-e643-4f10-b6bd-68316973fd02",
              "corporateId": "corporate3"
            },
            "device": {
              "osVersion": "4",
              "osName": "Android",
              "deviceName": "Test Device 2",
              "uuid": "3f3283b0-8b9f-4471-a48e-d3e19f724d3a"
            },
            "timestamp": {
              "utcTimestamp": "2018-07-04T09:21:22.272Z",
              "localTZ": "Canada/Central"
            }
          },
          "eventName": "screenDisplay",
          "properties": {
            "screenName": "AirBookClicked"
          }
        },
        hotelBook: {
          "common": {
            "app": {
              "appVersion": "1.2",
              "appName": "TripAssist",
              "appBuild": "3"
            },
            "id": "457dfa2b-f34e-4799-b281-15e4b62372a7-888",
            "user": {
              "loyaltyProgramMember": "YES",
              "tenantId": "tmc1",
              "userId": "d964d047-e643-4f10-b6bd-68316973fd02",
              "corporateId": "corporate3"
            },
            "device": {
              "osVersion": "4",
              "osName": "Android",
              "deviceName": "Test Device 2",
              "uuid": "3f3283b0-8b9f-4471-a48e-d3e19f724d3a"
            },
            "timestamp": {
              "utcTimestamp": "2018-07-04T09:21:22.272Z",
              "localTZ": "Canada/Central"
            }
          },
          "eventName": "screenDisplay",
          "properties": {
            "screenName": "HotelBookClicked"
          }
        },
        carBook: {
          "common": {
            "app": {
              "appVersion": "1.2",
              "appName": "TripAssist",
              "appBuild": "3"
            },
            "id": "457dfa2b-f34e-4799-b281-15e4b62372a7-777",
            "user": {
              "loyaltyProgramMember": "YES",
              "tenantId": "tmc1",
              "userId": "d964d047-e643-4f10-b6bd-68316973fd02",
              "corporateId": "corporate3"
            },
            "device": {
              "osVersion": "4",
              "osName": "Android",
              "deviceName": "Test Device 2",
              "uuid": "3f3283b0-8b9f-4471-a48e-d3e19f724d3a"
            },
            "timestamp": {
              "utcTimestamp": "2018-07-04T09:21:22.272Z",
              "localTZ": "Canada/Central"
            }
          },
          "eventName": "screenDisplay",
          "properties": {
            "screenName": "CarBookClicked"
          }
        }
      }
    },
    methods: {
      emitAirBookEvent: function () {
        console.log('*** Air book')
        analyticsLib.emitEvent(JSON.stringify(this.airBook));
      },
      emitHotelBookEvent: function () {
        console.log('*** Hotel book')
        analyticsLib.emitEvent(JSON.stringify(this.hotelBook));
      },
      emitCarBookEvent: function () {
        console.log('*** Car book')
        analyticsLib.emitEvent(JSON.stringify(this.carBook));
      }
    }
  }
</script>
