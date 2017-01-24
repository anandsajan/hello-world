# hello-world
asd
		'click .cancel': 'cancel',
		'click .delete-book': 'delete'
		
	},
	 
	edit: function() {
		$('.edit-book').hide();
		$('.delete-book').hide();
		this.$('.update-book').show();
sadbhdgashgdjhabgsld
a'sldljahsd
'laspjhda;
ksdpkaks;kd
aksodpalsl
\'l;hjkcf
\llh
	},
	this sis somethin g thatcan be rendered using backbone layout manager
	
});

// Backbone View for collection

var BooksView = Backbone.View.extend({
	model: books,
	el: $('.catalogue'),
	initialize: function() {
		var self = this;
		this.model.on('add', this.render, this);
		this.model.on('change', function() {
			setTimeout(function() {
				self.render();
			}, 30);
		},this);
	
		this.model.on('remove', this.render, this);
	},
	render: function() {
		var self = this;
		this.$el.html('');
		
		_.each(this.model.toArray(), function(book) {
			
			self.$el.append((new BookView({model: book})).render().$el);
		});
		return this;
	}
});


var booksView = new BooksView();

$(document).ready(function() {
	booksView.render();
		booksView.render();
			booksView.render();
				booksView.render();
	$('.add-input').on('click', function() {
		var bookNew = new Book({
			book: $('.book-input').val(),
			author: $('.author-input').val(),
			price: $('.price-input').val()
		});
		$('.book-input').val('');
		$('.author-input').val('');
		$('.price-input').val('');
		console.log(bookNew.toJSON());
		books.add(bookNew);
	})

})
