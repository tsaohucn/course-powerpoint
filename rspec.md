設定檔

spec_helper

rails_helper

---
基本語法

---
情境描述

<span style="color:red">describe</span>

<span style="color:blue">context</span>

<span style="color:green">it</span>

---

<span style="color:red">describe</span> 
<span style="color:Yellow">"Class/Method Name"</span> do
<br>
 ...
<br>
<span style="text-align:left">end</span>

---
<span style="color: blue"> context </span> 
<span style="color:Yellow">"Context-Describe"</span> do
<br>
 ...
<br>
<span style="text-align:left">end</span>

---
<span style="color: green"> it </span> 
<span style="color:Yellow">"Behavior-Describe"</span> do
<br>
 ...
<br>
<span style="text-align:left">end</span>

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

<span style="color:blue">after</span>

<span style="color:green">around</span>

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

<span style="color:blue">let</span>

---
MOCK

---
HTTP MOCK

---
TIME MOCK

---
Shared Example Groups

---
factory_girl <https://github.com/thoughtbot/factory_girl>

rspec-html-matchers <https://github.com/kucaahbe/rspec-html-matchers>

vcr <https://github.com/vcr/vcr>

webmock <https://github.com/bblimke/webmock>

rr <https://github.com/mozilla/rr>