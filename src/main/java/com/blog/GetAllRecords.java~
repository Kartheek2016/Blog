package com.blog;

import org.hibernate.Session;
import org.hibernate.Query;

import java.util.List;
import java.util.Iterator; 

public class GetAllRecords {
 
	public static void main(String[] args) {
		Session session = HibernateSessionManager.getSessionFactory().openSession();
		session.beginTransaction();

		Query query = session.createQuery("from Post");
		List list = query.list();
		for (Iterator iterator = list.iterator(); iterator.hasNext();){
			Post post = (Post) iterator.next(); 
			System.out.print(post.getPostId() +". ");
			System.out.print(post.getTitle() +": ");
			System.out.println(post.getBody());
 	        }
 	}

}
