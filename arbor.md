Arborescence 

pages :         route :

. index         /
. login         /login
. register      /register
. shop          /shop       (liste des produits) catalogue de produit
. product       /product    (détails du produit) 
. cart          /cart       
. song          /song       (trouver un autre blaze)
. workshop      /workshop
. post          /post       (Optionnel)
. contact       /contact    (Peut être en footer) (Mail)
. dashboard     /dashboard 
. concert       lien vers bandcamp



- assets
    - styles
        - css
            .style.css  
        - scss
            .style.scss
    - js

- controller
    . AbstractController.php
    . CategoriesController.php
    . AuthController.php
    . ProductController.php
    . MediaController.php   
    . SongController.php

    . WorkshopController.php / Réfléchir à son utilité 
    . AdminController.php

- manager
    . AbstractManager.php
    . CategoriesManager.php
    . UserManager.php
    . ProductManager.php
    . MediaManager.php
    . SongManager.php
    . WorkshopManager.php / Réfléchir à son utilité *

- models
    . Category.php
    . User.php
    . Product.php
    . Media.php
    . Song.php (à réflechir / comment faire pour un album ou une mixtape ?)
    . Workshop.php / Réfléchir à son utilité 

- services
    . router.php

- config
    . autoload.php / à required en index.php
    . database.txt / Coordonnée d'accès à la BDD

- templates
    - partials
        . _header.phtml
        . _footer.phtml

    - auth
        . login.phtml
        . register.phtml
        
    - shop
        . index.phtml   Catalogue de produit / nous contacter pour acheter un vétêment
        . product.phtml A voir si on fait une vue individuel 
        
    - Song
        . index.phtml
        . product.phtml
        
    - Post     /     Optionnel
        . index.phtml
        
    - workshop
        . index.phtml
        
    - contact   /   Autonome ou en footer ?
        . contact.phtml
        
    - admin
        . dashboard.phtml
        . manage_products.phtml
        . manage_artists.phtml
        . manage_workshops.phtml
        . manage_song.phtml
        
    . layout.phtml
    
. index.php

Réfléchir à sur comment renvoyer vers des sites tiers, ex linkfire pour rediriger vers les plateforme de stream
Pareil pour les concerts voir le site de Nes 

Element à rajouter si création d'un shop :

Controller :
    . OrderController.php
    
Manager :
    . OrderManager.php / lien carts  

    
models :
    . Order.php
    . OrderItems.php
    . Carts.php

templates :
    - cart 
        . cart.phtml / Structure globale du panier, recap achat + btn paiement
        . cart_item.phtml / Affiche un élément individuel 