---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseimportexportstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
ms.openlocfilehash: c64f726e8ff553aa42cb8580cee2349b35de519e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374978"
---
# <span data-ttu-id="a5a20-101">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="a5a20-101">Get-AzSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="a5a20-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a5a20-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a20-103">Pobiera szczegóły importu lub eksportu bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a5a20-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

## <span data-ttu-id="a5a20-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a5a20-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseImportExportStatus [-OperationStatusLink] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5a20-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a5a20-105">DESCRIPTION</span></span>
<span data-ttu-id="a5a20-106">Polecenie cmdlet **Get-AzSqlDatabaseImportExportStatus** pobiera szczegóły importu pliku BACPAC z konta magazynu do bazy danych SQL Azure lub eksportu bazy danych SQL Azure jako pliku BACPAC do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="a5a20-106">The **Get-AzSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>
<span data-ttu-id="a5a20-107">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="a5a20-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a5a20-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a5a20-108">EXAMPLES</span></span>

### <span data-ttu-id="a5a20-109">Przykład 1: uzyskiwanie stanu importu i eksportu bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="a5a20-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="a5a20-110">To polecenie uzyskuje stan żądania importu lub eksportu bazy danych pod określonym adresem URL.</span><span class="sxs-lookup"><span data-stu-id="a5a20-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="a5a20-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a5a20-111">PARAMETERS</span></span>

### <span data-ttu-id="a5a20-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a20-112">-DefaultProfile</span></span>
<span data-ttu-id="a5a20-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a5a20-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a20-114">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="a5a20-114">-OperationStatusLink</span></span>
<span data-ttu-id="a5a20-115">Umożliwia określenie łącza stanu zwróconego przez aplety poleceń New-AzSqlDatabaseExport lub New-AzSqlDatabaseImport.</span><span class="sxs-lookup"><span data-stu-id="a5a20-115">Specifies the status link that is returned from the New-AzSqlDatabaseExport or New-AzSqlDatabaseImport cmdlets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5a20-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a5a20-116">-Confirm</span></span>
<span data-ttu-id="a5a20-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5a20-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a20-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5a20-118">-WhatIf</span></span>
<span data-ttu-id="a5a20-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5a20-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5a20-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a5a20-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a20-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a20-121">CommonParameters</span></span>
<span data-ttu-id="a5a20-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5a20-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a20-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5a20-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a20-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5a20-124">INPUTS</span></span>

### <span data-ttu-id="a5a20-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a5a20-125">System.String</span></span>

## <span data-ttu-id="a5a20-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a5a20-126">OUTPUTS</span></span>

### <span data-ttu-id="a5a20-127">Microsoft. Azure. Commands. SQL. ImportExport. model. AzureSqlDatabaseImportExportStatusModel</span><span class="sxs-lookup"><span data-stu-id="a5a20-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span></span>

## <span data-ttu-id="a5a20-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a5a20-128">NOTES</span></span>
* <span data-ttu-id="a5a20-129">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="a5a20-129">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="a5a20-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5a20-130">RELATED LINKS</span></span>

[<span data-ttu-id="a5a20-131">Nowe — AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="a5a20-131">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="a5a20-132">Nowe — AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="a5a20-132">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="a5a20-133">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="a5a20-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
