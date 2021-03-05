---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 81db149500ce489801a25437fbb7a50443d7426a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974170"
---
# <span data-ttu-id="498c0-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="498c0-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="498c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="498c0-102">SYNOPSIS</span></span>
<span data-ttu-id="498c0-103">Tworzy lub aktualizuje politykę immutability kontenerów obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="498c0-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="498c0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="498c0-104">SYNTAX</span></span>

### <span data-ttu-id="498c0-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="498c0-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="498c0-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="498c0-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="498c0-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="498c0-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="498c0-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="498c0-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="498c0-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="498c0-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="498c0-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="498c0-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="498c0-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="498c0-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="498c0-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="498c0-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="498c0-113">OPIS</span><span class="sxs-lookup"><span data-stu-id="498c0-113">DESCRIPTION</span></span>
<span data-ttu-id="498c0-114">Polecenie **cmdlet Set-AzRmStorageContainerImmutabilityPolicy** tworzy lub aktualizuje politykę immutability dla kontenerów obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="498c0-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="498c0-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="498c0-115">EXAMPLES</span></span>

### <span data-ttu-id="498c0-116">Przykład 1. Tworzenie lub aktualizowanie pola ImmutabilityPolicy kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="498c0-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="498c0-117">To polecenie tworzy lub aktualizuje politykę immutability dla kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="498c0-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="498c0-118">Przykład 2. Rozszerzanie właściwości ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem konta magazynu</span><span class="sxs-lookup"><span data-stu-id="498c0-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="498c0-119">To polecenie rozszerza pole "ImmutabilityPolicy" kontenera obiektów blob magazynu z obiektem konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="498c0-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="498c0-120">Rozszerzenie danych immutabilityPolicy można uruchomić tylko po zablokowaniu komunikacji immutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="498c0-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="498c0-121">Przykład 3. Aktualizowanie danych immutabilitypolicy kontenera obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="498c0-121">Example 3: Update ImmutabilityPolicy of a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -AllowProtectedAppendWrite $true
```

<span data-ttu-id="498c0-122">To polecenie aktualizuje 3 razy pole ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem kontenera magazynu: najpierw do właściwości ImmutabilityPeriod 12 dni bez tagu etag, a następnie do właściwości ImmutabilityPeriod 9 dni za pomocą tagu etag, a na koniec do funkcji AllowProtectedAppendWrite.</span><span class="sxs-lookup"><span data-stu-id="498c0-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 3 times: First to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag, finally enabled AllowProtectedAppendWrite.</span></span>

### <span data-ttu-id="498c0-123">Przykład 4. Rozszerzanie właściwości ImmutabilityPolicy kontenera obiektów blob magazynu przy użyciu obiektu ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="498c0-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="498c0-124">To polecenie rozszerza politykę immutability dla kontenera obiektów blob magazynu przy użyciu obiektu ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="498c0-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="498c0-125">Rozszerzenie danych immutabilityPolicy można uruchomić tylko po zablokowaniu komunikacji immutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="498c0-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="498c0-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="498c0-126">PARAMETERS</span></span>

### <span data-ttu-id="498c0-127">-AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="498c0-127">-AllowProtectedAppendWrite</span></span>
<span data-ttu-id="498c0-128">Tę właściwość można zmienić tylko w przypadku odblokowanych zasad przechowywania opartych na czasie.</span><span class="sxs-lookup"><span data-stu-id="498c0-128">This property can only be changed for unlocked time-based retention policies.</span></span> <span data-ttu-id="498c0-129">Gdy ta właściwość jest włączona, nowe bloki można zapisywać w obiekcie blob dołączania przy zachowaniu ochrony i zgodności z możliwością komunikacji.</span><span class="sxs-lookup"><span data-stu-id="498c0-129">With this property enabled, new blocks can be written to an append blob while maintaining immutability protection and compliance.</span></span> <span data-ttu-id="498c0-130">Można dodawać tylko nowe bloki i nie można modyfikować ani usuwać żadnych istniejących bloków.</span><span class="sxs-lookup"><span data-stu-id="498c0-130">Only new blocks can be added and any existing blocks cannot be modified or deleted.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AccountName, AccountObject, ContainerObject, ImmutabilityPolicyObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="498c0-131">— Kontener</span><span class="sxs-lookup"><span data-stu-id="498c0-131">-Container</span></span>
<span data-ttu-id="498c0-132">Obiekt kontener magazynu</span><span class="sxs-lookup"><span data-stu-id="498c0-132">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject, ExtendContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="498c0-133">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="498c0-133">-ContainerName</span></span>
<span data-ttu-id="498c0-134">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="498c0-134">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName, AccountObject, ExtendAccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="498c0-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="498c0-135">-DefaultProfile</span></span>
<span data-ttu-id="498c0-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="498c0-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="498c0-137">— Otagowanie</span><span class="sxs-lookup"><span data-stu-id="498c0-137">-Etag</span></span>
<span data-ttu-id="498c0-138">Tag etag zasad wiadomości błyskawicznych.</span><span class="sxs-lookup"><span data-stu-id="498c0-138">Immutability policy etag.</span></span> <span data-ttu-id="498c0-139">Jeśli argument -ExtendPolicy nie jest określony, tag Etag jest opcjonalny. w innym przypadku jest wymagany tag Etag.</span><span class="sxs-lookup"><span data-stu-id="498c0-139">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="498c0-140">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="498c0-140">-ExtendPolicy</span></span>
<span data-ttu-id="498c0-141">Wskaż rozszerzeniePoleci, aby rozszerzyć istniejącą politykę immutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="498c0-141">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="498c0-142">Po zablokowaniu środowiska ImmutabilityPolicy można ją rozszerzyć.</span><span class="sxs-lookup"><span data-stu-id="498c0-142">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="498c0-143">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="498c0-143">-ImmutabilityPeriod</span></span>
<span data-ttu-id="498c0-144">Okres niemutywności od momentu utworzenia w dniach.</span><span class="sxs-lookup"><span data-stu-id="498c0-144">Immutability period since creation in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: AccountName, AccountObject, ContainerObject, ImmutabilityPolicyObject
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="498c0-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="498c0-145">-InputObject</span></span>
<span data-ttu-id="498c0-146">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="498c0-146">Container Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="498c0-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="498c0-147">-ResourceGroupName</span></span>
<span data-ttu-id="498c0-148">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="498c0-148">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="498c0-149">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="498c0-149">-StorageAccount</span></span>
<span data-ttu-id="498c0-150">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="498c0-150">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, ExtendAccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="498c0-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="498c0-151">-StorageAccountName</span></span>
<span data-ttu-id="498c0-152">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="498c0-152">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="498c0-153">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="498c0-153">-Confirm</span></span>
<span data-ttu-id="498c0-154">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="498c0-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="498c0-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="498c0-155">-WhatIf</span></span>
<span data-ttu-id="498c0-156">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="498c0-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="498c0-157">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="498c0-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="498c0-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="498c0-158">CommonParameters</span></span>
<span data-ttu-id="498c0-159">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="498c0-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="498c0-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="498c0-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="498c0-161">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="498c0-161">INPUTS</span></span>

### <span data-ttu-id="498c0-162">System.String</span><span class="sxs-lookup"><span data-stu-id="498c0-162">System.String</span></span>

### <span data-ttu-id="498c0-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="498c0-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="498c0-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="498c0-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="498c0-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="498c0-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="498c0-166">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="498c0-166">OUTPUTS</span></span>

### <span data-ttu-id="498c0-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="498c0-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="498c0-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="498c0-168">NOTES</span></span>

## <span data-ttu-id="498c0-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="498c0-169">RELATED LINKS</span></span>
