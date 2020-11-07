---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: b7686b57175958ec2ce4bd1466ca111cce219e05
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707554"
---
# <span data-ttu-id="3c67b-101">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3c67b-101">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="3c67b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3c67b-102">SYNOPSIS</span></span>
<span data-ttu-id="3c67b-103">Usuwa ImmutabilityPolicy kontenera obiektów BLOB magazynowania</span><span class="sxs-lookup"><span data-stu-id="3c67b-103">Removes ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="3c67b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3c67b-104">SYNTAX</span></span>

### <span data-ttu-id="3c67b-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3c67b-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c67b-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="3c67b-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c67b-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="3c67b-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c67b-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="3c67b-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c67b-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3c67b-109">DESCRIPTION</span></span>
<span data-ttu-id="3c67b-110">Polecenie cmdlet **Remove-AzRmStorageContainerImmutabilityPolicy** usuwa ImmutabilityPolicy kontenerów blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="3c67b-110">The **Remove-AzRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="3c67b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3c67b-111">EXAMPLES</span></span>

### <span data-ttu-id="3c67b-112">Przykład 1: usuwanie ImmutabilityPolicy kontenera obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="3c67b-112">Example 1: Remove ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="3c67b-113">To polecenie usuwa ImmutabilityPolicy kontenera obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="3c67b-113">This command removes ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="3c67b-114">Przykład 2: usuwanie ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem konta magazynu</span><span class="sxs-lookup"><span data-stu-id="3c67b-114">Example 2: Remove ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="3c67b-115">To polecenie usuwa ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3c67b-115">This command removes ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="3c67b-116">Przykład 3: usuwanie ImmutabilityPolicyof kontenera obiektów blob magazynu z obiektem kontenera</span><span class="sxs-lookup"><span data-stu-id="3c67b-116">Example 3: Remove ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="3c67b-117">To polecenie usuwa ImmutabilityPolicy kontenera obiektów BLOB magazynowania z obiektem kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="3c67b-117">This command removes ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="3c67b-118">Przykład 4: usuwanie ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3c67b-118">Example 4: Remove ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="3c67b-119">To polecenie usuwa ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="3c67b-119">This command removes ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="3c67b-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3c67b-120">PARAMETERS</span></span>

### <span data-ttu-id="3c67b-121">-Kontener</span><span class="sxs-lookup"><span data-stu-id="3c67b-121">-Container</span></span>
<span data-ttu-id="3c67b-122">Obiekt kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="3c67b-122">Storage container object</span></span>

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

### <span data-ttu-id="3c67b-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="3c67b-123">-ContainerName</span></span>
<span data-ttu-id="3c67b-124">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="3c67b-124">Container Name</span></span>

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

### <span data-ttu-id="3c67b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c67b-125">-DefaultProfile</span></span>
<span data-ttu-id="3c67b-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3c67b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c67b-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="3c67b-127">-Etag</span></span>
<span data-ttu-id="3c67b-128">Element ETag zasad Immutability.</span><span class="sxs-lookup"><span data-stu-id="3c67b-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="3c67b-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3c67b-129">-InputObject</span></span>
<span data-ttu-id="3c67b-130">Obiekt ImmutabilityPolicy do usunięcia</span><span class="sxs-lookup"><span data-stu-id="3c67b-130">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="3c67b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c67b-131">-ResourceGroupName</span></span>
<span data-ttu-id="3c67b-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3c67b-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="3c67b-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="3c67b-133">-StorageAccount</span></span>
<span data-ttu-id="3c67b-134">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="3c67b-134">Storage account object</span></span>

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

### <span data-ttu-id="3c67b-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3c67b-135">-StorageAccountName</span></span>
<span data-ttu-id="3c67b-136">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3c67b-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="3c67b-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3c67b-137">-Confirm</span></span>
<span data-ttu-id="3c67b-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c67b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c67b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c67b-139">-WhatIf</span></span>
<span data-ttu-id="3c67b-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c67b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c67b-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3c67b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c67b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c67b-142">CommonParameters</span></span>
<span data-ttu-id="3c67b-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c67b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c67b-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c67b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c67b-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c67b-145">INPUTS</span></span>

### <span data-ttu-id="3c67b-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3c67b-146">System.String</span></span>

### <span data-ttu-id="3c67b-147">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3c67b-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="3c67b-148">Microsoft. Azure. Commands. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="3c67b-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="3c67b-149">Microsoft. Azure. Commands. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3c67b-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="3c67b-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3c67b-150">OUTPUTS</span></span>

### <span data-ttu-id="3c67b-151">Microsoft. Azure. Commands. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="3c67b-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="3c67b-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3c67b-152">NOTES</span></span>

## <span data-ttu-id="3c67b-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c67b-153">RELATED LINKS</span></span>