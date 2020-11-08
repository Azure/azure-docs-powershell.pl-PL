---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: fb0e73d338c54b93626ee3a5ee78bbbe4adca884
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064173"
---
# <span data-ttu-id="e61e1-101">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="e61e1-101">Get-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="e61e1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e61e1-102">SYNOPSIS</span></span>
<span data-ttu-id="e61e1-103">Pobiera element lub typy elementów wykazu usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e61e1-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

## <span data-ttu-id="e61e1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e61e1-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e61e1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e61e1-105">DESCRIPTION</span></span>
<span data-ttu-id="e61e1-106">Polecenie **Get-AzDataLakeAnalyticsCatalogItem** Pobiera określony element wykazu usługi Azure Data Lake Analytics lub Pobiera elementy wykazu określonego typu.</span><span class="sxs-lookup"><span data-stu-id="e61e1-106">The **Get-AzDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="e61e1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e61e1-107">EXAMPLES</span></span>

### <span data-ttu-id="e61e1-108">Przykład 1: uzyskiwanie określonej bazy danych</span><span class="sxs-lookup"><span data-stu-id="e61e1-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="e61e1-109">To polecenie pobiera określoną bazę danych.</span><span class="sxs-lookup"><span data-stu-id="e61e1-109">This command gets the specified database.</span></span>

### <span data-ttu-id="e61e1-110">Przykład 2: Pobieranie tabel w określonej bazie danych i schemacie</span><span class="sxs-lookup"><span data-stu-id="e61e1-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="e61e1-111">To polecenie pobiera listę tabel w określonej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="e61e1-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="e61e1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e61e1-112">PARAMETERS</span></span>

### <span data-ttu-id="e61e1-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="e61e1-113">-Account</span></span>
<span data-ttu-id="e61e1-114">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e61e1-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="e61e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e61e1-115">-DefaultProfile</span></span>
<span data-ttu-id="e61e1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e61e1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e61e1-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="e61e1-117">-ItemType</span></span>
<span data-ttu-id="e61e1-118">Określa typ elementu wykazu dla elementów, które są pobierane lub wyświetlane na liście.</span><span class="sxs-lookup"><span data-stu-id="e61e1-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="e61e1-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e61e1-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e61e1-120">Bazy danych</span><span class="sxs-lookup"><span data-stu-id="e61e1-120">Database</span></span>
- <span data-ttu-id="e61e1-121">Schematu</span><span class="sxs-lookup"><span data-stu-id="e61e1-121">Schema</span></span>
- <span data-ttu-id="e61e1-122">Zespołu</span><span class="sxs-lookup"><span data-stu-id="e61e1-122">Assembly</span></span>
- <span data-ttu-id="e61e1-123">Tworząc</span><span class="sxs-lookup"><span data-stu-id="e61e1-123">Table</span></span>
- <span data-ttu-id="e61e1-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="e61e1-124">TableValuedFunction</span></span>
- <span data-ttu-id="e61e1-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="e61e1-125">TableStatistics</span></span>
- <span data-ttu-id="e61e1-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="e61e1-126">ExternalDataSource</span></span>
- <span data-ttu-id="e61e1-127">Przeglądania</span><span class="sxs-lookup"><span data-stu-id="e61e1-127">View</span></span>
- <span data-ttu-id="e61e1-128">Wewnętrznym</span><span class="sxs-lookup"><span data-stu-id="e61e1-128">Procedure</span></span>
- <span data-ttu-id="e61e1-129">Haseł</span><span class="sxs-lookup"><span data-stu-id="e61e1-129">Secret</span></span>
- <span data-ttu-id="e61e1-130">Mobilne</span><span class="sxs-lookup"><span data-stu-id="e61e1-130">Credential</span></span>
- <span data-ttu-id="e61e1-131">Gatunków</span><span class="sxs-lookup"><span data-stu-id="e61e1-131">Types</span></span>
- <span data-ttu-id="e61e1-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="e61e1-132">TablePartition</span></span>

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

### <span data-ttu-id="e61e1-133">-Path</span><span class="sxs-lookup"><span data-stu-id="e61e1-133">-Path</span></span>
<span data-ttu-id="e61e1-134">Określa ścieżkę wielu części do elementu, który ma zostać pobrany, lub element nadrzędny elementów do listy.</span><span class="sxs-lookup"><span data-stu-id="e61e1-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="e61e1-135">Części ścieżki powinny być oddzielone kropką (.).</span><span class="sxs-lookup"><span data-stu-id="e61e1-135">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="e61e1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e61e1-136">CommonParameters</span></span>
<span data-ttu-id="e61e1-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e61e1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e61e1-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e61e1-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e61e1-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e61e1-139">INPUTS</span></span>

### <span data-ttu-id="e61e1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e61e1-140">System.String</span></span>

### <span data-ttu-id="e61e1-141">Microsoft. Azure. Commands. DataLakeAnalytics. models. DataLakeAnalyticsEnums + CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="e61e1-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="e61e1-142">Microsoft. Azure. Commands. DataLakeAnalytics. models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="e61e1-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="e61e1-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e61e1-143">OUTPUTS</span></span>

### <span data-ttu-id="e61e1-144">Microsoft. Azure. Management. datalake. Analytics. modele. CatalogItem</span><span class="sxs-lookup"><span data-stu-id="e61e1-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span></span>

## <span data-ttu-id="e61e1-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e61e1-145">NOTES</span></span>

## <span data-ttu-id="e61e1-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e61e1-146">RELATED LINKS</span></span>

[<span data-ttu-id="e61e1-147">Test — AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="e61e1-147">Test-AzDataLakeAnalyticsCatalogItem</span></span>](./Test-AzDataLakeAnalyticsCatalogItem.md)


