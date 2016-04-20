######
Vector
######

.. highlight:: cpp
.. default-domain:: cpp

*******
Methods
*******

.. function:: Vector(size_t size)
              Vector(Vector rhs)
              Vector(Vector &&rhs)

   构造函数

.. function:: ~Vector()

   析构函数

.. function:: Vector& operator=(Vector rhs)
              Vector& operator=(Vector &&rhs)

   赋值操作

.. function:: bool empty() const
              size_t size() const
              size_t capacity() const
              void resize(size_t newSize)
              void reserve(size_t newSize)

   size查询和操作

.. function:: Object& front()
              const Object& front() const
              Object& back()
              const Object& back() const
              void push_back(Object &x)
              void push_back(Object &&x)
              void pop_back()
              clear()

   元素操作

.. function:: operator[](size_t idx)

   下标运算

.. function:: iterator begin()
              const_iterator end() const
              iterator end()
              const_iterator begin() const

   iterator操作

**********
简单实现
**********
