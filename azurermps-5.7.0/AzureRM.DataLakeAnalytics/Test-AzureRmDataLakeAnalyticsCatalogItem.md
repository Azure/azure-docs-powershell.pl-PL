---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/test-azurermdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: deb93fb17c2c739dcf377665f8b2f604a2fb4847
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544376"
---
# <span data-ttu-id="7af28-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="7af28-101">Test-AzureRmDataLakeAnalyticsCatalogItem</span></span>

## <span data-ttu-id="7af28-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7af28-102">SYNOPSIS</span></span>
<span data-ttu-id="7af28-103">Sprawdza obecność elementu wykazu.</span><span class="sxs-lookup"><span data-stu-id="7af28-103">Checks for the existence of a catalog item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7af28-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7af28-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7af28-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7af28-105">DESCRIPTION</span></span>
<span data-ttu-id="7af28-106">Polecenie cmdlet **test-AzureRmDataLakeAnalyticsCatalogItem** sprawdza obecność elementu wykazu usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="7af28-106">The **Test-AzureRmDataLakeAnalyticsCatalogItem** cmdlet checks for the existence of an Azure Data Lake Analytics catalog item.</span></span>

## <span data-ttu-id="7af28-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7af28-107">EXAMPLES</span></span>

### <span data-ttu-id="7af28-108">Przykład 1: Sprawdzanie, czy istnieje element wykazu</span><span class="sxs-lookup"><span data-stu-id="7af28-108">Example 1: Test whether a catalog item exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

<span data-ttu-id="7af28-109">To polecenie sprawdza, czy istnieje określony element schematu.</span><span class="sxs-lookup"><span data-stu-id="7af28-109">This command tests whether a specified Schema item exists.</span></span>

## <span data-ttu-id="7af28-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7af28-110">PARAMETERS</span></span>

### <span data-ttu-id="7af28-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="7af28-111">-Account</span></span>
<span data-ttu-id="7af28-112">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="7af28-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7af28-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7af28-113">-DefaultProfile</span></span>
<span data-ttu-id="7af28-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7af28-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7af28-115">-ItemType</span><span class="sxs-lookup"><span data-stu-id="7af28-115">-ItemType</span></span>
<span data-ttu-id="7af28-116">Określa typ elementu wykazu elementu do sprawdzenia.</span><span class="sxs-lookup"><span data-stu-id="7af28-116">Specifies the catalog item type of the item to check.</span></span>
<span data-ttu-id="7af28-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7af28-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7af28-118">Bazy danych</span><span class="sxs-lookup"><span data-stu-id="7af28-118">Database</span></span>
- <span data-ttu-id="7af28-119">Schematu</span><span class="sxs-lookup"><span data-stu-id="7af28-119">Schema</span></span>
- <span data-ttu-id="7af28-120">Zespołu</span><span class="sxs-lookup"><span data-stu-id="7af28-120">Assembly</span></span>
- <span data-ttu-id="7af28-121">Tworząc</span><span class="sxs-lookup"><span data-stu-id="7af28-121">Table</span></span>
- <span data-ttu-id="7af28-122">TablePartition</span><span class="sxs-lookup"><span data-stu-id="7af28-122">TablePartition</span></span>
- <span data-ttu-id="7af28-123">TableValuedFunction</span><span class="sxs-lookup"><span data-stu-id="7af28-123">TableValuedFunction</span></span>
- <span data-ttu-id="7af28-124">TableStatistics</span><span class="sxs-lookup"><span data-stu-id="7af28-124">TableStatistics</span></span>
- <span data-ttu-id="7af28-125">ExternalDataSource</span><span class="sxs-lookup"><span data-stu-id="7af28-125">ExternalDataSource</span></span>
- <span data-ttu-id="7af28-126">Przeglądania</span><span class="sxs-lookup"><span data-stu-id="7af28-126">View</span></span>
- <span data-ttu-id="7af28-127">Wewnętrznym</span><span class="sxs-lookup"><span data-stu-id="7af28-127">Procedure</span></span>
- <span data-ttu-id="7af28-128">Haseł</span><span class="sxs-lookup"><span data-stu-id="7af28-128">Secret</span></span>
- <span data-ttu-id="7af28-129">Mobilne</span><span class="sxs-lookup"><span data-stu-id="7af28-129">Credential</span></span>
- <span data-ttu-id="7af28-130">Gatunków</span><span class="sxs-lookup"><span data-stu-id="7af28-130">Types</span></span>

```yaml
Type: CatalogItemType
Parameter Sets: (All)
Aliases: 
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7af28-131">-Path</span><span class="sxs-lookup"><span data-stu-id="7af28-131">-Path</span></span>
<span data-ttu-id="7af28-132">Określa ścieżkę do elementu, który ma zostać pobrany, lub ścieżkę do elementu nadrzędnego na liście elementy do listy.</span><span class="sxs-lookup"><span data-stu-id="7af28-132">Specifies the path to the item to fetch, or the path to the parent item of the items to list.</span></span>

```yaml
Type: CatalogPathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7af28-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7af28-133">CommonParameters</span></span>
<span data-ttu-id="7af28-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7af28-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7af28-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7af28-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7af28-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7af28-136">INPUTS</span></span>

### <span data-ttu-id="7af28-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7af28-137">None</span></span>
<span data-ttu-id="7af28-138">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="7af28-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7af28-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7af28-139">OUTPUTS</span></span>

### <span data-ttu-id="7af28-140">logiczną</span><span class="sxs-lookup"><span data-stu-id="7af28-140">bool</span></span>
<span data-ttu-id="7af28-141">Prawda lub FAŁSZ wskazujący, czy określony element wykazu istnieje, czy nie.</span><span class="sxs-lookup"><span data-stu-id="7af28-141">True or false indicating if the specified catalog item exists or not.</span></span>

## <span data-ttu-id="7af28-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7af28-142">NOTES</span></span>

## <span data-ttu-id="7af28-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7af28-143">RELATED LINKS</span></span>

[<span data-ttu-id="7af28-144">Get-AzureRmDataLakeAnalyticsCatalogItem</span><span class="sxs-lookup"><span data-stu-id="7af28-144">Get-AzureRmDataLakeAnalyticsCatalogItem</span></span>](./Get-AzureRmDataLakeAnalyticsCatalogItem.md)


