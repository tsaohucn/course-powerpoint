設定檔

<span style="color:red">spec_helper</span>

<span style="color:red">rails_helper</span>

---
基本語法

---
情境描述

<span style="color:red">describe</span>

<span style="color:red">context</span>

<span style="color:red">it</span>

<span style="color:red">specify</span>

---

<span style="color:red">describe</span> 
<span style="color:Yellow">"Class/Method Name"</span> do

 ...

end

---
<span style="color:red">context</span> 
<span style="color:Yellow">"Context-Describe"</span> do

 ...

end

---
<span style="color:red">it</span> 
<span style="color:Yellow">"Behavior-Describe"</span> do

 ...

end

---
<pre>
  describe "#check" do
    context "when excute the agent first time" do
      it "must create one event"
    end
  end
</pre>

---
HOOK

<span style="color:red">before</span>

<span style="color:red">after</span>

<span style="color:red">around</span>

---
<span style="color:red">before(:all)</span> do

...

end

<span style="color:red">before(:each)</span> do

...

end

---
<pre>
  before(:each) do
    @agent = Agents::NexmoServiceAgentV1.new(
      name: 'NexmoServiceAgentV1',
      options: {
        mode: "VoiceCall",
        message: "Hi, I'm tomato.",
        voice: "female",
        callNumber: "886988341426"
      }
    )
  end
</pre>

---
<span style="color:red">subject</span>

<span style="color:red">let</span>

---
<pre>
let(:address) { { street: street, city: city } }let(:street)  { "123 Any Street"               }let(:city)    { "Anytown"                      }
</pre>

---
MOCK

<span style="color:red">Test Doubles</span>

<span style="color:red">Method Stubs</span>

rspec-mocks <https://github.com/rspec/rspec-mocks>

rr <https://github.com/mozilla/rr>

---
HTTP MOCK

webmock <https://github.com/bblimke/webmock>

vcr <https://github.com/vcr/vcr>

---
TIME MOCK

timecop <https://github.com/travisjeffery/timecop>

delorean <https://github.com/bebanjo/delorean>

---
FrontEnd Test

capybara <https://github.com/teamcapybara/capybara>

selenium <https://github.com/SeleniumHQ/selenium>

---
Shared Example Groups

<span style="color:red">shared_examples_for</span><span style="color:Yellow">"xxx"</span> do

...

end

<span style="color:red">it_behaves_like</span><span style="color:Yellow">"xxx"</span> do

...

end

---
factory_girl <https://github.com/thoughtbot/factory_girl>

<http://betterspecs.org/zh_tw/>

Adam Cuppy <https://www.youtube.com/watch?v=KjENZNjRCWM&t=1228s>

<http://carlos-blog.logdown.com/posts/2016/05/24/rails-pacific-2016-about-adam-cuppy-of-rspec>
