# Guess-api

[![Build Status](https://travis-ci.org/z-song/Guess-api.svg?branch=master)](https://travis-ci.org/z-song/Guess-api)
[![StyleCI](https://styleci.io/repos/48796179/shield)](https://styleci.io/repos/48796179)
[![Packagist](https://img.shields.io/packagist/l/encore/Guess-api.svg?maxAge=2592000)](https://packagist.org/packages/encore/Guess-api)
[![Total Downloads](https://img.shields.io/packagist/dt/encore/Guess-api.svg?style=flat-square)](https://packagist.org/packages/encore/Guess-api)

`Guess-api` description

> 基于`PHP 7+`和`Laravel 5.5`, 如果你使用更早的版本，

## 特性
```bash
composer create-project --prefer-dist laravel/laravel guess
cd guess;
ls -a
php artisan key:generate
cp .env* .env
php artisan key:generate
```
```php
public function team()
    {
        $request = $this->request;
        $match_id = $request['match_id'];
        // 运行sql获取数据数组
        $result = DB::table('guess_team')
            ->get()->where('match_id', $match_id)
            ->map(function ($value) {
                return (array)$value;
            })->toArray();
        $html = '<div class="btn-group input-group">';
        foreach ($result as $k => $v)
        {
            $name = $v['name'];
            $html .= "<span style='margin-left: 5px' class=\"btn btn-default btn-sm\" type=\"button\">$name</span>";
        }
        $html .= '</div>';
       return $this->returnApi($html);
    }
```

# 依赖

`Guess-api` 基于以下组件或者服务:

+ [Laravel](https://laravel.com/)
+ [AdminLTE](https://almsaeedstudio.com/)
+ [Datetimepicker](http://eonasdan.github.io/bootstrap-datetimepicker/)
+ [font-awesome](http://fontawesome.io)

## 交流

EMAIL:chendonghai888@gmail.com



## 支持

如果觉得这个项目帮你节约了时间，不妨支持一下;)

## License

Guess-api is licensed under the [MIT License](LICENSE).