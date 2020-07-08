# Tabs
By connecting this file to HTML markup, you can hide unnecessary blocks in separate parts of the site, 
and show only the one that is related to this part of the site.
```
let tab,info,tabContent;
    function createVariable(tabs, inf, tabContents){
        tab = document.querySelectorAll('.' + tabs + '');
        info = document.querySelector('.' + inf + '');
        tabContent = document.querySelectorAll('.' + tabContents + '');
           
    }
    
    createVariable('info-header-tab','info-header','info-tabcontent');
```
### Description of variables: 
#### tab - parts of the site, when clicked, show the information attached to them and hide the rest.
#### info - parent which include in self parts of the site (tab).
#### tabContent - site blocks containing information displayed in tabs (tab)

### Values passed to the function createVariable('info-header-tab','info-header','info-tabcontent');
#### 1 - the class name of HTML elements that contain tabs.
```
          <div class="info-header-tab">Лечение</div>
					<div class="info-header-tab">Отдых</div>
					<div class="info-header-tab">Природа</div>
					<div class="info-header-tab">Йога</div>
```

#### 2 - the class name of HTML element that is the parent of the tabs(1);
```
        <div class="info-header">
					<div class="info-header-tab">Лечение</div>
					<div class="info-header-tab">Отдых</div>
					<div class="info-header-tab">Природа</div>
					<div class="info-header-tab">Йога</div>
				</div>
```

#### 3 - the name of the class of HTML elements that contain the information that should be displayed inside the tabs
```
<div class="info-tabcontent fade">
					<div class="description">
						<div class="description-title">Здоровый позвоночник</div>
						<div class="description-text">Йога, массажи и плавание в море - помогут уставшей спине! Индийские йоги считали, что здоровье человека можно определить по тому, насколько здоров и гибок у него позвоночник.<br> Интересно, что бы древние йоги сказали, глядя на современного человека, который уже со школьного возраста мучается болями в спине, работает подолгу в неудобных сидячих позах и не умеет расслабляться, имеет искривление, которое в итоге приведет к болезням других органов? Йоги сказали бы – займись собой и срочно!
						</div>
						<div class="description-btn">
							Узнать подробнее
						</div>
					</div>
					<div class="photo">
						<img src="img/massage.jpg" alt="Massage">
					</div>
				</div>
```


### classes are hidden and displayed in functions taken from style.css
