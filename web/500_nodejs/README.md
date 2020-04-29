Name:

	Node.js jedi

Score:

	500

Description:

	EN: Get access to secret information
	RU: Получить доступ к секретной информации
	URL: http://fhq2015-500-nodejs-jedi.freehackquest.com

	Hint 1. See in styles

Answer:

	Ride_The_Lightning

Author:

	[keva] Nitive

Solution:

* по `<link src='static/...'>` понимаем, что исходники раздаются как статика (альтернатива - пытаемся перейти на `http://fhq2015-500-nodejs-jedi.freehackquest.com/package.json`)
* переходим в `package.json` (присутствует почти в любом проекте на node.js)
* переходим в `README.md` (указано в `package.json`)
* в `README.md` описан процесс установки и запуска => переходим к файлам `start.sh` и `index.coffee`
* `start.sh`: находим опечатку (`ADMIN_PAS` вместо `ADMIN_PASS`)
* `index.coffee`: понимаем, что `"#{process.env.ADMIN_PASS} === 'undefined'"`
* подстановка `undefined` вместо пароля открывает доступ к админке
* заходим в админку и получаем флаг
