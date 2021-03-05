---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
ms.openlocfilehash: c3ce4a8051867b535ba2aff4429b5bcfa0b9ab53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010625"
---
# <span data-ttu-id="8f3f3-101">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8f3f3-101">Remove-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="8f3f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f3f3-102">SYNOPSIS</span></span>
<span data-ttu-id="8f3f3-103">Usuwa plik lub folder z magazynu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8f3f3-103">Deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="8f3f3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8f3f3-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f3f3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8f3f3-105">DESCRIPTION</span></span>
<span data-ttu-id="8f3f3-106">Polecenie **cmdlet Remove-AzDataLakeStoreItem** usuwa plik lub folder z magazynu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8f3f3-106">The **Remove-AzDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="8f3f3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8f3f3-107">EXAMPLES</span></span>

### <span data-ttu-id="8f3f3-108">Przykład 1. Usuwanie wielu elementów</span><span class="sxs-lookup"><span data-stu-id="8f3f3-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="8f3f3-109">To polecenie usuwa pliki File01.txt i File.csv z magazynu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8f3f3-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="8f3f3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f3f3-110">PARAMETERS</span></span>

### <span data-ttu-id="8f3f3-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="8f3f3-111">-Account</span></span>
<span data-ttu-id="8f3f3-112">Określa nazwę konta sklepu Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8f3f3-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="8f3f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f3f3-113">-DefaultProfile</span></span>
<span data-ttu-id="8f3f3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8f3f3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f3f3-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="8f3f3-115">-Force</span></span>
<span data-ttu-id="8f3f3-116">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8f3f3-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f3f3-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f3f3-117">-PassThru</span></span>
<span data-ttu-id="8f3f3-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="8f3f3-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8f3f3-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="8f3f3-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f3f3-120">— Ścieżki</span><span class="sxs-lookup"><span data-stu-id="8f3f3-120">-Paths</span></span>
<span data-ttu-id="8f3f3-121">Określa tablicę ścieżek do plików do usunięcia przez magazyn Data Lake Store, zaczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="8f3f3-121">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f3f3-122">- Rekurencie</span><span class="sxs-lookup"><span data-stu-id="8f3f3-122">-Recurse</span></span>
<span data-ttu-id="8f3f3-123">Wskazuje, że ta operacja powoduje usunięcie wszystkich elementów w folderze docelowym, w tym podfolderów.</span><span class="sxs-lookup"><span data-stu-id="8f3f3-123">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f3f3-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8f3f3-124">-Confirm</span></span>
<span data-ttu-id="8f3f3-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8f3f3-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3f3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f3f3-126">-WhatIf</span></span>
<span data-ttu-id="8f3f3-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f3f3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f3f3-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8f3f3-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f3f3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f3f3-129">CommonParameters</span></span>
<span data-ttu-id="8f3f3-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f3f3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f3f3-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f3f3-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f3f3-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f3f3-132">INPUTS</span></span>

### <span data-ttu-id="8f3f3-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8f3f3-133">System.String</span></span>

### <span data-ttu-id="8f3f3-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span><span class="sxs-lookup"><span data-stu-id="8f3f3-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="8f3f3-135">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="8f3f3-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8f3f3-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f3f3-136">OUTPUTS</span></span>

### <span data-ttu-id="8f3f3-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8f3f3-137">System.Boolean</span></span>

## <span data-ttu-id="8f3f3-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8f3f3-138">NOTES</span></span>

## <span data-ttu-id="8f3f3-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f3f3-139">RELATED LINKS</span></span>

[<span data-ttu-id="8f3f3-140">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8f3f3-140">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="8f3f3-141">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8f3f3-141">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="8f3f3-142">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8f3f3-142">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="8f3f3-143">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8f3f3-143">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="8f3f3-144">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8f3f3-144">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="8f3f3-145">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8f3f3-145">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


