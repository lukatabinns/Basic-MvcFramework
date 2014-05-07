<?php
class Dash extends Controller{


	function __construct(){
		parent::__construct();
		Start::init();
		$logged = Start::get('loggedIn');
		
		if ($logged == false){
			Start::destroy();
			header ('location:' .URL. 'login');
			exit;
		}
		//echo 'we are in index';
		//$this->view->render('login/index');
		$this->view->js = array('dash/js/default.js');
	}
	
	function index() {
		
		$this->view->render('dash/index');
	}
	function logout(){
	
		Start::destroy();
			header ('location: ../login');
			exit;
	}
	
	function xhrInsert()
	{
		$this->model->xhrInsert();
	
	}
	
	function xhrGetListings ()
	{
		$this->model->xhrGetListings();

		
	}
}
