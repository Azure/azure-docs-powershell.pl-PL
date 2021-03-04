---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: ba8a97e96a07e63cd3b1f63c85a71291c59fdab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956225"
---
# <span data-ttu-id="d96f6-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="d96f6-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="d96f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d96f6-102">SYNOPSIS</span></span>
<span data-ttu-id="d96f6-103">Przywracanie usuniętego pliku lub folderu w usłudze Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="d96f6-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="d96f6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d96f6-104">SYNTAX</span></span>

### <span data-ttu-id="d96f6-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d96f6-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d96f6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d96f6-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d96f6-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d96f6-107">DESCRIPTION</span></span>
<span data-ttu-id="d96f6-108">Polecenie **cmdlet Restore-AzDataLakeStoreDeletedItem** przywraca usunięty plik lub folder w magazynie Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d96f6-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="d96f6-109">Wymaga ścieżki usuniętego elementu w Koszu zwróconej przez element Get-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="d96f6-109">Requires the path of deleted item in trash returned by Get-AzDataLakeStoreDeletedItem.</span></span>
<span data-ttu-id="d96f6-110">Przestroga: Cofanie delegowania plików to operacja o najlepszym namysłu.</span><span class="sxs-lookup"><span data-stu-id="d96f6-110">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="d96f6-111">Nie ma żadnych gwarancji, że plik można przywrócić po jego usunięciu.</span><span class="sxs-lookup"><span data-stu-id="d96f6-111">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="d96f6-112">Korzystanie z tego interfejsu API jest włączane za pośrednictwem list białych.</span><span class="sxs-lookup"><span data-stu-id="d96f6-112">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="d96f6-113">Jeśli Twoje konto ADL nie jest na liście na liście, użycie tego interfejsu API spowoduje nie zaimplementowanie wyjątku.</span><span class="sxs-lookup"><span data-stu-id="d96f6-113">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="d96f6-114">Aby uzyskać więcej informacji i uzyskać pomoc, skontaktuj się z pomocą techniczną firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d96f6-114">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="d96f6-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d96f6-115">EXAMPLES</span></span>

### <span data-ttu-id="d96f6-116">Przykład 1. Przywracanie pliku ze sklepu Data Lake Store przy użyciu opcji wymuszania</span><span class="sxs-lookup"><span data-stu-id="d96f6-116">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
```
PS > Restore-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Path 927e8fb1-a287-4353-b50e-3b4a39ae4088 -Destination adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 -Type "file" -Force
PS >

### Example 2: Restore a file from Data Lake Store using user confirmation

PS > restore-azdatalakestoredeleteditem -account ml1ptrashtest -path 927e8fb1-a287-4353-b50e-3b4a39ae4088 -destination adl://ml1ptrashtest.azuredatalake.com/test4/file_1115 -type file

Restore user data ?
From - 927e8fb1-a287-4353-b50e-3b4a39ae4088
To   - adl://ml1ptrashtest.azuredatalake.com/test4/file_1115
Type - file
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
PS >
```

## <span data-ttu-id="d96f6-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d96f6-117">PARAMETERS</span></span>

### <span data-ttu-id="d96f6-118">— Konto</span><span class="sxs-lookup"><span data-stu-id="d96f6-118">-Account</span></span>
<span data-ttu-id="d96f6-119">Określa nazwę konta sklepu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d96f6-119">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d96f6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d96f6-120">-DefaultProfile</span></span>
<span data-ttu-id="d96f6-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d96f6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d96f6-122">-DeletedItem</span><span class="sxs-lookup"><span data-stu-id="d96f6-122">-DeletedItem</span></span>
<span data-ttu-id="d96f6-123">Obiekt elementu usuniętego.</span><span class="sxs-lookup"><span data-stu-id="d96f6-123">The deleted item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d96f6-124">— miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="d96f6-124">-Destination</span></span>
<span data-ttu-id="d96f6-125">Ścieżka docelowa, do której należy przywrócić usunięty plik lub folder.</span><span class="sxs-lookup"><span data-stu-id="d96f6-125">The destination path to where the deleted file or folder should be restored.</span></span> 

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d96f6-126">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="d96f6-126">-Force</span></span>
<span data-ttu-id="d96f6-127">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d96f6-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d96f6-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d96f6-128">-PassThru</span></span>
<span data-ttu-id="d96f6-129">Zwraca wartość logiczną prawda w przypadku sukcesu.</span><span class="sxs-lookup"><span data-stu-id="d96f6-129">Return boolean true on success.</span></span>

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

### <span data-ttu-id="d96f6-130">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="d96f6-130">-Path</span></span>
<span data-ttu-id="d96f6-131">Ścieżka usuniętego pliku lub folderu w Koszu.</span><span class="sxs-lookup"><span data-stu-id="d96f6-131">The path of the deleted file or folder in trash.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d96f6-132">-RestoreAction</span><span class="sxs-lookup"><span data-stu-id="d96f6-132">-RestoreAction</span></span>
<span data-ttu-id="d96f6-133">Akcja do podjęcia w przypadku konfliktów nazwy miejsca docelowego — "kopiowanie" lub "zastępowanie"</span><span class="sxs-lookup"><span data-stu-id="d96f6-133">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d96f6-134">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="d96f6-134">-Type</span></span>
<span data-ttu-id="d96f6-135">Typ przywracanych wpisów — "plik" lub "folder"</span><span class="sxs-lookup"><span data-stu-id="d96f6-135">The type of entry being restored - "file" or "folder"</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d96f6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d96f6-136">CommonParameters</span></span>
<span data-ttu-id="d96f6-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d96f6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d96f6-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d96f6-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d96f6-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d96f6-139">INPUTS</span></span>

### <span data-ttu-id="d96f6-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d96f6-140">System.String</span></span>

## <span data-ttu-id="d96f6-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d96f6-141">OUTPUTS</span></span>

### <span data-ttu-id="d96f6-142">Brak</span><span class="sxs-lookup"><span data-stu-id="d96f6-142">None</span></span>

## <span data-ttu-id="d96f6-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d96f6-143">NOTES</span></span>

## <span data-ttu-id="d96f6-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d96f6-144">RELATED LINKS</span></span>

[<span data-ttu-id="d96f6-145">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="d96f6-145">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)