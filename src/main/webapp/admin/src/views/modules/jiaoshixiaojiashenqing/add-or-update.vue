<template>
  <div class="addEdit-block">
    <el-form
      class="detail-form-content"
      ref="ruleForm"
      :model="ruleForm"
      :rules="rules"
      label-width="80px"
	  :style="{backgroundColor:addEditForm.addEditBoxColor}"
    >
      <el-row>
      <el-col :span="12">
        <el-form-item class="input" v-if="type!='info'"  label="教师工号" prop="jiaoshigonghao">
          <el-input v-model="ruleForm.jiaoshigonghao" 
              placeholder="教师工号" clearable  :readonly="ro.jiaoshigonghao"></el-input>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="教师工号" prop="jiaoshigonghao">
              <el-input v-model="ruleForm.jiaoshigonghao" 
                placeholder="教师工号" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
      <el-col :span="12">
        <el-form-item class="input" v-if="type!='info'"  label="教师姓名" prop="jiaoshixingming">
          <el-input v-model="ruleForm.jiaoshixingming" 
              placeholder="教师姓名" clearable  :readonly="ro.jiaoshixingming"></el-input>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="教师姓名" prop="jiaoshixingming">
              <el-input v-model="ruleForm.jiaoshixingming" 
                placeholder="教师姓名" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
      <el-col :span="12">
        <el-form-item class="input" v-if="type!='info'"  label="学院" prop="xueyuan">
          <el-input v-model="ruleForm.xueyuan" 
              placeholder="学院" clearable  :readonly="ro.xueyuan"></el-input>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="学院" prop="xueyuan">
              <el-input v-model="ruleForm.xueyuan" 
                placeholder="学院" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
      <el-col :span="12">
        <el-form-item class="input" v-if="type!='info'"  label="请假类型" prop="qingjialeixing">
          <el-input v-model="ruleForm.qingjialeixing" 
              placeholder="请假类型" clearable  :readonly="ro.qingjialeixing"></el-input>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="请假类型" prop="qingjialeixing">
              <el-input v-model="ruleForm.qingjialeixing" 
                placeholder="请假类型" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
      <el-col :span="12">
        <el-form-item class="input" v-if="type!='info'"  label="请假时间" prop="qingjiashijian">
          <el-input v-model="ruleForm.qingjiashijian" 
              placeholder="请假时间" clearable  :readonly="ro.qingjiashijian"></el-input>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="请假时间" prop="qingjiashijian">
              <el-input v-model="ruleForm.qingjiashijian" 
                placeholder="请假时间" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
      <el-col :span="12">
        <el-form-item class="input" v-if="type!='info'"  label="结束时间" prop="jieshushijian">
          <el-input v-model="ruleForm.jieshushijian" 
              placeholder="结束时间" clearable  :readonly="ro.jieshushijian"></el-input>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="结束时间" prop="jieshushijian">
              <el-input v-model="ruleForm.jieshushijian" 
                placeholder="结束时间" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
      <el-col :span="12">
        <el-form-item class="input" v-if="type!='info'"  label="请假天数" prop="qingjiatianshu">
          <el-input v-model="ruleForm.qingjiatianshu" 
              placeholder="请假天数" clearable  :readonly="ro.qingjiatianshu"></el-input>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="请假天数" prop="qingjiatianshu">
              <el-input v-model="ruleForm.qingjiatianshu" 
                placeholder="请假天数" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
      <el-col :span="12">
        <el-form-item class="input" v-if="type!='info'"  label="是否离校" prop="shifoulixiao">
          <el-input v-model="ruleForm.shifoulixiao" 
              placeholder="是否离校" clearable  :readonly="ro.shifoulixiao"></el-input>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="是否离校" prop="shifoulixiao">
              <el-input v-model="ruleForm.shifoulixiao" 
                placeholder="是否离校" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
      <el-col :span="12">
        <el-form-item class="input" v-if="type!='info'"  label="是否前往疫情中高风险地区" prop="shifouqianwangyiqingzhonggaofengxiandiqu">
          <el-input v-model="ruleForm.shifouqianwangyiqingzhonggaofengxiandiqu" 
              placeholder="是否前往疫情中高风险地区" clearable  :readonly="ro.shifouqianwangyiqingzhonggaofengxiandiqu"></el-input>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="是否前往疫情中高风险地区" prop="shifouqianwangyiqingzhonggaofengxiandiqu">
              <el-input v-model="ruleForm.shifouqianwangyiqingzhonggaofengxiandiqu" 
                placeholder="是否前往疫情中高风险地区" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
      <el-col :span="12">
        <el-form-item class="input" v-if="type!='info'"  label="请假理由" prop="qingjialiyou">
          <el-input v-model="ruleForm.qingjialiyou" 
              placeholder="请假理由" clearable  :readonly="ro.qingjialiyou"></el-input>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="请假理由" prop="qingjialiyou">
              <el-input v-model="ruleForm.qingjialiyou" 
                placeholder="请假理由" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
      <el-col :span="12">
        <el-form-item class="input" v-if="type!='info'"  label="提交时间" prop="tijiaoshijian">
          <el-input v-model="ruleForm.tijiaoshijian" 
              placeholder="提交时间" clearable  :readonly="ro.tijiaoshijian"></el-input>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="提交时间" prop="tijiaoshijian">
              <el-input v-model="ruleForm.tijiaoshijian" 
                placeholder="提交时间" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
      <el-col :span="12">
        <el-form-item class="input" v-if="type!='info'"  label="个人健康状态" prop="gerenjiankangzhuangtai">
          <el-input v-model="ruleForm.gerenjiankangzhuangtai" 
              placeholder="个人健康状态" clearable  :readonly="ro.gerenjiankangzhuangtai"></el-input>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="个人健康状态" prop="gerenjiankangzhuangtai">
              <el-input v-model="ruleForm.gerenjiankangzhuangtai" 
                placeholder="个人健康状态" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
      <el-col :span="12">
        <el-form-item class="select" v-if="type!='info'"  label="请假期间是否接触感染病毒人员" prop="qingjiaqijianshifoujiechuganranbingdurenyuan">
          <el-select v-model="ruleForm.qingjiaqijianshifoujiechuganranbingdurenyuan" placeholder="请选择请假期间是否接触感染病毒人员">
            <el-option
                v-for="(item,index) in qingjiaqijianshifoujiechuganranbingdurenyuanOptions"
                v-bind:key="index"
                :label="item"
                :value="item">
            </el-option>
          </el-select>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="请假期间是否接触感染病毒人员" prop="qingjiaqijianshifoujiechuganranbingdurenyuan">
	      <el-input v-model="ruleForm.qingjiaqijianshifoujiechuganranbingdurenyuan"
                placeholder="请假期间是否接触感染病毒人员" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
      <el-col :span="12">
        <el-form-item class="select" v-if="type!='info'"  label="状态" prop="zhuangtai">
          <el-select v-model="ruleForm.zhuangtai" placeholder="请选择状态">
            <el-option
                v-for="(item,index) in zhuangtaiOptions"
                v-bind:key="index"
                :label="item"
                :value="item">
            </el-option>
          </el-select>
        </el-form-item>
        <div v-else>
          <el-form-item class="input" label="状态" prop="zhuangtai">
	      <el-input v-model="ruleForm.zhuangtai"
                placeholder="状态" readonly></el-input>
          </el-form-item>
        </div>
      </el-col>
      </el-row>
      <el-form-item class="btn">
        <el-button v-if="type!='info'" type="primary" class="btn-success" @click="onSubmit">提交</el-button>
        <el-button v-if="type!='info'" class="btn-close" @click="back()">取消</el-button>
        <el-button v-if="type=='info'" class="btn-close" @click="back()">返回</el-button>
      </el-form-item>
    </el-form>
    

  </div>
</template>
<script>
// 数字，邮件，手机，url，身份证校验
import { isNumber,isIntNumer,isEmail,isPhone, isMobile,isURL,checkIdCard } from "@/utils/validate";
export default {
  data() {
    let self = this
    var validateIdCard = (rule, value, callback) => {
      if(!value){
        callback();
      } else if (!checkIdCard(value)) {
        callback(new Error("请输入正确的身份证号码"));
      } else {
        callback();
      }
    };
    var validateUrl = (rule, value, callback) => {
      if(!value){
        callback();
      } else if (!isURL(value)) {
        callback(new Error("请输入正确的URL地址"));
      } else {
        callback();
      }
    };
    var validateMobile = (rule, value, callback) => {
      if(!value){
        callback();
      } else if (!isMobile(value)) {
        callback(new Error("请输入正确的手机号码"));
      } else {
        callback();
      }
    };
    var validatePhone = (rule, value, callback) => {
      if(!value){
        callback();
      } else if (!isPhone(value)) {
        callback(new Error("请输入正确的电话号码"));
      } else {
        callback();
      }
    };
    var validateEmail = (rule, value, callback) => {
      if(!value){
        callback();
      } else if (!isEmail(value)) {
        callback(new Error("请输入正确的邮箱地址"));
      } else {
        callback();
      }
    };
    var validateNumber = (rule, value, callback) => {
      if(!value){
        callback();
      } else if (!isNumber(value)) {
        callback(new Error("请输入数字"));
      } else {
        callback();
      }
    };
    var validateIntNumber = (rule, value, callback) => {
      if(!value){
        callback();
      } else if (!isIntNumer(value)) {
        callback(new Error("请输入整数"));
      } else {
        callback();
      }
    };
    return {
	  addEditForm: {"btnSaveFontColor":"#fff","selectFontSize":"14px","btnCancelBorderColor":"#DCDFE6","inputBorderRadius":"4px","inputFontSize":"14px","textareaBgColor":"#fff","btnSaveFontSize":"14px","textareaBorderRadius":"4px","uploadBgColor":"#fff","textareaBorderStyle":"solid","btnCancelWidth":"88px","textareaHeight":"120px","dateBgColor":"#fff","btnSaveBorderRadius":"4px","uploadLableFontSize":"14px","textareaBorderWidth":"1px","inputLableColor":"rgba(199, 21, 133, 1)","addEditBoxColor":"rgba(242, 241, 242, 1)","dateIconFontSize":"14px","btnSaveBgColor":"rgba(199, 21, 133, 1)","uploadIconFontColor":"#8c939d","textareaBorderColor":"#DCDFE6","btnCancelBgColor":"rgba(253, 252, 254, 1)","selectLableColor":"rgba(199, 21, 133, 1)","btnSaveBorderStyle":"solid","dateBorderWidth":"1px","dateLableFontSize":"14px","dateBorderRadius":"4px","btnCancelBorderStyle":"solid","selectLableFontSize":"14px","selectBorderStyle":"solid","selectIconFontColor":"#C0C4CC","btnCancelHeight":"44px","inputHeight":"40px","btnCancelFontColor":"rgba(106, 0, 138, 1)","dateBorderColor":"#DCDFE6","dateIconFontColor":"#C0C4CC","uploadBorderStyle":"solid","dateBorderStyle":"solid","dateLableColor":"rgba(199, 21, 133, 1)","dateFontSize":"14px","inputBorderWidth":"1px","uploadIconFontSize":"28px","selectHeight":"40px","inputFontColor":"#606266","uploadHeight":"148px","textareaLableColor":"rgba(199, 21, 133, 1)","textareaLableFontSize":"14px","btnCancelFontSize":"14px","inputBorderStyle":"solid","btnCancelBorderRadius":"4px","inputBgColor":"#fff","inputLableFontSize":"14px","uploadLableColor":"rgba(199, 21, 133, 1)","uploadBorderRadius":"4px","btnSaveHeight":"44px","selectBgColor":"rgba(255, 255, 255, 1)","btnSaveWidth":"88px","selectIconFontSize":"14px","dateHeight":"40px","selectBorderColor":"#DCDFE6","inputBorderColor":"#DCDFE6","uploadBorderColor":"#DCDFE6","textareaFontColor":"#606266","selectBorderWidth":"1px","dateFontColor":"#606266","btnCancelBorderWidth":"1px","uploadBorderWidth":"1px","textareaFontSize":"14px","selectBorderRadius":"4px","selectFontColor":"rgba(10, 10, 10, 1)","btnSaveBorderColor":"#409EFF","btnSaveBorderWidth":"0px"},
      id: '',
      type: '',
      ro:{
	jiaoshigonghao : false,
	jiaoshixingming : false,
	xueyuan : false,
	qingjialeixing : false,
	qingjiashijian : false,
	jieshushijian : false,
	qingjiatianshu : false,
	shifoulixiao : false,
	shifouqianwangyiqingzhonggaofengxiandiqu : false,
	qingjialiyou : false,
	tijiaoshijian : false,
	gerenjiankangzhuangtai : false,
	qingjiaqijianshifoujiechuganranbingdurenyuan : false,
	zhuangtai : false,
	sfsh : false,
	shhf : false,
      },
      ruleForm: {
        jiaoshigonghao: '',
        jiaoshixingming: '',
        xueyuan: '',
        qingjialeixing: '',
        qingjiashijian: '',
        jieshushijian: '',
        qingjiatianshu: '',
        shifoulixiao: '',
        shifouqianwangyiqingzhonggaofengxiandiqu: '',
        qingjialiyou: '',
        tijiaoshijian: '',
        gerenjiankangzhuangtai: '',
        qingjiaqijianshifoujiechuganranbingdurenyuan: '',
        zhuangtai: '',
        shhf: '',
      },
          qingjiaqijianshifoujiechuganranbingdurenyuanOptions: [],
          zhuangtaiOptions: [],
      rules: {
          jiaoshigonghao: [
          ],
          jiaoshixingming: [
          ],
          xueyuan: [
          ],
          qingjialeixing: [
          ],
          qingjiashijian: [
          ],
          jieshushijian: [
          ],
          qingjiatianshu: [
                { validator: validateIntNumber, trigger: 'blur' },
          ],
          shifoulixiao: [
          ],
          shifouqianwangyiqingzhonggaofengxiandiqu: [
          ],
          qingjialiyou: [
          ],
          tijiaoshijian: [
          ],
          gerenjiankangzhuangtai: [
          ],
          qingjiaqijianshifoujiechuganranbingdurenyuan: [
          ],
          zhuangtai: [
          ],
          sfsh: [
          ],
          shhf: [
          ],
      }
    };
  },
  props: ["parent"],
  computed: {
  },
  created() {
	this.addEditStyleChange()
	this.addEditUploadStyleChange()
  },
  methods: {
    // 下载
    download(file){
      window.open(`${file}`)
    },
    // 初始化
    init(id,type) {
      if (id) {
        this.id = id;
        this.type = type;
      }
      if(this.type=='info'||this.type=='else'){
        this.info(id);
      }else if(this.type=='cross'){
        var obj = this.$storage.getObj('crossObj');
        for (var o in obj){
          if(o=='jiaoshigonghao'){
            this.ruleForm.jiaoshigonghao = obj[o];
	    this.ro.jiaoshigonghao = true;
            continue;
          }
          if(o=='jiaoshixingming'){
            this.ruleForm.jiaoshixingming = obj[o];
	    this.ro.jiaoshixingming = true;
            continue;
          }
          if(o=='xueyuan'){
            this.ruleForm.xueyuan = obj[o];
	    this.ro.xueyuan = true;
            continue;
          }
          if(o=='qingjialeixing'){
            this.ruleForm.qingjialeixing = obj[o];
	    this.ro.qingjialeixing = true;
            continue;
          }
          if(o=='qingjiashijian'){
            this.ruleForm.qingjiashijian = obj[o];
	    this.ro.qingjiashijian = true;
            continue;
          }
          if(o=='jieshushijian'){
            this.ruleForm.jieshushijian = obj[o];
	    this.ro.jieshushijian = true;
            continue;
          }
          if(o=='qingjiatianshu'){
            this.ruleForm.qingjiatianshu = obj[o];
	    this.ro.qingjiatianshu = true;
            continue;
          }
          if(o=='shifoulixiao'){
            this.ruleForm.shifoulixiao = obj[o];
	    this.ro.shifoulixiao = true;
            continue;
          }
          if(o=='shifouqianwangyiqingzhonggaofengxiandiqu'){
            this.ruleForm.shifouqianwangyiqingzhonggaofengxiandiqu = obj[o];
	    this.ro.shifouqianwangyiqingzhonggaofengxiandiqu = true;
            continue;
          }
          if(o=='qingjialiyou'){
            this.ruleForm.qingjialiyou = obj[o];
	    this.ro.qingjialiyou = true;
            continue;
          }
          if(o=='tijiaoshijian'){
            this.ruleForm.tijiaoshijian = obj[o];
	    this.ro.tijiaoshijian = true;
            continue;
          }
          if(o=='gerenjiankangzhuangtai'){
            this.ruleForm.gerenjiankangzhuangtai = obj[o];
	    this.ro.gerenjiankangzhuangtai = true;
            continue;
          }
          if(o=='qingjiaqijianshifoujiechuganranbingdurenyuan'){
            this.ruleForm.qingjiaqijianshifoujiechuganranbingdurenyuan = obj[o];
	    this.ro.qingjiaqijianshifoujiechuganranbingdurenyuan = true;
            continue;
          }
          if(o=='zhuangtai'){
            this.ruleForm.zhuangtai = obj[o];
	    this.ro.zhuangtai = true;
            continue;
          }
        }
      }
      // 获取用户信息
      this.$http({
        url: `${this.$storage.get('sessionTable')}/session`,
        method: "get"
      }).then(({ data }) => {
        if (data && data.code === 0) {
          var json = data.data;
		if(json.jiaoshigonghao!=''&&json.jiaoshigonghao){
              		this.ruleForm.jiaoshigonghao = json.jiaoshigonghao
		}
		if(json.jiaoshixingming!=''&&json.jiaoshixingming){
              		this.ruleForm.jiaoshixingming = json.jiaoshixingming
		}
		if(json.xueyuan!=''&&json.xueyuan){
              		this.ruleForm.xueyuan = json.xueyuan
		}
        } else {
          this.$message.error(data.msg);
        }
      });
            this.qingjiaqijianshifoujiechuganranbingdurenyuanOptions = "是,否".split(',')
            this.zhuangtaiOptions = "正常,已逾期,已销假".split(',')
    },
    // 多级联动参数
    info(id) {
      this.$http({
        url: `jiaoshixiaojiashenqing/info/${id}`,
        method: "get"
      }).then(({ data }) => {
        if (data && data.code === 0) {
        this.ruleForm = data.data;
	//解决前台上传图片后台不显示的问题
	let reg=new RegExp('../../../upload','g')//g代表全部
        } else {
          this.$message.error(data.msg);
        }
      });
    },
    // 提交
    onSubmit() {
      // ${column.compare}
      // ${column.compare}
      // ${column.compare}
      // ${column.compare}
      // ${column.compare}
      // ${column.compare}
      // ${column.compare}
      // ${column.compare}
      // ${column.compare}
      // ${column.compare}
      // ${column.compare}
      // ${column.compare}
      // ${column.compare}
      // ${column.compare}
      // ${column.compare}
      // ${column.compare}
















      this.$refs["ruleForm"].validate(valid => {
        if (valid) {
          this.$http({
            url: `jiaoshixiaojiashenqing/${!this.ruleForm.id ? "save" : "update"}`,
            method: "post",
            data: this.ruleForm
          }).then(({ data }) => {
            if (data && data.code === 0) {
              this.$message({
                message: "操作成功",
                type: "success",
                duration: 1500,
                onClose: () => {
                  this.parent.showFlag = true;
                  this.parent.addOrUpdateFlag = false;
                  this.parent.jiaoshixiaojiashenqingCrossAddOrUpdateFlag = false;
                  this.parent.search();
                  this.parent.contentStyleChange();
                }
              });
            } else {
              this.$message.error(data.msg);
            }
          });
        }
      });
    },
    // 获取uuid
    getUUID () {
      return new Date().getTime();
    },
    // 返回
    back() {
      this.parent.showFlag = true;
      this.parent.addOrUpdateFlag = false;
      this.parent.jiaoshixiaojiashenqingCrossAddOrUpdateFlag = false;
      this.parent.contentStyleChange();
    },
	addEditStyleChange() {
	  this.$nextTick(()=>{
	    // input
	    document.querySelectorAll('.addEdit-block .input .el-input__inner').forEach(el=>{
	      el.style.height = this.addEditForm.inputHeight
	      el.style.color = this.addEditForm.inputFontColor
	      el.style.fontSize = this.addEditForm.inputFontSize
	      el.style.borderWidth = this.addEditForm.inputBorderWidth
	      el.style.borderStyle = this.addEditForm.inputBorderStyle
	      el.style.borderColor = this.addEditForm.inputBorderColor
	      el.style.borderRadius = this.addEditForm.inputBorderRadius
	      el.style.backgroundColor = this.addEditForm.inputBgColor
	    })
	    document.querySelectorAll('.addEdit-block .input .el-form-item__label').forEach(el=>{
	      el.style.lineHeight = this.addEditForm.inputHeight
	      el.style.color = this.addEditForm.inputLableColor
	      el.style.fontSize = this.addEditForm.inputLableFontSize
	    })
	    // select
	    document.querySelectorAll('.addEdit-block .select .el-input__inner').forEach(el=>{
	      el.style.height = this.addEditForm.selectHeight
	      el.style.color = this.addEditForm.selectFontColor
	      el.style.fontSize = this.addEditForm.selectFontSize
	      el.style.borderWidth = this.addEditForm.selectBorderWidth
	      el.style.borderStyle = this.addEditForm.selectBorderStyle
	      el.style.borderColor = this.addEditForm.selectBorderColor
	      el.style.borderRadius = this.addEditForm.selectBorderRadius
	      el.style.backgroundColor = this.addEditForm.selectBgColor
	    })
	    document.querySelectorAll('.addEdit-block .select .el-form-item__label').forEach(el=>{
	      el.style.lineHeight = this.addEditForm.selectHeight
	      el.style.color = this.addEditForm.selectLableColor
	      el.style.fontSize = this.addEditForm.selectLableFontSize
	    })
	    document.querySelectorAll('.addEdit-block .select .el-select__caret').forEach(el=>{
	      el.style.color = this.addEditForm.selectIconFontColor
	      el.style.fontSize = this.addEditForm.selectIconFontSize
	    })
	    // date
	    document.querySelectorAll('.addEdit-block .date .el-input__inner').forEach(el=>{
	      el.style.height = this.addEditForm.dateHeight
	      el.style.color = this.addEditForm.dateFontColor
	      el.style.fontSize = this.addEditForm.dateFontSize
	      el.style.borderWidth = this.addEditForm.dateBorderWidth
	      el.style.borderStyle = this.addEditForm.dateBorderStyle
	      el.style.borderColor = this.addEditForm.dateBorderColor
	      el.style.borderRadius = this.addEditForm.dateBorderRadius
	      el.style.backgroundColor = this.addEditForm.dateBgColor
	    })
	    document.querySelectorAll('.addEdit-block .date .el-form-item__label').forEach(el=>{
	      el.style.lineHeight = this.addEditForm.dateHeight
	      el.style.color = this.addEditForm.dateLableColor
	      el.style.fontSize = this.addEditForm.dateLableFontSize
	    })
	    document.querySelectorAll('.addEdit-block .date .el-input__icon').forEach(el=>{
	      el.style.color = this.addEditForm.dateIconFontColor
	      el.style.fontSize = this.addEditForm.dateIconFontSize
	      el.style.lineHeight = this.addEditForm.dateHeight
	    })
	    // upload
	    let iconLineHeight = parseInt(this.addEditForm.uploadHeight) - parseInt(this.addEditForm.uploadBorderWidth) * 2 + 'px'
	    document.querySelectorAll('.addEdit-block .upload .el-upload--picture-card').forEach(el=>{
	      el.style.width = this.addEditForm.uploadHeight
	      el.style.height = this.addEditForm.uploadHeight
	      el.style.borderWidth = this.addEditForm.uploadBorderWidth
	      el.style.borderStyle = this.addEditForm.uploadBorderStyle
	      el.style.borderColor = this.addEditForm.uploadBorderColor
	      el.style.borderRadius = this.addEditForm.uploadBorderRadius
	      el.style.backgroundColor = this.addEditForm.uploadBgColor
	    })
	    document.querySelectorAll('.addEdit-block .upload .el-form-item__label').forEach(el=>{
	      el.style.lineHeight = this.addEditForm.uploadHeight
	      el.style.color = this.addEditForm.uploadLableColor
	      el.style.fontSize = this.addEditForm.uploadLableFontSize
	    })
	    document.querySelectorAll('.addEdit-block .upload .el-icon-plus').forEach(el=>{
	      el.style.color = this.addEditForm.uploadIconFontColor
	      el.style.fontSize = this.addEditForm.uploadIconFontSize
	      el.style.lineHeight = iconLineHeight
	      el.style.display = 'block'
	    })
	    // 多文本输入框
	    document.querySelectorAll('.addEdit-block .textarea .el-textarea__inner').forEach(el=>{
	      el.style.height = this.addEditForm.textareaHeight
	      el.style.color = this.addEditForm.textareaFontColor
	      el.style.fontSize = this.addEditForm.textareaFontSize
	      el.style.borderWidth = this.addEditForm.textareaBorderWidth
	      el.style.borderStyle = this.addEditForm.textareaBorderStyle
	      el.style.borderColor = this.addEditForm.textareaBorderColor
	      el.style.borderRadius = this.addEditForm.textareaBorderRadius
	      el.style.backgroundColor = this.addEditForm.textareaBgColor
	    })
	    document.querySelectorAll('.addEdit-block .textarea .el-form-item__label').forEach(el=>{
	      // el.style.lineHeight = this.addEditForm.textareaHeight
	      el.style.color = this.addEditForm.textareaLableColor
	      el.style.fontSize = this.addEditForm.textareaLableFontSize
	    })
	    // 保存
	    document.querySelectorAll('.addEdit-block .btn .btn-success').forEach(el=>{
	      el.style.width = this.addEditForm.btnSaveWidth
	      el.style.height = this.addEditForm.btnSaveHeight
	      el.style.color = this.addEditForm.btnSaveFontColor
	      el.style.fontSize = this.addEditForm.btnSaveFontSize
	      el.style.borderWidth = this.addEditForm.btnSaveBorderWidth
	      el.style.borderStyle = this.addEditForm.btnSaveBorderStyle
	      el.style.borderColor = this.addEditForm.btnSaveBorderColor
	      el.style.borderRadius = this.addEditForm.btnSaveBorderRadius
	      el.style.backgroundColor = this.addEditForm.btnSaveBgColor
	    })
	    // 返回
	    document.querySelectorAll('.addEdit-block .btn .btn-close').forEach(el=>{
	      el.style.width = this.addEditForm.btnCancelWidth
	      el.style.height = this.addEditForm.btnCancelHeight
	      el.style.color = this.addEditForm.btnCancelFontColor
	      el.style.fontSize = this.addEditForm.btnCancelFontSize
	      el.style.borderWidth = this.addEditForm.btnCancelBorderWidth
	      el.style.borderStyle = this.addEditForm.btnCancelBorderStyle
	      el.style.borderColor = this.addEditForm.btnCancelBorderColor
	      el.style.borderRadius = this.addEditForm.btnCancelBorderRadius
	      el.style.backgroundColor = this.addEditForm.btnCancelBgColor
	    })
	  })
	},
	addEditUploadStyleChange() {
		this.$nextTick(()=>{
		  document.querySelectorAll('.addEdit-block .upload .el-upload-list--picture-card .el-upload-list__item').forEach(el=>{
			el.style.width = this.addEditForm.uploadHeight
			el.style.height = this.addEditForm.uploadHeight
			el.style.borderWidth = this.addEditForm.uploadBorderWidth
			el.style.borderStyle = this.addEditForm.uploadBorderStyle
			el.style.borderColor = this.addEditForm.uploadBorderColor
			el.style.borderRadius = this.addEditForm.uploadBorderRadius
			el.style.backgroundColor = this.addEditForm.uploadBgColor
		  })
	  })
	},
  }
};
</script>
<style lang="scss">
.editor{
  height: 500px;
  
  & /deep/ .ql-container {
	  height: 310px;
  }
}
.amap-wrapper {
  width: 100%;
  height: 500px;
}
.search-box {
  position: absolute;
}
.addEdit-block {
	margin: -10px;
}
.detail-form-content {
	padding: 12px;
}
.btn .el-button {
  padding: 0;
}
</style>
