---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 2642a310e2a318498b3d170b463ac7e366bf5818
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957338"
---
# <span data-ttu-id="fe7e5-101">Test-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="fe7e5-101">Test-AzDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="fe7e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe7e5-102">SYNOPSIS</span></span>
<span data-ttu-id="fe7e5-103">Sprawdza, czy istnieje element wykazu.</span><span class="sxs-lookup"><span data-stu-id="fe7e5-103">Checks for the existence of a catalog item.</span></span>

## <span data-ttu-id="fe7e5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fe7e5-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe7e5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fe7e5-105">DESCRIPTION</span></span>
<span data-ttu-id="fe7e5-106">Polecenie **cmdlet Test-AzDataLakeAnalyticsCatalogItem** sprawdza, czy istnieje element wykazu usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="fe7e5-106">The **Test-AzDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="fe7e5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fe7e5-107">EXAMPLES</span></span>

### <span data-ttu-id="fe7e5-108">Przykład 1. Testowanie, czy istnieje element wykazu</span><span class="sxs-lookup"><span data-stu-id="fe7e5-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="fe7e5-109">To polecenie sprawdza, czy istnieje określony element schematu.</span><span class="sxs-lookup"><span data-stu-id="fe7e5-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="fe7e5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe7e5-110">PARAMETERS</span></span>

### <span data-ttu-id="fe7e5-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="fe7e5-111">-Account</span></span>
<span data-ttu-id="fe7e5-112">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="fe7e5-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="fe7e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe7e5-113">-DefaultProfile</span></span>
<span data-ttu-id="fe7e5-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="fe7e5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe7e5-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="fe7e5-115">-ItemType</span></span>
<span data-ttu-id="fe7e5-116">Określa typ elementu wykazu, który ma być sprawdzany.</span><span class="sxs-lookup"><span data-stu-id="fe7e5-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="fe7e5-117">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="fe7e5-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fe7e5-118">Baza danych</span><span class="sxs-lookup"><span data-stu-id="fe7e5-118">Database</span></span>
- <span data-ttu-id="fe7e5-119">Schemat</span><span class="sxs-lookup"><span data-stu-id="fe7e5-119">Schema</span></span>
- <span data-ttu-id="fe7e5-120">Zestaw</span><span class="sxs-lookup"><span data-stu-id="fe7e5-120">Assembly</span></span>
- <span data-ttu-id="fe7e5-121">Tabela</span><span class="sxs-lookup"><span data-stu-id="fe7e5-121">Table</span></span>
- <span data-ttu-id="fe7e5-122">TablePartition</span><span class="sxs-lookup"><span data-stu-id="fe7e5-122">TablePartition</span></span>
- <span data-ttu-id="fe7e5-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="fe7e5-123">TableValuedFunction</span></span>
- <span data-ttu-id="fe7e5-124">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="fe7e5-124">TableStatistics</span></span>
- <span data-ttu-id="fe7e5-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="fe7e5-125">ExternalDataSource</span></span>
- <span data-ttu-id="fe7e5-126">Widok</span><span class="sxs-lookup"><span data-stu-id="fe7e5-126">View</span></span>
- <span data-ttu-id="fe7e5-127">Procedura</span><span class="sxs-lookup"><span data-stu-id="fe7e5-127">Procedure</span></span>
- <span data-ttu-id="fe7e5-128">Tajny</span><span class="sxs-lookup"><span data-stu-id="fe7e5-128">Secret</span></span>
- <span data-ttu-id="fe7e5-129">Poświadczenia</span><span class="sxs-lookup"><span data-stu-id="fe7e5-129">Credential</span></span>
- <span data-ttu-id="fe7e5-130">Typy</span><span class="sxs-lookup"><span data-stu-id="fe7e5-130">Types</span></span>

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

### <span data-ttu-id="fe7e5-131">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="fe7e5-131">-Path</span></span>
<span data-ttu-id="fe7e5-132">Określa ścieżkę do elementu, który ma być pobierany, lub ścieżkę do elementu nadrzędnego elementów listy.</span><span class="sxs-lookup"><span data-stu-id="fe7e5-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

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

### <span data-ttu-id="fe7e5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe7e5-133">CommonParameters</span></span>
<span data-ttu-id="fe7e5-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe7e5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe7e5-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe7e5-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe7e5-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe7e5-136">INPUTS</span></span>

### <span data-ttu-id="fe7e5-137">System.String</span><span class="sxs-lookup"><span data-stu-id="fe7e5-137">System.String</span></span>

### <span data-ttu-id="fe7e5-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span><span class="sxs-lookup"><span data-stu-id="fe7e5-138">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType</span></span>

### <span data-ttu-id="fe7e5-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="fe7e5-139">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="fe7e5-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe7e5-140">OUTPUTS</span></span>

### <span data-ttu-id="fe7e5-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fe7e5-141">System.Boolean</span></span>

## <span data-ttu-id="fe7e5-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fe7e5-142">NOTES</span></span>

## <span data-ttu-id="fe7e5-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe7e5-143">RELATED LINKS</span></span>

[<span data-ttu-id="fe7e5-144">Get-AzDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="fe7e5-144">Get-AzDataLakeAnalyticsCatalogItem</span></span>](./Get-AzDataLakeAnalyticsCatalogItem.md)


