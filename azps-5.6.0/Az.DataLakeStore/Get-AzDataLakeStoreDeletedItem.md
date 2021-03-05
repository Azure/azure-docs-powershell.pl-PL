---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BF0A5D64-AC93-48F5-AED2-C21CC8829053
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 92ad3143a52f0d9a81505375ff5abd221784fb2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986126"
---
# <span data-ttu-id="36949-101">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="36949-101">Get-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="36949-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36949-102">SYNOPSIS</span></span>
<span data-ttu-id="36949-103">Wyszukuje usunięte wpisy w Koszu, które są zgodne z filtrem.</span><span class="sxs-lookup"><span data-stu-id="36949-103">Searches for deleted entries in trash which match the filter.</span></span>

## <span data-ttu-id="36949-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="36949-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreDeletedItem [-Account] <String> [-Filter] <String> [-Count <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36949-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="36949-105">DESCRIPTION</span></span>
<span data-ttu-id="36949-106">Polecenie **cmdlet Get-AzDataLakeStoreDeletedItem** przeszukuje usunięte pliki lub foldery w magazynie Data Lake Store, które są zgodne z danym filtrem.</span><span class="sxs-lookup"><span data-stu-id="36949-106">The **Get-AzDataLakeStoreDeletedItem** cmdlet searches the deleted files or folders in Data Lake Store which match the given filter.</span></span>
<span data-ttu-id="36949-107">Wyświetlane są następujące atrybuty elementów usuniętych: OriginalPath, TrashDirPath, Type, CreationTime.</span><span class="sxs-lookup"><span data-stu-id="36949-107">It displays the following attributes of the deleted items - OriginalPath, TrashDirPath, Type, CreationTime.</span></span>
<span data-ttu-id="36949-108">Może to być długa operacja, ponieważ może ona wymagać przeszukania milionów plików w Koszu i może zostać uruchomiona jako zadanie.</span><span class="sxs-lookup"><span data-stu-id="36949-108">This could be a long running operation as it may have to search through millions of files in trash and could be run as a job.</span></span>
<span data-ttu-id="36949-109">Przestroga: Cofanie delegowania plików to operacja o najlepszym namysłu.</span><span class="sxs-lookup"><span data-stu-id="36949-109">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="36949-110">Nie ma żadnych gwarancji, że plik można przywrócić po jego usunięciu.</span><span class="sxs-lookup"><span data-stu-id="36949-110">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="36949-111">Korzystanie z tego interfejsu API jest włączane za pośrednictwem list białych.</span><span class="sxs-lookup"><span data-stu-id="36949-111">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="36949-112">Jeśli Twoje konto ADL nie jest na liście na liście, użycie tego interfejsu API spowoduje nie zaimplementowanie wyjątku.</span><span class="sxs-lookup"><span data-stu-id="36949-112">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="36949-113">Aby uzyskać więcej informacji i uzyskać pomoc, skontaktuj się z pomocą techniczną firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="36949-113">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="36949-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="36949-114">EXAMPLES</span></span>

### <span data-ttu-id="36949-115">Przykład: Uzyskiwanie szczegółów pliku ze sklepu Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="36949-115">Example: Get details of a file from the Data Lake Store</span></span>
```
PS> Get-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Filter test0/file_123

TrashDirPath                         OriginalPath                                          Type CreationTime
------------                         ------------                                          ---- ------------
cd6ad5ce-792b-4812-8a33-8f9ed19eb532 adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 FILE 2/8/2019 8:12:18 AM
356cfd42-39c7-451e-96cb-9f47883d91e2 adl://ml1ptrashtest.azuredatalake.com/test0/file_1232 FILE 2/8/2019 8:12:18 AM
e7b30ac8-2dbc-43a3-8ca6-2d420ac0c488 adl://ml1ptrashtest.azuredatalake.com/test0/file_1237 FILE 2/8/2019 8:12:18 AM
```

## <span data-ttu-id="36949-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36949-116">PARAMETERS</span></span>

### <span data-ttu-id="36949-117">— Konto</span><span class="sxs-lookup"><span data-stu-id="36949-117">-Account</span></span>
<span data-ttu-id="36949-118">Określa nazwę konta sklepu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="36949-118">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="36949-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="36949-119">-AsJob</span></span>
<span data-ttu-id="36949-120">Uruchom polecenie cmdlet w tle.</span><span class="sxs-lookup"><span data-stu-id="36949-120">Run cmdlet in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36949-121">— Liczba</span><span class="sxs-lookup"><span data-stu-id="36949-121">-Count</span></span>
<span data-ttu-id="36949-122">Określa liczbę wyników, które użytkownik chce znaleźć.</span><span class="sxs-lookup"><span data-stu-id="36949-122">Specifies the number of results the user wants to find.</span></span> <span data-ttu-id="36949-123">Zapytanie będzie uruchamiane do momentu wyszukania wyników zliczania lub przeszukania całego kosza w zależności od tego, co nastąpi najpierw.</span><span class="sxs-lookup"><span data-stu-id="36949-123">The query runs until it finds Count results or it searches through entire trash, whichever happens first.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36949-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36949-124">-DefaultProfile</span></span>
<span data-ttu-id="36949-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="36949-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36949-126">— Filtr</span><span class="sxs-lookup"><span data-stu-id="36949-126">-Filter</span></span>
<span data-ttu-id="36949-127">Określa zapytanie wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="36949-127">Specifies the search query.</span></span> <span data-ttu-id="36949-128">Bardziej szczegółowe wartości dają bardziej trafne wyniki.</span><span class="sxs-lookup"><span data-stu-id="36949-128">A more specific value gives more relevant results.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36949-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36949-129">CommonParameters</span></span>
<span data-ttu-id="36949-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36949-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36949-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36949-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36949-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36949-132">INPUTS</span></span>

### <span data-ttu-id="36949-133">System.String</span><span class="sxs-lookup"><span data-stu-id="36949-133">System.String</span></span>

## <span data-ttu-id="36949-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36949-134">OUTPUTS</span></span>

### <span data-ttu-id="36949-135">System.Collections.generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span><span class="sxs-lookup"><span data-stu-id="36949-135">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span></span>

## <span data-ttu-id="36949-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="36949-136">NOTES</span></span>

## <span data-ttu-id="36949-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36949-137">RELATED LINKS</span></span>

[<span data-ttu-id="36949-138">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="36949-138">Restore-AzDataLakeStoreDeletedItem</span></span>](./Restore-AzDataLakeStoreDeletedItem.md)