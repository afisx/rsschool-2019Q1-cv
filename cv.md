***
[![My photo](https://pp.userapi.com/c850616/v850616672/3e093/PLwvmXNhQPY.jpg?ava=1)](https://github.com/afisx)
# Aliaksei Maiseyenka
***
## Contacts:
* **mobile:** *+375 (29) 703-32-89*
* **email:** *alexej.moiseenko@gmail.com*
* **skype:** *afisx@outlook.com*
* **vk:** *[Sorok2](https://vk.com/sorok2)*
* **facebook:** *[Afisx](https://www.facebook.com/Afisx)*

***

## About me:

> Although my main specialty has always been architecture, almost immediately after graduation from Belarusian national Polytechnic Univercity i began to study programming and markup languages. This first became my hobby, and then my second profession. I was always ready for self-education. I hope that it will help me to become an excellent specialist in IT.

***

## Skills:
* **Programming languages:** *C (few), C++ (few), PHP, JavaScript, SQL*
* **Markup languages:** *HTML, CSS, LESS, Markdown*
* **Frameworks:** *[Yii2 framework](https://www.yiiframework.com/), Wordpress, [ExpressJs](http://expressjs.com/)*
* **Database:** *MySQL (SQL), [MongoDB](https://www.mongodb.com/) (NoSQL)*
* **IDE:** *VisualStudio, PHP Storm, Web Storm, [Cloud 9](http://c9.io)*
* **Technologies:** *jQuery(JavaScript Library), Ajax, Socket.io, NodeJs*

#### Projects:
 * My firs project was online store which used PHP and build on it [Yii2 framework](https://www.yiiframework.com/). This framework is built on the classic based MVC, and use ***OOP***.


**Controller example:** ```public function actionIndex()
	{
        $homeContent = Page::find()->where(array('alias' => 'home'))->one();
        $model = $this->fillPageModel($homeContent);
        $model->setCarouselHeight($this->getSettings('CarouselHeight'));
        $model->setCarouselDelay($this->getSettings('CarouselDelay'));
        $model->setImages(Gallery::find()->all());
		$rootCategories = $this->getRootCategories();
        $list = $this->mapCategories($rootCategories, true);
		$model->setCategories($list);
        $this->fillSeoParams($model);
		return $this->render('index', array('model' => $model));
	}```


**ViewModel example:** ```class HomeModel extends Model {
    private $content;
    private $images;
    private $carouselHeight;
    private $title;
    private $metaKeywords;
    private $metaDescription;
	private $categories;		
	public function setCategories($categories) {		
	    $this->categories = $categories;	
	}		
	public function getCategories() {	
	    return $this->categories;
	}
    public function setMetaDescription($metaDescription)
    {
        $this->metaDescription = $metaDescription;
    }
    public function getMetaDescription()
    {
        return $this->metaDescription;
    }
    public function setMetaKeywords($metaKeywords)
    {
        $this->metaKeywords = $metaKeywords;
    }
    public function getMetaKeywords()
    {
        return $this->metaKeywords;
    }
    public function setTitle($title)
    {
        $this->title = $title;
    }
    public function getTitle()
    {
        return $this->title;
    }
    public function setCarouselDelay($carouselDelay)
    {
        $this->carouselDelay = $carouselDelay;
    }
    public function getCarouselDelay()
    {
        return $this->carouselDelay;
    }
    public function setCarouselHeight($carouselHeight)
    {
        $this->carouselHeight = $carouselHeight;
    }
    public function getCarouselHeight()
    {
        return $this->carouselHeight;
    }
    private $carouselDelay;
    public function setContent($content)
    {
        $this->content = $content;
    }
    public function getContent()
    {
        return $this->content;
    }
    public function getImages()
    {
        return $this->images;
    }
    public function setImages($images)
    {
        $this->images = $images;
    }
}```


**and View example:** ```$this->title = 'About'; $this->params['breadcrumbs'][] = $this->title;```
 <div class="site-about">
	<p>This is the About page. You may modify the following file to customize its content:</p>
	<code>
	```<?php echo __FILE__; ?>```
	</code>
</div>


* Now I learn NodeJs and build on it ***[Express Js](http://expressjs.com/)*** famework, and create on its base CMS system for me. I use NoSqL database ***[MongoDB](https://www.mongodb.com/)***, and Promise consept in this project.
This project is created on IDE ***[Cloud 9](https://c9.io)***
**Below are examples:**

**Controller example:** ```router.get('/user/signOut', (req, res, next) => {
	if (!req.session.user){
		res.redirect('/login');
	} else {
		req.session.destroy();
		res.json({url: '/login', message: 'Сейчас будет произведено перенаправление на страницу входа.'});
	}
});```


**View model example:** ```module.exports = function(userDatabase, userID){
	const UserModel = userModel(userDatabase);
	let list = {};
	return new Promise((resolve, reject) => {
		UserModel.findByUserId(userID, function(user){
			list.id = user._id;
			list.name = user.userName;
			list.userMail = user.eMail;
			list.registred = user.createdAt;
			list.config = user.config;
			resolve(list);
		}, function(err){
			reject(err);
		});
	});
};```


**View example used EJS template:** ```<% for(var i = 0; i<contentBlocks.length; i++){%>
	<% if (contentBlocks[i].type === 'img'){ %>
		<<%- contentBlocks[i].type %> class="<%- contentBlocks[i].gridClass %> img-fluid" data-id="<%- contentBlocks[i].id %>" data-type="<%- contentBlocks[i].category %>" data-pos="<%- contentBlocks[i].position %>" data-name="<%- contentBlocks[i].name %>" src="/<%- user.name+contentBlocks[i].content %>">
		</<%- contentBlocks[i].type %>>
	<% }else{ %>
		<<%- contentBlocks[i].type %> class="<%- contentBlocks[i].gridClass %>" data-id="<%- contentBlocks[i].id %>" data-type="<%- contentBlocks[i].category %>" data-pos="<%- contentBlocks[i].position %>" data-name="<%- contentBlocks[i].name %>">
		<% if (contentBlocks[i].children.length && contentBlocks[i].children.length > 0) { %>
			<%- include('./items', {contentBlocks: contentBlocks[i].children}) %>
		<% } else if (contentBlocks[i].content !== '') { %>
			<%- contentBlocks[i].content %>
		<% } else { %>
			Empty block <%- contentBlocks[i].type %>
		<% } %>
		</<%- contentBlocks[i].type %>>
	<% } %>
<% } %>```

***

## Education:
* **Base education:** *School № 163 of Minsk* ***(1999)***
* **Secondary education:** *Lyceum at the Belarusian state Polytechnic Academy (now Belarusian national Polytechnic University)* ***(2001)***
* **Higher education:** *Belarusian national Polytechnic University* ***(2007)***
* **Self-education:**
    * *Google, different forums like the* ***[Stack Overflow](https://stackoverflow.com/)***, ***[Wikipedia](https://en.wikipedia.org/wiki/Main_Page)***
    * *Computer Science Center* ***[Lektorium](https://www.lektorium.tv/university/2932)***
    * *Different books on the subject*
    * *[Codeacademy](https://www.codecademy.com) HTML and CSS basic courses* 
    * *[Htmlacademy](https://htmlacademy.ru) HTML and CSS basic courses* 

##### English level:
* **A1** (basic)
* **A2** (pre-intermediate)

> I didn't use spoken English after graduation. I used English to ask questions in the discussion forums.

***
 created with [Dillinger](https://dillinger.io/) 