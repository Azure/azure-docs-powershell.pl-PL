---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 2879923b38b6813213fe6819f84fa55a593f6930
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501514"
---
# <span data-ttu-id="04b96-101">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="04b96-101">Test-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="04b96-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="04b96-102">SYNOPSIS</span></span>
<span data-ttu-id="04b96-103">Sprawdza obecność elementu wykazu.</span><span class="sxs-lookup"><span data-stu-id="04b96-103">Checks for the existence of a catalog item.</span></span>

## <span data-ttu-id="04b96-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="04b96-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04b96-105">Opis</span><span class="sxs-lookup"><span data-stu-id="04b96-105">DESCRIPTION</span></span>
<span data-ttu-id="04b96-106">Polecenie cmdlet **test-AzDataLakeAnalyticsCatalogItem** sprawdza obecność elementu wykazu usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="04b96-106">The **Test-AzDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="04b96-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="04b96-107">EXAMPLES</span></span>

### <span data-ttu-id="04b96-108">Przykład 1: Sprawdzanie, czy istnieje element wykazu</span><span class="sxs-lookup"><span data-stu-id="04b96-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="04b96-109">To polecenie sprawdza, czy istnieje określony element schematu.</span><span class="sxs-lookup"><span data-stu-id="04b96-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="04b96-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="04b96-110">PARAMETERS</span></span>

### <span data-ttu-id="04b96-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="04b96-111">-Account</span></span>
<span data-ttu-id="04b96-112">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="04b96-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="04b96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04b96-113">-DefaultProfile</span></span>
<span data-ttu-id="04b96-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="04b96-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04b96-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="04b96-115">-ItemType</span></span>
<span data-ttu-id="04b96-116">Określa typ elementu wykazu elementu do sprawdzenia.</span><span class="sxs-lookup"><span data-stu-id="04b96-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="04b96-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="04b96-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="04b96-118">Bazy danych</span><span class="sxs-lookup"><span data-stu-id="04b96-118">Database</span></span>
- <span data-ttu-id="04b96-119">Schematu</span><span class="sxs-lookup"><span data-stu-id="04b96-119">Schema</span></span>
- <span data-ttu-id="04b96-120">Zespołu</span><span class="sxs-lookup"><span data-stu-id="04b96-120">Assembly</span></span>
- <span data-ttu-id="04b96-121">Tworząc</span><span class="sxs-lookup"><span data-stu-id="04b96-121">Table</span></span>
- <span data-ttu-id="04b96-122">TablePartition</span><span class="sxs-lookup"><span data-stu-id="04b96-122">TablePartition</span></span>
- <span data-ttu-id="04b96-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="04b96-123">TableValuedFunction</span></span>
- <span data-ttu-id="04b96-124">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="04b96-124">TableStatistics</span></span>
- <span data-ttu-id="04b96-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="04b96-125">ExternalDataSource</span></span>
- <span data-ttu-id="04b96-126">Przeglądania</span><span class="sxs-lookup"><span data-stu-id="04b96-126">View</span></span>
- <span data-ttu-id="04b96-127">Wewnętrznym</span><span class="sxs-lookup"><span data-stu-id="04b96-127">Procedure</span></span>
- <span data-ttu-id="04b96-128">Haseł</span><span class="sxs-lookup"><span data-stu-id="04b96-128">Secret</span></span>
- <span data-ttu-id="04b96-129">Mobilne</span><span class="sxs-lookup"><span data-stu-id="04b96-129">Credential</span></span>
- <span data-ttu-id="04b96-130">Gatunków</span><span class="sxs-lookup"><span data-stu-id="04b96-130">Types</span></span>

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

### <span data-ttu-id="04b96-131">-Path</span><span class="sxs-lookup"><span data-stu-id="04b96-131">-Path</span></span>
<span data-ttu-id="04b96-132">Określa ścieżkę do elementu, który ma zostać pobrany, lub ścieżkę do elementu nadrzędnego na liście elementy do listy.</span><span class="sxs-lookup"><span data-stu-id="04b96-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04b96-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04b96-133">CommonParameters</span></span>
<span data-ttu-id="04b96-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04b96-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04b96-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04b96-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04b96-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04b96-136">INPUTS</span></span>

### <span data-ttu-id="04b96-137">System. String</span><span class="sxs-lookup"><span data-stu-id="04b96-137">System.String</span></span>

### <span data-ttu-id="04b96-138">Microsoft. Azure. Commands. DataLakeAnalytics. models. DataLakeAnalyticsEnums + CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="04b96-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="04b96-139">Microsoft. Azure. Commands. DataLakeAnalytics. models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="04b96-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="04b96-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="04b96-140">OUTPUTS</span></span>

### <span data-ttu-id="04b96-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04b96-141">System.Boolean</span></span>

## <span data-ttu-id="04b96-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="04b96-142">NOTES</span></span>

## <span data-ttu-id="04b96-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04b96-143">RELATED LINKS</span></span>

[<span data-ttu-id="04b96-144">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="04b96-144">Get-AzDataLakeAnalyticsCatalogItem</span></span>](./Get-AzDataLakeAnalyticsCatalogItem.md)


