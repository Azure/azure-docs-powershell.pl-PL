---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: d94b84455f18a2823612ae1592e9cb337a4be3c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970154"
---
# <span data-ttu-id="1e042-101">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1e042-101">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="1e042-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e042-102">SYNOPSIS</span></span>
<span data-ttu-id="1e042-103">Usuwa zasady immutabilitypolicy z kontenera obiektów blob magazynu z odblokowanych zasad</span><span class="sxs-lookup"><span data-stu-id="1e042-103">Removes ImmutabilityPolicy of a Storage blob container with an unlocked policy</span></span>

## <span data-ttu-id="1e042-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1e042-104">SYNTAX</span></span>

### <span data-ttu-id="1e042-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="1e042-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e042-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="1e042-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e042-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="1e042-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e042-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="1e042-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e042-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="1e042-109">DESCRIPTION</span></span>
<span data-ttu-id="1e042-110">Polecenie **cmdlet Remove-AzRmStorageContainerImmutabilityPolicy** usuwa zasady ImmutabilityPolicy z kontenera obiektów blob magazynu z odblokowanych zasad.</span><span class="sxs-lookup"><span data-stu-id="1e042-110">The **Remove-AzRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob container with an unlocked policy.</span></span>

## <span data-ttu-id="1e042-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1e042-111">EXAMPLES</span></span>

### <span data-ttu-id="1e042-112">Przykład 1. Usunięcie odblokowanego środowiska ImmutabilityPolicy z kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="1e042-112">Example 1: Remove unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="1e042-113">To polecenie usuwa odblokowaną politykę immutability z kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="1e042-113">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="1e042-114">Przykład 2. Usunięcie odblokowanego środowiska ImmutabilityPolicy z kontenera obiektów blob magazynu z obiektem konta magazynu</span><span class="sxs-lookup"><span data-stu-id="1e042-114">Example 2: Remove unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="1e042-115">To polecenie usuwa odblokowaną politykę immutability z kontenera obiektów blob magazynu z obiektem konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="1e042-115">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="1e042-116">Przykład 3. Usunięcie odblokowanego środowiska ImmutabilityPolicy z kontenera obiektów blob magazynu z obiektem kontenerowym</span><span class="sxs-lookup"><span data-stu-id="1e042-116">Example 3: Remove unlocked ImmutabilityPolicy of a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="1e042-117">To polecenie usuwa odblokowaną politykę immutability z kontenera obiektów blob magazynu z obiektem kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="1e042-117">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="1e042-118">Przykład 4. Usunięcie odblokowanego środowiska ImmutabilityPolicy z kontenera obiektów blob magazynu z obiektem ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1e042-118">Example 4: Remove unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="1e042-119">To polecenie usuwa odblokowaną politykę immutability z kontenera obiektów blob magazynu z obiektem ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="1e042-119">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="1e042-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e042-120">PARAMETERS</span></span>

### <span data-ttu-id="1e042-121">— Kontener</span><span class="sxs-lookup"><span data-stu-id="1e042-121">-Container</span></span>
<span data-ttu-id="1e042-122">Obiekt kontener magazynu</span><span class="sxs-lookup"><span data-stu-id="1e042-122">Storage container object</span></span>

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

### <span data-ttu-id="1e042-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="1e042-123">-ContainerName</span></span>
<span data-ttu-id="1e042-124">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="1e042-124">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e042-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e042-125">-DefaultProfile</span></span>
<span data-ttu-id="1e042-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1e042-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e042-127">— Otagowanie</span><span class="sxs-lookup"><span data-stu-id="1e042-127">-Etag</span></span>
<span data-ttu-id="1e042-128">Tag etag zasad wiadomości błyskawicznych.</span><span class="sxs-lookup"><span data-stu-id="1e042-128">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e042-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e042-129">-InputObject</span></span>
<span data-ttu-id="1e042-130">Odblokowany obiekt ImmutabilityPolicy do usunięcia</span><span class="sxs-lookup"><span data-stu-id="1e042-130">Unlocked ImmutabilityPolicy Object to Remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e042-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e042-131">-ResourceGroupName</span></span>
<span data-ttu-id="1e042-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1e042-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="1e042-133">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e042-133">-StorageAccount</span></span>
<span data-ttu-id="1e042-134">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="1e042-134">Storage account object</span></span>

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

### <span data-ttu-id="1e042-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1e042-135">-StorageAccountName</span></span>
<span data-ttu-id="1e042-136">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="1e042-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="1e042-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1e042-137">-Confirm</span></span>
<span data-ttu-id="1e042-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1e042-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e042-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e042-139">-WhatIf</span></span>
<span data-ttu-id="1e042-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e042-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e042-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1e042-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e042-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e042-142">CommonParameters</span></span>
<span data-ttu-id="1e042-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e042-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e042-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e042-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e042-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e042-145">INPUTS</span></span>

### <span data-ttu-id="1e042-146">System.String</span><span class="sxs-lookup"><span data-stu-id="1e042-146">System.String</span></span>

### <span data-ttu-id="1e042-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1e042-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="1e042-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="1e042-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="1e042-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1e042-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="1e042-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e042-150">OUTPUTS</span></span>

### <span data-ttu-id="1e042-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1e042-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="1e042-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1e042-152">NOTES</span></span>

## <span data-ttu-id="1e042-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e042-153">RELATED LINKS</span></span>
