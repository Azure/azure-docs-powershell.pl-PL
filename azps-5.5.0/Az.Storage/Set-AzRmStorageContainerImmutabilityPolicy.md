---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 9631855803b4ad16312c907c1d1c747b3aee6fdf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197499"
---
# <span data-ttu-id="61885-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="61885-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="61885-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61885-102">SYNOPSIS</span></span>
<span data-ttu-id="61885-103">Tworzy lub aktualizuje politykę immutability kontenerów obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="61885-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="61885-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="61885-104">SYNTAX</span></span>

### <span data-ttu-id="61885-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="61885-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61885-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="61885-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61885-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="61885-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61885-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="61885-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61885-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="61885-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61885-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="61885-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61885-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="61885-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61885-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="61885-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61885-113">OPIS</span><span class="sxs-lookup"><span data-stu-id="61885-113">DESCRIPTION</span></span>
<span data-ttu-id="61885-114">Polecenie **cmdlet Set-AzRmStorageContainerImmutabilityPolicy** tworzy lub aktualizuje politykę immutability dla kontenerów obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="61885-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="61885-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="61885-115">EXAMPLES</span></span>

### <span data-ttu-id="61885-116">Przykład 1. Tworzenie lub aktualizowanie pola ImmutabilityPolicy kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="61885-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="61885-117">To polecenie tworzy lub aktualizuje politykę immutability dla kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="61885-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="61885-118">Przykład 2. Rozszerzanie właściwości ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem konta magazynu</span><span class="sxs-lookup"><span data-stu-id="61885-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="61885-119">To polecenie rozszerza politykę immutability w kontenerze obiektów blob magazynu z obiektem konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="61885-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="61885-120">Rozszerzenie danych immutabilityPolicy można uruchomić tylko po zablokowaniu komunikacji immutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="61885-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="61885-121">Przykład 3. Aktualizowanie danych immutabilitypolicy kontenera obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="61885-121">Example 3: Update ImmutabilityPolicy of a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -AllowProtectedAppendWrite $true
```

<span data-ttu-id="61885-122">To polecenie aktualizuje 3 razy pole ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem kontenera magazynu: najpierw do właściwości ImmutabilityPeriod 12 dni bez tagu etag, a następnie do właściwości ImmutabilityPeriod 9 dni za pomocą tagu etag, a na koniec do funkcji AllowProtectedAppendWrite.</span><span class="sxs-lookup"><span data-stu-id="61885-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 3 times: First to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag, finally enabled AllowProtectedAppendWrite.</span></span>

### <span data-ttu-id="61885-123">Przykład 4. Rozszerzanie właściwości ImmutabilityPolicy kontenera obiektów blob magazynu za pomocą obiektu ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="61885-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="61885-124">To polecenie rozszerza politykę immutability w kontenerze obiektów blob magazynu przy użyciu obiektu ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="61885-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="61885-125">Rozszerzenie danych immutabilityPolicy można uruchomić tylko po zablokowaniu komunikacji immutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="61885-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="61885-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61885-126">PARAMETERS</span></span>

### <span data-ttu-id="61885-127">-AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="61885-127">-AllowProtectedAppendWrite</span></span>
<span data-ttu-id="61885-128">Tę właściwość można zmienić tylko w przypadku odblokowanych zasad przechowywania opartych na czasie.</span><span class="sxs-lookup"><span data-stu-id="61885-128">This property can only be changed for unlocked time-based retention policies.</span></span> <span data-ttu-id="61885-129">Gdy ta właściwość jest włączona, nowe bloki można zapisywać w obiekcie blob do dołączania przy zachowaniu ochrony i zgodności z możliwością komunikacji.</span><span class="sxs-lookup"><span data-stu-id="61885-129">With this property enabled, new blocks can be written to an append blob while maintaining immutability protection and compliance.</span></span> <span data-ttu-id="61885-130">Można dodawać tylko nowe bloki i nie można modyfikować ani usuwać żadnych istniejących bloków.</span><span class="sxs-lookup"><span data-stu-id="61885-130">Only new blocks can be added and any existing blocks cannot be modified or deleted.</span></span>

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

### <span data-ttu-id="61885-131">— Kontener</span><span class="sxs-lookup"><span data-stu-id="61885-131">-Container</span></span>
<span data-ttu-id="61885-132">Obiekt kontener magazynu</span><span class="sxs-lookup"><span data-stu-id="61885-132">Storage container object</span></span>

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

### <span data-ttu-id="61885-133">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="61885-133">-ContainerName</span></span>
<span data-ttu-id="61885-134">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="61885-134">Container Name</span></span>

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

### <span data-ttu-id="61885-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61885-135">-DefaultProfile</span></span>
<span data-ttu-id="61885-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="61885-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61885-137">— Otagowanie</span><span class="sxs-lookup"><span data-stu-id="61885-137">-Etag</span></span>
<span data-ttu-id="61885-138">Tag etag zasad wiadomości błyskawicznych.</span><span class="sxs-lookup"><span data-stu-id="61885-138">Immutability policy etag.</span></span> <span data-ttu-id="61885-139">Jeśli argument -ExtendPolicy nie jest określony, tag Etag jest opcjonalny. w innym przypadku jest wymagany tag Etag.</span><span class="sxs-lookup"><span data-stu-id="61885-139">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

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

### <span data-ttu-id="61885-140">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="61885-140">-ExtendPolicy</span></span>
<span data-ttu-id="61885-141">Wskaż rozszerzeniePoleci, aby rozszerzyć istniejącą politykę immutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="61885-141">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="61885-142">Po zablokowaniu środowiska ImmutabilityPolicy można ją rozszerzyć.</span><span class="sxs-lookup"><span data-stu-id="61885-142">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

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

### <span data-ttu-id="61885-143">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="61885-143">-ImmutabilityPeriod</span></span>
<span data-ttu-id="61885-144">Okres niemutywności od momentu utworzenia w dniach.</span><span class="sxs-lookup"><span data-stu-id="61885-144">Immutability period since creation in days.</span></span>

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

### <span data-ttu-id="61885-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61885-145">-InputObject</span></span>
<span data-ttu-id="61885-146">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="61885-146">Container Name</span></span>

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

### <span data-ttu-id="61885-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61885-147">-ResourceGroupName</span></span>
<span data-ttu-id="61885-148">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="61885-148">Resource Group Name.</span></span>

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

### <span data-ttu-id="61885-149">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="61885-149">-StorageAccount</span></span>
<span data-ttu-id="61885-150">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="61885-150">Storage account object</span></span>

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

### <span data-ttu-id="61885-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="61885-151">-StorageAccountName</span></span>
<span data-ttu-id="61885-152">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="61885-152">Storage Account Name.</span></span>

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

### <span data-ttu-id="61885-153">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="61885-153">-Confirm</span></span>
<span data-ttu-id="61885-154">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="61885-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61885-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61885-155">-WhatIf</span></span>
<span data-ttu-id="61885-156">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61885-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61885-157">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="61885-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61885-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61885-158">CommonParameters</span></span>
<span data-ttu-id="61885-159">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61885-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61885-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61885-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61885-161">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61885-161">INPUTS</span></span>

### <span data-ttu-id="61885-162">System.String</span><span class="sxs-lookup"><span data-stu-id="61885-162">System.String</span></span>

### <span data-ttu-id="61885-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="61885-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="61885-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="61885-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="61885-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="61885-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="61885-166">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61885-166">OUTPUTS</span></span>

### <span data-ttu-id="61885-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="61885-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="61885-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="61885-168">NOTES</span></span>

## <span data-ttu-id="61885-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61885-169">RELATED LINKS</span></span>
