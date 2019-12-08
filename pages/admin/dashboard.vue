<template>
	<div>
		<el-row >
			<el-col>
				<span class="dashboard-title">Microcept Dashboard</span>
			</el-col>
		</el-row>
		<el-row :gutter="10">
		  <el-col :xs="24" :sm="24" :md="24" :lg="18" :xl="18">
		  	<el-card class="box-card" style="margin-top:18px;">
				<la-cartesian :bound="[0, n => n + 1000]" :data="values" :width="700" :height="325">
					<la-line dot curve prop="pv"></la-line>
					<la-line dot curve prop="uv"></la-line>
					<la-line dot curve prop="amt"></la-line>
					<la-x-axis prop="name"></la-x-axis>
					<la-y-axis></la-y-axis>
					<la-tooltip></la-tooltip>
				</la-cartesian>
			</el-card>
		  </el-col>
		  <el-col :xs="24" :sm="24" :md="24" :lg="6" :xl="6">
		  	<el-card class="box-card" style="margin-top:18px;">
			  <el-row>
			  	<span class="card-title" style="color:#959CB6;">Sales Total</span><span style="float:right;"><i class="fas fa-chart-line" style="color:#67C23A;"></i></span>
			  </el-row>
			  <el-row style="margin-top:14px;">
			  	<p style="color:#334151;font-weight:550;font-size:18px;">500</p>
			  	<el-progress :percentage="50"></el-progress>
			  </el-row>
			</el-card>
			<el-card class="box-card" style="margin-top:18px;">
			  <el-row>
			  	<span class="card-title" style="color:#959CB6;">New Revenue</span><span style="float:right;"><i class="fas fa-chart-line" style="color:#67C23A;"></i></span>
			  </el-row>
			  <el-row style="margin-top:14px;">
			  	<p style="color:#334151;font-weight:550;font-size:18px;">Rs. 50000</p>
			  	<el-progress :percentage="30" color="#67C23A"></el-progress>
			  </el-row>
			</el-card>
			<el-card class="box-card" style="margin-top:18px;">
			  <el-row>
			  	<span class="card-title" style="color:#959CB6;">Total Cost</span><span style="float:right;"><i class="fas fa-chart-line" style="color:#F56C6C;"></i></span>
			  </el-row>
			  <el-row style="margin-top:14px;">
			  	<p style="color:#334151;font-weight:550;font-size:18px;">Rs. 250000</p>
			  	<el-progress :percentage="70" color="#E6A23C"></el-progress>
			  </el-row>
			</el-card>
		  </el-col>
		</el-row>
		<el-row :gutter="10">
		  <el-col :xs="24" :sm="24" :md="24" :lg="12" :xl="12">
		  	<el-card class="box-card" style="margin-top:18px;">
		  		<el-row style="margin-bottom:16px;">
		  			<p style="color:#959CB6;">Recent Registrations</p>
		  		</el-row>
		  		<el-row>
					<el-table
				      :data="tableData"
				      style="width: 100%">
				      <el-table-column
				        prop="date"
				        label="Date">
				      </el-table-column>
				      <el-table-column
				        prop="name"
				        label="Name">
				      </el-table-column>
				      <el-table-column
				        prop="address"
				        label="Address">
				      </el-table-column>
				    </el-table>
				</el-row>
			</el-card>
		  </el-col>
		  <el-col :xs="24" :sm="24" :md="24" :lg="12" :xl="12">
		  	<el-card class="box-card" style="margin-top:18px;">
		  		<el-row style="margin-bottom:16px;">
		  			<p style="color:#959CB6;">Recent Purchases</p>
		  		</el-row>
		  		<el-row>
					<el-table
				      :data="tableData"
				      style="width: 100%">
				      <el-table-column
				        prop="date"
				        label="Date">
				      </el-table-column>
				      <el-table-column
				        prop="name"
				        label="Name">
				      </el-table-column>
				      <el-table-column
				        prop="address"
				        label="Address">
				      </el-table-column>
				    </el-table>
				</el-row>
			</el-card>
		  </el-col>
		</el-row>
	</div>
</template>
<script>
export default {
	layout: 'AdminLayout',
    data() {
      return{
        values: [
	      { name: 'Page A', uv: 4000, pv: 2400, amt: 2400 },
	      { name: 'Page B', uv: 3000, pv: 1398, amt: 2210 },
	      { name: 'Page C', uv: 2000, pv: 9800, amt: 2290 },
	      { name: 'Page D', uv: 2780, pv: 3908, amt: 2000 },
	      { name: 'Page E', uv: 1890, pv: 4800, amt: 1700 },
	      { name: 'Page F', uv: 2390, pv: 3800, amt: 2500 },
	      { name: 'Page G', uv: 3490, pv: 4300, amt: 2100 },
	      { name: 'Page F', uv: 2390, pv: 3800, amt: 2500 },
	      { name: 'Page G', uv: 3490, pv: 4300, amt: 2100 }
	    ],
	    tableData: [{
            date: '2016-05-03',
            name: 'Pahi',
            address: 'Guwahati , India'
          }, {
            date: '2016-05-02',
            name: 'Pahi',
            address: 'Guwahati , India'
          }, {
            date: '2016-05-04',
            name: 'Pahi',
            address: 'Guwahati , India'
          }, {
            date: '2016-05-01',
            name: 'Pahi',
            address: 'Guwahati , India'
        }]
	    
      }
    }
};
</script>
<style>
	.dashboard-title{
		color: #959CB6;
		font-weight: 600;
		font-size: 18px;
	}
</style>