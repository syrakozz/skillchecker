##  <u> *[Home](README.md)* </u>
## Books concepts

Google Books is built upon four basic concepts:

*   **Volume**: A volume represents the data that Google Books hosts about a book or magazine. It is the primary resource in the Books API. All other resources in this API either contain or annotate a volume.
*   **Bookshelf**: A bookshelf is a collection of volumes. Google Books provides a set of predefined bookshelves for each user, some of which are completely managed by the user, some of which are automatically filled in based on the user's activity, and some of which are mixed. Users can create, modify or delete other bookshelves, which are always filled with volumes manually. Bookshelves can be made private or public by the user.

**Note:** Creating and deleting bookshelves and modifying privacy settings on bookshelves can currently only be done through the [Google Books](https://books.google.com/) site.

*   **Review**: A volume review combines a star rating and/or text. A user can submit one review per volume. Reviews are also available from outside sources and are attributed appropriately.
*   **Reading Position**: A reading position indicates a user's last read position in a volume. A user can only have one reading position per volume. If the user has not opened that volume before, then the reading position does not exist. The reading position can store detailed position information down to the resolution of a word. This information is always private to the user.

### Books API data model

A resource is an individual data entity with a unique identifier. The Books API operates on two types of resources, based on the concepts described above:

*   **Volume resource**: Represents a volume.
*   **Bookshelf resource**: Represents a single bookshelf for a particular user.

The Books API data model is based on groups of resources, called collections:

Volume collection

The volume collection, is a collection of every volume resources managed by Google Books. As such, you cannot list all volume resources, but you can list all volumes that match a set of search terms.  
 

Bookshelf collection

A bookshelf collection consists of all the bookshelf resources managed by Google Books. Bookshelves must always be referenced in the context of a specific user's library. Bookshelves can contain zero or more volumes.

Google provides a set of pre-defined bookshelves for each user:

*   Favorites: Mutable bookshelf.
*   Purchased: Populated with volumes the user has purchased. The user cannot manually add or remove volumes.
*   To Read: Mutable bookshelf.
*   Reading Now: Mutable bookshelf.
*   Have Read: Mutable bookshelf.
*   Reviewed: Populated with volumes the user has reviewed. The user cannot manually add or remove volumes.
*   Recently Viewed: Populated with volumes the user has recently opened in a web reader. The user cannot manually add volumes.
*   My eBooks: Mutable bookshelf. Purchased books are automatically added, but can be manually removed.
*   Books For You: Populated with personalized volume recommendations. _If we have no recommendations for the user, this bookshelf does not exist._

Example bookshelves:

*   "Favorites"
    *   "Harry Potter"
*   "My eBooks"
    *   "Switch"
    *   "Twilight"
    *   "The Girl with the Dragon Tattoo"

### Books API operations

You can invoke five different methods for collections and resources in the Books API, as described in the following table.

| Operation | Description                                                         | REST HTTP mappings                                                               |
| --------- | ------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| list      | Lists a specified subset of resources within a collection.          | `GET` on a collection URI.                                                       |
| insert    | Inserts a new resource into a collection (creating a new resource). | `POST` on a collection URI, where you pass in data for a new resource.           |
| get       | Gets a specific resource.                                           | `GET` on resource URI.                                                           |
| update    | Updates a specific resource.                                        | `PUT` on resource URI, where you pass in data for the updated resource.          |
| delete    | Deletes a specific resource.                                        | `DELETE` on resource URI, where you pass in data for the resource to be deleted. |

