---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
ms.openlocfilehash: 06bb30dd98c491267675893192f61d4eb61529bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190818"
---
# <span data-ttu-id="f09d4-101">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f09d4-101">Remove-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="f09d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f09d4-102">SYNOPSIS</span></span>
<span data-ttu-id="f09d4-103">Usuwanie pliku lub katalogu.</span><span class="sxs-lookup"><span data-stu-id="f09d4-103">Remove a file or directory.</span></span>

## <span data-ttu-id="f09d4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f09d4-104">SYNTAX</span></span>

### <span data-ttu-id="f09d4-105">ReceiveManual (Default)</span><span class="sxs-lookup"><span data-stu-id="f09d4-105">ReceiveManual (Default)</span></span>
```
Remove-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f09d4-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="f09d4-106">ItemPipeline</span></span>
```
Remove-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f09d4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f09d4-107">DESCRIPTION</span></span>
<span data-ttu-id="f09d4-108">Polecenie **cmdlet Remove-AzDataLakeGen2Item** usuwa plik lub katalog z konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="f09d4-108">The **Remove-AzDataLakeGen2Item** cmdlet removes a file or directory from a Storage account.</span></span>
<span data-ttu-id="f09d4-109">To polecenie cmdlet działa tylko wtedy, gdy dla konta magazynu włączono hierarchiczną przestrzeń nazw.</span><span class="sxs-lookup"><span data-stu-id="f09d4-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="f09d4-110">Tego rodzaju konto można utworzyć, uruchamiam polecenie cmdlet "New-AzStorageAccount" z poleceniem "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="f09d4-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="f09d4-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f09d4-111">EXAMPLES</span></span>

### <span data-ttu-id="f09d4-112">Przykład 1. Usuwanie katalogu</span><span class="sxs-lookup"><span data-stu-id="f09d4-112">Example 1: Removes a directory</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/"
```

<span data-ttu-id="f09d4-113">To polecenie usuwa katalog z systemu plików.</span><span class="sxs-lookup"><span data-stu-id="f09d4-113">This command removes a directory from a Filesystem.</span></span>

### <span data-ttu-id="f09d4-114">Przykład 2. Usuwanie pliku bez monitu</span><span class="sxs-lookup"><span data-stu-id="f09d4-114">Example 2: Removes a file without prompt</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/file1" -Force
```

<span data-ttu-id="f09d4-115">To polecenie usuwa katalog z systemu plików bez monitu.</span><span class="sxs-lookup"><span data-stu-id="f09d4-115">This command removes a directory from a Filesystem, without prompt.</span></span>

### <span data-ttu-id="f09d4-116">Przykład 3. Usuwanie wszystkich elementów w systemie plików z potokiem</span><span class="sxs-lookup"><span data-stu-id="f09d4-116">Example 3: Remove all items in a Filesystem with pipeline</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" | Remove-AzDataLakeGen2Item -Force
```

<span data-ttu-id="f09d4-117">To polecenie usuwa wszystkie elementy w systemie plików z potokiem.</span><span class="sxs-lookup"><span data-stu-id="f09d4-117">This command removes all items in a Filesystem with pipeline.</span></span>

## <span data-ttu-id="f09d4-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f09d4-118">PARAMETERS</span></span>

### <span data-ttu-id="f09d4-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f09d4-119">-AsJob</span></span>
<span data-ttu-id="f09d4-120">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f09d4-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f09d4-121">— kontekst</span><span class="sxs-lookup"><span data-stu-id="f09d4-121">-Context</span></span>
<span data-ttu-id="f09d4-122">Obiekt kontekstowy magazynu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="f09d4-122">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f09d4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f09d4-123">-DefaultProfile</span></span>
<span data-ttu-id="f09d4-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f09d4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f09d4-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="f09d4-125">-FileSystem</span></span>
<span data-ttu-id="f09d4-126">Nazwa systemu plików</span><span class="sxs-lookup"><span data-stu-id="f09d4-126">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f09d4-127">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="f09d4-127">-Force</span></span>
<span data-ttu-id="f09d4-128">Wymuszanie usunięcia systemu plików i całej jego zawartości</span><span class="sxs-lookup"><span data-stu-id="f09d4-128">Force to remove the Filesystem and all content in it</span></span>

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

### <span data-ttu-id="f09d4-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f09d4-129">-InputObject</span></span>
<span data-ttu-id="f09d4-130">Obiekt elementu Platformy Azure Datalake Gen2 do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="f09d4-130">Azure Datalake Gen2 Item Object to remove.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item
Parameter Sets: ItemPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f09d4-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f09d4-131">-PassThru</span></span>
<span data-ttu-id="f09d4-132">Zwracanie, czy określony system plików został pomyślnie usunięty</span><span class="sxs-lookup"><span data-stu-id="f09d4-132">Return whether the specified Filesystem is successfully removed</span></span>

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

### <span data-ttu-id="f09d4-133">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="f09d4-133">-Path</span></span>
<span data-ttu-id="f09d4-134">Ścieżka w określonym systemie plików, która powinna zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="f09d4-134">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="f09d4-135">Może być plikiem lub katalogiem w formacie "katalog/file.txt" lub "katalog1/katalog2/"</span><span class="sxs-lookup"><span data-stu-id="f09d4-135">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f09d4-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f09d4-136">-Confirm</span></span>
<span data-ttu-id="f09d4-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f09d4-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f09d4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f09d4-138">-WhatIf</span></span>
<span data-ttu-id="f09d4-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f09d4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f09d4-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f09d4-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f09d4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f09d4-141">CommonParameters</span></span>
<span data-ttu-id="f09d4-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f09d4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f09d4-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f09d4-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f09d4-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f09d4-144">INPUTS</span></span>

### <span data-ttu-id="f09d4-145">System.String</span><span class="sxs-lookup"><span data-stu-id="f09d4-145">System.String</span></span>

### <span data-ttu-id="f09d4-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f09d4-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="f09d4-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f09d4-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f09d4-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f09d4-148">OUTPUTS</span></span>

### <span data-ttu-id="f09d4-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f09d4-149">System.Boolean</span></span>

## <span data-ttu-id="f09d4-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f09d4-150">NOTES</span></span>

## <span data-ttu-id="f09d4-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f09d4-151">RELATED LINKS</span></span>
