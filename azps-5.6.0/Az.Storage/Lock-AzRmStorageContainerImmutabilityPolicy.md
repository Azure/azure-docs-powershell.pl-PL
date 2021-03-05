---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/lock-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 44d0f6b9717e51aec508da76a9ef9b776891d8c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994764"
---
# <span data-ttu-id="90a7e-101">Lock-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="90a7e-101">Lock-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="90a7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90a7e-102">SYNOPSIS</span></span>
<span data-ttu-id="90a7e-103">Blokuje politykę przydatności do wiadomości dla kontenerów obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="90a7e-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="90a7e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="90a7e-104">SYNTAX</span></span>

### <span data-ttu-id="90a7e-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="90a7e-105">AccountName (Default)</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90a7e-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="90a7e-106">AccountObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90a7e-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="90a7e-107">ContainerObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90a7e-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="90a7e-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90a7e-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="90a7e-109">DESCRIPTION</span></span>
<span data-ttu-id="90a7e-110">Polecenie **cmdlet Lock-AzRmStorageContainerImmutabilityPolicy** blokuje obiekt ImmutabilityPolicy kontenerów obiektów blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="90a7e-110">The **Lock-AzRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="90a7e-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="90a7e-111">EXAMPLES</span></span>

### <span data-ttu-id="90a7e-112">Przykład 1. Blokowanie wiadomości błyskawicznychPolicy kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="90a7e-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="90a7e-113">To polecenie blokuje politykę immutability dla kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="90a7e-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="90a7e-114">Przykład 2. Blokowanie właściwości ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem konta magazynu</span><span class="sxs-lookup"><span data-stu-id="90a7e-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="90a7e-115">To polecenie blokuje politykę immutability dla kontenera obiektów blob magazynu z obiektem konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="90a7e-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="90a7e-116">Przykład 3. Blokowanie właściwości ImmutabilityPolicy z kontenera obiektów blob magazynu z obiektem container</span><span class="sxs-lookup"><span data-stu-id="90a7e-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="90a7e-117">To polecenie blokuje politykę immutability dla kontenera obiektów blob magazynu z obiektem kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="90a7e-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="90a7e-118">Przykład 4. Blokowanie właściwości ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="90a7e-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="90a7e-119">To polecenie blokuje politykę immutability dla kontenera obiektów blob magazynu z obiektem ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="90a7e-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="90a7e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90a7e-120">PARAMETERS</span></span>

### <span data-ttu-id="90a7e-121">— Kontener</span><span class="sxs-lookup"><span data-stu-id="90a7e-121">-Container</span></span>
<span data-ttu-id="90a7e-122">Obiekt kontener magazynu</span><span class="sxs-lookup"><span data-stu-id="90a7e-122">Storage container object</span></span>

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

### <span data-ttu-id="90a7e-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="90a7e-123">-ContainerName</span></span>
<span data-ttu-id="90a7e-124">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="90a7e-124">Container Name</span></span>

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

### <span data-ttu-id="90a7e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90a7e-125">-DefaultProfile</span></span>
<span data-ttu-id="90a7e-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="90a7e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90a7e-127">— Otagowanie</span><span class="sxs-lookup"><span data-stu-id="90a7e-127">-Etag</span></span>
<span data-ttu-id="90a7e-128">Tag etag zasad wiadomości błyskawicznych.</span><span class="sxs-lookup"><span data-stu-id="90a7e-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="90a7e-129">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="90a7e-129">-Force</span></span>
<span data-ttu-id="90a7e-130">Wymuszanie usunięcia wiadomości błyskawicznychPolicy.</span><span class="sxs-lookup"><span data-stu-id="90a7e-130">Force to remove the ImmutabilityPolicy.</span></span>

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

### <span data-ttu-id="90a7e-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90a7e-131">-InputObject</span></span>
<span data-ttu-id="90a7e-132">Obiekt ImmutabilityPolicy do usunięcia</span><span class="sxs-lookup"><span data-stu-id="90a7e-132">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="90a7e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90a7e-133">-ResourceGroupName</span></span>
<span data-ttu-id="90a7e-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="90a7e-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="90a7e-135">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="90a7e-135">-StorageAccount</span></span>
<span data-ttu-id="90a7e-136">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="90a7e-136">Storage account object</span></span>

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

### <span data-ttu-id="90a7e-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="90a7e-137">-StorageAccountName</span></span>
<span data-ttu-id="90a7e-138">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="90a7e-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="90a7e-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="90a7e-139">-Confirm</span></span>
<span data-ttu-id="90a7e-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="90a7e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90a7e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90a7e-141">-WhatIf</span></span>
<span data-ttu-id="90a7e-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90a7e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90a7e-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="90a7e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90a7e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90a7e-144">CommonParameters</span></span>
<span data-ttu-id="90a7e-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90a7e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90a7e-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90a7e-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90a7e-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90a7e-147">INPUTS</span></span>

### <span data-ttu-id="90a7e-148">System.String</span><span class="sxs-lookup"><span data-stu-id="90a7e-148">System.String</span></span>

### <span data-ttu-id="90a7e-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="90a7e-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="90a7e-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="90a7e-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="90a7e-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="90a7e-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="90a7e-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90a7e-152">OUTPUTS</span></span>

### <span data-ttu-id="90a7e-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="90a7e-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="90a7e-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="90a7e-154">NOTES</span></span>

## <span data-ttu-id="90a7e-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90a7e-155">RELATED LINKS</span></span>
