Introduction
============

OpportunisticOwnCloud (OOC) is an Android application designed to interface with WebDAV servers in contexts with variable connectivity. 
For this particular project, we assume that the application will be interfacing with an instance of an ownCloud server, but
this does not necessarily need to be the case (although we have not tested with alternative WebDAV servers). 

ownCloud is an open source technology that provides cloud ownership and management tools. The technology was designed to be used
on a small, residential scale for file storage and sharing. However, the `<http://moment.cs.ucsb.edu/?q=content/villageshare-localized-network-architecture>`_ 
project has developed modules for ownCloud that allow for its sharing properties to extend over multiple ownCloud instances over 
wide area networks. While ownCloud currently has an Android application, it is designed around the paradigm of ownCloud operating
as a single instance for users with easy access to network connectivity. We designed OOC in hopes that it might act as a complementary
technology to the VillageShare use of ownCloud instances--that is, facilitating the sharing and storage of locally generated content
in communities with limited resources.  

Future of OOC
-------------

This application began as a project for the Modern Programming Languages and Implementations class at UCSB. We intend
to incorporate this opportunistic model for the deployed VillageShare version of the ownCloud Android application. 
Presently, we are not certain if this will entail modifying the original ownCloud Android application or incorporating
more of the functionality into OpportunisticOwnCloud.

Intstalling OOC vs. Contributing to OOC
---------------------------------------

While OOC should work with any WebDAV server, we have only tested it using ownCloud servers. To install and configure your own lightweight instance of
ownCloud, see `<https://mvigil-cs263-technology-project.readthedocs.org/en/latest/>`_ and `<http://owncloud.org/install/>`_.

For those readers interested in installing OOC, please refer to the Phone page before going to the Installation section.

For reasers interested in contributing to OOC, please refer to the Android section before proceeding to Installation section.
