		jQuery(document).ready(function(){
			var reelOne = $('#frame-one'),
				reelTwo = $('#frame-two'),
				reelThree = $('#frame-three');

			function spinReel(domObj, bgValue){
				console.log('I spun');
				domObj.animate({'background-position': bgValue}, 3500);
			};
			function resetReel(){
				console.log('I reset');
				// var x = '50% 0%'
				reelOne.css('background-position', '50% 0%');
				reelTwo.css('background-position', '50% 0%');
				reelThree.css('background-position', '50% 0%');
			};
			$('body').on('click', '#spin', function(){
				resetReel();
				$('.winning-message').hide();
				 generateSpinAmount(reelOne);
				 generateSpinAmount(reelTwo);
				 generateSpinAmount(reelThree);
				 checkForWin();
			});
			function generateSpinAmount(theDomObject){
				var randomNum = Math.floor(Math.random() * 3) + 1;
				if(randomNum === 3){
					spinReel(theDomObject, '50% 12000px'); 
				} else if(randomNum === 2){
					spinReel(theDomObject, '50% 10000px');
				} else {
					spinReel(theDomObject, '50% 8000px');
				}
				theDomObject.randomNum = randomNum;
			};
			function checkForWin(){
				if (reelOne.randomNum == reelTwo.randomNum && reelOne.randomNum == reelThree.randomNum){
					setTimeout(function(){
					 	$('.winning-message').fadeIn('slow');
					}, 3600);
					
				} else{

				}
			};
		});