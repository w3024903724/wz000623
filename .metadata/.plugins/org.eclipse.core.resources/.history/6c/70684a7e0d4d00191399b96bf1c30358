package com.yychatserver.controller;

import java.io.IOException;
import java.io.ObjectInputStream;
import java.net.*;

import com.yychat.model.User;

public class StartServer {
	ServerSocket ss;
	public StartServer(){
		try{
		ss=new ServerSocket(3456);
		System.out.println("服务器已经启动，监听3456端口");//1024以上的端口
		Socket s=ss.accept();
		System.out.println("连接成功:"+s);
		
		ObjectInputStream ois=new ObjectInputStream(s.getInputStream());
		User user=(User)ois.readObject();
		System.out.println(user.getUserName());
		System.out.println(user.getPassWord());
	    
	}catch (IOException e){
		e.printStackTrace();
	}catch (ClassNotFoundException e){
		e.printStackTrace();
	}
  }
}
