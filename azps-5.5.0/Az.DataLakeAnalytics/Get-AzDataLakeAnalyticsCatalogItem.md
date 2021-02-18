---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: fb0e73d338c54b93626ee3a5ee78bbbe4adca884
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180971"
---
# <span data-ttu-id="acb82-101">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="acb82-101">Get-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="acb82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acb82-102">SYNOPSIS</span></span>
<span data-ttu-id="acb82-103">Pobiera element katalogu Data Lake Analytics lub typy elementów.</span><span class="sxs-lookup"><span data-stu-id="acb82-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

## <span data-ttu-id="acb82-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="acb82-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acb82-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="acb82-105">DESCRIPTION</span></span>
<span data-ttu-id="acb82-106">Element **Get-AzDataLakeAnalyticsCatalogItem** pobiera określony element wykazu usługi Azure Data Lake Analytics lub pobiera elementy wykazu określonego typu.</span><span class="sxs-lookup"><span data-stu-id="acb82-106">The **Get-AzDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="acb82-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="acb82-107">EXAMPLES</span></span>

### <span data-ttu-id="acb82-108">Przykład 1. Uzyskiwanie określonej bazy danych</span><span class="sxs-lookup"><span data-stu-id="acb82-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="acb82-109">To polecenie pobiera określoną bazę danych.</span><span class="sxs-lookup"><span data-stu-id="acb82-109">This command gets the specified database.</span></span>

### <span data-ttu-id="acb82-110">Przykład 2. Uzyskiwanie tabel w określonej bazie danych i schemacie</span><span class="sxs-lookup"><span data-stu-id="acb82-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="acb82-111">To polecenie pobiera listę tabel w określonej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="acb82-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="acb82-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acb82-112">PARAMETERS</span></span>

### <span data-ttu-id="acb82-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="acb82-113">-Account</span></span>
<span data-ttu-id="acb82-114">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="acb82-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acb82-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acb82-115">-DefaultProfile</span></span>
<span data-ttu-id="acb82-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="acb82-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="acb82-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="acb82-117">-ItemType</span></span>
<span data-ttu-id="acb82-118">Określa typy elementów wykazu, do których są pobierane lub wyświetlane.</span><span class="sxs-lookup"><span data-stu-id="acb82-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="acb82-119">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="acb82-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="acb82-120">Baza danych</span><span class="sxs-lookup"><span data-stu-id="acb82-120">Database</span></span>
- <span data-ttu-id="acb82-121">Schemat</span><span class="sxs-lookup"><span data-stu-id="acb82-121">Schema</span></span>
- <span data-ttu-id="acb82-122">Zestaw</span><span class="sxs-lookup"><span data-stu-id="acb82-122">Assembly</span></span>
- <span data-ttu-id="acb82-123">Tabela</span><span class="sxs-lookup"><span data-stu-id="acb82-123">Table</span></span>
- <span data-ttu-id="acb82-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="acb82-124">TableValuedFunction</span></span>
- <span data-ttu-id="acb82-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="acb82-125">TableStatistics</span></span>
- <span data-ttu-id="acb82-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="acb82-126">ExternalDataSource</span></span>
- <span data-ttu-id="acb82-127">Widok</span><span class="sxs-lookup"><span data-stu-id="acb82-127">View</span></span>
- <span data-ttu-id="acb82-128">Procedura</span><span class="sxs-lookup"><span data-stu-id="acb82-128">Procedure</span></span>
- <span data-ttu-id="acb82-129">Tajny</span><span class="sxs-lookup"><span data-stu-id="acb82-129">Secret</span></span>
- <span data-ttu-id="acb82-130">Poświadczenia</span><span class="sxs-lookup"><span data-stu-id="acb82-130">Credential</span></span>
- <span data-ttu-id="acb82-131">Typy</span><span class="sxs-lookup"><span data-stu-id="acb82-131">Types</span></span>
- <span data-ttu-id="acb82-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="acb82-132">TablePartition</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType
Parameter Sets: (All)
Aliases:
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acb82-133">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="acb82-133">-Path</span></span>
<span data-ttu-id="acb82-134">Określa wieloetapową ścieżkę do elementu do pobrania lub do elementu nadrzędnego elementów do listy.</span><span class="sxs-lookup"><span data-stu-id="acb82-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="acb82-135">Części ścieżki powinny być oddzielone kropka (.).</span><span class="sxs-lookup"><span data-stu-id="acb82-135">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acb82-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acb82-136">CommonParameters</span></span>
<span data-ttu-id="acb82-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acb82-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acb82-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acb82-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acb82-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="acb82-139">INPUTS</span></span>

### <span data-ttu-id="acb82-140">System.String</span><span class="sxs-lookup"><span data-stu-id="acb82-140">System.String</span></span>

### <span data-ttu-id="acb82-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="acb82-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="acb82-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="acb82-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="acb82-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="acb82-143">OUTPUTS</span></span>

### <span data-ttu-id="acb82-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span><span class="sxs-lookup"><span data-stu-id="acb82-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span></span>

## <span data-ttu-id="acb82-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="acb82-145">NOTES</span></span>

## <span data-ttu-id="acb82-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="acb82-146">RELATED LINKS</span></span>

[<span data-ttu-id="acb82-147">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="acb82-147">Test-AzDataLakeAnalyticsCatalogItem</span></span>](./Test-AzDataLakeAnalyticsCatalogItem.md)


