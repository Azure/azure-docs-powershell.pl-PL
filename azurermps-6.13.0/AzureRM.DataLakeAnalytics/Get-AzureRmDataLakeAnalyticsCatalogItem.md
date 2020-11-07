---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: bac4e3e2cc4471b8cf015f2f3ebeab421097f81c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718341"
---
# <span data-ttu-id="04c2d-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="04c2d-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="04c2d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="04c2d-102">SYNOPSIS</span></span>
<span data-ttu-id="04c2d-103">Pobiera element lub typy elementów wykazu usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="04c2d-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04c2d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="04c2d-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04c2d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="04c2d-105">DESCRIPTION</span></span>
<span data-ttu-id="04c2d-106">Polecenie **Get-AzureRmDataLakeAnalyticsCatalogItem** Pobiera określony element wykazu usługi Azure Data Lake Analytics lub Pobiera elementy wykazu określonego typu.</span><span class="sxs-lookup"><span data-stu-id="04c2d-106">The **Get-AzureRmDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="04c2d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="04c2d-107">EXAMPLES</span></span>

### <span data-ttu-id="04c2d-108">Przykład 1: uzyskiwanie określonej bazy danych</span><span class="sxs-lookup"><span data-stu-id="04c2d-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="04c2d-109">To polecenie pobiera określoną bazę danych.</span><span class="sxs-lookup"><span data-stu-id="04c2d-109">This command gets the specified database.</span></span>

### <span data-ttu-id="04c2d-110">Przykład 2: Pobieranie tabel w określonej bazie danych i schemacie</span><span class="sxs-lookup"><span data-stu-id="04c2d-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="04c2d-111">To polecenie pobiera listę tabel w określonej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="04c2d-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="04c2d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="04c2d-112">PARAMETERS</span></span>

### <span data-ttu-id="04c2d-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="04c2d-113">-Account</span></span>
<span data-ttu-id="04c2d-114">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="04c2d-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="04c2d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04c2d-115">-DefaultProfile</span></span>
<span data-ttu-id="04c2d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="04c2d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04c2d-117">-ItemType</span><span class="sxs-lookup"><span data-stu-id="04c2d-117">-ItemType</span></span>
<span data-ttu-id="04c2d-118">Określa typ elementu wykazu dla elementów, które są pobierane lub wyświetlane na liście.</span><span class="sxs-lookup"><span data-stu-id="04c2d-118">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="04c2d-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="04c2d-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="04c2d-120">Bazy danych</span><span class="sxs-lookup"><span data-stu-id="04c2d-120">Database</span></span>
- <span data-ttu-id="04c2d-121">Schematu</span><span class="sxs-lookup"><span data-stu-id="04c2d-121">Schema</span></span>
- <span data-ttu-id="04c2d-122">Zespołu</span><span class="sxs-lookup"><span data-stu-id="04c2d-122">Assembly</span></span>
- <span data-ttu-id="04c2d-123">Tworząc</span><span class="sxs-lookup"><span data-stu-id="04c2d-123">Table</span></span>
- <span data-ttu-id="04c2d-124">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="04c2d-124">TableValuedFunction</span></span>
- <span data-ttu-id="04c2d-125">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="04c2d-125">TableStatistics</span></span>
- <span data-ttu-id="04c2d-126">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="04c2d-126">ExternalDataSource</span></span>
- <span data-ttu-id="04c2d-127">Przeglądania</span><span class="sxs-lookup"><span data-stu-id="04c2d-127">View</span></span>
- <span data-ttu-id="04c2d-128">Wewnętrznym</span><span class="sxs-lookup"><span data-stu-id="04c2d-128">Procedure</span></span>
- <span data-ttu-id="04c2d-129">Haseł</span><span class="sxs-lookup"><span data-stu-id="04c2d-129">Secret</span></span>
- <span data-ttu-id="04c2d-130">Mobilne</span><span class="sxs-lookup"><span data-stu-id="04c2d-130">Credential</span></span>
- <span data-ttu-id="04c2d-131">Gatunków</span><span class="sxs-lookup"><span data-stu-id="04c2d-131">Types</span></span>
- <span data-ttu-id="04c2d-132">TablePartition</span><span class="sxs-lookup"><span data-stu-id="04c2d-132">TablePartition</span></span>

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

### <span data-ttu-id="04c2d-133">-Path</span><span class="sxs-lookup"><span data-stu-id="04c2d-133">-Path</span></span>
<span data-ttu-id="04c2d-134">Określa ścieżkę wielu części do elementu, który ma zostać pobrany, lub element nadrzędny elementów do listy.</span><span class="sxs-lookup"><span data-stu-id="04c2d-134">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="04c2d-135">Części ścieżki powinny być oddzielone kropką (.).</span><span class="sxs-lookup"><span data-stu-id="04c2d-135">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="04c2d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04c2d-136">CommonParameters</span></span>
<span data-ttu-id="04c2d-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04c2d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04c2d-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04c2d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04c2d-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04c2d-139">INPUTS</span></span>

### <span data-ttu-id="04c2d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="04c2d-140">System.String</span></span>

### <span data-ttu-id="04c2d-141">Microsoft. Azure. Commands. DataLakeAnalytics. models. DataLakeAnalyticsEnums + CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="04c2d-141">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="04c2d-142">Microsoft. Azure. Commands. DataLakeAnalytics. models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="04c2d-142">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="04c2d-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="04c2d-143">OUTPUTS</span></span>

### <span data-ttu-id="04c2d-144">Microsoft. Azure. Management. datalake. Analytics. modele. CatalogItem</span><span class="sxs-lookup"><span data-stu-id="04c2d-144">Microsoft.Azure.Management.DataLake.Analytics.Models.CatalogItem</span></span>

## <span data-ttu-id="04c2d-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="04c2d-145">NOTES</span></span>

## <span data-ttu-id="04c2d-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04c2d-146">RELATED LINKS</span></span>

[<span data-ttu-id="04c2d-147">Test — AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="04c2d-147">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Test-AzureRmDataLakeAnalyticsCatalogItem.md)


