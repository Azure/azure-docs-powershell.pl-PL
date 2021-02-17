---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseimportexportstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
ms.openlocfilehash: c64f726e8ff553aa42cb8580cee2349b35de519e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197723"
---
# <span data-ttu-id="53d2a-101">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="53d2a-101">Get-AzSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="53d2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53d2a-102">SYNOPSIS</span></span>
<span data-ttu-id="53d2a-103">Pobiera szczegółowe informacje dotyczące importu lub eksportu bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="53d2a-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

## <span data-ttu-id="53d2a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="53d2a-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseImportExportStatus [-OperationStatusLink] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53d2a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="53d2a-105">DESCRIPTION</span></span>
<span data-ttu-id="53d2a-106">Polecenie cmdlet **Get-AzSqlDatabaseImportExportStatus** pobiera szczegóły dotyczące importu pliku bacpac z konta magazynu do bazy danych Azure SQL Database lub eksportu bazy danych Azure SQL Database jako pliku bacpac do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="53d2a-106">The **Get-AzSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>
<span data-ttu-id="53d2a-107">To polecenie cmdlet jest również obsługiwane przez usługę SQL Server Stretch Database na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="53d2a-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="53d2a-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="53d2a-108">EXAMPLES</span></span>

### <span data-ttu-id="53d2a-109">Przykład 1. Uzyskiwanie stanu importu i eksportu bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="53d2a-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="53d2a-110">To polecenie pobiera stan żądania importu lub eksportu dla bazy danych pod określonym adresem URL.</span><span class="sxs-lookup"><span data-stu-id="53d2a-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="53d2a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53d2a-111">PARAMETERS</span></span>

### <span data-ttu-id="53d2a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53d2a-112">-DefaultProfile</span></span>
<span data-ttu-id="53d2a-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="53d2a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53d2a-114">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="53d2a-114">-OperationStatusLink</span></span>
<span data-ttu-id="53d2a-115">Określa link stanu zwracany z New-AzSqlDatabaseExport lub New-AzSqlDatabaseImport cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53d2a-115">Specifies the status link that is returned from the New-AzSqlDatabaseExport or New-AzSqlDatabaseImport cmdlets.</span></span>

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

### <span data-ttu-id="53d2a-116">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="53d2a-116">-Confirm</span></span>
<span data-ttu-id="53d2a-117">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="53d2a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53d2a-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53d2a-118">-WhatIf</span></span>
<span data-ttu-id="53d2a-119">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53d2a-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53d2a-120">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="53d2a-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53d2a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53d2a-121">CommonParameters</span></span>
<span data-ttu-id="53d2a-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53d2a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53d2a-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53d2a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53d2a-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53d2a-124">INPUTS</span></span>

### <span data-ttu-id="53d2a-125">System.String</span><span class="sxs-lookup"><span data-stu-id="53d2a-125">System.String</span></span>

## <span data-ttu-id="53d2a-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53d2a-126">OUTPUTS</span></span>

### <span data-ttu-id="53d2a-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span><span class="sxs-lookup"><span data-stu-id="53d2a-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span></span>

## <span data-ttu-id="53d2a-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="53d2a-128">NOTES</span></span>
* <span data-ttu-id="53d2a-129">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="53d2a-129">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="53d2a-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53d2a-130">RELATED LINKS</span></span>

[<span data-ttu-id="53d2a-131">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="53d2a-131">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="53d2a-132">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="53d2a-132">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="53d2a-133">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="53d2a-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
