---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseimportexportstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseImportExportStatus.md
ms.openlocfilehash: ad5e5bb73b3611c3c56c7340f740947134f72d39
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526030"
---
# <span data-ttu-id="6cae3-101">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="6cae3-101">Get-AzureRmSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="6cae3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6cae3-102">SYNOPSIS</span></span>
<span data-ttu-id="6cae3-103">Pobiera szczegóły importu lub eksportu bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="6cae3-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cae3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6cae3-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseImportExportStatus [-OperationStatusLink] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cae3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6cae3-105">DESCRIPTION</span></span>
<span data-ttu-id="6cae3-106">Polecenie cmdlet **Get-AzureRmSqlDatabaseImportExportStatus** pobiera szczegóły importu pliku BACPAC z konta magazynu do bazy danych SQL Azure lub eksportu bazy danych SQL Azure jako pliku BACPAC do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="6cae3-106">The **Get-AzureRmSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>
<span data-ttu-id="6cae3-107">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="6cae3-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="6cae3-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6cae3-108">EXAMPLES</span></span>

### <span data-ttu-id="6cae3-109">Przykład 1: uzyskiwanie stanu importu i eksportu bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="6cae3-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="6cae3-110">To polecenie uzyskuje stan żądania importu lub eksportu bazy danych pod określonym adresem URL.</span><span class="sxs-lookup"><span data-stu-id="6cae3-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="6cae3-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6cae3-111">PARAMETERS</span></span>

### <span data-ttu-id="6cae3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cae3-112">-DefaultProfile</span></span>
<span data-ttu-id="6cae3-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6cae3-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cae3-114">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="6cae3-114">-OperationStatusLink</span></span>
<span data-ttu-id="6cae3-115">Umożliwia określenie łącza stanu zwróconego przez aplety poleceń New-AzureRmSqlDatabaseExport lub New-AzureRmSqlDatabaseImport.</span><span class="sxs-lookup"><span data-stu-id="6cae3-115">Specifies the status link that is returned from the New-AzureRmSqlDatabaseExport or New-AzureRmSqlDatabaseImport cmdlets.</span></span>

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

### <span data-ttu-id="6cae3-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6cae3-116">-Confirm</span></span>
<span data-ttu-id="6cae3-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cae3-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cae3-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cae3-118">-WhatIf</span></span>
<span data-ttu-id="6cae3-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cae3-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cae3-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6cae3-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cae3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cae3-121">CommonParameters</span></span>
<span data-ttu-id="6cae3-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cae3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cae3-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cae3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cae3-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6cae3-124">INPUTS</span></span>

### <span data-ttu-id="6cae3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6cae3-125">System.String</span></span>

## <span data-ttu-id="6cae3-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6cae3-126">OUTPUTS</span></span>

### <span data-ttu-id="6cae3-127">Microsoft. Azure. Commands. SQL. ImportExport. model. AzureSqlDatabaseImportExportStatusModel</span><span class="sxs-lookup"><span data-stu-id="6cae3-127">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportStatusModel</span></span>

## <span data-ttu-id="6cae3-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6cae3-128">NOTES</span></span>
* <span data-ttu-id="6cae3-129">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="6cae3-129">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="6cae3-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6cae3-130">RELATED LINKS</span></span>

[<span data-ttu-id="6cae3-131">Nowe — AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="6cae3-131">New-AzureRmSqlDatabaseExport</span></span>](./New-AzureRmSqlDatabaseExport.md)

[<span data-ttu-id="6cae3-132">Nowe — AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="6cae3-132">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="6cae3-133">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="6cae3-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
