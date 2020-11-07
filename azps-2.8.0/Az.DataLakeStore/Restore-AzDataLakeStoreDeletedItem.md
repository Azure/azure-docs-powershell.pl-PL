---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 7df59f75200bbc0d52c595c263228d7bf9801486
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705775"
---
# <span data-ttu-id="f31e0-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="f31e0-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="f31e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f31e0-102">SYNOPSIS</span></span>
<span data-ttu-id="f31e0-103">Przywracanie usuniętego pliku lub folderu w usłudze Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="f31e0-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="f31e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f31e0-104">SYNTAX</span></span>

### <span data-ttu-id="f31e0-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f31e0-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f31e0-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="f31e0-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f31e0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f31e0-107">DESCRIPTION</span></span>
<span data-ttu-id="f31e0-108">Polecenie cmdlet **Restore-AzDataLakeStoreDeletedItem** przywraca usunięty plik lub folder w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f31e0-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="f31e0-109">Wymaga ścieżki elementu usuniętego w koszu zwracanym przez polecenie Get-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="f31e0-109">Requires the path of deleted item in trash returned by Get-AzDataLakeStoreDeletedItem.</span></span>

## <span data-ttu-id="f31e0-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f31e0-110">EXAMPLES</span></span>

### <span data-ttu-id="f31e0-111">Przykład 1: Przywracanie pliku z opcji Data Lake Store using-Force</span><span class="sxs-lookup"><span data-stu-id="f31e0-111">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
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

## <span data-ttu-id="f31e0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f31e0-112">PARAMETERS</span></span>

### <span data-ttu-id="f31e0-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="f31e0-113">-Account</span></span>
<span data-ttu-id="f31e0-114">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f31e0-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f31e0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f31e0-115">-DefaultProfile</span></span>
<span data-ttu-id="f31e0-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f31e0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f31e0-117">-DeletedItem</span><span class="sxs-lookup"><span data-stu-id="f31e0-117">-DeletedItem</span></span>
<span data-ttu-id="f31e0-118">Usunięty obiekt elementu.</span><span class="sxs-lookup"><span data-stu-id="f31e0-118">The deleted item object.</span></span>

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

### <span data-ttu-id="f31e0-119">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="f31e0-119">-Destination</span></span>
<span data-ttu-id="f31e0-120">Ścieżka docelowa, w której ma zostać przywrócony usunięty plik lub folder.</span><span class="sxs-lookup"><span data-stu-id="f31e0-120">The destination path to where the deleted file or folder should be restored.</span></span> 

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

### <span data-ttu-id="f31e0-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f31e0-121">-Force</span></span>
<span data-ttu-id="f31e0-122">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f31e0-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f31e0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f31e0-123">-PassThru</span></span>
<span data-ttu-id="f31e0-124">Zwraca wartość logiczną PRAWDA po powodzeniu.</span><span class="sxs-lookup"><span data-stu-id="f31e0-124">Return boolean true on success.</span></span>

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

### <span data-ttu-id="f31e0-125">-Path</span><span class="sxs-lookup"><span data-stu-id="f31e0-125">-Path</span></span>
<span data-ttu-id="f31e0-126">Ścieżka usuniętego pliku lub folderu w koszu.</span><span class="sxs-lookup"><span data-stu-id="f31e0-126">The path of the deleted file or folder in trash.</span></span>

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

### <span data-ttu-id="f31e0-127">-RestoreAction</span><span class="sxs-lookup"><span data-stu-id="f31e0-127">-RestoreAction</span></span>
<span data-ttu-id="f31e0-128">Akcja wykonywana w przypadku konfliktów nazw docelowych — "kopia" lub "zastępowanie"</span><span class="sxs-lookup"><span data-stu-id="f31e0-128">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

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

### <span data-ttu-id="f31e0-129">-Type</span><span class="sxs-lookup"><span data-stu-id="f31e0-129">-Type</span></span>
<span data-ttu-id="f31e0-130">Typ przywracanego wpisu — "plik" lub "folder"</span><span class="sxs-lookup"><span data-stu-id="f31e0-130">The type of entry being restored - "file" or "folder"</span></span>

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

### <span data-ttu-id="f31e0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f31e0-131">CommonParameters</span></span>
<span data-ttu-id="f31e0-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f31e0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f31e0-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f31e0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f31e0-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f31e0-134">INPUTS</span></span>

### <span data-ttu-id="f31e0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f31e0-135">System.String</span></span>

## <span data-ttu-id="f31e0-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f31e0-136">OUTPUTS</span></span>

### <span data-ttu-id="f31e0-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f31e0-137">None</span></span>

## <span data-ttu-id="f31e0-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f31e0-138">NOTES</span></span>

## <span data-ttu-id="f31e0-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f31e0-139">RELATED LINKS</span></span>

[<span data-ttu-id="f31e0-140">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="f31e0-140">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)