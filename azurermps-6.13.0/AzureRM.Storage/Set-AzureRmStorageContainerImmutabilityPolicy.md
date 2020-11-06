---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/set-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 7717aaa76efba736015a1cf762c95af440b28218
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547303"
---
# <span data-ttu-id="b804a-101">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b804a-101">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="b804a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b804a-102">SYNOPSIS</span></span>
<span data-ttu-id="b804a-103">Tworzy lub aktualizuje ImmutabilityPolicy kontenery blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="b804a-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b804a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b804a-104">SYNTAX</span></span>

### <span data-ttu-id="b804a-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="b804a-105">AccountName (Default)</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> -ImmutabilityPeriod <Int32> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b804a-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="b804a-106">ExtendAccountName</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b804a-107">AccountName</span><span class="sxs-lookup"><span data-stu-id="b804a-107">AccountObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b804a-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="b804a-108">ExtendAccountObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b804a-109">Containerobject</span><span class="sxs-lookup"><span data-stu-id="b804a-109">ContainerObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b804a-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="b804a-110">ExtendContainerObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b804a-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="b804a-111">ImmutabilityPolicyObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b804a-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="b804a-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b804a-113">Opis</span><span class="sxs-lookup"><span data-stu-id="b804a-113">DESCRIPTION</span></span>
<span data-ttu-id="b804a-114">Polecenie cmdlet **Set-AzureRmStorageContainerImmutabilityPolicy** tworzy lub aktualizuje ImmutabilityPolicy kontenerów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="b804a-114">The **Set-AzureRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="b804a-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b804a-115">EXAMPLES</span></span>

### <span data-ttu-id="b804a-116">Przykład 1: Tworzenie lub aktualizowanie ImmutabilityPolicy kontenera obiektu blob magazynu przy użyciu nazwy konta magazynu i nazwy kontenera</span><span class="sxs-lookup"><span data-stu-id="b804a-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10 
```

<span data-ttu-id="b804a-117">To polecenie umożliwia utworzenie lub zaktualizowanie ImmutabilityPolicy kontenera obiektu BLOB przechowywania z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="b804a-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="b804a-118">Przykład 2: rozszerzanie ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem konta magazynu</span><span class="sxs-lookup"><span data-stu-id="b804a-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="b804a-119">To polecenie rozszerza ImmutabilityPolicy kontenera obiektu blob magazynu z obiektem konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b804a-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="b804a-120">Rozszerzanie ImmutabilityPolicy może być uruchamiane tylko po zablokowaniu ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="b804a-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="b804a-121">Przykład 3: aktualizowanie ImmutabilityPolicyof kontenera obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="b804a-121">Example 3: Update ImmutabilityPolicyof a Storage blob container</span></span> 
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
```

<span data-ttu-id="b804a-122">To polecenie aktualizuje ImmutabilityPolicy kontenera obiektów blob magazynu za pomocą obiektu kontenera magazynu o wartości 2 razy, a najpierw ImmutabilityPeriod 12 dni bez elementu ETag, a następnie do ImmutabilityPeriod 9 dni przy użyciu elementu ETag.</span><span class="sxs-lookup"><span data-stu-id="b804a-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 2 times, first to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag.</span></span>

### <span data-ttu-id="b804a-123">Przykład 4: rozszerzanie ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b804a-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzureRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="b804a-124">To polecenie rozszerza ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="b804a-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="b804a-125">Rozszerzanie ImmutabilityPolicy może być uruchamiane tylko po zablokowaniu ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="b804a-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="b804a-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b804a-126">PARAMETERS</span></span>

### <span data-ttu-id="b804a-127">-Kontener</span><span class="sxs-lookup"><span data-stu-id="b804a-127">-Container</span></span>
<span data-ttu-id="b804a-128">Obiekt kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="b804a-128">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject, ExtendContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b804a-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="b804a-129">-ContainerName</span></span>
<span data-ttu-id="b804a-130">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="b804a-130">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, ExtendAccountName, AccountObject, ExtendAccountObject
Aliases: N

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b804a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b804a-131">-DefaultProfile</span></span>
<span data-ttu-id="b804a-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b804a-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b804a-133">-ETag</span><span class="sxs-lookup"><span data-stu-id="b804a-133">-Etag</span></span>
<span data-ttu-id="b804a-134">Element ETag zasad Immutability.</span><span class="sxs-lookup"><span data-stu-id="b804a-134">Immutability policy etag.</span></span> <span data-ttu-id="b804a-135">Jeśli nie określono parametru-ExtendPolicy, element ETag jest opcjonalny; wymagany jest element ETag.</span><span class="sxs-lookup"><span data-stu-id="b804a-135">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b804a-136">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="b804a-136">-ExtendPolicy</span></span>
<span data-ttu-id="b804a-137">Wskaż ExtendPolicy, aby przedłużyć istniejący ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="b804a-137">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="b804a-138">Po zablokowaniu ImmutabilityPolicy można go przedłużyć.</span><span class="sxs-lookup"><span data-stu-id="b804a-138">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

```yaml
Type: SwitchParameter
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b804a-139">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="b804a-139">-ImmutabilityPeriod</span></span>
<span data-ttu-id="b804a-140">Immutability okres od utworzenia w ciągu dni.</span><span class="sxs-lookup"><span data-stu-id="b804a-140">Immutability period since creation in days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b804a-141">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b804a-141">-InputObject</span></span>
<span data-ttu-id="b804a-142">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="b804a-142">Container Name</span></span>

```yaml
Type: PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b804a-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b804a-143">-ResourceGroupName</span></span>
<span data-ttu-id="b804a-144">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b804a-144">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, ExtendAccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b804a-145">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b804a-145">-StorageAccount</span></span>
<span data-ttu-id="b804a-146">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="b804a-146">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject, ExtendAccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b804a-147">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b804a-147">-StorageAccountName</span></span>
<span data-ttu-id="b804a-148">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="b804a-148">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, ExtendAccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b804a-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b804a-149">-Confirm</span></span>
<span data-ttu-id="b804a-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b804a-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b804a-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b804a-151">-WhatIf</span></span>
<span data-ttu-id="b804a-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b804a-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b804a-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b804a-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b804a-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b804a-154">CommonParameters</span></span>
<span data-ttu-id="b804a-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b804a-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b804a-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b804a-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b804a-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b804a-157">INPUTS</span></span>

### <span data-ttu-id="b804a-158">System. String</span><span class="sxs-lookup"><span data-stu-id="b804a-158">System.String</span></span>
<span data-ttu-id="b804a-159">Microsoft. Azure. Commands. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b804a-159">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="b804a-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b804a-160">OUTPUTS</span></span>

### <span data-ttu-id="b804a-161">Microsoft. Azure. Commands. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b804a-161">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="b804a-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b804a-162">NOTES</span></span>

## <span data-ttu-id="b804a-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b804a-163">RELATED LINKS</span></span>

