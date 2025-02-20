# Inconsistencies regarding vulnerable software versions across multiple POC data sources.
## Introduction(介绍) 

We have comprehensively collected all Proof-of-Concept (POC) reports from four data sources: CXSecurity, Exploitdb, Packet Storm Security, and Openwall. From these reports, we extracted information on the affected software names and their corresponding vulnerable software versions. Based on the correspondence with CVE IDs (Common Vulnerabilities and Exposures), we organized and saved the affected software names and version information from the POC reports related to specific CVE IDs, which were obtained from the four data sources, into an Excel file named "Inconsistencies in POC data on vulnerable software versions.xlsx".

>> 我们全面搜集了来自CXSecurity、Exploitdb、Packet Storm Security以及Openwall这四个数据源的所有POC（Proof-of-Concept）报告，并从中提取了受影响的软件名称及其对应的易受攻击的软件版本信息。基于CVE ID（Common Vulnerabilities and Exposures，通用漏洞披露）的对应关系，我们将这些从四个数据源中获取的、与特定CVE ID相关的POC报告中的受影响软件名称及版本信息，整理并保存在了名为“Inconsistencies in POC data on vulnerable software versions.xlsx”的Excel文件中。

The first column of this Excel file is the CVE ID, and the four subsequent columns (from the 2nd to the 5th) respectively display the affected software names and version information mentioned in the POC reports associated with each CVE ID, sourced from CXSecurity, Exploitdb, Packet Storm Security, and Openwall.

>> 该Excel文件的第一列是CVE ID，紧接着的四列（第2至第5列）分别展示了CXSecurity、Exploitdb、Packet Storm Security以及Openwall这四个数据源中，与每个CVE ID相关联的POC报告所提及的受影响软件名称及其版本信息。
>> 
![image](https://github.com/baimuDing/Inconsistencies-in-POC-Data-Regarding-Vulnerable-Software-Versions/blob/main/1.png)

The next six columns (from the 6th to the 11th), on the other hand, detail the inconsistencies found between any two data sources regarding the vulnerable software version information associated with the same CVE ID.

>> 而接下来的六列（第6至第11列），则详细记录了任意两个数据源之间，针对同一CVE ID的易受攻击软件版本信息所存在的不一致情况。
>> 
![image](https://github.com/baimuDing/Inconsistencies-in-POC-Data-Regarding-Vulnerable-Software-Versions/blob/main/2.png)

## Type Definitions(类型定义)

To more precisely describe these inconsistencies, we have defined the following three matching types:
>> 为了更精确地描述这些不一致性，我们定义了以下三种匹配类型：

**Strict Match**: When the vulnerable software version information mentioned in the POC reports for the same CVE ID in two data sources is completely identical, we refer to it as an exact match.
>> **严格匹配**：当两个数据源中，针对同一CVE ID的POC报告所提及的易受攻击软件版本信息完全一致时，我们称之为严格匹配。

**Loose Match**: If the vulnerable software version information mentioned in the POC reports for the same CVE ID in two data sources overlaps partially but is not completely identical, we refer to it as a partial match.
>>**松散匹配**：若两个数据源中，针对同一CVE ID的POC报告所提及的易受攻击软件版本信息存在部分重叠，但并非完全一致，我们则称之为松散匹配。

**Complete Mismatch**: When the vulnerable software version information mentioned in the POC reports for the same CVE ID in two data sources neither overlaps nor conforms to the definitions of an exact match or a partial match, we refer to it as a no match.
>>**完全不匹配**：当两个数据源中，针对同一CVE ID的POC报告所提及的易受攻击软件版本信息既不存在重叠部分，也不符合严格匹配或松散匹配的定义时，我们称之为完全不匹配。

## Search Path(查找路径)

All POC reports associated with the CVE IDs in the "Inconsistencies in POC data on vulnerable software versions.xlsx" file are saved in the "four_poc_data" subfolder under the "main" folder. This subfolder is organized by the names of the data sources, with each data source having its corresponding folder where the related POC reports are stored.
>>所有与Inconsistencies in POC data on vulnerable software versions.xlsx文件中CVE ID相关联的POC报告，均保存在名为“main”的文件夹下的“four_poc_data”子文件夹中。该子文件夹以数据源名称命名，每个数据源对应的文件夹内均存放了与该数据源相关的POC报告。
