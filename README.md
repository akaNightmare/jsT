jsT
===
Краткое описание: Yii-extesion для перевода сообщений с помощью Javascript.
Для этого он использует уже готовые PHP-переводы. То есть если у вас на странице исользуются слова с app-словаря,
все слова из этого словаря автоматически подключатся для JS.

1. Кидаем папку в protected/extension
2. подключаем в main.php

  'import' => array(
      //  ...
      'ext.yii-js-t.*',
      //  ...
  )
 
  'components' => array(
      //  ...
      'messages' => array(
          'class' => 'JsTPhpMessageSource'
      ),
      //  ...
  ),
4. Унаследуем с Controller c JsTController
3. исмользуем
<script>
  alert (Yii.t('any words'));
  alert (_t('any words'));
</script>

Примечания
===
Если у вас нет перевода некоторого сообщения, Вам понадобиться включить его в соварь на PHP стороне.
