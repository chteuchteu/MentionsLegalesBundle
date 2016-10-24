# MentionsLegalesBundle
This bundle provides easy integration of french legal notice page on symfony websites.

Read [Quelles sont les mentions obligatoires sur un site internet ?](https://www.service-public.fr/professionnels-entreprises/vosdroits/F31228)
on service-public.fr for more information.

## Usage
1. `composer require chteuchteu/mentions-legales-bundle`

2. Include this anywhere you want (a new `/mentions-legales` route with its own twig page would be great):
    
    ```twig
    {% include '@MentionsLegales/mentions-legales.html.twig' with {
        url: absolute_url(path('homepage')),
        proprietaire: {
            raison_sociale: '',
            forme_juridique: '',
            adresse: '',
            capital_social: '',
            more: {
                'N° d\'immatriculation au répertoire des métiers': '123456789'
            }
        },
        editeur: {
            nom: '',
            statut: '',
            url: ''
        },
        responsable_publication: {
            nom: '',
            email: ''
        },
        webmaster: {
            nom: '',
            email: ''
        },
        hebergeur: {
            nom: '',
            adresse: ''
        }
    } %}
    ```
