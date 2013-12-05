iOS Drag-n-Drop Between Helper
==============================

Objective-C helper class(es) for the iOS platform that handle drag and drop logic between 2 UITableView s and/or UICollectionView s.


Installation
------------

To use this in your project, copy the I3DragBetweenHelper class into your project directory - there is no Podspec (at the moment).

This repo also contains and example project where you can see the helper class in action.

This project requires ARC to compile.


Stabillity
----------

At the moment, this helper is not yet stable - use it at your own risk.

Its been tested on iOS 6 and iOS 7 iPads for dragging between a UITableView and a UICollectionView.

Below are the test/example cases included in the project.

######Example Case 1 - I32RearrangeableTablesViewController######
- 2 Table Views
- Src table does not except cells from the Dst table
- Dst table does not except cells from the Src table
- Src table is rearrangeable
- Dst table is rearrangeable
- Other: the dragging views are not duplicates

######Example Case 2 - I32ExchangeableTableViewsController######
- 2 Table Views
- Src table excepts cells from the Dst table
- Dst table excepts cells from the Src table
- Src table is not rearrangeable
- Dst table is not rearrangeable
- Other: the dragging views are duplicates, see issue #4 for the reason for this

######Example Case 3 - I32RearrangeableExchangeableTablesViewController######
- 2 Table Views
- Src table excepts cells from the Dst table
- Dst table excepts cells from the Src table
- Src table is rearrangeable
- Dst table is rearrangeable
- Both tables contain 1 cell that isn't draggable but is rearrangeable
- Both tables contain 1 cell that isn't rearrangeable but is draggable
- Both tables contain 1 cell that is neither draggable nor rearrangeable


Notes on App Store Approval
---------------------------

I haven't used this helper in an App Store approved project yet - the rearranging functionallity is already built into UITableView/UICollectionView s in the form of 'Edit mode', and I have no idea how Apple will respond to this ad-hoc approach to rearranging table/collection views. It might _just_ be a cause for rejection, but who knows..

Just something to bear in mind.
