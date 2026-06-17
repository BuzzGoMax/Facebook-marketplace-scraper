[Facebook Marketplace Scraper](https://apify.com/datavoyantlab/Facebook-marketplace-scraper?fpr=data)

## Facebook Marketplace Scraper – Unlock Market Insights Across All Categories!

Introducing the **Facebook Marketplace Scraper**—your ultimate tool for effortlessly extracting detailed information from Facebook Marketplace listings. Whether you're diving into research, conducting analysis, or tracking market trends, this powerful scraper simplifies the data-gathering process for **all categories**, including Vehicles, Electronics, Classifieds, and **Real Estate**!

### Why Choose Our Scraper?

- **Comprehensive Data Collection**: Capture essential details like item descriptions, prices, and advanced listing information to get a holistic view of the market.
- **Real Estate Made Easy**: Gain instant insights into property listings—just a click away!

### 💰 Pricing

**Pay-Per-Event** - Only pay for what you scrape:

| Event | Free Tier | Bronze | Silver | Gold |
| --- | --- | --- | --- | --- |
| Actor start | $0.05/run | $0.004/run | $0.003/run | $0.003/run |
| Basic listing | $2.00/1K | $0.48/1K | $0.46/1K | $0.45/1K |
| Detailed listing | $4.00/1K | $0.90/1K | $0.85/1K | $0.80/1K |

**Free Tier:**

- 1 URL per run
- 100 items maximum
- All features enabled

### 💳 What Data Can You Extract?

*Discover key data points available for extraction (not an exhaustive list):*

| **ID** 🆔 | **Primary Photo URI** 📸 | **Listing Price** 💵 | **Location** 🌐 |
| --- | --- | --- | --- |
| **Condition** ℹ️ | **Inventory Count** #️⃣ | **Creation Time** 📅 | **Vehicle Info** 🚗 |
| **Delivery Types** 🚚 | **Seller Info** 👤 | **Vehicle Features** 🚘 | **Safety Ratings** 📊 |
| **Listing Photos** 📷 | **Additional Data** 📚 | **Reviews** 💬 | **and More...** |

### 📊 Use Cases for Facebook Marketplace Scraper

1. **Market Research**: Analyze pricing and trends across local listings.
2. **Competitive Analysis**: Monitor competitors’ pricing and inventory strategies.
3. **Product Sourcing**: Identify profitable products for resale.
4. **Real Estate Insights**: Gather data on property prices and trends.
5. **Vehicle Pricing**: Analyze used vehicle listings for pricing trends.
6. **User Feedback**: Evaluate customer satisfaction through reviews.
7. **Inventory Management**: Track stock levels of specific items.
8. **Event Planning**: Find local items related to upcoming events.
9. **Academic Research**: Use data for studies on consumer behavior.
10. **Personal Shopping**: Create alerts for specific items or deals.

### 📤 Output Sample

The **Facebook Marketplace Scraper** produces structured output in JSON format. Here’s a sample of what you can expect:

```
[{
  "id": "464852716160618",
  "primary_listing_photo": {
    "image": {
      "uri": "https://scontent-iad3-1.xx.fbcdn.net/v/t45.5328-4/448669566_935633465000468_5157298062483481406_n.jpg?stp=c0.43.261.261a_dst-jpg_p261x260&_nc_cat=107&ccb=1-7&_nc_sid=247b10&_nc_aid=0&_nc_ohc=pjnluxmbc1UQ7kNvgHhVleV&_nc_ht=scontent-iad3-1.xx&oh=00_AYA1cqrOWO3v7KylZX6gXILtOhOtlUlff5za7-slIjEepA&oe=66F28454"
    },
    "id": "935633461667135"
  },
  "listing_price": {
    "formatted_amount": "$52,000",
    "amount_with_offset_in_currency": "5200000",
    "amount": "52000.00"
  },
  "strikethrough_price": {
    "formatted_amount": "$66,500",
    "amount": "66500.00"
  },
  "comparable_price": null,
  "comparable_price_type": null,
  "location": {
    "reverse_geocode": {
      "city": "San Francisco",
      "state": "CA",
      "city_page": {
        "display_name": "San Francisco, California",
        "id": "114952118516947"
      }
    }
  },
  "is_hidden": false,
  "is_live": true,
  "is_pending": false,
  "is_sold": false,
  "is_viewer_seller": false,
  "min_listing_price": null,
  "max_listing_price": null,
  "marketplace_listing_category_id": "807311116002614",
  "marketplace_listing_title": "2015 Transcraft Fassi Crane Perkins Custom",
  "custom_title": "2015 Transcraft Fassi Crane Perkins custom",
  "custom_sub_titles_with_rendering_flags": [
    {
      "subtitle": ""
    }
  ],
  "origin_group": null,
  "listing_video": {
    "id": "1147767813219137"
  },
  "parent_listing": null,
  "marketplace_listing_seller": {
    "name": "Vladimir Mikshansky",
    "id": "pfbid0pmDV6LQCr22oJuKtFePzExzYi9bFw7FpUwpSE8Bo1nV4vkr5pCBG1VaNFeyKFpgEl"
  },
  "delivery_types": [
    "IN_PERSON"
  ],
  "listing_details": {
    "marketplace_listing_title": "2015 Transcraft Fassi Crane Perkins Custom",
    "id": "464852716160618",
    "story": {
      "translation_available_for_viewer": false,
      "translatability_for_viewer": {
        "source_dialect_name": "English"
      },
      "translated_message_for_viewer": null,
      "id": "UzpfSTExNzA0NzQ0OlZLOjQ2NDg1MjcxNjE2MDYxOA==",
      "actors": [
        {
          "name": "Vladimir Mikshansky",
          "id": "pfbid0pmDV6LQCr22oJuKtFePzExzYi9bFw7FpUwpSE8Bo1nV4vkr5pCBG1VaNFeyKFpgEl"
        }
      ],
      "url": "https://www.facebook.com/marketplace/item/464852716160618/",
      "tracking": "{\"story_location\":26,\"story_attachment_style\":\"native_templates\",\"ent_attachement_type\":\"LegacyCommerceAttachment\",\"actrs\":\"11704744\"}",
      "save_info": {
        "viewer_save_state": "NOT_SAVED"
      },
      "post_id": "7789060431187075"
    },
    "redacted_description": {
      "text": "For sale is our 2015 Crane Works self powered Perkins Powered hydraulic pump unit Fassi Knuckle boom trailer. The Trailer has a Fassi F335A.2.25CW knuckle boom and Perkins hydraulic power unit sit on a Transcraft trailer which is rated at 80,000 Lb. It has low usage, a remote, 2 outriggers as well as 2 downriggers and ready for work. Truck not included but can be purchased for an additional cost with the trailer."
    },
    "creation_time": 1718825686,
    "location_text": {
      "text": "San Francisco, CA"
    },
    "location_vanity_or_id": "sanfrancisco",
    "is_viewer_seller": false,
    "listing_inventory_type": "SINGLE_QUANTITY",
    "formatted_price": {
      "text": "$52,000"
    },
    "listing_price": {
      "amount_with_offset": "5200000",
      "currency": "USD",
      "amount": "52000.00"
    },
    "payment_time_period": null,
    "condition": "USED",
    "custom_title": "2015 Transcraft Fassi Crane Perkins custom",
    "is_live": true,
    "is_pending": false,
    "is_sold": false,
    "logging_id": "7789060431187075",
    "marketplace_lead_gen_form": null,
    "listed_by": null,
    "real_estate_listing_agent": null,
    "inventory_count": null,
    "legal_reporting_cta_type": null,
    "legal_reporting_uri": null,
    "messaging_enabled": true,
    "listing_is_rejected": false,
    "seller_message_thread": null,
    "is_checkout_enabled": false,
    "is_draft": false,
    "can_seller_edit": false,
    "origin_group": null,
    "default_variant_listing": null,
    "is_hidden": false,
    "marketplace_listing_seller": {
      "id": "pfbid0pmDV6LQCr22oJuKtFePzExzYi9bFw7FpUwpSE8Bo1nV4vkr5pCBG1VaNFeyKFpgEl",
      "user_id": "pfbid0pmDV6LQCr22oJuKtFePzExzYi9bFw7FpUwpSE8Bo1nV4vkr5pCBG1VaNFeyKFpgEl",
      "marketplace_user_profile": {
        "c2c_orders_shipped": null,
        "id": "10103629887677908"
      },
      "name": "Vladimir Mikshansky",
      "profile_picture": {
        "uri": "https://scontent-phx1-1.xx.fbcdn.net/v/t1.6435-1/187798740_10104306706941678_6769379530235797617_n.jpg?stp=cp0_dst-jpg_s80x80&_nc_cat=107&ccb=1-7&_nc_sid=e4545e&_nc_ohc=_1Ct536EurMQ7kNvgFMzUV2&_nc_ht=scontent-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYCEL1mz4sWudLiR_GQUeN4FZ2flXv1Hupg4E3Hchznu0Q&oe=671428D6"
      },
      "profile_picture_160": {
        "uri": "https://scontent-phx1-1.xx.fbcdn.net/v/t1.6435-1/187798740_10104306706941678_6769379530235797617_n.jpg?stp=dst-jpg_s240x240&_nc_cat=107&ccb=1-7&_nc_sid=e4545e&_nc_ohc=_1Ct536EurMQ7kNvgFMzUV2&_nc_ht=scontent-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYAHsjp63cYR-S3l_skTg7bUGon3YODjtt1ZIH0KfKLbLA&oe=671428D6"
      },
      "profile_picture_112": {
        "uri": "https://scontent-phx1-1.xx.fbcdn.net/v/t1.6435-1/187798740_10104306706941678_6769379530235797617_n.jpg?stp=dst-jpg_s200x200&_nc_cat=107&ccb=1-7&_nc_sid=e4545e&_nc_ohc=_1Ct536EurMQ7kNvgFMzUV2&_nc_ht=scontent-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYAdj2UW6qMjd2A4H3-CQzjbsH9g45mkn3RirP8TIhbOFg&oe=671428D6"
      },
      "profile_picture_64": {
        "uri": "https://scontent-phx1-1.xx.fbcdn.net/v/t1.6435-1/187798740_10104306706941678_6769379530235797617_n.jpg?stp=dst-jpg_s100x100&_nc_cat=107&ccb=1-7&_nc_sid=e4545e&_nc_ohc=_1Ct536EurMQ7kNvgFMzUV2&_nc_ht=scontent-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYBlCaBoSAvXwCR7TFUOOEJp_KHqTmiI18XSYRpNOA6bIA&oe=671428D6"
      },
      "profile_picture_60": {
        "uri": "https://scontent-phx1-1.xx.fbcdn.net/v/t1.6435-1/187798740_10104306706941678_6769379530235797617_n.jpg?stp=dst-jpg_s100x100&_nc_cat=107&ccb=1-7&_nc_sid=e4545e&_nc_ohc=_1Ct536EurMQ7kNvgFMzUV2&_nc_ht=scontent-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYBlCaBoSAvXwCR7TFUOOEJp_KHqTmiI18XSYRpNOA6bIA&oe=671428D6"
      },
      "profile_picture_50": {
        "uri": "https://scontent-phx1-1.xx.fbcdn.net/v/t1.6435-1/187798740_10104306706941678_6769379530235797617_n.jpg?stp=cp0_dst-jpg_s80x80&_nc_cat=107&ccb=1-7&_nc_sid=e4545e&_nc_ohc=_1Ct536EurMQ7kNvgFMzUV2&_nc_ht=scontent-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYCEL1mz4sWudLiR_GQUeN4FZ2flXv1Hupg4E3Hchznu0Q&oe=671428D6"
      },
      "commerce_profile_picture_with_fallback_160": {
        "uri": "https://scontent-phx1-1.xx.fbcdn.net/v/t1.6435-1/187798740_10104306706941678_6769379530235797617_n.jpg?stp=dst-jpg_s240x240&_nc_cat=107&ccb=1-7&_nc_sid=e4545e&_nc_ohc=_1Ct536EurMQ7kNvgFMzUV2&_nc_ht=scontent-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYAHsjp63cYR-S3l_skTg7bUGon3YODjtt1ZIH0KfKLbLA&oe=671428D6"
      },
      "commerce_profile_picture_with_fallback_112": {
        "uri": "https://scontent-phx1-1.xx.fbcdn.net/v/t1.6435-1/187798740_10104306706941678_6769379530235797617_n.jpg?stp=dst-jpg_s200x200&_nc_cat=107&ccb=1-7&_nc_sid=e4545e&_nc_ohc=_1Ct536EurMQ7kNvgFMzUV2&_nc_ht=scontent-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYAdj2UW6qMjd2A4H3-CQzjbsH9g45mkn3RirP8TIhbOFg&oe=671428D6"
      },
      "commerce_profile_picture_with_fallback_64": {
        "uri": "https://scontent-phx1-1.xx.fbcdn.net/v/t1.6435-1/187798740_10104306706941678_6769379530235797617_n.jpg?stp=dst-jpg_s100x100&_nc_cat=107&ccb=1-7&_nc_sid=e4545e&_nc_ohc=_1Ct536EurMQ7kNvgFMzUV2&_nc_ht=scontent-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYBlCaBoSAvXwCR7TFUOOEJp_KHqTmiI18XSYRpNOA6bIA&oe=671428D6"
      },
      "commerce_profile_picture_with_fallback_60": {
        "uri": "https://scontent-phx1-1.xx.fbcdn.net/v/t1.6435-1/187798740_10104306706941678_6769379530235797617_n.jpg?stp=dst-jpg_s100x100&_nc_cat=107&ccb=1-7&_nc_sid=e4545e&_nc_ohc=_1Ct536EurMQ7kNvgFMzUV2&_nc_ht=scontent-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYBlCaBoSAvXwCR7TFUOOEJp_KHqTmiI18XSYRpNOA6bIA&oe=671428D6"
      },
      "commerce_profile_picture_with_fallback_50": {
        "uri": "https://scontent-phx1-1.xx.fbcdn.net/v/t1.6435-1/187798740_10104306706941678_6769379530235797617_n.jpg?stp=cp0_dst-jpg_s80x80&_nc_cat=107&ccb=1-7&_nc_sid=e4545e&_nc_ohc=_1Ct536EurMQ7kNvgFMzUV2&_nc_ht=scontent-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYCEL1mz4sWudLiR_GQUeN4FZ2flXv1Hupg4E3Hchznu0Q&oe=671428D6"
      },
      "join_time": 1118201584,
      "marketplace_ratings_stats_by_role": {
        "seller_stats": {
          "five_star_ratings_average": 1,
          "five_star_total_rating_count_by_role": 1
        },
        "seller_ratings_are_private": true
      },
      "marketplace_should_display_verified_badge": false
    },
    "reportable_ent_id": "7789060431187075",
    "hidden_from_friends": "VISIBLE_TO_EVERYONE",
    "can_share": true,
    "can_seller_change_availability": false,
    "messagingEnabled": true,
    "has_children": false,
    "active_order": null,
    "rebuy_order_receipt": null,
    "c2c_shipping_eligible": false,
    "is_shipping_offered": false,
    "most_recent_active_order_as_buyer": null,
    "order_summaries": [],
    "delivery_types": [
      "IN_PERSON"
    ],
    "should_hide_pdp_shipping_content": true,
    "shipping_profile": null,
    "primary_listing_photo": {
      "listing_image": {
        "uri": "https://scontent-phx1-1.xx.fbcdn.net/v/t45.5328-4/448669566_935633465000468_5157298062483481406_n.jpg?stp=c0.22.133.133a_dst-jpg_p133x133&_nc_cat=107&ccb=1-7&_nc_sid=247b10&_nc_aid=0&_nc_ohc=pjnluxmbc1UQ7kNvgGOR7PS&_nc_ht=scontent-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYBbIOtZ-6I4K-ZV4gBhXQrCx3VuYZkaKp1J1C58A9-SNw&oe=66F28454"
      },
      "id": "935633461667135"
    },
    "is_seller_business_onboarded": false,
    "product_item": {
      "id": "7789060431187075",
      "viewer_purchase_limit": -1,
      "boosted_marketplace_listing": null,
      "promoted_listing": null
    },
    "is_buy_now_enabled": false,
    "is_purchase_protected": false,
    "can_buyer_make_checkout_offer": false,
    "is_cart_enabled": false,
    "vacation_mode": null,
    "all_message_threads": {
      "is_empty": true
    },
    "marketplace_listing_category_id": "807311116002614",
    "should_show_txn_survey_on_mas": false,
    "incentive_campaign_for_free_shipping": null,
    "first_message_suggested_value": null,
    "marketplace_bump_info": null,
    "fi_enhanced_appeal_data": null,
    "listing_seller_notices": [],
    "fair_market_value_data": null,
    "vehicle_condition": null,
    "vehicle_exterior_color": "black",
    "vehicle_features": [],
    "vehicle_fuel_type": null,
    "vehicle_identification_number": null,
    "vehicle_interior_color": "black",
    "vehicle_is_paid_off": null,
    "vehicle_make_display_name": "Transcraft Fassi Crane Perkins",
    "vehicle_model_display_name": "custom",
    "vehicle_number_of_owners": "TWO",
    "vehicle_odometer_data": {
      "unit": "MILES",
      "value": null
    },
    "vehicle_registration_plate_information": null,
    "vehicle_seller_type": "PRIVATE_SELLER",
    "vehicle_specifications": {
      "co2_emissions": null,
      "engine_size": null,
      "gas_mileage_city": null,
      "gas_mileage_combined": null,
      "gas_mileage_highway": null,
      "horse_power": null,
      "safety_rating_front": null,
      "safety_rating_overall": null,
      "safety_rating_rollover": null,
      "safety_rating_side": null,
      "safety_rating_side_barrier": null
    },
    "vehicle_title_status": null,
    "vehicle_transmission_type": null,
    "vehicle_trim_display_name": null,
    "vehicle_carfax_report": null,
    "attribute_data": [],
    "location": {
      "latitude": 37.729797363281,
      "longitude": -122.38220214844,
      "reverse_geocode_detailed": {
        "country_alpha_two": "US",
        "postal_code_trimmed": "94124-2872"
      }
    },
    "origin_target": {
      "id": "1663689853903557"
    },
    "shipping_offered": false,
    "legal_disclosure_impressum_url": null,
    "commerce_badges_info": {
      "source_summary": null,
      "badges": []
    },
    "listing_address": null,
    "seller_phone_number": null,
    "vehicle_website_link": null,
    "dealership_name": null,
    "seller": {
      "id": "pfbid0pmDV6LQCr22oJuKtFePzExzYi9bFw7FpUwpSE8Bo1nV4vkr5pCBG1VaNFeyKFpgEl",
      "marketplace_user_profile": {
        "business_information": null,
        "id": "10103629887677908"
      }
    },
    "energy_efficiency_class_eu": null,
    "listing_photos": [
      {
        "accessibility_caption": "No photo description available.",
        "image": {
          "height": 960,
          "width": 720,
          "uri": "https://scontent-phx1-1.xx.fbcdn.net/v/t45.5328-4/448669566_935633465000468_5157298062483481406_n.jpg?_nc_cat=107&ccb=1-7&_nc_sid=247b10&_nc_aid=0&_nc_ohc=pjnluxmbc1UQ7kNvgGOR7PS&_nc_ht=scontent-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYDmQ1NRuvTNj3sSnPvmKNUAHlqLweCqOuOSuT73mZCsyA&oe=66F28454"
        },
        "id": "935633461667135"
      },
      {
        "accessibility_caption": "No photo description available.",
        "image": {
          "height": 720,
          "width": 960,
          "uri": "https://scontent-phx1-1.xx.fbcdn.net/v/t45.5328-4/421640031_266026116567266_6256020285154582873_n.jpg?_nc_cat=107&ccb=1-7&_nc_sid=247b10&_nc_ohc=wFLQ16f2A5UQ7kNvgFDSHWg&_nc_ht=scontent-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYBBijdrWA-dNk62-l83Q4JpSCikwBmz3Xkr4jVWUVqMWA&oe=66F279B1"
        },
        "id": "266026113233933"
      },
      {
        "accessibility_caption": "No photo description available.",
        "image": {
          "height": 960,
          "width": 449,
          "uri": "https://scontent-phx1-1.xx.fbcdn.net/v/t45.5328-4/426416781_784267686836750_3300542603384759717_n.jpg?_nc_cat=104&ccb=1-7&_nc_sid=247b10&_nc_ohc=8os9EyxJUqwQ7kNvgFl5CBt&_nc_ht=scontent-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYDA4QpfXlxdbjYxB4ZdLkxfojYF1k6SEZiyX3IcxQFjLA&oe=66F29165"
        },
        "id": "784267683503417"
      },
      {
        "accessibility_caption": "No photo description available.",
        "image": {
          "height": 720,
          "width": 960,
          "uri": "https://scontent-phx1-1.xx.fbcdn.net/v/t45.5328-4/442994935_452850384161111_6004566060700819927_n.jpg?_nc_cat=102&ccb=1-7&_nc_sid=247b10&_nc_ohc=aMkuCToFilgQ7kNvgHBeFCZ&_nc_ht=scontent-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYBK2bJhNA7xi2uScygaBuhLAvFxQBPTNJJ8deyhKASEYw&oe=66F27E90"
        },
        "id": "452850380827778"
      },
      {
        "accessibility_caption": "No photo description available.",
        "image": {
          "height": 720,
          "width": 960,
          "uri": "https://scontent-phx1-1.xx.fbcdn.net/v/t45.5328-4/442994480_1190194739066815_1237906764615120177_n.jpg?_nc_cat=108&ccb=1-7&_nc_sid=247b10&_nc_ohc=6Lefv9mGdigQ7kNvgHbAU2S&_nc_ht=scontent-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYAdTy3pX0hxaGvZvQorxpUWAoRBcAmimIa232o4dPXLrA&oe=66F2892E"
        },
        "id": "1190194735733482"
      },
      {
        "accessibility_caption": "No photo description available.",
        "image": {
          "height": 960,
          "width": 720,
          "uri": "https://scontent-phx1-1.xx.fbcdn.net/v/t45.5328-4/442994515_832516235476989_8719329906623744910_n.jpg?_nc_cat=103&ccb=1-7&_nc_sid=247b10&_nc_ohc=CfBv7hi8C7IQ7kNvgHI9uhq&_nc_ht=scontent-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYAieTCdoF8rzIZ6kx6qs9jFpOrPOxTWxewgQYxiYw4AwQ&oe=66F286DB"
        },
        "id": "832516232143656"
      },
      {
        "accessibility_caption": "No photo description available.",
        "image": {
          "height": 720,
          "width": 960,
          "uri": "https://scontent-phx1-1.xx.fbcdn.net/v/t45.5328-4/448528616_1658500464967023_9011784083542646732_n.jpg?_nc_cat=109&ccb=1-7&_nc_sid=247b10&_nc_ohc=TMtJD03PapQQ7kNvgH1FWdr&_nc_ht=scontent-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYCOYOjARtEa5uVD5rupvHJKxw41aMt0OgNG5zebB6Jdnw&oe=66F26289"
        },
        "id": "1658500461633690"
      },
      {
        "accessibility_caption": "No photo description available.",
        "image": {
          "height": 720,
          "width": 960,
          "uri": "https://scontent-phx1-1.xx.fbcdn.net/v/t45.5328-4/448606872_449825037861111_4421415103210870424_n.jpg?_nc_cat=109&ccb=1-7&_nc_sid=247b10&_nc_ohc=l112uX1aOkQQ7kNvgFKP0se&_nc_ht=scontent-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYC9OOzC9Wror2aBWkMuW0l9Bb6g778qo2We4HmPdBfpJg&oe=66F28958"
        },
        "id": "449825034527778"
      },
      {
        "accessibility_caption": "No photo description available.",
        "image": {
          "height": 617,
          "width": 960,
          "uri": "https://scontent-phx1-1.xx.fbcdn.net/v/t45.5328-4/435845571_1204648560703018_6978010795308010265_n.jpg?_nc_cat=105&ccb=1-7&_nc_sid=247b10&_nc_ohc=MeSjA7y332YQ7kNvgG1U3kb&_nc_ht=scontent-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYC67KlVoX_XG7f8xqxGvqQ9NsYnYttUhYDp50MmaU9CpA&oe=66F28195"
        },
        "id": "1204648557369685"
      },
      {
        "accessibility_caption": "No photo description available.",
        "image": {
          "height": 608,
          "width": 960,
          "uri": "https://scontent-phx1-1.xx.fbcdn.net/v/t45.5328-4/442733567_1045635226905165_3656146094832653748_n.jpg?_nc_cat=105&ccb=1-7&_nc_sid=247b10&_nc_ohc=C_VDkVfnDFMQ7kNvgFSpF_J&_nc_ht=scontent-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYAuFLSuwEhizx3hrrYUFsRhxwX05DmZtyHoGugjypCbIQ&oe=66F262DB"
        },
        "id": "1045635223571832"
      },
      {
        "accessibility_caption": "No photo description available.",
        "image": {
          "height": 960,
          "width": 720,
          "uri": "https://scontent-phx1-1.xx.fbcdn.net/v/t45.5328-4/448502182_1596941251163664_1218525730750414110_n.jpg?_nc_cat=102&ccb=1-7&_nc_sid=247b10&_nc_ohc=bBtWIEP_YlgQ7kNvgFQXV1t&_nc_ht=scontent-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYCoq8pFsRTKwHsnUYjTUvjE2mGHk8a2SMTThsBt5ATHtg&oe=66F263B7"
        },
        "id": "1596941247830331"
      }
    ],
    "pre_recorded_videos": [
      {
        "id": "1147767813219137",
        "image": {
          "uri": "https://scontent-phx1-1.xx.fbcdn.net/v/t15.5256-10/442038356_2378858668976427_710315203557006479_n.jpg?stp=dst-jpg_s960x960&_nc_cat=108&ccb=1-7&_nc_sid=c3bc4c&_nc_ohc=rC5jFXbwqPkQ7kNvgHvBlcp&_nc_ht=scontent-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYBUGAOKgqJZ7RmgVAlCDEdekw0m810npSUrcOJohpFlFA&oe=66F26AF3"
        },
        "width": 720,
        "height": 1280,
        "playable_url_hd": "https://video-phx1-1.xx.fbcdn.net/o1/v/t2/f2/m69/AQN6HAM2Id9L82bnrd3m7iRCip8O3l-rafJbXOCyZ_uMBq-d4MQEkkYoWMej5rAx0YJIg92SiqZCXoGrlIoFhvbF.mp4?efg=eyJ2ZW5jb2RlX3RhZyI6Im9lcF9oZCJ9&_nc_ht=video-phx1-1.xx.fbcdn.net&_nc_cat=103&strext=1&vs=24f64af07863532a&_nc_vs=HBksFQIYOnBhc3N0aHJvdWdoX2V2ZXJzdG9yZS9HTUd1eUJySnNBWW5kVW9CQU1tU0IzZjRieklNYm1kakFBQUYVAALIAQAVAhg6cGFzc3Rocm91Z2hfZXZlcnN0b3JlL0dPYkV4QnFqREJlQ0VVRUZBRW1CUlZnNVh0Vl9ickZxQUFBRhUCAsgBAEsHiBJwcm9ncmVzc2l2ZV9yZWNpcGUBMQ1zdWJzYW1wbGVfZnBzABB2bWFmX2VuYWJsZV9uc3ViACBtZWFzdXJlX29yaWdpbmFsX3Jlc29sdXRpb25fc3NpbQAoY29tcHV0ZV9zc2ltX29ubHlfYXRfb3JpZ2luYWxfcmVzb2x1dGlvbgAddXNlX2xhbmN6b3NfZm9yX3ZxbV91cHNjYWxpbmcAEWRpc2FibGVfcG9zdF9wdnFzABUAJQAcjBdAAAAAAAAAABERAAAAJr6Jlci89JkDFQIoAkMzGAt2dHNfcHJldmlldxwXQCPul41P3zsYGWRhc2hfaDI2NC1iYXNpYy1nZW4yXzcyMHASABgYdmlkZW9zLnZ0cy5jYWxsYmFjay5wcm9kOBJWSURFT19WSUVXX1JFUVVFU1QbCogVb2VtX3RhcmdldF9lbmNvZGVfdGFnBm9lcF9oZBNvZW1fcmVxdWVzdF90aW1lX21zATAMb2VtX2NmZ19ydWxlB3VubXV0ZWQTb2VtX3JvaV9yZWFjaF9jb3VudAM4NjQRb2VtX2lzX2V4cGVyaW1lbnQADG9lbV92aWRlb19pZBAxMTQ3NzY3ODEzMjE5MTM3Em9lbV92aWRlb19hc3NldF9pZA8zOTcxNDA4OTY2ODk0NDMVb2VtX3ZpZGVvX3Jlc291cmNlX2lkDzkwMTQwMTUwNTA3OTkwMxxvZW1fc291cmNlX3ZpZGVvX2VuY29kaW5nX2lkDzgzMzk3ODUwMjAxMTA4MA52dHNfcmVxdWVzdF9pZAAlAhwAJcQBGweIAXMEMzU2OQJjZAoyMDI0LTA2LTI1A3JjYgM4MDADYXBwE0ZhY2Vib29rIGZvciBpUGhvbmUCY3QeTUFSS0VUUExBQ0VfUFJFX1JFQ09SREVEX1ZJREVPE29yaWdpbmFsX2R1cmF0aW9uX3MIOS45NjY2NjcCdHMVcHJvZ3Jlc3NpdmVfZW5jb2RpbmdzAA&ccb=9-4&oh=00_AYDiv1hjisFht99K_5lz3j-Pk-xs2k0ugEOgjm4KvmfsQg&oe=66EE7712&_nc_sid=1d576d&_nc_rid=105059147734385&_nc_store_type=1",
        "playable_url": "https://video-phx1-1.xx.fbcdn.net/v/t42.1790-2/449103550_356485417206494_8211214264662323839_n.mp4?_nc_cat=110&ccb=1-7&_nc_sid=55d0d3&efg=eyJybHIiOjU2NSwicmxhIjo1MTIsInZlbmNvZGVfdGFnIjoic3ZlX3NkIiwidmlkZW9faWQiOjExNDc3Njc4MTMyMTkxMzd9&_nc_ohc=PgW3LOpb1MgQ7kNvgH3zRyM&rl=565&vabr=314&_nc_ht=video-phx1-1.xx&_nc_gid=AeY4xBF5ziAIXpg_mudkpNH&oh=00_AYA9xlijGKTih9MpA_xkd0a7Nw1I_JA3vxLljQf8MF54rA&oe=66F29635"
      }
    ]
  }
}]
```

### 📥 Input for Facebook Marketplace Scraper

To use the **Facebook Marketplace Scraper**, provide the following inputs:

1. **Facebook Marketplace URLs**: The scraper accepts three types of URLs:

- 🔍 **Location**: `https://www.facebook.com/marketplace/boston/`
- 🔍 **Category**: `https://www.facebook.com/marketplace/boston/electronics`
- 🔍 **Search Query**: `https://www.facebook.com/marketplace/boston/search/?query=tesla`
2. **Scrape Item Details**: Optionally, check the box to scrape item details pages for more comprehensive data (this may increase scraping time).
3. **Proxy Settings**: Customize proxy settings to improve scraping results based on location. Default settings use the Apify proxy with US residential IPs.
4. **Max Items**: Specify how many listings to collect per page. Leave blank to scrape all available items.
5. **Deduplicate across runs** This is useful when you run the actor repeatedly and want to prevent duplicates
6. **Stop on First Page All Duplicates** (`stop_on_first_page_all_duplicates`):

If enabled, the scraper will **immediately stop** when it encounters a page where **all** items are duplicates (i.e., already seen in previous runs).

> **Note:** This option only works **if Deduplicate Across Runs is also enabled**, since it relies on stored item history to detect duplicates.

### 💡 Tips

**Customizing Search Radius**: To search within a specific radius around a location, you can add radius parameters to your URLs:

- Format: `?exact=false&radius=X` (where X is the radius in kilometers)
- Example: `https://www.facebook.com/marketplace/boston/apparel?exact=false&radius=90` (searches within 90km of Boston)

This is particularly useful when you want to:

- Expand your search area for rare items
- Focus on a specific local area
- Find items in neighboring cities

### ⚖️ Legal and Ethical Considerations

Our scrapers are ethical and only extract publicly shared content. We do not collect private user data, such as email addresses, gender, or location. While we believe our scrapers are safe when used responsibly, be aware that your results may still contain personal data protected by GDPR and other regulations.

You should only scrape personal data if you have a legitimate reason. If you're unsure about the legitimacy of your use case, consult legal advice. For more information, check out our blog post on the legality of web scraping.

## Integrations

Connect the Facebook Marketplace Scraper with various cloud services and web apps via the [Apify platform](https://apify.com/integrations), including:

- Zapier
- Make
- Slack
- Airbyte
- GitHub
- Google Sheets
- Google Drive

Use [webhooks](https://docs.apify.com/integrations/webhooks) to automate actions, like receiving notifications when an extraction is complete.

## Using Facebook Marketplace Scraper with the Apify API

The Apify API allows programmatic access to manage, schedule, and run Apify actors. You can also access datasets, monitor performance, and more.

For Node.js, use the `apify-client` NPM package. For Python, use the `apify-client` PyPI package.

Visit the [Apify API reference](https://docs.apify.com/api/v2) for details or check the [API tab](https://apify.com/datavoyantlab/Facebook-marketplace-scrape/api) for code examples.

## Feedback and Support

We welcome your feedback! If you have issues or suggestions:

1. Visit the [Issues tab](https://apify.com/datavoyantlab/Facebook-marketplace-scraper/issues) in the Apify Console
2. Create a new issue with your feedback or bug report

Your input helps us improve the Facebook Marketplace Scraper's performance and features.