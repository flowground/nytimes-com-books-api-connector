# ![LOGO](logo.png) Books **flow**ground Connector

## Description

A generated **flow**ground connector for the Books API (version 3.0.0).

Generated from: https://api.apis.guru/v2/specs/nytimes.com/books_api/3.0.0/swagger.json<br/>
Generated at: 2019-06-11T18:14:41+03:00

## API Description

The Books API provides information about book reviews and The New York Times bestsellers lists.

## Authorization

Supported authorization schemes:
- API Key
## Actions

### Best Seller List

#### Input Parameters
* `list` - _optional_ - The name of the Times best-seller list. To get valid values, use a list names request.

Be sure to replace spaces with hyphens (e.g., e-book-fiction or hardcover-fiction, not E-Book Fiction or Hardcover Fiction). (The parameter is not case sensitive.)
* `weeks-on-list` - _optional_ - The number of weeks that the best seller has been on list-name, as of bestsellers-date
* `bestsellers-date` - _optional_ - YYYY-MM-DD

The week-ending date for the sales reflected on list-name. Times best-seller lists are compiled using available book sale data. The bestsellers-date may be significantly earlier than published-date. For additional information, see the explanation at the bottom of any best-seller list page on NYTimes.com (example: Hardcover Fiction, published Dec. 5 but reflecting sales to Nov. 29).
* `date` - _optional_ - YYYY-MM-DD  The date the best-seller list was published on NYTimes.com (compare bestsellers-date)
* `isbn` - _optional_ - International Standard Book Number, 10 or 13 digits
* `published-date` - _optional_ - YYYY-MM-DD

The date the best-seller list was published on NYTimes.com (compare bestsellers-date)
* `rank` - _optional_ - The rank of the best seller on list-name as of bestsellers-date
* `rank-last-week` - _optional_ - The rank of the best seller on list-name one week prior to bestsellers-date
* `offset` - _optional_ - Sets the starting point of the result set
* `sort-order` - _optional_ - Sets the sort order of the result set
    Possible values: ASC, DESC.

### Best Seller History List

#### Input Parameters
* `age-group` - _optional_ - The target age group for the best seller.
* `author` - _optional_ - The author of the best seller. The author field does not include additional contributors (see Data Structure for more details about the author and contributor fields).

When searching the author field, you can specify any combination of first, middle and last names.

When sort-by is set to author, the results will be sorted by author's first name. 
* `contributor` - _optional_ - The author of the best seller, as well as other contributors such as the illustrator (to search or sort by author name only, use author instead).

When searching, you can specify any combination of first, middle and last names of any of the contributors.

When sort-by is set to contributor, the results will be sorted by the first name of the first contributor listed. 
* `isbn` - _optional_ - International Standard Book Number, 10 or 13 digits

A best seller may have both 10-digit and 13-digit ISBNs, and may have multiple ISBNs of each type. To search on multiple ISBNs, separate the ISBNs with semicolons (example: 9780446579933;0061374229).
* `price` - _optional_ - The publisher's list price of the best seller, including decimal point
* `publisher` - _optional_ - The standardized name of the publisher
* `title` - _optional_ - The title of the best seller

When searching, you can specify a portion of a title or a full title.

### Best Seller List Names

#### Input Parameters
* `api-key` - _optional_

### Best Seller List Overview

#### Input Parameters
* `published_date` - _optional_ - The best-seller list publication date. YYYY-MM-DD

You do not have to specify the exact date the list was published. The service will search forward (into the future) for the closest publication date to the date you specify. For example, a request for lists/overview/2013-05-22 will retrieve the list that was published on 05-26.

If you do not include a published_date, the current week's best-sellers lists will be returned.
* `api-key` - _optional_

### Best Seller List by Date

#### Input Parameters
* `isbn` - _optional_ - International Standard Book Number, 10 or 13 digits
* `list-name` - _optional_ - The name of the Times best-seller list. To get valid values, use a list names request.

Be sure to replace spaces with hyphens (e.g., e-book-fiction or hardcover-fiction, not E-Book Fiction or Hardcover Fiction). (The parameter is not case sensitive.)
* `published-date` - _optional_ - YYYY-MM-DD

The date the best-seller list was published on NYTimes.com (compare bestsellers-date)
* `bestsellers-date` - _optional_ - YYYY-MM-DD

The week-ending date for the sales reflected on list-name. Times best-seller lists are compiled using available book sale data. The bestsellers-date may be significantly earlier than published-date. For additional information, see the explanation at the bottom of any best-seller list page on NYTimes.com (example: Hardcover Fiction, published Dec. 5 but reflecting sales to Nov. 29).
* `weeks-on-list` - _optional_ - The number of weeks that the best seller has been on list-name, as of bestsellers-date
* `rank` - _optional_ - The rank of the best seller on list-name as of bestsellers-date
* `rank-last-week` - _optional_ - The rank of the best seller on list-name one week prior to bestsellers-date
* `offset` - _optional_ - Sets the starting point of the result set
* `sort-order` - _optional_ - The default is ASC (ascending). The sort-order parameter is used with the sort-by parameter -- for details, see each request type.
    Possible values: ASC, DESC.

### Reviews

#### Input Parameters
* `isbn` - _optional_ - Searching by ISBN is the recommended method. You can enter 10- or 13-digit ISBNs.
* `title` - _optional_ - You'll need to enter the full title of the book. Spaces in the title will be converted into the characters %20.
* `author` - _optional_ - You'll need to enter the author's first and last name, separated by a space. This space will be converted into the characters %20.
* `api-key` - _optional_

## License

**flow**ground :- Telekom iPaaS / nytimes-com-books-api-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
