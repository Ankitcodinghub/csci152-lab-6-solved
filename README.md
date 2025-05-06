# csci152-lab-6-solved
**TO GET THIS SOLUTION VISIT:** [CSCI152 Lab 6 Solved](https://www.ankitcodinghub.com/product/csci152-lab-6-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;96949&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSCI152 Lab 6 Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
<ol start="0">
<li>Goal of this exercise is to make you familiar with implementation of set using a hash table.
A set contains elements, but it does not distinguish how often an element occurs. A hash table uses a hash function to compute an index in a vector where the string will be stored. Because there are more strings than possible indices in the vector, it will happen that two different strings have the same index. In order to deal with this, we list to store the strings that have the same index in the vector. In theory, a hash table should be more efficient than a binary search tree, because computation of the hash function can be done in constant time, and the size of the lists will be bounded by a constant.

In this task, you have to complete an implementation of set over std::string using a hash table. If everything goes well, you will see that the asymptotic performance of set, implemented with a hash table has has a somewhat better performance than the implementation of set implemented with BST.

Lab exercise 6 is a continuation of exercises 3, 4 and 5. In order to make the measurements, reuse the classes timer and timetable from the previous exercises. Explanations about their use were given in lab exercise 3.

Download files set.h, set.cpp, main.cpp and Makefile. Set, using hash map, is implemented as follows:
</li>
</ol>
</div>
</div>
<div class="layoutArea">
<div class="column">
class set {

</div>
</div>
<div class="layoutArea">
<div class="column">
1

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
size_t set_size;

double max_load_factor;

std::vector&lt; std::list&lt; std::string &gt;&gt; buckets;

};

Field set_size contains the number of string in the hash table. max_load_factor defines the maximal value that the load factor set_size / buckets. size( ) can have. The load factor is the average size of the list in the vector. If the load factor becomes bigger than the allowed maximum, the set must be rehashed.

As in previous exercises, strings are compared without distinguishing be- tween upper and lower case. You have already implemented a function

bool equal( const std::string&amp; , const std::string&amp; ) that is case in- sensitive. The hash function must agree with equal. Strings for which equal returns true must have the same hash value.

<ol>
<li>Complete the function hash( const std::string&amp; s ) that computes a hash value for s. This function must agree with equal, which means that it must not distinguish between upper and lower case characters.
So, hash( “NurSultan” ) == hash( “nursultan” ) must return true.
</li>
<li>Complete the method bool simp_insert( const std::string&amp; s ) in file set.cpp. As usual, simp_insert returns true, when insertion takes place. It is called ’simp’, because it does not rehash. Do not forget to update set_size when s is inserted.</li>
<li>Implementthemethodstd::ostream&amp;print(std::ostream&amp;out)const. When you are finished, you can remove #if 0 and #endif around std::ostream&amp; operator &lt;&lt; ( std::ostream&amp; out, const set&amp; s ).</li>
<li>Implement bool remove( const std::string&amp; s ) in file set.cpp. The function must return true if s was found and removed. Do not forget
to update set_size when s is removed.
</li>
<li>Complete the method void clear( ) in file set.cpp.</li>
<li>Complete the method void rehash( size_t newbucketsize ). It should start with
if( newbucketsize &lt; 4 ) newbucketsize = 4;

std::vector&lt; std::list&lt; std::string &gt;&gt; newbuckets = std::vector&lt; std::list&lt; std::string &gt;&gt; ( newbucketsize );
</li>
<li>Complete method bool set::insert( const std::string&amp; s ). First call simp_insert( const std::string&amp; s ), and after that, decide if a
2
</li>
</ol>
</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
rehash is necessary. As with ensure_capacity, make sure that the bucket size is at least doubled in size.

8. As in the previous lab exercises, you can now do some measurements. The code for doing this is present in main.cpp. The performance should be O(n), and it should be better than the performance of the BST-based implementation of set.

Make two measurements: One for set someset1 (default max_load_factor of 3.0), and one using set someset1( 4, 25.0 ) (max_load_factor is 25.0).

</div>
</div>
<div class="layoutArea">
<div class="column">
3

</div>
</div>
</div>
