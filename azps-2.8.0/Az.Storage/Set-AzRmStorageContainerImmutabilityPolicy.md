---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: c216765657cc87c958cc20dd0f2014f0e1c16970
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888261"
---
# <span data-ttu-id="91ed0-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="91ed0-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="91ed0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="91ed0-102">SYNOPSIS</span></span>
<span data-ttu-id="91ed0-103">Tworzy lub aktualizuje ImmutabilityPolicy kontenery blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="91ed0-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="91ed0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="91ed0-104">SYNTAX</span></span>

### <span data-ttu-id="91ed0-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="91ed0-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91ed0-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="91ed0-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91ed0-107">AccountName</span><span class="sxs-lookup"><span data-stu-id="91ed0-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91ed0-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="91ed0-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91ed0-109">Containerobject</span><span class="sxs-lookup"><span data-stu-id="91ed0-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91ed0-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="91ed0-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91ed0-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="91ed0-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91ed0-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="91ed0-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91ed0-113">Opis</span><span class="sxs-lookup"><span data-stu-id="91ed0-113">DESCRIPTION</span></span>
<span data-ttu-id="91ed0-114">Polecenie cmdlet **Set-AzRmStorageContainerImmutabilityPolicy** tworzy lub aktualizuje ImmutabilityPolicy kontenerów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="91ed0-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="91ed0-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="91ed0-115">EXAMPLES</span></span>

### <span data-ttu-id="91ed0-116">Przykład 1: Tworzenie lub aktualizowanie ImmutabilityPolicy kontenera obiektu blob magazynu przy użyciu nazwy konta magazynu i nazwy kontenera</span><span class="sxs-lookup"><span data-stu-id="91ed0-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="91ed0-117">To polecenie umożliwia utworzenie lub zaktualizowanie ImmutabilityPolicy kontenera obiektu BLOB przechowywania z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="91ed0-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="91ed0-118">Przykład 2: rozszerzanie ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem konta magazynu</span><span class="sxs-lookup"><span data-stu-id="91ed0-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="91ed0-119">To polecenie rozszerza ImmutabilityPolicy kontenera obiektu blob magazynu z obiektem konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="91ed0-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="91ed0-120">Rozszerzanie ImmutabilityPolicy może być uruchamiane tylko po zablokowaniu ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="91ed0-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="91ed0-121">Przykład 3: aktualizowanie ImmutabilityPolicyof kontenera obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="91ed0-121">Example 3: Update ImmutabilityPolicyof a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
```

<span data-ttu-id="91ed0-122">To polecenie aktualizuje ImmutabilityPolicy kontenera obiektów blob magazynu za pomocą obiektu kontenera magazynu o wartości 2 razy, a najpierw ImmutabilityPeriod 12 dni bez elementu ETag, a następnie do ImmutabilityPeriod 9 dni przy użyciu elementu ETag.</span><span class="sxs-lookup"><span data-stu-id="91ed0-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 2 times, first to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag.</span></span>

### <span data-ttu-id="91ed0-123">Przykład 4: rozszerzanie ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="91ed0-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="91ed0-124">To polecenie rozszerza ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="91ed0-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="91ed0-125">Rozszerzanie ImmutabilityPolicy może być uruchamiane tylko po zablokowaniu ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="91ed0-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="91ed0-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="91ed0-126">PARAMETERS</span></span>

### <span data-ttu-id="91ed0-127">-Kontener</span><span class="sxs-lookup"><span data-stu-id="91ed0-127">-Container</span></span>
<span data-ttu-id="91ed0-128">Obiekt kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="91ed0-128">Storage container object</span></span>

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

### <span data-ttu-id="91ed0-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="91ed0-129">-ContainerName</span></span>
<span data-ttu-id="91ed0-130">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="91ed0-130">Container Name</span></span>

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

### <span data-ttu-id="91ed0-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91ed0-131">-DefaultProfile</span></span>
<span data-ttu-id="91ed0-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="91ed0-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91ed0-133">-ETag</span><span class="sxs-lookup"><span data-stu-id="91ed0-133">-Etag</span></span>
<span data-ttu-id="91ed0-134">Element ETag zasad Immutability.</span><span class="sxs-lookup"><span data-stu-id="91ed0-134">Immutability policy etag.</span></span> <span data-ttu-id="91ed0-135">Jeśli nie określono parametru-ExtendPolicy, element ETag jest opcjonalny; wymagany jest element ETag.</span><span class="sxs-lookup"><span data-stu-id="91ed0-135">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

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

### <span data-ttu-id="91ed0-136">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="91ed0-136">-ExtendPolicy</span></span>
<span data-ttu-id="91ed0-137">Wskaż ExtendPolicy, aby przedłużyć istniejący ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="91ed0-137">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="91ed0-138">Po zablokowaniu ImmutabilityPolicy można go przedłużyć.</span><span class="sxs-lookup"><span data-stu-id="91ed0-138">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

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

### <span data-ttu-id="91ed0-139">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="91ed0-139">-ImmutabilityPeriod</span></span>
<span data-ttu-id="91ed0-140">Immutability okres od utworzenia w ciągu dni.</span><span class="sxs-lookup"><span data-stu-id="91ed0-140">Immutability period since creation in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ed0-141">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="91ed0-141">-InputObject</span></span>
<span data-ttu-id="91ed0-142">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="91ed0-142">Container Name</span></span>

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

### <span data-ttu-id="91ed0-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91ed0-143">-ResourceGroupName</span></span>
<span data-ttu-id="91ed0-144">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="91ed0-144">Resource Group Name.</span></span>

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

### <span data-ttu-id="91ed0-145">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="91ed0-145">-StorageAccount</span></span>
<span data-ttu-id="91ed0-146">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="91ed0-146">Storage account object</span></span>

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

### <span data-ttu-id="91ed0-147">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="91ed0-147">-StorageAccountName</span></span>
<span data-ttu-id="91ed0-148">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="91ed0-148">Storage Account Name.</span></span>

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

### <span data-ttu-id="91ed0-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="91ed0-149">-Confirm</span></span>
<span data-ttu-id="91ed0-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91ed0-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91ed0-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91ed0-151">-WhatIf</span></span>
<span data-ttu-id="91ed0-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91ed0-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91ed0-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="91ed0-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91ed0-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91ed0-154">CommonParameters</span></span>
<span data-ttu-id="91ed0-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91ed0-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91ed0-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91ed0-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91ed0-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91ed0-157">INPUTS</span></span>

### <span data-ttu-id="91ed0-158">System. String</span><span class="sxs-lookup"><span data-stu-id="91ed0-158">System.String</span></span>

### <span data-ttu-id="91ed0-159">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="91ed0-159">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="91ed0-160">Microsoft. Azure. Commands. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="91ed0-160">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="91ed0-161">Microsoft. Azure. Commands. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="91ed0-161">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="91ed0-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="91ed0-162">OUTPUTS</span></span>

### <span data-ttu-id="91ed0-163">Microsoft. Azure. Commands. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="91ed0-163">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="91ed0-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="91ed0-164">NOTES</span></span>

## <span data-ttu-id="91ed0-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91ed0-165">RELATED LINKS</span></span>
