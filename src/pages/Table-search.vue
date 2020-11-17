<template>
	<div>
		<!-- begin breadcrumb -->
		<ol class="breadcrumb pull-right">
			<li class="breadcrumb-item"><a href="javascript:;">Home</a></li>
			<li class="breadcrumb-item active"><a href="javascript:;">Work Order</a></li>
		</ol>
		<!-- end breadcrumb -->
		<!-- begin page-header -->
		<h1 class="page-header">Work Order</h1>
		<!-- end page-header -->
		
        <div class="srch-wrapper">
            <form>
                <div class="form-group row">
                    <label for="staticWo" class="col-sm-2 col-form-label">WO</label>
                    <div class="col-sm-4">
                        <input type="text" class="form-control" id="staticWo" value="" placeholder="WO">
                    </div>
                    <label for="staticId" class="col-sm-2 col-form-label">Request ID</label>
                    <div class="col-sm-4">
                        <input type="text" class="form-control" id="staticId" value="" placeholder="Request ID">
                    </div>
                </div>
                <div class="form-group row">
                    <label for="staticPo" class="col-sm-2 col-form-label">PO Number</label>
                    <div class="col-sm-4">
                        <input type="text" class="form-control" id="staticPo" value="" placeholder="PO Number">
                    </div>
                    <label for="staticBy" class="col-sm-2 col-form-label">Request By</label>
                    <div class="col-sm-4">
                        <input type="text" class="form-control" id="staticBy" value="" placeholder="Request By">
                    </div>
                </div>
                <div class="form-group row">
                    <label for="staticInvoice" class="col-sm-2 col-form-label">Invoice Number</label>
                    <div class="col-sm-4">
                        <input type="text" class="form-control" id="staticInvoice" value="" placeholder="Invoice Number">
                    </div>
                    <label for="staticDate" class="col-sm-2 col-form-label">Request Date</label>
                    <div class="col-sm-4">
                        <datepicker placeholder="Select Date" input-class="form-control bg-white"></datepicker>
                    </div>
                </div>
                <div class="form-group row">
                    <label for="staticLocation" class="col-sm-2 col-form-label">Funtional Location</label>
                    <div class="col-sm-4">
                        <input type="text" class="form-control" id="staticLocation" value="" placeholder="Funtional Location">
                    </div>
                    <label for="staticType" class="col-sm-2 col-form-label">Request Type</label>
                    <div class="col-sm-4">
                        <select class="form-control">
                            <option>Select</option>
                            <option>Select</option>
                            <option>Select</option>
                            <option>Select</option>
                            <option>Select</option>
                        </select>
                    </div>
                </div>
                <div class="form-group row">
                    <label for="staticTag" class="col-sm-2 col-form-label">Equipment Tag</label>
                    <div class="col-sm-4">
                        <input type="text" class="form-control" id="staticTag" value="" placeholder="Equipment Tag">
                    </div>
                    <label for="staticStatus" class="col-sm-2 col-form-label">Status</label>
                    <div class="col-sm-4">
                        <select class="form-control">
                            <option>Select</option>
                            <option>Select</option>
                            <option>Select</option>
                            <option>Select</option>
                            <option>Select</option>
                        </select>
                    </div>
                </div>
                <div class="form-group row">
                    <div class="col-sm-2 offset-sm-4">
						<b-button block variant="info"><i class="fas fa-lg fa-fw m-r-10 fa-search"></i> Search</b-button>
                    </div>
                    <div class="col-sm-2">
						<b-button block variant="default"><i class="fas fa-lg fa-fw m-r-10 fa-undo"></i> Clear</b-button>
                    </div>
                    <div class="col-sm-2">
						<b-link href="#nogo" class="btn btn-danger btn-block"><i class="fas fa-lg fa-fw m-r-10 fa-plus"></i> Request</b-link>
                    </div>
                    <div class="col-sm-2">
						<b-button block variant="green"><i class="far fa-lg fa-fw m-r-10 fa-file-excel"></i> Export Excel</b-button>
                    </div>
                </div>
            </form>
        </div>

		<vue-good-table 
			:columns="columns" 
			:rows="rows" 
			:lineNumbers="false"
			:search-options="{ enabled: true, placeholder: 'Search this table' }" 
			:pagination-options="{ enabled: true,  position: 'top' }"
			:selectOptions="{
				enabled: false,
				selectOnCheckboxOnly: true,
				selectionInfoClass: 'alert alert-info m-b-0 no-rounded-corner',
				selectionText: 'rows selected',
				clearSelectionText: 'clear',
			}"
		>
			<div slot="selected-row-actions" style="margin: -2px 0;">
				<button class="btn btn-xs btn-primary m-r-5">Action 1</button>
				<button class="btn btn-xs btn-grey">Action 2</button>
			</div>
			<template slot="table-row" slot-scope="props">
				<span v-if="props.column.field == 'btn'">
					<!-- <img v-bind:src="props.row.image" class="rounded" width="24" style="margin: -3px" /> -->
					<b-link href="#nogo" class="btn btn-success btn-icon btn-circle m-r-5"><i class="far fa-edit"></i></b-link>
					<b-link href="#nogo" class="btn btn-warning btn-icon btn-circle m-r-5"><i class="far fa-copy"></i></b-link>
					<b-link href="#nogo" class="btn btn-danger btn-icon btn-circle m-r-5"><i class="far fa-trash-alt"></i></b-link>
					<b-link href="#nogo" class="btn btn-info btn-icon btn-circle m-r-5"><i class="far fa-eye"></i></b-link>
				</span>
				<span v-else>
					{{props.formattedRow[props.column.field]}}
				</span>
			</template>
		</vue-good-table>
	</div>
</template>

<script>
export default {
  data(){
    return {
      columns: [{
				label: 'Action',
				field: 'btn',
                width: '15%',
				thClass: 'text-nowrap',
				tdClass: 'text-nowrap'
			}, {
				label: 'Request Type',
				field: 'requesttype',
				width: '15%',
				thClass: 'text-nowrap',
				tdClass: 'text-nowrap'
			}, {
				label: 'Request ID',
				field: 'requestid',
				thClass: 'text-nowrap',
				tdClass: 'text-nowrap'
			}, {
				label: 'WO',
				field: 'wo',
				width: '10%',
				tdClass: 'text-nowrap',
				thClass: 'text-nowrap'
			}, {
				label: 'Plant',
				field: 'plant',
				width: '10%',
				tdClass: 'text-nowrap',
				thClass: 'text-nowrap'
			}, {
				label: 'WO Description',
				field: 'wod',
				width: '10%',
				tdClass: 'text-nowrap',
				thClass: 'text-nowrap'
			}, {
				label: 'Job Description',
				field: 'description',
				width: '10%',
				tdClass: 'text-nowrap',
				thClass: 'text-nowrap'
			}, {
				label: 'Funtional Location',
				field: 'location',
				width: '10%',
				tdClass: 'text-nowrap',
				thClass: 'text-nowrap'
			}, {
				label: 'Equipment Tag',
				field: 'tag',
				width: '10%',
				tdClass: 'text-nowrap',
				thClass: 'text-nowrap'
			}, {
				label: 'Status',
				field: 'status',
				width: '10%',
				tdClass: 'text-nowrap',
				thClass: 'text-nowrap'
			}],
      rows: [
        { requesttype:'Scaffold', requestid: 'MTPMTCSC200001', wo: 'test001', plant: 'PO', wod: 'test1', description: 'test3', location: 'test5', tag: 'test7', status: 'Draft' },
        { requesttype:'Insulation', requestid: 'MTPMTCSC200002', wo: 'test002', plant: 'PO', score: 0.036, wod: 'test2', description: 'test4', location: 'test6', tag: 'test8', status: 'Approved' },
      ],
    };
  }
}
</script>