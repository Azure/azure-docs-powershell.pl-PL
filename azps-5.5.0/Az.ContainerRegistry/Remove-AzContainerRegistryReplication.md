---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
ms.openlocfilehash: 41bdf9bbc33239590f9d3a6db4ffaa88ddf752a1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199122"
---
# <span data-ttu-id="c285a-101">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c285a-101">Remove-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="c285a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c285a-102">SYNOPSIS</span></span>
<span data-ttu-id="c285a-103">Usuwa replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="c285a-103">Removes a container registry replication.</span></span>

## <span data-ttu-id="c285a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c285a-104">SYNTAX</span></span>

### <span data-ttu-id="c285a-105">NameResourceGroupParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c285a-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c285a-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c285a-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -Replication <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c285a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c285a-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c285a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c285a-108">DESCRIPTION</span></span>
<span data-ttu-id="c285a-109">Polecenie Remove-AzContainerRegistryReplication cmdlet usuwa replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="c285a-109">The Remove-AzContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="c285a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c285a-110">EXAMPLES</span></span>

### <span data-ttu-id="c285a-111">Przykład 1. Usuwa replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="c285a-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="c285a-112">Usuwa replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="c285a-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="c285a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c285a-113">PARAMETERS</span></span>

### <span data-ttu-id="c285a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c285a-114">-DefaultProfile</span></span>
<span data-ttu-id="c285a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c285a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c285a-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c285a-116">-Name</span></span>
<span data-ttu-id="c285a-117">Nazwa replikacji rejestru kontenerów.</span><span class="sxs-lookup"><span data-stu-id="c285a-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="c285a-118">Domyślnie jest to nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c285a-118">Default to the location name.</span></span>

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

### <span data-ttu-id="c285a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c285a-119">-PassThru</span></span>
<span data-ttu-id="c285a-120">Wskazuje, że to polecenie cmdlet zwraca wartość prawda, jeśli usunięcie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="c285a-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="c285a-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="c285a-121">-RegistryName</span></span>
<span data-ttu-id="c285a-122">Container Registry Name (Nazwa rejestru kontenera).</span><span class="sxs-lookup"><span data-stu-id="c285a-122">Container Registry Name.</span></span>

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

### <span data-ttu-id="c285a-123">— Replikacja</span><span class="sxs-lookup"><span data-stu-id="c285a-123">-Replication</span></span>
<span data-ttu-id="c285a-124">Obiekt Container Registry.</span><span class="sxs-lookup"><span data-stu-id="c285a-124">Container Registry Object.</span></span>

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

### <span data-ttu-id="c285a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c285a-125">-ResourceGroupName</span></span>
<span data-ttu-id="c285a-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c285a-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="c285a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c285a-127">-ResourceId</span></span>
<span data-ttu-id="c285a-128">Identyfikator zasobu replikacji rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="c285a-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="c285a-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c285a-129">-Confirm</span></span>
<span data-ttu-id="c285a-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c285a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c285a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c285a-131">-WhatIf</span></span>
<span data-ttu-id="c285a-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c285a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c285a-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c285a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c285a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c285a-134">CommonParameters</span></span>
<span data-ttu-id="c285a-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c285a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c285a-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c285a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c285a-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c285a-137">INPUTS</span></span>

### <span data-ttu-id="c285a-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c285a-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

### <span data-ttu-id="c285a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c285a-139">System.String</span></span>

## <span data-ttu-id="c285a-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c285a-140">OUTPUTS</span></span>

### <span data-ttu-id="c285a-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c285a-141">System.Boolean</span></span>

## <span data-ttu-id="c285a-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c285a-142">NOTES</span></span>

## <span data-ttu-id="c285a-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c285a-143">RELATED LINKS</span></span>

[<span data-ttu-id="c285a-144">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c285a-144">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="c285a-145">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c285a-145">Get-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)

