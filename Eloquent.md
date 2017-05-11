

1. 定义模型
	php artisan make:model User -m 
	定义模型并生成迁移
2. protected $table = 'user';指定表
   $primaryKey = 'id'; 指定主键
   $incrementing = false; 主键不自增
   $timestamps = false; 取消时间戳
   protected $dateFrmat = 'U'; 时间戳格式
   protected $fillable = ['name'];白名单
   protected $guarded = ['price'];黑名单
3. get();
   all();
   chunk(200, function(){});	组块
   cursor()	一次执行单个查询
   find($id)
   first();
   findOrFail($id);
   firstOrFail($id);
   firstOrCreate([]);查询，不存在则创建
   firstOrNew([]);查询，不存在则new实例
   delete(); 通过实例删除
   destory($id);通过id删除
   count();
   sum();
   max();
   save();插入更新纪录
   update();

4. 软删除
   use Illuminate\Database\Eloquent\SoftDeletes
   protected $dates = ['deleted_at'];
   Schema::table('user', function($table){
	$table->softDeletes();创建软删除列
   }
   trashed()	判断是否被软删除
   onlyTrashed()获取删除模型
   restore()	恢复软删除
   withTrashed();查询软包含删除结果
   forceDelete();永久删除
   App\User::where('status', 1)
	->orderB('name', 'desc')
	->take(10)
	->get();


