Template Front-end para os serviços do RS Móvel
===============================================

Template para ser usado como base na construção das interfaces dos serviços do RS Móvel, é baseado em Bootstrap from Twitter e não depende de tecnologias de back-end.

* * *

##Exemplo de comunicação AJAX/JSON(P)

	$.ajax({
		url: "http://gd.geobytes.com/AutoCompleteCity",
		dataType: "jsonp",
		data: { q : $("#f_busca").val() },
		success: function(response) {
			$("#cities ul").empty();
			$.each(response, function(i, item) {
				$("#cities ul:last").append("<li>"+item+"</li>");
			});
		}
	});
