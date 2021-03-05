---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
ms.openlocfilehash: 696070e19f1810ab352abde4ad6248f4bf42b180
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973322"
---
# <span data-ttu-id="70163-101">Update-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="70163-101">Update-AzRmStorageContainer</span></span>

## <span data-ttu-id="70163-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70163-102">SYNOPSIS</span></span>
<span data-ttu-id="70163-103">Modyfikuje kontener obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="70163-103">Modifies a Storage blob container</span></span>

## <span data-ttu-id="70163-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="70163-104">SYNTAX</span></span>

### <span data-ttu-id="70163-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="70163-105">AccountName (Default)</span></span>
```
Update-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70163-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="70163-106">AccountObject</span></span>
```
Update-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70163-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="70163-107">ContainerObject</span></span>
```
Update-AzRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70163-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="70163-108">DESCRIPTION</span></span>
<span data-ttu-id="70163-109">Polecenie **cmdlet Update-AzRmStorageContainer** modyfikuje kontener obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="70163-109">The **Update-AzRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="70163-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="70163-110">EXAMPLES</span></span>

### <span data-ttu-id="70163-111">Przykład 1. Modyfikuje metadane kontenera obiektów blob magazynu i dostęp publiczny przy użyciu nazwy konta magazynu i nazwy kontenera</span><span class="sxs-lookup"><span data-stu-id="70163-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="70163-112">To polecenie modyfikuje metadane kontenera obiektów blob magazynu i dostęp publiczny przy użyciu nazwy konta magazynu i nazwy kontenera.</span><span class="sxs-lookup"><span data-stu-id="70163-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="70163-113">Przykład 2. Wyłączanie dostępu publicznego do kontenera obiektów blob magazynu z obiektem konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="70163-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="70163-114">To polecenie wyłącza dostęp publiczny do kontenera obiektów blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="70163-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="70163-115">Przykład 3. Ustawianie dostępu publicznego jako obiektu blob dla wszystkich kontenerów obiektów blob magazynu na koncie magazynu z potokiem</span><span class="sxs-lookup"><span data-stu-id="70163-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="70163-116">To polecenie ustaw dostęp publiczny jako obiekt blob dla wszystkich kontenerów obiektów blob magazynu na koncie magazynu z potokiem.</span><span class="sxs-lookup"><span data-stu-id="70163-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="70163-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70163-117">PARAMETERS</span></span>

### <span data-ttu-id="70163-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70163-118">-DefaultProfile</span></span>
<span data-ttu-id="70163-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="70163-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70163-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70163-120">-InputObject</span></span>
<span data-ttu-id="70163-121">Obiekt kontener magazynu</span><span class="sxs-lookup"><span data-stu-id="70163-121">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70163-122">— Metadane</span><span class="sxs-lookup"><span data-stu-id="70163-122">-Metadata</span></span>
<span data-ttu-id="70163-123">Metadane kontenera</span><span class="sxs-lookup"><span data-stu-id="70163-123">Container Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70163-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="70163-124">-Name</span></span>
<span data-ttu-id="70163-125">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="70163-125">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70163-126">- PublicAccess</span><span class="sxs-lookup"><span data-stu-id="70163-126">-PublicAccess</span></span>
<span data-ttu-id="70163-127">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="70163-127">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70163-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70163-128">-ResourceGroupName</span></span>
<span data-ttu-id="70163-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="70163-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="70163-130">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="70163-130">-StorageAccount</span></span>
<span data-ttu-id="70163-131">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="70163-131">Storage account object</span></span>

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

### <span data-ttu-id="70163-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="70163-132">-StorageAccountName</span></span>
<span data-ttu-id="70163-133">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="70163-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="70163-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="70163-134">-Confirm</span></span>
<span data-ttu-id="70163-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="70163-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70163-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70163-136">-WhatIf</span></span>
<span data-ttu-id="70163-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70163-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70163-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="70163-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70163-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70163-139">CommonParameters</span></span>
<span data-ttu-id="70163-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70163-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70163-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70163-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70163-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70163-142">INPUTS</span></span>

### <span data-ttu-id="70163-143">System.String</span><span class="sxs-lookup"><span data-stu-id="70163-143">System.String</span></span>

### <span data-ttu-id="70163-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="70163-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="70163-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="70163-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="70163-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70163-146">OUTPUTS</span></span>

### <span data-ttu-id="70163-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="70163-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="70163-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="70163-148">NOTES</span></span>

## <span data-ttu-id="70163-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70163-149">RELATED LINKS</span></span>
