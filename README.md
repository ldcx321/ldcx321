前端学习笔记
1. li选中显示指定div
<ul>
  <li>1</li>
  <li>2</li>
  <li>3</li>
</ul>
<div>
  <div>1</div>
  <div>2</div>
  <div>3</div>
</div>
<script>
  $(window).load(function() {
		  $(".right-div>div").eq(0).show().siblings().hide();
		});  
		$(".wrap>li").click(function() {
		 	$(this).addClass('active').siblings().removeClass('active');
			var index = $(this).index();
			$(".right-div>div").eq(index).show().siblings().hide();
		});  
  </script>
  
