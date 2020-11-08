---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: fb0e73d338c54b93626ee3a5ee78bbbe4adca884
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051338"
---
# <span data-ttu-id="dd88d-101">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="dd88d-101">Get-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="dd88d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd88d-102">SYNOPSIS</span></span>
<span data-ttu-id="dd88d-103">Pobiera element lub typy elementów wykazu usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="dd88d-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

## <span data-ttu-id="dd88d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd88d-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd88d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dd88d-105">DESCRIPTION</span></span>
<span data-ttu-id="dd88d-106">Polecenie **Get-AzDataLakeAnalyticsCatalogItem** Pobiera określony element wykazu usługi Azure Data Lake Analytics lub Pobiera elementy wykazu określonego typu.</span><span class="sxs-lookup"><span data-stu-id="dd88d-106">The **Get-AzDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="dd88d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd88d-107">EXAMPLES</span></span>

### <span data-ttu-id="dd88d-108">Przykład 1: uzyskiwanie określonej bazy danych</span><span class="sxs-lookup"><span data-stu-id="dd88d-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="dd88d-109">To polecenie pobiera określoną bazę danych.</span><span class="sxs-lookup"><span data-stu-id="dd88d-109">This command gets the specified database.</span></span>

### <span data-ttu-id="dd88d-110">Przykład 2: Pobieranie tabel w określonej bazie danych i schemacie</span><span class="sxs-lookup"><span data-stu-id="dd88d-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="dd88d-111">To polecenie pobiera listę tabel w określonej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="dd88d-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="dd88d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd88d-112">PARAMETERS</span></span>

### <span data-ttu-id="dd88d-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="dd88d-113">-Account</span></span>
<span data-ttu-id="dd88d-114">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="dd88d-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="dd88d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd88d-115">-DefaultProfile</span></span>
<span data-ttu-id="dd88d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="dd88d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd88d-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="dd88d-117">-ItemType</span></span>
<span data-ttu-id="dd88d-118">Określa typ elementu wykazu dla elementów, które są pobierane lub wyświetlane na liście.</span><span class="sxs-lookup"><span data-stu-id="dd88d-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="dd88d-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="dd88d-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dd88d-120">Bazy danych</span><span class="sxs-lookup"><span data-stu-id="dd88d-120">Database</span></span>
- <span data-ttu-id="dd88d-121">Schematu</span><span class="sxs-lookup"><span data-stu-id="dd88d-121">Schema</span></span>
- <span data-ttu-id="dd88d-122">Zespołu</span><span class="sxs-lookup"><span data-stu-id="dd88d-122">Assembly</span></span>
- <span data-ttu-id="dd88d-123">Tworząc</span><span class="sxs-lookup"><span data-stu-id="dd88d-123">Table</span></span>
- <span data-ttu-id="dd88d-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="dd88d-124">TableValuedFunction</span></span>
- <span data-ttu-id="dd88d-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="dd88d-125">TableStatistics</span></span>
- <span data-ttu-id="dd88d-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="dd88d-126">ExternalDataSource</span></span>
- <span data-ttu-id="dd88d-127">Przeglądania</span><span class="sxs-lookup"><span data-stu-id="dd88d-127">View</span></span>
- <span data-ttu-id="dd88d-128">Wewnętrznym</span><span class="sxs-lookup"><span data-stu-id="dd88d-128">Procedure</span></span>
- <span data-ttu-id="dd88d-129">Haseł</span><span class="sxs-lookup"><span data-stu-id="dd88d-129">Secret</span></span>
- <span data-ttu-id="dd88d-130">Mobilne</span><span class="sxs-lookup"><span data-stu-id="dd88d-130">Credential</span></span>
- <span data-ttu-id="dd88d-131">Gatunków</span><span class="sxs-lookup"><span data-stu-id="dd88d-131">Types</span></span>
- <span data-ttu-id="dd88d-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="dd88d-132">TablePartition</span></span>

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

### <span data-ttu-id="dd88d-133">-Path</span><span class="sxs-lookup"><span data-stu-id="dd88d-133">-Path</span></span>
<span data-ttu-id="dd88d-134">Określa ścieżkę wielu części do elementu, który ma zostać pobrany, lub element nadrzędny elementów do listy.</span><span class="sxs-lookup"><span data-stu-id="dd88d-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="dd88d-135">Części ścieżki powinny być oddzielone kropką (.).</span><span class="sxs-lookup"><span data-stu-id="dd88d-135">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="dd88d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd88d-136">CommonParameters</span></span>
<span data-ttu-id="dd88d-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd88d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd88d-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd88d-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd88d-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd88d-139">INPUTS</span></span>

### <span data-ttu-id="dd88d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="dd88d-140">System.String</span></span>

### <span data-ttu-id="dd88d-141">Microsoft. Azure. Commands. DataLakeAnalytics. models. DataLakeAnalyticsEnums + CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="dd88d-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="dd88d-142">Microsoft. Azure. Commands. DataLakeAnalytics. models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="dd88d-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="dd88d-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd88d-143">OUTPUTS</span></span>

### <span data-ttu-id="dd88d-144">Microsoft. Azure. Management. datalake. Analytics. modele. CatalogItem</span><span class="sxs-lookup"><span data-stu-id="dd88d-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span></span>

## <span data-ttu-id="dd88d-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd88d-145">NOTES</span></span>

## <span data-ttu-id="dd88d-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd88d-146">RELATED LINKS</span></span>

[<span data-ttu-id="dd88d-147">Test — AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="dd88d-147">Test-AzDataLakeAnalyticsCatalogItem</span></span>](./Test-AzDataLakeAnalyticsCatalogItem.md)


