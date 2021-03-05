---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseimportexportstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseImportExportStatus.md
ms.openlocfilehash: 218af86b3cdc97ecbfccb07e54a57646ab5ff414
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999697"
---
# <span data-ttu-id="6898e-101">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="6898e-101">Get-AzSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="6898e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6898e-102">SYNOPSIS</span></span>
<span data-ttu-id="6898e-103">Pobiera szczegółowe informacje dotyczące importu lub eksportu usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="6898e-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

## <span data-ttu-id="6898e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6898e-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseImportExportStatus [-OperationStatusLink] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6898e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6898e-105">DESCRIPTION</span></span>
<span data-ttu-id="6898e-106">Polecenie cmdlet **Get-AzSqlDatabaseImportExportStatus** pobiera szczegóły importu pliku bacpac z konta magazynu do bazy danych Azure SQL Database lub eksportu bazy danych Azure SQL Database jako pliku bacpac do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6898e-106">The **Get-AzSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>
<span data-ttu-id="6898e-107">To polecenie cmdlet jest również obsługiwane przez usługę SQL Server Stretch Database na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="6898e-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="6898e-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6898e-108">EXAMPLES</span></span>

### <span data-ttu-id="6898e-109">Przykład 1. Uzyskiwanie stanu importu i eksportu bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="6898e-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="6898e-110">To polecenie pobiera stan żądania importu lub eksportu dla bazy danych pod określonym adresem URL.</span><span class="sxs-lookup"><span data-stu-id="6898e-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="6898e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6898e-111">PARAMETERS</span></span>

### <span data-ttu-id="6898e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6898e-112">-DefaultProfile</span></span>
<span data-ttu-id="6898e-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="6898e-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6898e-114">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="6898e-114">-OperationStatusLink</span></span>
<span data-ttu-id="6898e-115">Określa link stanu zwracany z New-AzSqlDatabaseExport lub New-AzSqlDatabaseImport cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6898e-115">Specifies the status link that is returned from the New-AzSqlDatabaseExport or New-AzSqlDatabaseImport cmdlets.</span></span>

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

### <span data-ttu-id="6898e-116">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6898e-116">-Confirm</span></span>
<span data-ttu-id="6898e-117">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6898e-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6898e-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6898e-118">-WhatIf</span></span>
<span data-ttu-id="6898e-119">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6898e-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6898e-120">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6898e-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6898e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6898e-121">CommonParameters</span></span>
<span data-ttu-id="6898e-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6898e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6898e-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6898e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6898e-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6898e-124">INPUTS</span></span>

### <span data-ttu-id="6898e-125">System.String</span><span class="sxs-lookup"><span data-stu-id="6898e-125">System.String</span></span>

## <span data-ttu-id="6898e-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6898e-126">OUTPUTS</span></span>

### <span data-ttu-id="6898e-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span><span class="sxs-lookup"><span data-stu-id="6898e-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span></span>

## <span data-ttu-id="6898e-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6898e-128">NOTES</span></span>
* <span data-ttu-id="6898e-129">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="6898e-129">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="6898e-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6898e-130">RELATED LINKS</span></span>

[<span data-ttu-id="6898e-131">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="6898e-131">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="6898e-132">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="6898e-132">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="6898e-133">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="6898e-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
