<template>
  <div class="parent">
    <table>
      <tr>
        <div>
          <td class="Internerbedarf">
            <label class="internalNeedsLabel">Interner Bedarf</label>
            <draggable :list="internalneeds" group="items">
              <div v-for="element in internalneeds" :key="element.orderName">
                <div class="itemInternalNeeds">
                  <p class="elementOne">
                    {{ element.orderName }}<br />{{
                      element.orderDate.substring(0, 10)
                    }}
                  </p>
                </div>
              </div>
            </draggable>
          </td>
          <td class="Einkaufswagen">
            <label class="einkaufswagenLabel">Einkaufswagen</label>
            <draggable :list="shoppingcart" group="items">
              <div v-for="element in shoppingcart" :key="element.orderName">
                <div class="itemShoppingCart">
                  <p class="elementTwo">
                    {{ element.orderName }}<br />{{
                      element.orderDate.substring(0, 10)
                    }}
                  </p>
                </div>
              </div>
            </draggable>
          </td>
        </div>
      </tr>
    </table>
  </div>
</template>

<script>
//import draggable from "vuedraggable";
import { VueDraggableNext } from "vue-draggable-next";

export default {
  name: "Body",
  components: { draggable: VueDraggableNext },
  data() {
    return {
      internalneeds: [
        {
          orderName: "orderItem 1",
          orderDate: "2021-04-30T23:00:00+0000",
        },
        {
          orderName: "orderItem 2",
          orderDate: "2021-04-30T23:00:00+0000",
        },
        {
          orderName: "orderItem 3",
          orderDate: "2021-04-30T23:00:00+0000",
        },
        {
          orderName: "orderItem 4",
          orderDate: "2021-04-30T23:00:00+0000",
        },
      ],
      shoppingcart: [
        {
          orderName: "orderItem 5",
          orderDate: "2021-04-30T23:00:00+0000",
        },
        {
          orderName: "orderItem 6",
          orderDate: "2021-04-30T23:00:00+0000",
        },
        {
          orderName: "orderItem 7",
          orderDate: "2021-04-30T23:00:00+0000",
        },
        {
          orderName: "orderItem 8",
          orderDate: "2021-04-30T23:00:00+0000",
        },
      ],
    };
  },
};
</script>

<style scoped>
.itemInternalNeeds {
  border-radius: 5px;
  width: 140px;
  height: 50px;
  background-color: lightgray;
  margin-top: 10px;
}

.itemShoppingCart {
  border-radius: 5px;
  width: 140px;
  height: 50px;
  background-color: lightgray;
  margin-top: 10px;
}

.Internerbedarf {
  padding-left: 410px;
}
.Einkaufswagen {
  padding-top: 10px;
  padding-left: 140px;
}
.elementOne {
  padding-left: 10px;
}
.elementTwo {
  padding-left: 10px;
}
.internalNeedsLabel {
  text-decoration: underline;
  font-weight: bold;
}
.einkaufswagenLabel {
  text-decoration: underline;
  font-weight: bold;
}
</style>
