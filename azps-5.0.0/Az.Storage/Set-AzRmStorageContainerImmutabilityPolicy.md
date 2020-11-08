---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 9631855803b4ad16312c907c1d1c747b3aee6fdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224748"
---
# <span data-ttu-id="74aaa-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="74aaa-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="74aaa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="74aaa-102">SYNOPSIS</span></span>
<span data-ttu-id="74aaa-103">Tworzy lub aktualizuje ImmutabilityPolicy kontenery blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="74aaa-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="74aaa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="74aaa-104">SYNTAX</span></span>

### <span data-ttu-id="74aaa-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="74aaa-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74aaa-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="74aaa-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74aaa-107">AccountName</span><span class="sxs-lookup"><span data-stu-id="74aaa-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74aaa-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="74aaa-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74aaa-109">Containerobject</span><span class="sxs-lookup"><span data-stu-id="74aaa-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74aaa-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="74aaa-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74aaa-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="74aaa-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74aaa-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="74aaa-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74aaa-113">Opis</span><span class="sxs-lookup"><span data-stu-id="74aaa-113">DESCRIPTION</span></span>
<span data-ttu-id="74aaa-114">Polecenie cmdlet **Set-AzRmStorageContainerImmutabilityPolicy** tworzy lub aktualizuje ImmutabilityPolicy kontenerów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="74aaa-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="74aaa-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="74aaa-115">EXAMPLES</span></span>

### <span data-ttu-id="74aaa-116">Przykład 1: Tworzenie lub aktualizowanie ImmutabilityPolicy kontenera obiektu blob magazynu przy użyciu nazwy konta magazynu i nazwy kontenera</span><span class="sxs-lookup"><span data-stu-id="74aaa-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="74aaa-117">To polecenie umożliwia utworzenie lub zaktualizowanie ImmutabilityPolicy kontenera obiektu BLOB przechowywania z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="74aaa-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="74aaa-118">Przykład 2: rozszerzanie ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem konta magazynu</span><span class="sxs-lookup"><span data-stu-id="74aaa-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="74aaa-119">To polecenie rozszerza ImmutabilityPolicy kontenera obiektu blob magazynu z obiektem konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="74aaa-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="74aaa-120">Rozszerzanie ImmutabilityPolicy może być uruchamiane tylko po zablokowaniu ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="74aaa-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="74aaa-121">Przykład 3: aktualizowanie ImmutabilityPolicy kontenera obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="74aaa-121">Example 3: Update ImmutabilityPolicy of a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -AllowProtectedAppendWrite $true
```

<span data-ttu-id="74aaa-122">To polecenie aktualizuje ImmutabilityPolicy kontenera obiektów blob magazynu za pomocą obiektu kontenera magazynu o wartości 3 razy: najpierw ImmutabilityPeriod 12 dni bez elementu ETag, a następnie do ImmutabilityPeriod 9 dni przy użyciu elementu ETag, na koniec włączono AllowProtectedAppendWrite.</span><span class="sxs-lookup"><span data-stu-id="74aaa-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 3 times: First to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag, finally enabled AllowProtectedAppendWrite.</span></span>

### <span data-ttu-id="74aaa-123">Przykład 4: rozszerzanie ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="74aaa-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="74aaa-124">To polecenie rozszerza ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="74aaa-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="74aaa-125">Rozszerzanie ImmutabilityPolicy może być uruchamiane tylko po zablokowaniu ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="74aaa-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="74aaa-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74aaa-126">PARAMETERS</span></span>

### <span data-ttu-id="74aaa-127">-AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="74aaa-127">-AllowProtectedAppendWrite</span></span>
<span data-ttu-id="74aaa-128">Tę właściwość można zmienić tylko dla odblokowanych zasad przechowywania opartych na czasie.</span><span class="sxs-lookup"><span data-stu-id="74aaa-128">This property can only be changed for unlocked time-based retention policies.</span></span> <span data-ttu-id="74aaa-129">Po włączeniu tej właściwości nowe bloki można zapisywać w obiekcie blob dołączania, zachowując ochronę Immutability i zgodność.</span><span class="sxs-lookup"><span data-stu-id="74aaa-129">With this property enabled, new blocks can be written to an append blob while maintaining immutability protection and compliance.</span></span> <span data-ttu-id="74aaa-130">Można dodawać tylko nowe bloki i żadne istniejące bloki nie mogą być modyfikowane ani usuwane.</span><span class="sxs-lookup"><span data-stu-id="74aaa-130">Only new blocks can be added and any existing blocks cannot be modified or deleted.</span></span>

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

### <span data-ttu-id="74aaa-131">-Kontener</span><span class="sxs-lookup"><span data-stu-id="74aaa-131">-Container</span></span>
<span data-ttu-id="74aaa-132">Obiekt kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="74aaa-132">Storage container object</span></span>

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

### <span data-ttu-id="74aaa-133">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="74aaa-133">-ContainerName</span></span>
<span data-ttu-id="74aaa-134">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="74aaa-134">Container Name</span></span>

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

### <span data-ttu-id="74aaa-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74aaa-135">-DefaultProfile</span></span>
<span data-ttu-id="74aaa-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="74aaa-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74aaa-137">-ETag</span><span class="sxs-lookup"><span data-stu-id="74aaa-137">-Etag</span></span>
<span data-ttu-id="74aaa-138">Element ETag zasad Immutability.</span><span class="sxs-lookup"><span data-stu-id="74aaa-138">Immutability policy etag.</span></span> <span data-ttu-id="74aaa-139">Jeśli nie określono parametru-ExtendPolicy, element ETag jest opcjonalny; wymagany jest element ETag.</span><span class="sxs-lookup"><span data-stu-id="74aaa-139">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

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

### <span data-ttu-id="74aaa-140">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="74aaa-140">-ExtendPolicy</span></span>
<span data-ttu-id="74aaa-141">Wskaż ExtendPolicy, aby przedłużyć istniejący ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="74aaa-141">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="74aaa-142">Po zablokowaniu ImmutabilityPolicy można go przedłużyć.</span><span class="sxs-lookup"><span data-stu-id="74aaa-142">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

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

### <span data-ttu-id="74aaa-143">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="74aaa-143">-ImmutabilityPeriod</span></span>
<span data-ttu-id="74aaa-144">Immutability okres od utworzenia w ciągu dni.</span><span class="sxs-lookup"><span data-stu-id="74aaa-144">Immutability period since creation in days.</span></span>

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

### <span data-ttu-id="74aaa-145">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="74aaa-145">-InputObject</span></span>
<span data-ttu-id="74aaa-146">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="74aaa-146">Container Name</span></span>

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

### <span data-ttu-id="74aaa-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74aaa-147">-ResourceGroupName</span></span>
<span data-ttu-id="74aaa-148">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="74aaa-148">Resource Group Name.</span></span>

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

### <span data-ttu-id="74aaa-149">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="74aaa-149">-StorageAccount</span></span>
<span data-ttu-id="74aaa-150">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="74aaa-150">Storage account object</span></span>

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

### <span data-ttu-id="74aaa-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="74aaa-151">-StorageAccountName</span></span>
<span data-ttu-id="74aaa-152">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="74aaa-152">Storage Account Name.</span></span>

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

### <span data-ttu-id="74aaa-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74aaa-153">-Confirm</span></span>
<span data-ttu-id="74aaa-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74aaa-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74aaa-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74aaa-155">-WhatIf</span></span>
<span data-ttu-id="74aaa-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74aaa-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74aaa-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="74aaa-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74aaa-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74aaa-158">CommonParameters</span></span>
<span data-ttu-id="74aaa-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74aaa-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74aaa-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74aaa-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74aaa-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74aaa-161">INPUTS</span></span>

### <span data-ttu-id="74aaa-162">System. String</span><span class="sxs-lookup"><span data-stu-id="74aaa-162">System.String</span></span>

### <span data-ttu-id="74aaa-163">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="74aaa-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="74aaa-164">Microsoft. Azure. Commands. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="74aaa-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="74aaa-165">Microsoft. Azure. Commands. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="74aaa-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="74aaa-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="74aaa-166">OUTPUTS</span></span>

### <span data-ttu-id="74aaa-167">Microsoft. Azure. Commands. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="74aaa-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="74aaa-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="74aaa-168">NOTES</span></span>

## <span data-ttu-id="74aaa-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74aaa-169">RELATED LINKS</span></span>
