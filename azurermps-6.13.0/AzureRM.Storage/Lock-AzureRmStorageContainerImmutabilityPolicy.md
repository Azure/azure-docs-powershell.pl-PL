---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/lock-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Lock-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Lock-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 726dc9043c1082f97e32da46305cf81192e1806c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524273"
---
# <span data-ttu-id="94b8f-101">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="94b8f-101">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="94b8f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="94b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="94b8f-103">Blokuje ImmutabilityPolicy kontenerów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="94b8f-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94b8f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="94b8f-104">SYNTAX</span></span>

### <span data-ttu-id="94b8f-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="94b8f-105">AccountName (Default)</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94b8f-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="94b8f-106">AccountObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94b8f-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="94b8f-107">ContainerObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94b8f-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="94b8f-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94b8f-109">Opis</span><span class="sxs-lookup"><span data-stu-id="94b8f-109">DESCRIPTION</span></span>
<span data-ttu-id="94b8f-110">Polecenie cmdlet **Lock-AzureRmStorageContainerImmutabilityPolicy** blokuje ImmutabilityPolicy kontenerów blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="94b8f-110">The **Lock-AzureRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="94b8f-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="94b8f-111">EXAMPLES</span></span>

### <span data-ttu-id="94b8f-112">Przykład 1: zablokowanie ImmutabilityPolicy kontenera obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="94b8f-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="94b8f-113">To polecenie blokuje ImmutabilityPolicy kontenera obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="94b8f-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="94b8f-114">Przykład 2: zablokowanie ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem konta magazynu</span><span class="sxs-lookup"><span data-stu-id="94b8f-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="94b8f-115">To polecenie blokuje ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="94b8f-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="94b8f-116">Przykład 3: Zablokuj ImmutabilityPolicyof kontener obiektu blob magazynu z obiektem kontenera</span><span class="sxs-lookup"><span data-stu-id="94b8f-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="94b8f-117">To polecenie blokuje ImmutabilityPolicy kontenera obiektów BLOB magazynowania z obiektem kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="94b8f-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="94b8f-118">Przykład 4: zablokowanie ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="94b8f-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzureRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="94b8f-119">To polecenie blokuje ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="94b8f-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="94b8f-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="94b8f-120">PARAMETERS</span></span>

### <span data-ttu-id="94b8f-121">-Kontener</span><span class="sxs-lookup"><span data-stu-id="94b8f-121">-Container</span></span>
<span data-ttu-id="94b8f-122">Obiekt kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="94b8f-122">Storage container object</span></span>

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

### <span data-ttu-id="94b8f-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="94b8f-123">-ContainerName</span></span>
<span data-ttu-id="94b8f-124">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="94b8f-124">Container Name</span></span>

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

### <span data-ttu-id="94b8f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94b8f-125">-DefaultProfile</span></span>
<span data-ttu-id="94b8f-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="94b8f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94b8f-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="94b8f-127">-Etag</span></span>
<span data-ttu-id="94b8f-128">Element ETag zasad Immutability.</span><span class="sxs-lookup"><span data-stu-id="94b8f-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="94b8f-129">-Force</span><span class="sxs-lookup"><span data-stu-id="94b8f-129">-Force</span></span>
<span data-ttu-id="94b8f-130">Wymuś usunięcie ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="94b8f-130">Force to remove the ImmutabilityPolicy.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b8f-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="94b8f-131">-InputObject</span></span>
<span data-ttu-id="94b8f-132">Obiekt ImmutabilityPolicy do usunięcia</span><span class="sxs-lookup"><span data-stu-id="94b8f-132">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="94b8f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94b8f-133">-ResourceGroupName</span></span>
<span data-ttu-id="94b8f-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="94b8f-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="94b8f-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="94b8f-135">-StorageAccount</span></span>
<span data-ttu-id="94b8f-136">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="94b8f-136">Storage account object</span></span>

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

### <span data-ttu-id="94b8f-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="94b8f-137">-StorageAccountName</span></span>
<span data-ttu-id="94b8f-138">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="94b8f-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="94b8f-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="94b8f-139">-Confirm</span></span>
<span data-ttu-id="94b8f-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94b8f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94b8f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94b8f-141">-WhatIf</span></span>
<span data-ttu-id="94b8f-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94b8f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94b8f-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="94b8f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94b8f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94b8f-144">CommonParameters</span></span>
<span data-ttu-id="94b8f-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94b8f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94b8f-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94b8f-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94b8f-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94b8f-147">INPUTS</span></span>

### <span data-ttu-id="94b8f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="94b8f-148">System.String</span></span>
<span data-ttu-id="94b8f-149">Microsoft. Azure. Commands. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="94b8f-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="94b8f-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="94b8f-150">OUTPUTS</span></span>

### <span data-ttu-id="94b8f-151">Microsoft. Azure. Commands. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="94b8f-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="94b8f-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="94b8f-152">NOTES</span></span>

## <span data-ttu-id="94b8f-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94b8f-153">RELATED LINKS</span></span>

