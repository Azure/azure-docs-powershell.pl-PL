---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 494995a97ccb74df9ad9a9fc1f88272505598bb9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190794"
---
# <span data-ttu-id="9dca9-101">Remove-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="9dca9-101">Remove-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="9dca9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dca9-102">SYNOPSIS</span></span>
<span data-ttu-id="9dca9-103">Usuwa tagi przechowywania prawnego z kontenera obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="9dca9-103">Removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="9dca9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9dca9-104">SYNTAX</span></span>

### <span data-ttu-id="9dca9-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="9dca9-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9dca9-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="9dca9-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9dca9-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="9dca9-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dca9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9dca9-108">DESCRIPTION</span></span>
<span data-ttu-id="9dca9-109">Polecenie **cmdlet Remove-AzRmStorageContainerLegalHold** usuwa tagi przechowywania prawnego z kontenera obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="9dca9-109">The **Remove-AzRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="9dca9-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9dca9-110">EXAMPLES</span></span>

### <span data-ttu-id="9dca9-111">Przykład 1. Usuwanie tagów prawnych hold z kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="9dca9-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="9dca9-112">To polecenie usuwa tagi przechowywania prawnego z kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="9dca9-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="9dca9-113">Przykład 2. Usuwanie tagów prawnych hold z kontenera obiektów blob magazynu z obiektem konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="9dca9-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2
```

<span data-ttu-id="9dca9-114">To polecenie usuwa tagi przechowywania prawnego z kontenera obiektów blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="9dca9-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="9dca9-115">Przykład 3. Usuwanie tagów zdjęć ze wszystkich kontenerów obiektów blob magazynu na koncie magazynu z potokiem</span><span class="sxs-lookup"><span data-stu-id="9dca9-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="9dca9-116">To polecenie usuwa tagi przechowywania ze wszystkich kontenerów obiektów blob magazynu na koncie magazynu z potokiem.</span><span class="sxs-lookup"><span data-stu-id="9dca9-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="9dca9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9dca9-117">PARAMETERS</span></span>

### <span data-ttu-id="9dca9-118">— Kontener</span><span class="sxs-lookup"><span data-stu-id="9dca9-118">-Container</span></span>
<span data-ttu-id="9dca9-119">Obiekt kontener magazynu</span><span class="sxs-lookup"><span data-stu-id="9dca9-119">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9dca9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dca9-120">-DefaultProfile</span></span>
<span data-ttu-id="9dca9-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9dca9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9dca9-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9dca9-122">-Name</span></span>
<span data-ttu-id="9dca9-123">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="9dca9-123">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9dca9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dca9-124">-ResourceGroupName</span></span>
<span data-ttu-id="9dca9-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9dca9-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dca9-126">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="9dca9-126">-StorageAccount</span></span>
<span data-ttu-id="9dca9-127">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="9dca9-127">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9dca9-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9dca9-128">-StorageAccountName</span></span>
<span data-ttu-id="9dca9-129">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="9dca9-129">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dca9-130">— Tag</span><span class="sxs-lookup"><span data-stu-id="9dca9-130">-Tag</span></span>
<span data-ttu-id="9dca9-131">Container LegalHold Tags</span><span class="sxs-lookup"><span data-stu-id="9dca9-131">Container LegalHold Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dca9-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9dca9-132">-Confirm</span></span>
<span data-ttu-id="9dca9-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9dca9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dca9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dca9-134">-WhatIf</span></span>
<span data-ttu-id="9dca9-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dca9-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9dca9-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9dca9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dca9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dca9-137">CommonParameters</span></span>
<span data-ttu-id="9dca9-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dca9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dca9-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dca9-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dca9-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9dca9-140">INPUTS</span></span>

### <span data-ttu-id="9dca9-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9dca9-141">System.String</span></span>

### <span data-ttu-id="9dca9-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9dca9-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="9dca9-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="9dca9-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="9dca9-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9dca9-144">OUTPUTS</span></span>

### <span data-ttu-id="9dca9-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="9dca9-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="9dca9-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9dca9-146">NOTES</span></span>

## <span data-ttu-id="9dca9-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9dca9-147">RELATED LINKS</span></span>
