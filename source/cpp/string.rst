#######
String
#######
.. highlight:: cpp
   :linenothreshold: 5

.. default-domain:: cpp

*********
Methods
*********
.. function:: String()
              String(const char * ch)
              String(const String &rhs)
              String(String &&rhs)

   构造函数

.. function:: String& operator=(String &&rhs)
              String& operator=(const String &rhs)

   赋值运算符

.. function:: ~String()

   析构函数

.. function:: char& operator[](size_t index)
              const char& operator[](size_t index) const
              bool operator<(String &rhs) const
              bool operator==(String &rhs) const

   操作符

.. function:: size_t size()
              void swap(String &rhs)

   其他


************
一个实现
************
以下是一个String类的简单实现:

.. code-block:: cpp
   :linenos:
   :emphasize-lines: 3,4,5,6,7

   class String {
   public:
        String()
        : chars_(new char[1])
        {
            chars_[0] = '\0';
        }

        String(const char* chars)
        : chars_(new char[strlen(chars) + 1])
        {
            strcpy(chars_, chars);
        }

        String(const String &rhs)
        : chars_(new char[rhs.size() + 1]
        {
            strcpy(chars_, rhs.chars_);
        }

        String(Strig &&rhs)
        : chars_(rhs.chars_)
        {
            rhs.chars_ = nullptr;
        }

        ~String()
        {
            delete[] chars_;
        }

        String& operator=(String rhs)
        {
            std::swap(chars_, rhs.chars_);
            return *this;
        }

        String& operator=(String &&rhs)
        {
            std::swap(chars_, rhs.chars_);
            return *this;
        }

        bool operator==(const String &rhs)
        {
            return (strcmp(chars_, rhs.chars_) == 0);
        }

        bool operator<(const String &rhs)
        {
            return (strcmp(chars_, rhs.chars_) < 0);
        }

        char& operator[](size_t index) const
        {
            return chars_[index];
        }

        const char& operator[](size_t index) const
        {
            return chars_[index];
        }

        size_t size()
        {
            return strlen(chars_);
        }

    private:
        char * chars_;
    };
