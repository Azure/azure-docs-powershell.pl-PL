---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 74963ef36a33bed6145d315f5792aa776a36bc7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547312"
---
# <span data-ttu-id="d5a23-101">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d5a23-101">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="d5a23-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d5a23-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a23-103">Usuwa ImmutabilityPolicy kontenera obiektów BLOB magazynowania</span><span class="sxs-lookup"><span data-stu-id="d5a23-103">Removes ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5a23-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d5a23-104">SYNTAX</span></span>

### <span data-ttu-id="d5a23-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d5a23-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5a23-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="d5a23-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5a23-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="d5a23-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5a23-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="d5a23-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5a23-109">Opis</span><span class="sxs-lookup"><span data-stu-id="d5a23-109">DESCRIPTION</span></span>
<span data-ttu-id="d5a23-110">Polecenie cmdlet **Remove-AzureRmStorageContainerImmutabilityPolicy** usuwa ImmutabilityPolicy kontenerów blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="d5a23-110">The **Remove-AzureRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="d5a23-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d5a23-111">EXAMPLES</span></span>

### <span data-ttu-id="d5a23-112">Przykład 1: usuwanie ImmutabilityPolicy kontenera obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="d5a23-112">Example 1: Remove ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="d5a23-113">To polecenie usuwa ImmutabilityPolicy kontenera obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="d5a23-113">This command removes ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="d5a23-114">Przykład 2: usuwanie ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem konta magazynu</span><span class="sxs-lookup"><span data-stu-id="d5a23-114">Example 2: Remove ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="d5a23-115">To polecenie usuwa ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d5a23-115">This command removes ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="d5a23-116">Przykład 3: usuwanie ImmutabilityPolicyof kontenera obiektów blob magazynu z obiektem kontenera</span><span class="sxs-lookup"><span data-stu-id="d5a23-116">Example 3: Remove ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="d5a23-117">To polecenie usuwa ImmutabilityPolicy kontenera obiektów BLOB magazynowania z obiektem kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="d5a23-117">This command removes ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="d5a23-118">Przykład 4: usuwanie ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d5a23-118">Example 4: Remove ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzureRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="d5a23-119">To polecenie usuwa ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="d5a23-119">This command removes ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="d5a23-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d5a23-120">PARAMETERS</span></span>

### <span data-ttu-id="d5a23-121">-Kontener</span><span class="sxs-lookup"><span data-stu-id="d5a23-121">-Container</span></span>
<span data-ttu-id="d5a23-122">Obiekt kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="d5a23-122">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a23-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="d5a23-123">-ContainerName</span></span>
<span data-ttu-id="d5a23-124">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="d5a23-124">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a23-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a23-125">-DefaultProfile</span></span>
<span data-ttu-id="d5a23-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5a23-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5a23-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="d5a23-127">-Etag</span></span>
<span data-ttu-id="d5a23-128">Element ETag zasad Immutability.</span><span class="sxs-lookup"><span data-stu-id="d5a23-128">Immutability policy etag.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a23-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d5a23-129">-InputObject</span></span>
<span data-ttu-id="d5a23-130">Obiekt ImmutabilityPolicy do usunięcia</span><span class="sxs-lookup"><span data-stu-id="d5a23-130">ImmutabilityPolicy Object to Remove</span></span>

```yaml
Type: PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a23-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5a23-131">-ResourceGroupName</span></span>
<span data-ttu-id="d5a23-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d5a23-132">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a23-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d5a23-133">-StorageAccount</span></span>
<span data-ttu-id="d5a23-134">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="d5a23-134">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a23-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d5a23-135">-StorageAccountName</span></span>
<span data-ttu-id="d5a23-136">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d5a23-136">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a23-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d5a23-137">-Confirm</span></span>
<span data-ttu-id="d5a23-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5a23-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5a23-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5a23-139">-WhatIf</span></span>
<span data-ttu-id="d5a23-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5a23-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5a23-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d5a23-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5a23-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a23-142">CommonParameters</span></span>
<span data-ttu-id="d5a23-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5a23-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a23-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5a23-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a23-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5a23-145">INPUTS</span></span>

### <span data-ttu-id="d5a23-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d5a23-146">System.String</span></span>
<span data-ttu-id="d5a23-147">Microsoft. Azure. Commands. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d5a23-147">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="d5a23-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d5a23-148">OUTPUTS</span></span>

### <span data-ttu-id="d5a23-149">Microsoft. Azure. Commands. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d5a23-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="d5a23-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d5a23-150">NOTES</span></span>

## <span data-ttu-id="d5a23-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5a23-151">RELATED LINKS</span></span>

