<template>
	<div>
		<!-- begin breadcrumb -->
		<ol class="breadcrumb pull-right">
			<li class="breadcrumb-item"><a href="javascript:;">Home</a></li>
            <li class="breadcrumb-item"><a href="javascript:;">Request form</a></li>
			<li class="breadcrumb-item active"><a href="javascript:;">Insulation</a></li>
		</ol>
		<!-- end breadcrumb -->
		<!-- begin page-header -->
		<h1 class="page-header">Request Form</h1>
		<!-- end page-header -->

        <!-- begin nav-tabs-pills -->
        <b-tabs content-class="p-15 bg-white mb-4">
            <b-tab active>
                <template slot="title">
                    <span class="d-sm-none"><i class="far fa-lg fa-fw fa-file-alt"></i></span>
                    <span class="d-sm-block d-none"><i class="far fa-lg fa-fw m-r-10 fa-file-alt"></i>Form</span>
                </template>
                
                <h3 class="m-t-10">Insulation</h3>
                <div class="request-form-wrapper">
                    <form>
                        <div class="panel panel-inverse">
                            <div class="form-group row">
                                <label for="" class="col-sm-2 offset-sm-6 col-form-label">Request Type <span class="required">*</span></label>
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
                                <label for="" class="col-sm-2 offset-sm-6 col-form-label">ID</label>
                                <div class="col-sm-4">
                                    <input type="text" class="form-control" id="" value="MTPMTCSC200001" placeholder="" readonly>
                                </div>
                            </div>
                            <div class="form-group row">
                                <label for="" class="col-sm-2 offset-sm-6 col-form-label">Status</label>
                                <div class="col-sm-4">
                                    <select class="form-control" readonly>
                                        <option>Draft</option>
                                    </select>
                                </div>
                            </div>
                        </div>

                        <div class="panel panel-inverse">
                            <div class="row">
                                <div class="col-sm-6">
                                    <div class="panel-heading">
                                        <h3 class="panel-title">Work Order Information </h3>
                                    </div>
                                </div>
                            </div>
                            <div class="row">
                                <div class="col-12">
                                    <div class="panel-body hljs-wrapper">
                                        <div class="form-group row">
                                            <label for="" class="col-sm-2 col-form-label">WO <span class="required">*</span></label>
                                            <div class="col-sm-4">
                                                <input type="text" class="form-control" id="" value="" placeholder="WO">
                                            </div>
                                            <label for="" class="col-sm-2 col-form-label">WO Description</label>
                                            <div class="col-sm-4">
                                                <input type="text" class="form-control" id="" value="" placeholder="WO Description">
                                            </div>
                                        </div>
                                        <div class="form-group row">
                                            <label for="" class="col-sm-2 col-form-label">Plant <span class="required">*</span></label>
                                            <div class="col-sm-4">
                                                <input type="text" class="form-control" id="" value="" placeholder="Plant">
                                            </div>
                                            <label for="" class="col-sm-2 col-form-label">Order Type</label>
                                            <div class="col-sm-4">
                                                <input type="text" class="form-control" id="" value="" placeholder="Order Type">
                                            </div>
                                        </div>
                                        <div class="form-group row">
                                            <label class="col-sm-2 col-form-label">Execution Date (WAC) <span class="required">*</span></label>
                                            <div class="col-sm-4">
                                                <!-- <date-picker v-model="date" :config="options"></date-picker> -->
                                                <div class="input-group">
                                                    <date-picker v-model="executionDate" :config="options"></date-picker>
                                                    <div class="input-group-append">
                                                        <label for="dateTimeInput" class="input-group-text">
                                                            <i class="far fa-lg fa-fw fa-calendar-alt"></i>
                                                        </label>
                                                    </div>
                                                </div>
                                            </div>
                                            <label for="" class="col-sm-2 col-form-label">Planer Group</label>
                                            <div class="col-sm-4">
                                                <input type="text" class="form-control" id="" value="" placeholder="Planer Group">
                                            </div>
                                        </div>
                                        <div class="form-group row">
                                            <label for="" class="col-sm-2 col-form-label">Funtional Location <span class="required">*</span></label>
                                            <div class="col-sm-4">
                                                <input type="text" class="form-control" id="" value="" placeholder="Funtional Location">
                                            </div>
                                            <label for="" class="col-sm-2 col-form-label">Job complete</label>
                                            <div class="col-sm-4">
                                                <select class="form-control" readonly>
                                                    <option>NO</option>
                                                </select>
                                            </div>
                                        </div>
                                        <div class="form-group row">
                                            <label for="" class="col-sm-2 col-form-label">Lead Craft</label>
                                            <div class="col-sm-4">
                                                <input type="text" class="form-control" id="" value="" placeholder="Lead Craft">
                                            </div>
                                            <div class="col-sm-2 offset-sm-4">
                                                <button type="button" class="btn btn-primary btn-block">Update</button>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="row">
                                <div class="col-12">
                                    <div class="panel-body">
                                        <div class="form-group row">
                                            <label for="" class="col-sm-2 col-form-label">Request Note</label>
                                            <div class="col-sm-10">
                                                <textarea class="form-control" rows="3"></textarea>
                                            </div>
                                        </div>
                                        <div class="form-group row">
                                            <label for="" class="col-sm-2 col-form-label">Request Type <span class="required">*</span></label>
                                            <div class="col-sm-4">
                                                <input type="text" class="form-control" id="" value="George Michael" readonly>
                                            </div>
                                            <label for="" class="col-sm-2 col-form-label">Request Date <span class="required">*</span></label>
                                            <div class="col-sm-4">
                                                <input type="text" class="form-control" id="" value="30/10/2020 10.10 AM" readonly>
                                            </div>
                                        </div>
                                        <div class="form-group row">
                                            <label for="" class="col-sm-2 col-form-label">Work Group <span class="required">*</span></label>
                                            <div class="col-sm-4">
                                                <select class="form-control">
                                                    <option>Select</option>
                                                    <option>Select</option>
                                                    <option>Select</option>
                                                    <option>Select</option>
                                                    <option>Select</option>
                                                </select>
                                            </div>
                                            <label for="" class="col-sm-2 col-form-label">Action Type <span class="required">*</span></label>
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
                                            <label for="" class="col-sm-2 col-form-label">Priority <span class="required">*</span></label>
                                            <div class="col-sm-4">
                                                <select class="form-control">
                                                    <option>Select</option>
                                                    <option>Select</option>
                                                    <option>Select</option>
                                                    <option>Select</option>
                                                    <option>Select</option>
                                                </select>
                                            </div>
                                            <label for="" class="col-sm-2 col-form-label">Crane Status</label>
                                            <div class="col-sm-4">
                                                <!-- <select class="form-control">
                                                    <option>Select</option>
                                                    <option>Select</option>
                                                    <option>Select</option>
                                                    <option>Select</option>
                                                    <option>Select</option>
                                                </select> -->
                                                <v-select :options="['Request','Approved']"></v-select>
                                            </div>
                                        </div>
                                        <div class="form-group row">
                                            <label for="" class="col-sm-2 col-form-label">Vendor Name <span class="required">*</span></label>
                                            <div class="col-sm-4">
                                                <input type="text" class="form-control" id="" value="" placeholder="Vendor Name">
                                            </div>
                                            <label for="" class="col-sm-2 col-form-label">Contact Mobile</label>
                                            <div class="col-sm-4">
                                                <masked-input pattern="111-111-1111" class="form-control" placeholder="0xx-xxx-xxxx"></masked-input>
                                            </div>
                                        </div>
                                        <div class="form-group row">
                                            <label for="" class="col-sm-2 col-form-label">Contact Person</label>
                                            <div class="col-sm-4">
                                                <input type="text" class="form-control" id="" value="" placeholder="Contact Person">
                                            </div>
                                            <label for="" class="col-sm-2 col-form-label">Contact Phone</label>
                                            <div class="col-sm-4">
                                                <masked-input pattern="11-111-1111" class="form-control" placeholder="02-xxx-xxxx"></masked-input>
                                            </div>
                                        </div>
                                        <div class="form-group row">
                                            <label for="" class="col-sm-2 col-form-label">Contact Email</label>
                                            <div class="col-sm-4">
                                                <input type="email" class="form-control" id="" value="" placeholder="Contact Email">
                                            </div>
                                            <label for="" class="col-sm-2 col-form-label">Job Description <span class="required">*</span></label>
                                            <div class="col-sm-4">
                                                <input type="text" class="form-control" id="" value="" placeholder="Job Description">
                                            </div>
                                        </div>
                                        <div class="form-group row">
                                            <label for="" class="col-sm-2 col-form-label">Equipment Tag <span class="required">*</span></label>
                                            <div class="col-sm-4">
                                                <input type="text" class="form-control" id="" value="" placeholder="Equipment Tag">
                                            </div>
                                            <label for="" class="col-sm-2 col-form-label">Need Date <span class="required">*</span></label>
                                            <div class="col-sm-4">
                                                <!-- <date-picker v-model="date2" :config="options2"></date-picker> -->
                                                <div class="input-group">
                                                    <date-picker v-model="needDate" :config="options"></date-picker>
                                                    <div class="input-group-append">
                                                        <label for="dateTimeInput2" class="input-group-text">
                                                            <i class="far fa-lg fa-fw fa-calendar-alt"></i>
                                                        </label>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="form-group row">
                                            <label for="" class="col-sm-2 col-form-label">Cost Center</label>
                                            <div class="col-sm-4">
                                                <input type="email" class="form-control" id="" value="" placeholder="Cost Center">
                                            </div>
                                            <label for="" class="col-sm-2 col-form-label">Size <span class="required">*</span></label>
                                            <div class="col-sm-4">
                                                <input type="text" class="form-control" id="" value="" placeholder="Size">
                                            </div>
                                        </div>
                                        <div class="form-group row">
                                            <label for="" class="col-sm-2 col-form-label">Duration <span class="required">*</span></label>
                                            <div class="col-sm-4">
                                                <input type="email" class="form-control" id="" value="" placeholder="Duration">
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="panel panel-inverse">
                            <div class="row">
                                <div class="col-sm-6">
                                    <div class="panel-heading">
                                        <h3 class="panel-title">ขอบเขต/เงื่อนไขของงาน (Scope of Works)</h3>
                                    </div>
                                </div>
                            </div>
                            <div class="row">
                                <div class="col-12">
                                    <div class="panel-body">
                                        <div class="form-group row">
                                            <label for="" class="col-sm-2 col-form-label">ขอบเขต (Scope) <span class="required">*</span></label>
                                            <div class="col-sm-10">
                                                <div class="row">
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="scope" id="scopeChk1" />
                                                            <label class="form-check-label" for="scopeChk1">รื้อ (Remove)</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="scope" id="scopeChk2" />
                                                            <label class="form-check-label" for="scopeChk2">ใส่กลับ (Install)</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="scope" id="scopeChk3" />
                                                            <label class="form-check-label" for="scopeChk3">งานใหม่ (New Installation)</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check" id="selector">
                                                            <input class="form-check-input" type="checkbox" value="" name="scope" id="scopeChk4" />
                                                            <label class="form-check-label" for="scopeChk4">อื่นๆ ระบุ (Other)</label>
                                                        </div>
                                                        <input type="text" class="form-control" id="scopeOther" value="" placeholder="อื่นๆ ระบุ (Other)">
                                                    </div>
                                                </div>
                                            </div>
                                        </div>

                                        <div class="form-group row">
                                            <label for="" class="col-sm-2 col-form-label">ฉนวน (Insulator) <span class="required">*</span></label>
                                            <div class="col-sm-10">
                                                <div class="row">
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="insulator" id="insulatorChk1" />
                                                            <label class="form-check-label" for="insulatorChk1">ใช้ของใหม่ (New)</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="insulator" id="insulatorChk2" />
                                                            <label class="form-check-label" for="insulatorChk2">ใส่กลับ (Existing Use)</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="insulator" id="insulatorChk3" />
                                                            <label class="form-check-label" for="insulatorChk3">อื่นๆ ระบุ (Other)</label>
                                                        </div>
                                                        <input type="text" class="form-control" id="insulatorOther" value="" placeholder="อื่นๆ ระบุ (Other)">
                                                    </div>
                                                </div>
                                            </div>
                                        </div>

                                        <div class="form-group row">
                                            <label for="" class="col-sm-2 col-form-label">แผ่นหุ้ม (Cadding) <span class="required">*</span></label>
                                            <div class="col-sm-10">
                                                <div class="row">
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="cadding" id="caddingChk1" />
                                                            <label class="form-check-label" for="caddingChk1">ใช้ของใหม่ (New)</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="cadding" id="caddingChk2" />
                                                            <label class="form-check-label" for="caddingChk2">ใส่กลับ (Existing Use)</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="cadding" id="caddingChk3" />
                                                            <label class="form-check-label" for="caddingChk3">อื่นๆ ระบุ (Other)</label>
                                                        </div>
                                                        <input type="text" class="form-control" id="caddingOther" value="" placeholder="อื่นๆ ระบุ (Other)">
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="panel panel-inverse">
                            <div class="row">
                                <div class="col-sm-6">
                                    <div class="panel-heading">
                                        <h3 class="panel-title">ขอบเขตงาน (Scope Of Works)</h3>
                                    </div>
                                </div>
                            </div>
                            <div class="row">
                                <div class="col-12">
                                    <div class="panel-body">
                                        <div class="form-group row">
                                            <label for="" class="col-sm-2 col-form-label">ชนิดของงานหุ้มฉนวน<br>(Type Of Insulator) <span class="required">*</span></label>
                                            <div class="col-sm-10">
                                                <div class="row">
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="insulatorType" id="insulatorTypeChk1" />
                                                            <label class="form-check-label" for="insulatorTypeChk1">ร้อน (Hot)</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="insulatorType" id="insulatorTypeChk2" />
                                                            <label class="form-check-label" for="insulatorTypeChk2">เย็น (Cold)</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="insulatorType" id="insulatorTypeChk3" />
                                                            <label class="form-check-label" for="insulatorTypeChk3">ร้อน/เย็น (Hot/Cold)</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="insulatorType" id="insulatorTypeChk4" />
                                                            <label class="form-check-label" for="insulatorTypeChk4">งานกันเสียง (Soundproofing)</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check" id="selector">
                                                            <input class="form-check-input" type="checkbox" value="" name="insulatorType" id="insulatorTypeChk5" />
                                                            <label class="form-check-label" for="insulatorTypeChk5">อื่นๆ ระบุ (Other)</label>
                                                        </div>
                                                        <input type="text" class="form-control" id="insulatorTypeOther" value="" placeholder="อื่นๆ ระบุ (Other)">
                                                    </div>
                                                </div>
                                            </div>
                                        </div>

                                        <div class="form-group row">
                                            <label for="" class="col-sm-2 col-form-label">ชนิดของวัสดุฉนวน<br>(Type Of Insulating Materials) <span class="required">*</span></label>
                                            <div class="col-sm-10">
                                                <div class="row">
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="insulatingType" id="insulatingTypeChk1" />
                                                            <label class="form-check-label" for="insulatingTypeChk1">ร๊อควูล (Rockwool)</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="insulatingType" id="insulatingTypeChk2" />
                                                            <label class="form-check-label" for="insulatingTypeChk2">กล๊าสวูล (Glasswool)</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="insulatingType" id="insulatingTypeChk3" />
                                                            <label class="form-check-label" for="insulatingTypeChk3">แคลเซียม (Calcium)</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="insulatingType" id="insulatingTypeChk4" />
                                                            <label class="form-check-label" for="insulatingTypeChk4">เซรามิค (Ceramic)</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="insulatingType" id="insulatingTypeChk5" />
                                                            <label class="form-check-label" for="insulatingTypeChk5">โฟมกล๊าส (Foamglass)</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="insulatingType" id="insulatingTypeChk6" />
                                                            <label class="form-check-label" for="insulatingTypeChk6">PU Foam</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="insulatingType" id="insulatingTypeChk7" />
                                                            <label class="form-check-label" for="insulatingTypeChk7">PIR Foam</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="insulatingType" id="insulatingTypeChk8" />
                                                            <label class="form-check-label" for="insulatingTypeChk8">แอโรเฟลต (Aeroflex)</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check" id="selector">
                                                            <input class="form-check-input" type="checkbox" value="" name="insulatingType" id="insulatingTypeChk9" />
                                                            <label class="form-check-label" for="insulatingTypeChk9">อื่นๆ ระบุ (Other)</label>
                                                        </div>
                                                        <input type="text" class="form-control" id="insulatingTypeOther" value="" placeholder="อื่นๆ ระบุ (Other)">
                                                    </div>
                                                </div>
                                            </div>
                                        </div>

                                        <div class="form-group row">
                                            <label for="" class="col-sm-2 col-form-label">ชนิดของแผ่น<br>(Type Of Sheet) <span class="required">*</span></label>
                                            <div class="col-sm-10">
                                                <div class="row">
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="sheetType" id="sheetTypeChk1" />
                                                            <label class="form-check-label" for="sheetTypeChk1">อลูมิเนียม (Aluminium)</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="sheetType" id="sheetTypeChk2" />
                                                            <label class="form-check-label" for="sheetTypeChk2">สแตนเลส (Stainless)</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="sheetType" id="sheetTypeChk3" />
                                                            <label class="form-check-label" for="sheetTypeChk3">สังกะสี (Zinc)</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="sheetType" id="sheetTypeChk4" />
                                                            <label class="form-check-label" for="sheetTypeChk4">อลูซิ้งค์ (Aluzin)</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check" id="selector">
                                                            <input class="form-check-input" type="checkbox" value="" name="sheetType" id="sheetTypeChk5" />
                                                            <label class="form-check-label" for="sheetTypeChk5">อื่นๆ ระบุ (Other)</label>
                                                        </div>
                                                        <input type="text" class="form-control" id="sheetTypeOther" value="" placeholder="อื่นๆ ระบุ (Other)">
                                                    </div>
                                                </div>
                                            </div>
                                        </div>

                                        <div class="form-group row">
                                            <label for="" class="col-sm-2 col-form-label">ขอบเขตงานที่ร้องขอ<br>(Scope Of Work Requested) <span class="required">*</span></label>
                                            <div class="col-sm-10">
                                                <div class="row">
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="scopeType" id="scopeTypeChk1" />
                                                            <label class="form-check-label" for="scopeTypeChk1">รื้อ (Remove)</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="scopeType" id="scopeTypeChk2" />
                                                            <label class="form-check-label" for="scopeTypeChk2">ใส่กลับ (Install)</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check">
                                                            <input class="form-check-input" type="checkbox" value="" name="scopeType" id="scopeTypeChk3" />
                                                            <label class="form-check-label" for="scopeTypeChk3">งานใหม่ (New Installation)</label>
                                                        </div>
                                                    </div>
                                                    <div class="col-sm-3">
                                                        <div class="form-check" id="selector">
                                                            <input class="form-check-input" type="checkbox" value="" name="scopeType" id="scopeTypeChk4" />
                                                            <label class="form-check-label" for="scopeTypeChk4">อื่นๆ ระบุ (Other)</label>
                                                        </div>
                                                        <input type="text" class="form-control" id="scopeTypeOther" value="" placeholder="อื่นๆ ระบุ (Other)">
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="panel panel-inverse">
                            <div class="row">
                                <div class="col-sm-6">
                                    <div class="panel-heading">
                                        <h3 class="panel-title">Cost Information </h3>
                                    </div>
                                </div>
                            </div>
                            <div class="row">
                                <div class="col-12">
                                    <div class="panel-body hljs-wrapper">
                                        <div class="form-group row">
                                            <label for="" class="col-sm-2 col-form-label">PO Number</label>
                                            <div class="col-sm-4">
                                                <input type="text" class="form-control" id="" value="" placeholder="PO Number">
                                            </div>
                                            <label for="" class="col-sm-2 col-form-label">Actual Cost</label>
                                            <div class="col-sm-4">
                                                <input type="text" class="form-control" id="" value="" placeholder="0.00">
                                            </div>
                                        </div>
                                        <div class="form-group row">
                                            <label for="" class="col-sm-2 col-form-label">Invoice Number</label>
                                            <div class="col-sm-4">
                                                <input type="text" class="form-control" id="" value="" placeholder="Invoice Number">
                                            </div>
                                            <label for="" class="col-sm-2 col-form-label">Actual Size</label>
                                            <div class="col-sm-4">
                                                <input type="text" class="form-control" id="" value="" placeholder="0.00">
                                            </div>
                                        </div>
                                        <div class="form-group row">
                                            <label for="" class="col-sm-2 col-form-label">Quotation</label>
                                            <div class="col-sm-4">
                                                <input type="text" class="form-control" id="" value="" placeholder="Quotation">
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="panel panel-inverse">
                            <div class="form-group row justify-content-sm-center">
                                <div class="col col-sm-auto">
                                    <button type="button" class="btn btn-primary btn-block">Save</button>
                                </div>
                                <div class="col col-sm-auto">
                                    <button type="button" class="btn btn-green btn-block">Submit</button>
                                </div>
                                <div class="col col-sm-auto">
                                    <button type="button" class="btn btn-green btn-block">Approved</button>
                                </div>
                                <div class="col col-sm-auto">
                                    <button type="button" class="btn btn-inverse btn-block">Copy</button>
                                </div>
                                <div class="col col-sm-auto">
                                    <button type="button" class="btn btn-warning btn-block">Delete</button>
                                </div>
                                <div class="col col-sm-auto">
                                    <button type="button" class="btn btn-info btn-block">Print</button>
                                </div>
                                <div class="col col-sm-auto">
                                    <button type="button" class="btn btn-danger btn-block">Close</button>
                                </div>
                            </div>
                        </div>
                    </form>
                </div>
            </b-tab>
            <b-tab>
                <template slot="title">
                    <span class="d-sm-none"><i class="far fa-lg fa-fw fa-file-image"></i></span>
                    <span class="d-sm-block d-none"><i class="far fa-lg fa-fw m-r-10 fa-file-image"></i>Image</span>
                </template>
                
                <h3 class="m-t-10">Nav Pills Tab 2</h3>
            </b-tab>
        </b-tabs>
        <!-- end nav-tabs-pills -->
	</div>
</template>

<script>
// import OtherInput from '@/components/MyCurrencyInput.vue'
export default {
	data () {
		return {
            executionDate: new Date(),
            needDate: new Date(),
            options: {
                format: 'DD/MM/YYYY',
                useCurrent: false,
            },
		}
    }
}
</script>