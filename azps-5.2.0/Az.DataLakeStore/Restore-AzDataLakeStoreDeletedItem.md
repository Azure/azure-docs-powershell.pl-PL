---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 9dcc45f8f082ce59a6082ad71c2084c5df10064c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344278"
---
# <span data-ttu-id="608a3-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="608a3-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="608a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="608a3-102">SYNOPSIS</span></span>
<span data-ttu-id="608a3-103">Przywracanie usuniętego pliku lub folderu w usłudze Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="608a3-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="608a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="608a3-104">SYNTAX</span></span>

### <span data-ttu-id="608a3-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="608a3-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="608a3-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="608a3-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="608a3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="608a3-107">DESCRIPTION</span></span>
<span data-ttu-id="608a3-108">Polecenie cmdlet **Restore-AzDataLakeStoreDeletedItem** przywraca usunięty plik lub folder w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="608a3-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="608a3-109">Wymaga ścieżki elementu usuniętego w koszu zwracanym przez polecenie Get-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="608a3-109">Requires the path of deleted item in trash returned by Get-AzDataLakeStoreDeletedItem.</span></span>
<span data-ttu-id="608a3-110">Przestroga: usuwanie plików jest najlepszym rozwiązaniem.</span><span class="sxs-lookup"><span data-stu-id="608a3-110">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="608a3-111">Nie ma gwarancji, że plik może zostać przywrócony po jego usunięciu.</span><span class="sxs-lookup"><span data-stu-id="608a3-111">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="608a3-112">Korzystanie z tego interfejsu API jest włączone za pośrednictwem whitelisting.</span><span class="sxs-lookup"><span data-stu-id="608a3-112">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="608a3-113">Jeśli Twoje konto usługi ADL nie jest whitelisted, użycie tego interfejsu API spowoduje zgłoszenie wyjątku niezaimplementowane.</span><span class="sxs-lookup"><span data-stu-id="608a3-113">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="608a3-114">Aby uzyskać więcej informacji i uzyskać pomoc, skontaktuj się z pomocą techniczną firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="608a3-114">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="608a3-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="608a3-115">EXAMPLES</span></span>

### <span data-ttu-id="608a3-116">Przykład 1: Przywracanie pliku z opcji Data Lake Store using-Force</span><span class="sxs-lookup"><span data-stu-id="608a3-116">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
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

## <span data-ttu-id="608a3-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="608a3-117">PARAMETERS</span></span>

### <span data-ttu-id="608a3-118">— Konto</span><span class="sxs-lookup"><span data-stu-id="608a3-118">-Account</span></span>
<span data-ttu-id="608a3-119">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="608a3-119">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="608a3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="608a3-120">-DefaultProfile</span></span>
<span data-ttu-id="608a3-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="608a3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="608a3-122">-DeletedItem</span><span class="sxs-lookup"><span data-stu-id="608a3-122">-DeletedItem</span></span>
<span data-ttu-id="608a3-123">Usunięty obiekt elementu.</span><span class="sxs-lookup"><span data-stu-id="608a3-123">The deleted item object.</span></span>

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

### <span data-ttu-id="608a3-124">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="608a3-124">-Destination</span></span>
<span data-ttu-id="608a3-125">Ścieżka docelowa, w której ma zostać przywrócony usunięty plik lub folder.</span><span class="sxs-lookup"><span data-stu-id="608a3-125">The destination path to where the deleted file or folder should be restored.</span></span> 

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

### <span data-ttu-id="608a3-126">-Force</span><span class="sxs-lookup"><span data-stu-id="608a3-126">-Force</span></span>
<span data-ttu-id="608a3-127">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="608a3-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="608a3-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="608a3-128">-PassThru</span></span>
<span data-ttu-id="608a3-129">Zwraca wartość logiczną PRAWDA po powodzeniu.</span><span class="sxs-lookup"><span data-stu-id="608a3-129">Return boolean true on success.</span></span>

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

### <span data-ttu-id="608a3-130">-Path</span><span class="sxs-lookup"><span data-stu-id="608a3-130">-Path</span></span>
<span data-ttu-id="608a3-131">Ścieżka usuniętego pliku lub folderu w koszu.</span><span class="sxs-lookup"><span data-stu-id="608a3-131">The path of the deleted file or folder in trash.</span></span>

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

### <span data-ttu-id="608a3-132">-RestoreAction</span><span class="sxs-lookup"><span data-stu-id="608a3-132">-RestoreAction</span></span>
<span data-ttu-id="608a3-133">Akcja wykonywana w przypadku konfliktów nazw docelowych — "kopia" lub "zastępowanie"</span><span class="sxs-lookup"><span data-stu-id="608a3-133">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

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

### <span data-ttu-id="608a3-134">-Type</span><span class="sxs-lookup"><span data-stu-id="608a3-134">-Type</span></span>
<span data-ttu-id="608a3-135">Typ przywracanego wpisu — "plik" lub "folder"</span><span class="sxs-lookup"><span data-stu-id="608a3-135">The type of entry being restored - "file" or "folder"</span></span>

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

### <span data-ttu-id="608a3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="608a3-136">CommonParameters</span></span>
<span data-ttu-id="608a3-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="608a3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="608a3-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="608a3-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="608a3-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="608a3-139">INPUTS</span></span>

### <span data-ttu-id="608a3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="608a3-140">System.String</span></span>

## <span data-ttu-id="608a3-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="608a3-141">OUTPUTS</span></span>

### <span data-ttu-id="608a3-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="608a3-142">None</span></span>

## <span data-ttu-id="608a3-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="608a3-143">NOTES</span></span>

## <span data-ttu-id="608a3-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="608a3-144">RELATED LINKS</span></span>

[<span data-ttu-id="608a3-145">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="608a3-145">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)