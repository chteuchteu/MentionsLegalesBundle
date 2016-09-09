# MentionsLegalesBundle
This bundle provides easy integration of french legal notice page on symfony websites.

Read [Quelles sont les mentions obligatoires sur un site internet ?](https://www.service-public.fr/professionnels-entreprises/vosdroits/F31228)
on service-public.fr for more information.

## Usage
```twig
{% include 'MentionsLegalesBundle::mentions-legales.html.twig' with {
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
``̀`
