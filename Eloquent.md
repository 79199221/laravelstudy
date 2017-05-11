

1. 定义模型
	php artisan make:model User -m 
	定义模型并生成迁移
2. protected $table = 'user';指定表
   $primaryKey = 'id'; 指定主键
   $incrementing = false; 主键不自增
   $timestamps = false; 取消时间戳
   protected $dateFrmat = 'U'; 时间戳格式

