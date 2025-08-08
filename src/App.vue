
<template>
  <div style="margin:10% 40%; width:250px;">
    <div>
    <ejs-combobox :dataSource='dataItem' :fields='dataFields'
    placeholder='Select a country' :change='onCountryChange'
    ref='comboboxInstance'>
    </ejs-combobox>
    </div>
    <div style="padding-top:20px;">
    <ejs-combobox :dataSource='stateDataItem' :fields='stateDataFields'
    placeholder='Select a state' :enabled='enableCombobox'
    :query='childDataQuery'>
    </ejs-combobox>
    </div>
  </div>
</template>

<script>
import { ComboBoxComponent} from '@syncfusion/ej2-vue-dropdowns';
import { Query } from "@syncfusion/ej2-data";

export default {
  name: 'App',
  components: {
    'ejs-combobox': ComboBoxComponent
  },
  data() {
    return {
      enableCombobox: false,
      childDataQuery: null,
       dataItem: [
        { CountryName: 'United States', CountryId: '1' },
        { CountryName: 'Australia', CountryId: '2' }
      ],
      dataFields: { text: 'CountryName', value: 'CountryId' },
      stateDataItem: [
       { StateName: 'New York', StateId: '101', CountryId: '1' },
       { StateName: 'Virginia ', StateId: '102', CountryId: '1' },
       { StateName: 'Tasmania ', StateId: '105', CountryId: '2' }
      ],
      stateDataFields: { text: 'StateName', value: 'StateId'},
    };
  },
  methods: {
    onCountryChange(args) {
      this.enableCombobox = true;
      this.childDataQuery = new Query().where('CountryId', 'equal', args.value);
    }
  }
};
</script>











<style>
@import url(https://cdn.syncfusion.com/ej2/material.css);
</style>
