class HomeController < ApplicationController
  
  around_filter :shopify_session, :except => 'welcome'
  
  def welcome
    current_host = "#{request.host}#{':' + request.port.to_s if request.port != 80}"
    @callback_url = "http://#{current_host}/login"
  end
  
  def index
    # get 10 products
    @products = ShopifyAPI::Product.find(:all, :params => {:limit => 10})

    # get latest 5 orders
    @orders   = ShopifyAPI::Order.find(:all, :params => {:limit => 5, :order => "created_at DESC" })

    #get talets 5 customers
    
    @customers = ShopifyAPI::Customer.find(:all,:params => {:limit => 5, :order => "created_at DESC" })

   order = ShopifyAPI::Order.find(267269727)	
   p order.shipping_address.address1 = 'new aaa addddddddddddddddddd'
p    order.save


return

c = ShopifyAPI::Order.create(

  :order=> {
    :line_items=> [
      {
        :variant_id=> 815525719,
        :quantity=> 1
      }
    ],
    :customer=> {
:send_email_invite=> true,
  :first_name => 'Steve test',
  :last_name  => 'Steve last name',
  :email      => 'wizardsasha@gmail.com'    
    },
    :billing_address=> {
      :first_name=> "John",
      :last_name=> "Smith",
      :address1=> "123 Fake Street",
      :phone=> "555-555-5555",
      :city=> "Fakecity",
      :province=> "Ontario",
      :country=> "Canada",
      :zip=> "H0H0H0"
    },
    :shipping_address=> {
      :first_name=> "Jane",
      :last_name=> "Smith",
      :address1=> "123 Fake Street",
      :phone=> "777-777-7777",
      :city=> "Fakecity",
      :province=> "Ontario",
      :country=> "Canada",
      :zip=> "H0H0H0"
    },
   :email      => 'wizardsasha@gmail.com' ,

    :financial_status=> "paid"
  }
)
p '-----------------------'
p c
p c.save
   return 
c = ShopifyAPI::Customer.create(
  :first_name => 'alex api test',
  :last_name  => 'test last name',
  :email      => 'wizardsasha@gmail.com',
:send_email_invite=> true,

  :addresses =>
      [{
        "address1"=> "123 Oak St",
        "city"=> "Ottawa",
        "province"=> "ON",
        "phone"=> "555-1212",
        "zip"=>"123 ABC",
        "last_name"=> "Lastnameson",
        "first_name"=> "Mother",
        "country"=> "CA"
      }]
    
)
p '-----------------------'
p c
p c.save

return


  end
  
end
