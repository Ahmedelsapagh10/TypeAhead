# TypeAhead
TypeAhead in Flutter

 •  من المكتبات المهمه جداً 

واللي هتساعدك ف بناء تطبيقك بشكل جيد و سلس و احترافي بالنسبه للمستخدم المكتبه بكل بساطه فكرتها هتساعدك تعمل قائمه من الاقتراحات و اللي بالضروره مهمه للمستخدم ف عملية البحث لجعل البحث بشكل اسرع و افضل

 • المكتبه سهله جداً في الاستخدام

 •  ودا مثال واقعي للتوضيح



 List<String> keywords = ["A","B","C","D"...];
-  app screens
<div>
<p align="left">
<img src='[https://github.com/Ahmedelsapagh10/seb7a/blob/master/screenshot/2.png](https://media.licdn.com/dms/image/D4D22AQE34GEQ_Ogtjg/feedshare-shrink_1280/0/1715192181975?e=1718841600&v=beta&t=wAIxsgble5akkRuql3CiNd2aMflV0fGqfQjk2wBjuJE)' width="30%"/>

</p>
   TypeAheadField<String>(

                suggestionsCallback: (search) => keywords

                    .where((suggestion) =>

                        suggestion.toLowerCase().contains(search.toLowerCase()))

                    .toList(),

                controller: cubit.searchTextFormController,

                builder: (context, controller, focusNode) {

                  return TextField(

                    controller: controller,

                    focusNode: focusNode,

                    onSubmitted: (value) {

                    // you can for ex: navigate to screen with value that user write it.

                    },

                    autofocus: true,

                    decoration: InputDecoration(

                      hintText: Config.localization['search'],

                      border: InputBorder.none,

                      helperStyle: TextStyle(

                        fontSize: getSize(context) / 22,

                      ), 

                    ),

                  );

                },

                itemBuilder: (context, item) {

                  return ListTile(

                    title: Text(item),

                  );

                },

                onSelected: (item) {

                // you can for ex: navigate to screen with value that user select it.

                },

              )



 • link: https://pub.dev/packages/flutter_typeahead
