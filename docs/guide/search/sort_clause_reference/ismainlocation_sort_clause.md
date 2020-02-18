# IsMainLocation Sort Clause

The [`Location\IsMainLocation` Sort Clause](https://github.com/ezsystems/ezpublish-kernel/blob/6.13.7/eZ/Publish/API/Repository/Values/Content/Query/SortClause/Location/IsMainLocation.php)
sorts search results by whether their Location is the main Location of the Content item.

Locations that are not main Locations are ranked as lower values (e.g. with ascending order they will be returned first).

## Arguments

- `sortDirection` (optional) - Query or LocationQuery constant, either `Query::SORT_ASC` or `Query::SORT_DESC`.

## Example

``` php
$query = new LocationQuery();
$query->sortClauses = [new SortClause\Location\InMainLocation()];
```