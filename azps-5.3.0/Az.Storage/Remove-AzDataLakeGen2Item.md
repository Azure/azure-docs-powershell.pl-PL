---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
ms.openlocfilehash: 06bb30dd98c491267675893192f61d4eb61529bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502712"
---
# <span data-ttu-id="34bb3-101">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="34bb3-101">Remove-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="34bb3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34bb3-102">SYNOPSIS</span></span>
<span data-ttu-id="34bb3-103">Usuwanie pliku lub katalogu.</span><span class="sxs-lookup"><span data-stu-id="34bb3-103">Remove a file or directory.</span></span>

## <span data-ttu-id="34bb3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34bb3-104">SYNTAX</span></span>

### <span data-ttu-id="34bb3-105">ReceiveManual (domyślny)</span><span class="sxs-lookup"><span data-stu-id="34bb3-105">ReceiveManual (Default)</span></span>
```
Remove-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34bb3-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="34bb3-106">ItemPipeline</span></span>
```
Remove-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34bb3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="34bb3-107">DESCRIPTION</span></span>
<span data-ttu-id="34bb3-108">Polecenie cmdlet **Remove-AzDataLakeGen2Item** usuwa plik lub katalog z konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="34bb3-108">The **Remove-AzDataLakeGen2Item** cmdlet removes a file or directory from a Storage account.</span></span>
<span data-ttu-id="34bb3-109">To polecenie cmdlet działa tylko wtedy, gdy dla konta magazynu jest włączone hierarchiczne obszary nazw.</span><span class="sxs-lookup"><span data-stu-id="34bb3-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="34bb3-110">Ten rodzaj konta można utworzyć, uruchamiając polecenie cmdlet "New-AzStorageAccount" z opcją "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="34bb3-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="34bb3-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34bb3-111">EXAMPLES</span></span>

### <span data-ttu-id="34bb3-112">Przykład 1. Usuwa katalog</span><span class="sxs-lookup"><span data-stu-id="34bb3-112">Example 1: Removes a directory</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/"
```

<span data-ttu-id="34bb3-113">To polecenie usuwa katalog z systemu plików.</span><span class="sxs-lookup"><span data-stu-id="34bb3-113">This command removes a directory from a Filesystem.</span></span>

### <span data-ttu-id="34bb3-114">Przykład 2: usuwa plik bez monitu</span><span class="sxs-lookup"><span data-stu-id="34bb3-114">Example 2: Removes a file without prompt</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/file1" -Force
```

<span data-ttu-id="34bb3-115">To polecenie usuwa katalog z systemu plików bez monitowania.</span><span class="sxs-lookup"><span data-stu-id="34bb3-115">This command removes a directory from a Filesystem, without prompt.</span></span>

### <span data-ttu-id="34bb3-116">Przykład 3: Usuwanie wszystkich elementów w systemie plików z potokiem</span><span class="sxs-lookup"><span data-stu-id="34bb3-116">Example 3: Remove all items in a Filesystem with pipeline</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" | Remove-AzDataLakeGen2Item -Force
```

<span data-ttu-id="34bb3-117">To polecenie usuwa wszystkie elementy z systemu plików z potokiem.</span><span class="sxs-lookup"><span data-stu-id="34bb3-117">This command removes all items in a Filesystem with pipeline.</span></span>

## <span data-ttu-id="34bb3-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34bb3-118">PARAMETERS</span></span>

### <span data-ttu-id="34bb3-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34bb3-119">-AsJob</span></span>
<span data-ttu-id="34bb3-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="34bb3-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34bb3-121">-Context</span><span class="sxs-lookup"><span data-stu-id="34bb3-121">-Context</span></span>
<span data-ttu-id="34bb3-122">Obiekt kontekstu usługi Azure Storage</span><span class="sxs-lookup"><span data-stu-id="34bb3-122">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="34bb3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34bb3-123">-DefaultProfile</span></span>
<span data-ttu-id="34bb3-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="34bb3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34bb3-125">— System plików</span><span class="sxs-lookup"><span data-stu-id="34bb3-125">-FileSystem</span></span>
<span data-ttu-id="34bb3-126">Nazwa systemu plików</span><span class="sxs-lookup"><span data-stu-id="34bb3-126">FileSystem name</span></span>

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

### <span data-ttu-id="34bb3-127">-Force</span><span class="sxs-lookup"><span data-stu-id="34bb3-127">-Force</span></span>
<span data-ttu-id="34bb3-128">Wymuś usunięcie systemu plików i całej zawartości</span><span class="sxs-lookup"><span data-stu-id="34bb3-128">Force to remove the Filesystem and all content in it</span></span>

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

### <span data-ttu-id="34bb3-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="34bb3-129">-InputObject</span></span>
<span data-ttu-id="34bb3-130">Obiekt usługi Azure datalake Gen2, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="34bb3-130">Azure Datalake Gen2 Item Object to remove.</span></span>

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

### <span data-ttu-id="34bb3-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34bb3-131">-PassThru</span></span>
<span data-ttu-id="34bb3-132">Zwracanie, czy określony system plików został pomyślnie usunięty</span><span class="sxs-lookup"><span data-stu-id="34bb3-132">Return whether the specified Filesystem is successfully removed</span></span>

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

### <span data-ttu-id="34bb3-133">-Path</span><span class="sxs-lookup"><span data-stu-id="34bb3-133">-Path</span></span>
<span data-ttu-id="34bb3-134">Ścieżka w określonym systemie plików, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="34bb3-134">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="34bb3-135">Może to być plik lub katalog w formacie "Directory/file.txt" lub "directory1/Directory2/"</span><span class="sxs-lookup"><span data-stu-id="34bb3-135">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="34bb3-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34bb3-136">-Confirm</span></span>
<span data-ttu-id="34bb3-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34bb3-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34bb3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34bb3-138">-WhatIf</span></span>
<span data-ttu-id="34bb3-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34bb3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34bb3-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="34bb3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34bb3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34bb3-141">CommonParameters</span></span>
<span data-ttu-id="34bb3-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34bb3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34bb3-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34bb3-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34bb3-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34bb3-144">INPUTS</span></span>

### <span data-ttu-id="34bb3-145">System. String</span><span class="sxs-lookup"><span data-stu-id="34bb3-145">System.String</span></span>

### <span data-ttu-id="34bb3-146">Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="34bb3-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="34bb3-147">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="34bb3-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="34bb3-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34bb3-148">OUTPUTS</span></span>

### <span data-ttu-id="34bb3-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="34bb3-149">System.Boolean</span></span>

## <span data-ttu-id="34bb3-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34bb3-150">NOTES</span></span>

## <span data-ttu-id="34bb3-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34bb3-151">RELATED LINKS</span></span>
