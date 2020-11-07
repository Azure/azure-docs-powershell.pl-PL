---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 5D4F13F9-57E7-446B-AA28-8C44B149E1CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseImportExportStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseImportExportStatus.md
ms.openlocfilehash: 5516556553931f7333e007edc6de1b4bd23b288d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716866"
---
# <span data-ttu-id="1859a-101">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="1859a-101">Get-AzureRmSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="1859a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1859a-102">SYNOPSIS</span></span>
<span data-ttu-id="1859a-103">Pobiera szczegóły importu lub eksportu bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1859a-103">Gets the details of an import or export of an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1859a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1859a-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseImportExportStatus [-OperationStatusLink] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1859a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1859a-105">DESCRIPTION</span></span>
<span data-ttu-id="1859a-106">Polecenie cmdlet **Get-AzureRmSqlDatabaseImportExportStatus** pobiera szczegóły importu pliku BACPAC z konta magazynu do bazy danych SQL Azure lub eksportu bazy danych SQL Azure jako pliku BACPAC do konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="1859a-106">The **Get-AzureRmSqlDatabaseImportExportStatus** cmdlet gets details of a bacpac file import from a storage account to an Azure SQL Database or an export of an Azure SQL Database as a bacpac file to a storage account.</span></span>

<span data-ttu-id="1859a-107">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="1859a-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="1859a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1859a-108">EXAMPLES</span></span>

### <span data-ttu-id="1859a-109">Przykład 1: uzyskiwanie stanu importu i eksportu bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="1859a-109">Example 1: Get the import and export status of a SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseImportExportStatus -OperationStatusLink "https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-000-0000-0000-000000000000?api-version=2014-04-01"
OperationStatusLink : 
ErrorMessage        : 
LastModifiedTime    : 4/15/2016 10:16:14 PM
QueuedTime          : 4/15/2016 10:16:13 PM
StatusMessage       : Running, Progress = 5.00 %
Status              : InProgress
```

<span data-ttu-id="1859a-110">To polecenie uzyskuje stan żądania importu lub eksportu bazy danych pod określonym adresem URL.</span><span class="sxs-lookup"><span data-stu-id="1859a-110">This command gets the status of an import or export request for a database at the specified URL.</span></span>

## <span data-ttu-id="1859a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1859a-111">PARAMETERS</span></span>

### <span data-ttu-id="1859a-112">-OperationStatusLink</span><span class="sxs-lookup"><span data-stu-id="1859a-112">-OperationStatusLink</span></span>
<span data-ttu-id="1859a-113">Umożliwia określenie łącza stanu zwróconego przez aplety poleceń New-AzureRmSqlDatabaseExport lub New-AzureRmSqlDatabaseImport.</span><span class="sxs-lookup"><span data-stu-id="1859a-113">Specifies the status link that is returned from the New-AzureRmSqlDatabaseExport or New-AzureRmSqlDatabaseImport cmdlets.</span></span>

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

### <span data-ttu-id="1859a-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1859a-114">-Confirm</span></span>
<span data-ttu-id="1859a-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1859a-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1859a-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1859a-116">-WhatIf</span></span>
<span data-ttu-id="1859a-117">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1859a-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1859a-118">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1859a-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1859a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1859a-119">-DefaultProfile</span></span>
<span data-ttu-id="1859a-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1859a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1859a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1859a-121">CommonParameters</span></span>
<span data-ttu-id="1859a-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1859a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1859a-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1859a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1859a-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1859a-124">INPUTS</span></span>

## <span data-ttu-id="1859a-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1859a-125">OUTPUTS</span></span>

## <span data-ttu-id="1859a-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1859a-126">NOTES</span></span>
* <span data-ttu-id="1859a-127">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="1859a-127">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="1859a-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1859a-128">RELATED LINKS</span></span>

[<span data-ttu-id="1859a-129">Nowe — AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="1859a-129">New-AzureRmSqlDatabaseExport</span></span>](./New-AzureRmSqlDatabaseExport.md)

[<span data-ttu-id="1859a-130">Nowe — AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="1859a-130">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="1859a-131">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="1859a-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
