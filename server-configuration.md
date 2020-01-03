# 伺服器管理

建立新的Thigner.io私有實例後，將為其提供一個標準的Web網域 \(similar to "https://mycompany.do.thinger.io"\) ，並使用具有標準Thinger.io品牌外觀的Web控制台。但也可以在此控制台上建立多個品牌重構(rebrand)與修改網域，以便為多個客戶品牌客製化平台的外觀。此功能為部署多租戶(multi-tenant)環境提供解決方案，也可以建立使用同一私有伺服器的多個使用者帳戶，從而為特定項目建立一個隔離的使用者網路。 

在本節中，說明了如何使用伺服器管理工具以簡單的方式設定伺服器以使用此功能。 

## Web控制台更名

Thinger.io實例支援自定義多租戶(multi-tenant)Web控制台。通過主選單"Rebranding"部分中提供的管理工具，可以建立和管理多個客制Web，以便通過更改某些元素將Web控制台的外觀客制給不同的客戶或項目。 例如：

* [x] 品牌色彩
* [x] Web,Favicon和主選單Logo
* [x] 鏈接、電子郵件帳戶、版權

{% hint style="info" %}
請注意，每個Web控制台品牌重構都需要一個獨立的Web網域來支援，可以在主選單的"網域"部分中對其進行管理。
{% endhint %}

### 建立新的Web控制台品牌重構設定檔

點擊"Rebranding"部分的"Add Brand"按鈕，可以建立新的品牌設定檔。該過程首先引入一個Web網域名，該網域名將作為品牌設定檔的ID：

![](.gitbook/assets/image%20%28134%29.png)

### 新增品牌詳細資料

如果網域名有效，則表單內容將擴展，允許編輯來自thinger.io的標準內容來完成品牌詳細資訊：

![](.gitbook/assets/image%20%2816%29.png)

接下來的所有元素都是非強制性的，因此可以將其保留為空，系統即從主選單中移除該按鈕：

* **Domain Name:** 是已更名Web控制台的URL。此Web網域需要如"自定義Web網域"部分中所述的那樣，在系統中引入。
* **Description:** 在此處加入一些有關品牌重構設定檔的其他資訊，以便與其他品牌進行識別。
* **Page title:** 網頁瀏覽器標籤的ID。
* **Page URL:** 引入到公司，客戶或項目網站的鏈接。
* **Company Name:** 此更名所屬的項目、客戶或公司的名稱。 
* **Contact Email:** 使用者用於聯繫以取得支援的主選單"電子郵件"按鈕的電子郵件地址。
* **Twitter Account:** 可以通過在此處新增Twitter社交媒體個人資料的完整URL。
* **Copyright:** 網站底部包含版權聲明，可以在此處自定義版權聲明以保護品牌權利。 

### 自定義Logo

建立品牌時想與眾不同，首選是使用自定義Logo。品牌編輯器的第二部分允許分別更改每個Web控制台Logo。為了獲得良好的結果，需要注意每個Logo的背景色，以獲得足夠的對比度。

![](.gitbook/assets/image%20%2878%29.png)

{% hint style="info" %}
需要以透明背景的SVG或PNG檔案格式引入Logo
{% endhint %}

### **自定義頂部欄**

頂部欄對網站方面也有很大的影響。品牌選單允許更改頂部欄外觀的兩個部分：頂部欄顏色和文字顏色：

![](.gitbook/assets/image%20%2859%29.png)

同樣重要的是要注意選定的顏色，使文字和背景間具有良好的對比度。

### **修改控制台品牌重構**

控制台品牌重命名設定檔完成後，新條目將顯示在品牌重構管理列表中，如下圖所示：

![](.gitbook/assets/image.png)

通過點擊Web網域相關的品牌設定檔標識，可以存取設定表並編輯所有參數。

### 刪除控制台品牌重構設定檔

私有實例中，Web網域可以替換為不同的自定義網域，提供額外的空白標籤(white labeling)功能，並支援多租戶(multi-tenant)部署，其中每個客戶都可以使用其自己的URL存取雲控制台的不同重構品牌。可使用Thinger.io主選單上的"Domain Administration Manager"輕鬆管理此功能。

![](.gitbook/assets/image%20%2876%29.png)

## 自定義Web網域

私有實例中，Web網域可以替換為不同的自定義網域，提供額外的空白標籤(white labeling)功能，並支援多租戶(multi-tenant)部署，其中每個客戶都可以使用其自己的URL存取雲控制台的不同重構品牌。可使用Thinger.io主選單上的"Domain Administration Manager"輕鬆管理此功能。

### 建立一個新的Web網域

在"Domains List"界面中點擊"Add Domain"按鈕，可以存取建立網域的表單內容，在其中可以將實例和說明引入新的Web網域，如下圖所示： 

![](.gitbook/assets/image%20%28155%29.png)

在新增新的Web網域之前，有必要驗證責任(verify the disponibility)並建立一個安全證書，該證書將提供與Web控制台的安全通訊。為此，請點擊"Verify Domain"按鈕。

![](.gitbook/assets/image%20%28170%29.png)

#### 重定向CNAME條目

此過程的重要部分是通過切換到網域管理服務來解決新的Web網域和私有伺服器的原始Web網域之間的重定向。 

![](.gitbook/assets/image%20%28157%29.png)

一旦進行了重定向並且DNS服務傳播了A暫存器，就可以使用"Domain Details"按鈕來驗證網域。 

![](.gitbook/assets/image%20%2836%29.png)

完成此過程後，即可將網域用於品牌重構設定檔中，從而使使用者可以使用自定義URL存取私有實例。

### 修改Web網域

在"Domain List"中，點擊網域名可以打開Web網域名參數。URL無法被更改，如果需要修改，則必須刪除設定檔並建立一個新的設定檔。

### 刪除Web網域

只要在網域列表中選擇任何Web控制台設定檔，然後點擊紅色的"Remove Domain"按鈕，就可以輕鬆刪除該設定檔。

![](.gitbook/assets/image%20%2880%29.png)

請注意，如果將Web網域與重新命名Web控制台相關聯，則將其刪除將阻止存取控制台。

## 管理使用者帳戶

Thinger.io伺服器實例可以支援多個使用者帳戶，這些帳戶可以通過管理者帳戶進行管理。此功能允許建立一個使用者網路，其中每個使用者帳戶都有其自己的資源，例如裝置，儀表板，數據桶甚至是自己的插件。

{% hint style="info" %}
請注意，每增加一個帳戶都會增加記憶體佔用和CPU負載，因此在建立新使用者帳戶時，尤其是在使用Node-RED插件時，監督剩餘的計算資源非常重要。
{% endhint %}

![](.gitbook/assets/image%20%28126%29.png)

管理使用者網路的第一步是點擊主選單上的"User Accounts"標籤。該界面允許顯示使用者帳戶列表並分別管理每個設定檔，如以下各節所述。

### 建立新的使用者帳戶

按下使用者管理列表中的"Add User"按鈕，將打開一個可在其中引入新使用者參數的表單：

![](.gitbook/assets/image%20%28154%29.png)

* **Username**: 帳戶使用者名，此參數用作使用者ID。
* **Email**: 必須是一個有效的電子郵件帳戶。只有此列表中加入的電子郵件才能建立使用者帳戶，以防止入侵者。
* **Pasword**: 是用於登錄到該新使用者帳戶的安全密鑰。
* **Enabled**: 只需點擊此開關即可啟用/禁用每個使用者帳戶
* **Email Verified**: 將此關閉將在註冊時向使用者發送郵件驗證，以確認電子郵件的真實性。

表單填寫完成後，點擊"add user"按鈕將新的使用者設定檔新增到IoT伺服器。

#### 使用者帳戶限制

在伺服器的合同和部署過程中定義了可以在一個實例中建立的使用者帳戶數量。如果達到此值（或未與其他使用者帳戶簽訂合同），則會出現錯誤資訊，如下圖所示：

![](.gitbook/assets/image%20%2839%29.png)

此閾值可以前往Subscriptions Management System進行升級，請使用"Admin Email Account"存取[**此鏈接**](https://thinger.chargebeeportal.com)。

### Remove User Account

使用者帳戶也可以從伺服器實例中刪除，只需選中使用者帳戶設定檔左側的複選框，然後點擊"Remove User"按鈕即可。 

![](.gitbook/assets/image%20%2886%29.png)

{% hint style="danger" %}
請注意，刪除使用者帳戶後，其所有IoT裝置，存儲桶，設定和個人資訊都將被刪除，並且將無法還原它們。
{% endhint %}