---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/lock-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 0cb3a4e65d8e464dda85e18e12dc106620e3eee8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195779"
---
# <span data-ttu-id="1afb7-101">Lock-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1afb7-101">Lock-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="1afb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1afb7-102">SYNOPSIS</span></span>
<span data-ttu-id="1afb7-103">Blokuje politykę imutalności kontenerów obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="1afb7-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="1afb7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1afb7-104">SYNTAX</span></span>

### <span data-ttu-id="1afb7-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="1afb7-105">AccountName (Default)</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1afb7-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="1afb7-106">AccountObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1afb7-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="1afb7-107">ContainerObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1afb7-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="1afb7-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1afb7-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="1afb7-109">DESCRIPTION</span></span>
<span data-ttu-id="1afb7-110">Polecenie **cmdlet Lock-AzRmStorageContainerImmutabilityPolicy** blokuje politykę ImmutabilityPolicy kontenerów obiektów blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="1afb7-110">The **Lock-AzRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="1afb7-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1afb7-111">EXAMPLES</span></span>

### <span data-ttu-id="1afb7-112">Przykład 1. Blokowanie wiadomości błyskawicznychPolicy kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="1afb7-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="1afb7-113">To polecenie blokuje politykę immutability dla kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="1afb7-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="1afb7-114">Przykład 2. Blokowanie właściwości ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem konta magazynu</span><span class="sxs-lookup"><span data-stu-id="1afb7-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="1afb7-115">To polecenie blokuje politykę immutability dla kontenera obiektów blob magazynu z obiektem konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="1afb7-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="1afb7-116">Przykład 3. Blokowanie właściwości ImmutabilityPolicy z kontenera obiektów blob magazynu z obiektem container</span><span class="sxs-lookup"><span data-stu-id="1afb7-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="1afb7-117">To polecenie blokuje politykę immutability dla kontenera obiektów blob magazynu z obiektem kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="1afb7-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="1afb7-118">Przykład 4. Blokowanie właściwości ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1afb7-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="1afb7-119">To polecenie blokuje politykę immutability dla kontenera obiektów blob magazynu z obiektem ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="1afb7-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="1afb7-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1afb7-120">PARAMETERS</span></span>

### <span data-ttu-id="1afb7-121">— Kontener</span><span class="sxs-lookup"><span data-stu-id="1afb7-121">-Container</span></span>
<span data-ttu-id="1afb7-122">Obiekt kontener magazynu</span><span class="sxs-lookup"><span data-stu-id="1afb7-122">Storage container object</span></span>

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

### <span data-ttu-id="1afb7-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="1afb7-123">-ContainerName</span></span>
<span data-ttu-id="1afb7-124">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="1afb7-124">Container Name</span></span>

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

### <span data-ttu-id="1afb7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1afb7-125">-DefaultProfile</span></span>
<span data-ttu-id="1afb7-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1afb7-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1afb7-127">— Otagowanie</span><span class="sxs-lookup"><span data-stu-id="1afb7-127">-Etag</span></span>
<span data-ttu-id="1afb7-128">Tag etag zasad wiadomości błyskawicznych.</span><span class="sxs-lookup"><span data-stu-id="1afb7-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="1afb7-129">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="1afb7-129">-Force</span></span>
<span data-ttu-id="1afb7-130">Wymuszanie usunięcia wiadomości błyskawicznychPolicy.</span><span class="sxs-lookup"><span data-stu-id="1afb7-130">Force to remove the ImmutabilityPolicy.</span></span>

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

### <span data-ttu-id="1afb7-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1afb7-131">-InputObject</span></span>
<span data-ttu-id="1afb7-132">Obiekt ImmutabilityPolicy do usunięcia</span><span class="sxs-lookup"><span data-stu-id="1afb7-132">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="1afb7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1afb7-133">-ResourceGroupName</span></span>
<span data-ttu-id="1afb7-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1afb7-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="1afb7-135">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="1afb7-135">-StorageAccount</span></span>
<span data-ttu-id="1afb7-136">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="1afb7-136">Storage account object</span></span>

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

### <span data-ttu-id="1afb7-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1afb7-137">-StorageAccountName</span></span>
<span data-ttu-id="1afb7-138">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="1afb7-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="1afb7-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1afb7-139">-Confirm</span></span>
<span data-ttu-id="1afb7-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1afb7-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1afb7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1afb7-141">-WhatIf</span></span>
<span data-ttu-id="1afb7-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1afb7-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1afb7-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1afb7-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1afb7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1afb7-144">CommonParameters</span></span>
<span data-ttu-id="1afb7-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1afb7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1afb7-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1afb7-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1afb7-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1afb7-147">INPUTS</span></span>

### <span data-ttu-id="1afb7-148">System.String</span><span class="sxs-lookup"><span data-stu-id="1afb7-148">System.String</span></span>

### <span data-ttu-id="1afb7-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1afb7-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="1afb7-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="1afb7-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="1afb7-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1afb7-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="1afb7-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1afb7-152">OUTPUTS</span></span>

### <span data-ttu-id="1afb7-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1afb7-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="1afb7-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1afb7-154">NOTES</span></span>

## <span data-ttu-id="1afb7-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1afb7-155">RELATED LINKS</span></span>
