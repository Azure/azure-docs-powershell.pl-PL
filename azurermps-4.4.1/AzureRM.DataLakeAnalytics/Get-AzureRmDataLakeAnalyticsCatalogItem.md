---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: b12b09c686a2e0a5fcd85854551608b16cb43d3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553343"
---
# <span data-ttu-id="f6001-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="f6001-101">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="f6001-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f6001-102">SYNOPSIS</span></span>
<span data-ttu-id="f6001-103">Pobiera element lub typy elementów wykazu usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="f6001-103">Gets a Data Lake Analytics catalog item or types of items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6001-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f6001-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6001-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f6001-105">DESCRIPTION</span></span>
<span data-ttu-id="f6001-106">Polecenie **Get-AzureRmDataLakeAnalyticsCatalogItem** Pobiera określony element wykazu usługi Azure Data Lake Analytics lub Pobiera elementy wykazu określonego typu.</span><span class="sxs-lookup"><span data-stu-id="f6001-106">The **Get-AzureRmDataLakeAnalyticsCatalogItem** gets a specified Azure Data Lake Analytics catalog item, or gets catalog items of a specified type.</span></span>

## <span data-ttu-id="f6001-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f6001-107">EXAMPLES</span></span>

### <span data-ttu-id="f6001-108">Przykład 1: uzyskiwanie określonej bazy danych</span><span class="sxs-lookup"><span data-stu-id="f6001-108">Example 1: Get a specified database</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

<span data-ttu-id="f6001-109">To polecenie pobiera określoną bazę danych.</span><span class="sxs-lookup"><span data-stu-id="f6001-109">This command gets the specified database.</span></span>

### <span data-ttu-id="f6001-110">Przykład 2: Pobieranie tabel w określonej bazie danych i schemacie</span><span class="sxs-lookup"><span data-stu-id="f6001-110">Example 2: Get tables in a specified database and schema</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

<span data-ttu-id="f6001-111">To polecenie pobiera listę tabel w określonej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="f6001-111">This command gets a list of tables in the specified database.</span></span>

## <span data-ttu-id="f6001-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f6001-112">PARAMETERS</span></span>

### <span data-ttu-id="f6001-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="f6001-113">-Account</span></span>
<span data-ttu-id="f6001-114">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="f6001-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="f6001-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="f6001-115">-ItemType</span></span>
<span data-ttu-id="f6001-116">Określa typ elementu wykazu dla elementów, które są pobierane lub wyświetlane na liście.</span><span class="sxs-lookup"><span data-stu-id="f6001-116">Specifies the catalog item type of the item(s) being fetched or listed.</span></span>
<span data-ttu-id="f6001-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f6001-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f6001-118">Bazy danych</span><span class="sxs-lookup"><span data-stu-id="f6001-118">Database</span></span>
- <span data-ttu-id="f6001-119">Schematu</span><span class="sxs-lookup"><span data-stu-id="f6001-119">Schema</span></span>
- <span data-ttu-id="f6001-120">Zespołu</span><span class="sxs-lookup"><span data-stu-id="f6001-120">Assembly</span></span>
- <span data-ttu-id="f6001-121">Tworząc</span><span class="sxs-lookup"><span data-stu-id="f6001-121">Table</span></span>
- <span data-ttu-id="f6001-122">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="f6001-122">TableValuedFunction</span></span>
- <span data-ttu-id="f6001-123">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="f6001-123">TableStatistics</span></span>
- <span data-ttu-id="f6001-124">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="f6001-124">ExternalDataSource</span></span>
- <span data-ttu-id="f6001-125">Przeglądania</span><span class="sxs-lookup"><span data-stu-id="f6001-125">View</span></span>
- <span data-ttu-id="f6001-126">Wewnętrznym</span><span class="sxs-lookup"><span data-stu-id="f6001-126">Procedure</span></span>
- <span data-ttu-id="f6001-127">Haseł</span><span class="sxs-lookup"><span data-stu-id="f6001-127">Secret</span></span>
- <span data-ttu-id="f6001-128">Mobilne</span><span class="sxs-lookup"><span data-stu-id="f6001-128">Credential</span></span>
- <span data-ttu-id="f6001-129">Gatunków</span><span class="sxs-lookup"><span data-stu-id="f6001-129">Types</span></span>
- <span data-ttu-id="f6001-130">TablePartition</span><span class="sxs-lookup"><span data-stu-id="f6001-130">TablePartition</span></span>

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

### <span data-ttu-id="f6001-131">-Path</span><span class="sxs-lookup"><span data-stu-id="f6001-131">-Path</span></span>
<span data-ttu-id="f6001-132">Określa ścieżkę wielu części do elementu, który ma zostać pobrany, lub element nadrzędny elementów do listy.</span><span class="sxs-lookup"><span data-stu-id="f6001-132">Specifies the multi-part path to the item to retrieve, or to the parent item of the items to list.</span></span>
<span data-ttu-id="f6001-133">Części ścieżki powinny być oddzielone kropką (.).</span><span class="sxs-lookup"><span data-stu-id="f6001-133">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="f6001-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6001-134">-DefaultProfile</span></span>
<span data-ttu-id="f6001-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f6001-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6001-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6001-136">CommonParameters</span></span>
<span data-ttu-id="f6001-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6001-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6001-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6001-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6001-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6001-139">INPUTS</span></span>

## <span data-ttu-id="f6001-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f6001-140">OUTPUTS</span></span>

### <span data-ttu-id="f6001-141">CatalogItem</span><span class="sxs-lookup"><span data-stu-id="f6001-141">CatalogItem</span></span>
<span data-ttu-id="f6001-142">Określony element katalogu.</span><span class="sxs-lookup"><span data-stu-id="f6001-142">The specified catalog item.</span></span>

### <span data-ttu-id="f6001-143">Lista<CatalogItem></span><span class="sxs-lookup"><span data-stu-id="f6001-143">List<CatalogItem></span></span>
<span data-ttu-id="f6001-144">Lista określonych elementów wykazu pod odpowiednim kontenerem.</span><span class="sxs-lookup"><span data-stu-id="f6001-144">The list of the specified catalog items underneath their corresponding container.</span></span>

## <span data-ttu-id="f6001-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f6001-145">NOTES</span></span>

## <span data-ttu-id="f6001-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6001-146">RELATED LINKS</span></span>

[<span data-ttu-id="f6001-147">Test — AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="f6001-147">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Test-AzureRmDataLakeAnalyticsCatalogItem.md)


