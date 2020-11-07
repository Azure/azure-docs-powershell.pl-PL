---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/lock-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Lock-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: f2c9181ab0abc6bf897a94e803caceadb587b296
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707600"
---
# <span data-ttu-id="a57cd-101">Lock-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a57cd-101">Lock-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="a57cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a57cd-102">SYNOPSIS</span></span>
<span data-ttu-id="a57cd-103">Blokuje ImmutabilityPolicy kontenerów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="a57cd-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="a57cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a57cd-104">SYNTAX</span></span>

### <span data-ttu-id="a57cd-105">AccountName (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="a57cd-105">AccountName (Default)</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a57cd-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="a57cd-106">AccountObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a57cd-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="a57cd-107">ContainerObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a57cd-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="a57cd-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a57cd-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a57cd-109">DESCRIPTION</span></span>
<span data-ttu-id="a57cd-110">Polecenie cmdlet **Lock-AzRmStorageContainerImmutabilityPolicy** blokuje ImmutabilityPolicy kontenerów blob magazynu.</span><span class="sxs-lookup"><span data-stu-id="a57cd-110">The **Lock-AzRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="a57cd-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a57cd-111">EXAMPLES</span></span>

### <span data-ttu-id="a57cd-112">Przykład 1: zablokowanie ImmutabilityPolicy kontenera obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="a57cd-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="a57cd-113">To polecenie blokuje ImmutabilityPolicy kontenera obiektu blob magazynu z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="a57cd-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="a57cd-114">Przykład 2: zablokowanie ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem konta magazynu</span><span class="sxs-lookup"><span data-stu-id="a57cd-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="a57cd-115">To polecenie blokuje ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="a57cd-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="a57cd-116">Przykład 3: Zablokuj ImmutabilityPolicyof kontener obiektu blob magazynu z obiektem kontenera</span><span class="sxs-lookup"><span data-stu-id="a57cd-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="a57cd-117">To polecenie blokuje ImmutabilityPolicy kontenera obiektów BLOB magazynowania z obiektem kontenera magazynu.</span><span class="sxs-lookup"><span data-stu-id="a57cd-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="a57cd-118">Przykład 4: zablokowanie ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a57cd-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="a57cd-119">To polecenie blokuje ImmutabilityPolicy kontenera obiektów blob magazynu z obiektem ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="a57cd-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="a57cd-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a57cd-120">PARAMETERS</span></span>

### <span data-ttu-id="a57cd-121">-Kontener</span><span class="sxs-lookup"><span data-stu-id="a57cd-121">-Container</span></span>
<span data-ttu-id="a57cd-122">Obiekt kontenera magazynu</span><span class="sxs-lookup"><span data-stu-id="a57cd-122">Storage container object</span></span>

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

### <span data-ttu-id="a57cd-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a57cd-123">-ContainerName</span></span>
<span data-ttu-id="a57cd-124">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="a57cd-124">Container Name</span></span>

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

### <span data-ttu-id="a57cd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a57cd-125">-DefaultProfile</span></span>
<span data-ttu-id="a57cd-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a57cd-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a57cd-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="a57cd-127">-Etag</span></span>
<span data-ttu-id="a57cd-128">Element ETag zasad Immutability.</span><span class="sxs-lookup"><span data-stu-id="a57cd-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="a57cd-129">-Force</span><span class="sxs-lookup"><span data-stu-id="a57cd-129">-Force</span></span>
<span data-ttu-id="a57cd-130">Wymuś usunięcie ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="a57cd-130">Force to remove the ImmutabilityPolicy.</span></span>

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

### <span data-ttu-id="a57cd-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a57cd-131">-InputObject</span></span>
<span data-ttu-id="a57cd-132">Obiekt ImmutabilityPolicy do usunięcia</span><span class="sxs-lookup"><span data-stu-id="a57cd-132">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="a57cd-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a57cd-133">-ResourceGroupName</span></span>
<span data-ttu-id="a57cd-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a57cd-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="a57cd-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a57cd-135">-StorageAccount</span></span>
<span data-ttu-id="a57cd-136">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="a57cd-136">Storage account object</span></span>

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

### <span data-ttu-id="a57cd-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a57cd-137">-StorageAccountName</span></span>
<span data-ttu-id="a57cd-138">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="a57cd-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="a57cd-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a57cd-139">-Confirm</span></span>
<span data-ttu-id="a57cd-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a57cd-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a57cd-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a57cd-141">-WhatIf</span></span>
<span data-ttu-id="a57cd-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a57cd-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a57cd-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a57cd-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a57cd-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a57cd-144">CommonParameters</span></span>
<span data-ttu-id="a57cd-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a57cd-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a57cd-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a57cd-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a57cd-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a57cd-147">INPUTS</span></span>

### <span data-ttu-id="a57cd-148">System. String</span><span class="sxs-lookup"><span data-stu-id="a57cd-148">System.String</span></span>

### <span data-ttu-id="a57cd-149">Microsoft. Azure. Commands. Management. Storage. models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a57cd-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="a57cd-150">Microsoft. Azure. Commands. Management. Storage. models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="a57cd-150">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="a57cd-151">Microsoft. Azure. Commands. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a57cd-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="a57cd-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a57cd-152">OUTPUTS</span></span>

### <span data-ttu-id="a57cd-153">Microsoft. Azure. Commands. Management. Storage. models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a57cd-153">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="a57cd-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a57cd-154">NOTES</span></span>

## <span data-ttu-id="a57cd-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a57cd-155">RELATED LINKS</span></span>