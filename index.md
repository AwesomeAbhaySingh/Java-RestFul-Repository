if you want get random record in database use Hibernate Criteria then Follow this code

Criteria criteria = session.createCriteria(Table.class);
criteria.add(Restrictions.eq("your database field name", put your value));
criteria.add(Restrictions.sqlRestriction("1=1 order by rand()"));
criteria.setMaxResults(1);
return criteria.list();
