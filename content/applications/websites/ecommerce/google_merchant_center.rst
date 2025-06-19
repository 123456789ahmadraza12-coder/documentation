======================
Google Merchant Center
======================

Google Merchant Center is a tool that allows ecommerce retailers to manage and submit product
data to Google. It serves as a central hub to upload and maintain product details, such as images,
prices, and descriptions so that products can appear across Google's platforms.

Google Merchant Center setup
============================

To connect your ecommerce with the :abbr:`GMC (Google Merchant Center)` platform, proceed as
follows:

#. Go to the `Google Merchant Center page <https://business.google.com/us/merchant-center/>`_.
#. Create or sign in to a Google account using the following link:
   `<https://business.google.com/us/merchant-center>`_.
#. Indicate that you sell products online, and enter :guilabel:`Your store's website`.
#. Click :guilabel:`Continue`, then click :guilabel:`Continue to Merchant Center`.
#. Enter your business details by adding the :guilabel:`Business name` and the
   :guilabel:`Registered country`, then click the :guilabel:`Continue to Merchant Center` button
   twice.
#. Add the relevant information and click :guilabel:`Continue`, or click :guilabel:`Do it later`
   to skip this step for now.
#. Go to the :guilabel:`Business info` tab in the left menu, and click :guilabel:`Confirm online
   store`.
#. `Verify your website's ownership <https://support.google.com/merchants/answer/11586344?hl=en&visit_id=638883410905570193-1093311043&p=help_11586344&rd=1>`_
   in one of the following ways:

   - Via :ref:`HTML tag <website/google_search_console/HTML-tag>` or :ref:`HTML file
     <GSC-HTML-file-upload>`
   - Via :ref:`Google Tag Manager <analytics/google-tag-manager>`
   - Via :ref:`Google Analytics <analytics/google-analytics>`

   .. tip::
      You can also verify your website's ownership from Google Merchant Center's dashboard by
      navigating to :menuselection:`Settings --> Business Info` in the left menu.

#. Return to :abbr:`GMC (Google Merchant Center)`, click :guilabel:`Verify your online store`,
   and :guilabel:`Continue`.

Linking Odoo to GMC
===================

.. important::
   To activate the :abbr:`GMC (Google Merchant Center)` integration in your Odoo database, at least
   one :ref:`pricelist <ecommerce/pricelists>` must be assigned to your website.

#. Go to :menuselection:`eCommerce --> Pricelists`, choose an existing pricelist
   or create a :guilabel:`New` one. On the pricelist form, navigate to the :guilabel:`Ecommerce`
   tab, and select a website in the :guilabel:`Website` field.
#. Navigate to :menuselection:`Website --> Configuration --> Settings`, and scroll to the
   :guilabel:`SEO - Search Engine Optimization` section. Then, enable the
   :guilabel:`Google Merchant Center Data Source` option, click the :guilabel:`Copy file link`
   button, and :guilabel:`Save`.

   .. note::
      By enabling the :guilabel:`Google Merchant Center Data Source` option`, your website will
      generate a dynamic `/gmc.xml` feed containing essential product information and availability.
      This feed can be :ref:`customized <ecommerce/GMC/localized-feed>` to include multiple
      languages and pricelists, ensuring your products are displayed correctly for different regions
      and audiences.

#. Go to the :abbr:`GMC (Google Merchant Center)` dashboard, navigate to the
   :menuselection:`Your business --> Products` tab in the left menu, and click :guilabel:`Add
   products`.
#. Choose :guilabel:`Add products from a file` and paste the URL of the copied file.

   .. important::
      Make sure to select all the countries where you intend to sell your products. You are not
      able to proceed without selecting at least one target country. Optionally, you have to choose
      a :guilabel:`feed label` as well.

      .. image:: google_merchant_center/gmc-select-countries.png
         :alt: Select countries in GMC.

#. Click :guilabel:`Continue`.

.. _ecommerce/GMC/localized-feed:

Localized feeds
===============

It is helpful to create language-specific feeds for each country/language you sell in. You can
always add new feeds by going to :guilabel:`Products` on the :abbr:`GMC` dashboard, clicking
:guilabel:`Add products` and choosing :guilabel:`Add another product source` from the
dropdown menu.

.. note::
   The selected language must first be enabled in your website's settings.

It is also possible to create different feeds for different currencies, which allows customers
to view prices in their local currency. To enable this feature, create a pricelist with the foreign
currency in Odoo. To do so, go to the product source in :abbr:`GMC`, navigate to the
:guilabel:`Data source setup` tab, collapse the :guilabel:`Show advanced options`, and choose a
:guilabel:`Currency`.

.. seealso::
   - For a detailed explanation of all fields in the `/gmc.xml` file, refer to
     `Google Merchant Center Product Feed Specifications <https://support.google.com/merchants/answer/7052112>`_.
   - Find more information on `Google Merchant Center Help <https://support.google.com/merchants/answer/12564959?hl=en>`_

.. tip::
   We recommend using the tool alongside other Google services, such as :doc:`Google Search Console
   <../website/configuration/google_search_console>`,
   :ref:`Google Analytics <analytics/google-analytics>` or :ref:`Google Tag Manager
   <analytics/google-tag-manager>` to obtain detailed reports on product listing issues,
   improve marketing strategies, increase your products' online visibility, and enhance
   the overall sales performance.
