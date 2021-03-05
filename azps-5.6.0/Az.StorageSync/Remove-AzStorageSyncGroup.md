---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: 38c6d45c4e49f86d3aacc2774942d15ddd50941e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974042"
---
# <span data-ttu-id="0f2a3-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0f2a3-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="0f2a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f2a3-102">SYNOPSIS</span></span>
<span data-ttu-id="0f2a3-103">To polecenie spowoduje usunięcie określonej grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="0f2a3-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="0f2a3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0f2a3-104">SYNTAX</span></span>

### <span data-ttu-id="0f2a3-105">StringParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="0f2a3-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f2a3-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f2a3-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f2a3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f2a3-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f2a3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0f2a3-108">DESCRIPTION</span></span>
<span data-ttu-id="0f2a3-109">To polecenie spowoduje usunięcie określonej grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="0f2a3-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="0f2a3-110">Grupę synchronizacji można usunąć tylko wtedy, gdy najpierw zostaną usunięte wszystkie zawarte punkty końcowe.</span><span class="sxs-lookup"><span data-stu-id="0f2a3-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="0f2a3-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0f2a3-111">EXAMPLES</span></span>

### <span data-ttu-id="0f2a3-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0f2a3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="0f2a3-113">To polecenie spowoduje usunięcie grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="0f2a3-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="0f2a3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f2a3-114">PARAMETERS</span></span>

### <span data-ttu-id="0f2a3-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0f2a3-115">-AsJob</span></span>
<span data-ttu-id="0f2a3-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0f2a3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f2a3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f2a3-117">-DefaultProfile</span></span>
<span data-ttu-id="0f2a3-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0f2a3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f2a3-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="0f2a3-119">-Force</span></span>
<span data-ttu-id="0f2a3-120">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="0f2a3-120">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f2a3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f2a3-121">-InputObject</span></span>
<span data-ttu-id="0f2a3-122">Obiekt wejściowy SyncGroup</span><span class="sxs-lookup"><span data-stu-id="0f2a3-122">SyncGroup Input Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f2a3-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0f2a3-123">-Name</span></span>
<span data-ttu-id="0f2a3-124">Nazwa grupy synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="0f2a3-124">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: SyncGroupName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f2a3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f2a3-125">-PassThru</span></span>
<span data-ttu-id="0f2a3-126">W normalnym wykonaniu to polecenie cmdlet nie zwraca żadnej wartości przy sukcesie.</span><span class="sxs-lookup"><span data-stu-id="0f2a3-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="0f2a3-127">Jeśli podasz parametr PassThru, po pomyślnym wykonaniu polecenie cmdlet zapisze wartość w potoku.</span><span class="sxs-lookup"><span data-stu-id="0f2a3-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="0f2a3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f2a3-128">-ResourceGroupName</span></span>
<span data-ttu-id="0f2a3-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0f2a3-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f2a3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f2a3-130">-ResourceId</span></span>
<span data-ttu-id="0f2a3-131">Identyfikator zasobu syncgroup</span><span class="sxs-lookup"><span data-stu-id="0f2a3-131">SyncGroup Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f2a3-132">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="0f2a3-132">-StorageSyncServiceName</span></span>
<span data-ttu-id="0f2a3-133">Nazwa usługi StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="0f2a3-133">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f2a3-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0f2a3-134">-Confirm</span></span>
<span data-ttu-id="0f2a3-135">Przed uruchomieniem polecenia cmdlet jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0f2a3-135">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f2a3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f2a3-136">-WhatIf</span></span>
<span data-ttu-id="0f2a3-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f2a3-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f2a3-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0f2a3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f2a3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f2a3-139">CommonParameters</span></span>
<span data-ttu-id="0f2a3-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f2a3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f2a3-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f2a3-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f2a3-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f2a3-142">INPUTS</span></span>

### <span data-ttu-id="0f2a3-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0f2a3-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="0f2a3-144">System.String</span><span class="sxs-lookup"><span data-stu-id="0f2a3-144">System.String</span></span>

### <span data-ttu-id="0f2a3-145">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="0f2a3-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0f2a3-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f2a3-146">OUTPUTS</span></span>

### <span data-ttu-id="0f2a3-147">System.Object</span><span class="sxs-lookup"><span data-stu-id="0f2a3-147">System.Object</span></span>
## <span data-ttu-id="0f2a3-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0f2a3-148">NOTES</span></span>

## <span data-ttu-id="0f2a3-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f2a3-149">RELATED LINKS</span></span>
