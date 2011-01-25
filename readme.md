SimpleCaptcha for CakePHP
=========================

Simple captcha plugin for CakePHP.

Install
-------

Checkout into plugin directory.

Usage Example
-------------
### Helper 

Include helper in the Controller:

	var $helpers = array (
			'SimpleCaptcha.SimpleCaptcha',
	);


### Behavior

Attach Behavior. E.g. dynamically in Controller:

		if (!empty($this->data)) {
			$this->User->Behaviors->attach('SimpleCaptcha');
			if ($this->User->save($this->data)) { 
				…


### Use in View

		 echo $this->SimpleCaptcha->input('User', 
				 array(
						 'error' => array(
								'captchaResultIncorrect' 	=> __('captcha_result_incorrect', true),
								'captchaResultTooLate' 		=> __('captcha_result_too_late', true),
							),
						 'div' =>  array( 'class' => 'required'),
						)
				 );


