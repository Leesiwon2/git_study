git study

<h1>1. click event bubbling</h1>
  - jQuery 클릭 이벤트 실행시 1번이 아니라 부모 노드까지 클릭 이벤트 실행

  1. .off()
      $(document).off('click').on('click','.btn_toggle', function(){
	      $(this).toggleClass('on');
      });
    - 이벤트 바인딩 해제하는 경우에 사용
 
 2. .stopPropagation()
    $(document).on('click', function(e){
      e.stopPropagation();
    });    
    - 부모 태그로의 이벤트 전파를 stop
    - 기본 이벤트를 막진 않음
    - e.isPropagationStopped() 를 사용하여 호출되었는지 확인 가능

 3. .preventDefault()
    $(document).on('click', function(e){
      e.preventDefault();
    });  
    - 기본 이벤트까지 막음
