---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
ms.openlocfilehash: 3fff7a0952f4ace41f76237a8fbf226e9bb58128
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015377"
---
# <span data-ttu-id="600f0-101">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="600f0-101">Remove-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="600f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="600f0-102">SYNOPSIS</span></span>
<span data-ttu-id="600f0-103">Usuwa replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="600f0-103">Removes a container registry replication.</span></span>

## <span data-ttu-id="600f0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="600f0-104">SYNTAX</span></span>

### <span data-ttu-id="600f0-105">NameResourceGroupParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="600f0-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="600f0-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="600f0-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -Replication <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="600f0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="600f0-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="600f0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="600f0-108">DESCRIPTION</span></span>
<span data-ttu-id="600f0-109">Polecenie Remove-AzContainerRegistryReplication cmdlet usuwa replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="600f0-109">The Remove-AzContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="600f0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="600f0-110">EXAMPLES</span></span>

### <span data-ttu-id="600f0-111">Przykład 1. Usuwa replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="600f0-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="600f0-112">Usuwa replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="600f0-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="600f0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="600f0-113">PARAMETERS</span></span>

### <span data-ttu-id="600f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="600f0-114">-DefaultProfile</span></span>
<span data-ttu-id="600f0-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="600f0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="600f0-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="600f0-116">-Name</span></span>
<span data-ttu-id="600f0-117">Nazwa replikacji rejestru kontenerów.</span><span class="sxs-lookup"><span data-stu-id="600f0-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="600f0-118">Domyślnie jest to nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="600f0-118">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="600f0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="600f0-119">-PassThru</span></span>
<span data-ttu-id="600f0-120">Wskazuje, że to polecenie cmdlet zwraca wartość prawda, jeśli usunięcie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="600f0-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="600f0-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="600f0-121">-RegistryName</span></span>
<span data-ttu-id="600f0-122">Container Registry Name (Nazwa rejestru kontenera).</span><span class="sxs-lookup"><span data-stu-id="600f0-122">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="600f0-123">—Replikacja</span><span class="sxs-lookup"><span data-stu-id="600f0-123">-Replication</span></span>
<span data-ttu-id="600f0-124">Obiekt Container Registry.</span><span class="sxs-lookup"><span data-stu-id="600f0-124">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases: Replicatoin

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="600f0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="600f0-125">-ResourceGroupName</span></span>
<span data-ttu-id="600f0-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="600f0-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="600f0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="600f0-127">-ResourceId</span></span>
<span data-ttu-id="600f0-128">Identyfikator zasobu replikacji rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="600f0-128">The container registry replication resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="600f0-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="600f0-129">-Confirm</span></span>
<span data-ttu-id="600f0-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="600f0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="600f0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="600f0-131">-WhatIf</span></span>
<span data-ttu-id="600f0-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="600f0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="600f0-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="600f0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="600f0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="600f0-134">CommonParameters</span></span>
<span data-ttu-id="600f0-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="600f0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="600f0-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="600f0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="600f0-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="600f0-137">INPUTS</span></span>

### <span data-ttu-id="600f0-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="600f0-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

### <span data-ttu-id="600f0-139">System.String</span><span class="sxs-lookup"><span data-stu-id="600f0-139">System.String</span></span>

## <span data-ttu-id="600f0-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="600f0-140">OUTPUTS</span></span>

### <span data-ttu-id="600f0-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="600f0-141">System.Boolean</span></span>

## <span data-ttu-id="600f0-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="600f0-142">NOTES</span></span>

## <span data-ttu-id="600f0-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="600f0-143">RELATED LINKS</span></span>

[<span data-ttu-id="600f0-144">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="600f0-144">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="600f0-145">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="600f0-145">Get-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)

