---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: 467fab7d2d7c344c3ffa2ca631addb538e790101
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988716"
---
# <span data-ttu-id="04a49-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="04a49-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="04a49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04a49-102">SYNOPSIS</span></span>
<span data-ttu-id="04a49-103">Usuwa kontener obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="04a49-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="04a49-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="04a49-104">SYNTAX</span></span>

### <span data-ttu-id="04a49-105">AccountName (Default)</span><span class="sxs-lookup"><span data-stu-id="04a49-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04a49-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="04a49-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04a49-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="04a49-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04a49-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="04a49-108">DESCRIPTION</span></span>
<span data-ttu-id="04a49-109">Polecenie **cmdlet Remove-AzRmStorageContainer** usuwa kontener obiektów blob magazynu</span><span class="sxs-lookup"><span data-stu-id="04a49-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="04a49-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="04a49-110">EXAMPLES</span></span>

### <span data-ttu-id="04a49-111">Przykład 1. Usuwanie kontenera obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="04a49-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="04a49-112">To polecenie usuwa kontener obiektów blob magazynu z nazwą konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="04a49-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="04a49-113">Przykład 2. Usuwanie kontenera obiektów blob magazynu z obiektem konta magazynu i nazwą kontenera</span><span class="sxs-lookup"><span data-stu-id="04a49-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="04a49-114">To polecenie usuwa kontener obiektów blob magazynu z obiektem konta magazynu i nazwą kontenera.</span><span class="sxs-lookup"><span data-stu-id="04a49-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="04a49-115">Przykład 3. Usuwanie wszystkich kontenerów obiektów blob magazynu na koncie magazynu z potokiem</span><span class="sxs-lookup"><span data-stu-id="04a49-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="04a49-116">To polecenie usuwa wszystkie kontenery obiektów blob magazynu na koncie magazynu z potokiem.</span><span class="sxs-lookup"><span data-stu-id="04a49-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="04a49-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04a49-117">PARAMETERS</span></span>

### <span data-ttu-id="04a49-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04a49-118">-DefaultProfile</span></span>
<span data-ttu-id="04a49-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="04a49-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04a49-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="04a49-120">-Force</span></span>
<span data-ttu-id="04a49-121">Wymuszanie usunięcia kontenera i całej jego zawartości</span><span class="sxs-lookup"><span data-stu-id="04a49-121">Force to remove the container and all content in it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a49-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04a49-122">-InputObject</span></span>
<span data-ttu-id="04a49-123">Obiekt kontener magazynu</span><span class="sxs-lookup"><span data-stu-id="04a49-123">Storage container object</span></span>

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

### <span data-ttu-id="04a49-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="04a49-124">-Name</span></span>
<span data-ttu-id="04a49-125">Nazwa kontenera</span><span class="sxs-lookup"><span data-stu-id="04a49-125">Container Name</span></span>

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

### <span data-ttu-id="04a49-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04a49-126">-PassThru</span></span>
<span data-ttu-id="04a49-127">Wskazuje, że to polecenie cmdlet zwraca **wartość** logiczną, która odzwierciedla sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="04a49-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="04a49-128">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="04a49-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="04a49-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04a49-129">-ResourceGroupName</span></span>
<span data-ttu-id="04a49-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="04a49-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="04a49-131">— StorageAccount</span><span class="sxs-lookup"><span data-stu-id="04a49-131">-StorageAccount</span></span>
<span data-ttu-id="04a49-132">Obiekt konta magazynu</span><span class="sxs-lookup"><span data-stu-id="04a49-132">Storage account object</span></span>

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

### <span data-ttu-id="04a49-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="04a49-133">-StorageAccountName</span></span>
<span data-ttu-id="04a49-134">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="04a49-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="04a49-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="04a49-135">-Confirm</span></span>
<span data-ttu-id="04a49-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="04a49-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a49-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04a49-137">-WhatIf</span></span>
<span data-ttu-id="04a49-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04a49-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04a49-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="04a49-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a49-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04a49-140">CommonParameters</span></span>
<span data-ttu-id="04a49-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04a49-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04a49-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04a49-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04a49-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04a49-143">INPUTS</span></span>

### <span data-ttu-id="04a49-144">System.String</span><span class="sxs-lookup"><span data-stu-id="04a49-144">System.String</span></span>

### <span data-ttu-id="04a49-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04a49-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="04a49-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="04a49-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="04a49-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04a49-147">OUTPUTS</span></span>

### <span data-ttu-id="04a49-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="04a49-148">System.Boolean</span></span>

## <span data-ttu-id="04a49-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="04a49-149">NOTES</span></span>

## <span data-ttu-id="04a49-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04a49-150">RELATED LINKS</span></span>
