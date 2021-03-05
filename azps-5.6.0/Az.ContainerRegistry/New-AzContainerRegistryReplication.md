---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/new-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
ms.openlocfilehash: a446fe34ba29789e93e8907d3155af654a93ff21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995716"
---
# <span data-ttu-id="70079-101">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="70079-101">New-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="70079-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70079-102">SYNOPSIS</span></span>
<span data-ttu-id="70079-103">Tworzy replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="70079-103">Creates a container registry replication.</span></span>

## <span data-ttu-id="70079-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="70079-104">SYNTAX</span></span>

### <span data-ttu-id="70079-105">NameResourceGroupParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="70079-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String> -Location <String>
 [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70079-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70079-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70079-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70079-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70079-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="70079-108">DESCRIPTION</span></span>
<span data-ttu-id="70079-109">Polecenie New-AzContainerRegistryReplication cmdlet tworzy nową replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="70079-109">The New-AzContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="70079-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="70079-110">EXAMPLES</span></span>

### <span data-ttu-id="70079-111">Przykład 1. Tworzenie nowego kontenera replikacji rejestru.</span><span class="sxs-lookup"><span data-stu-id="70079-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="70079-112">Utwórz nową replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="70079-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="70079-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70079-113">PARAMETERS</span></span>

### <span data-ttu-id="70079-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70079-114">-DefaultProfile</span></span>
<span data-ttu-id="70079-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="70079-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70079-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="70079-116">-Location</span></span>
<span data-ttu-id="70079-117">Container Registry Location (Lokalizacja rejestru kontenerów).</span><span class="sxs-lookup"><span data-stu-id="70079-117">Container Registry Location.</span></span>
<span data-ttu-id="70079-118">Domyślna lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="70079-118">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationLocation

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70079-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="70079-119">-Name</span></span>
<span data-ttu-id="70079-120">Nazwa replikacji rejestru kontenerów.</span><span class="sxs-lookup"><span data-stu-id="70079-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="70079-121">Domyślnie jest to nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="70079-121">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70079-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="70079-122">-Registry</span></span>
<span data-ttu-id="70079-123">Obiekt Container Registry.</span><span class="sxs-lookup"><span data-stu-id="70079-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70079-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="70079-124">-RegistryName</span></span>
<span data-ttu-id="70079-125">Container Registry Name (Nazwa rejestru kontenera).</span><span class="sxs-lookup"><span data-stu-id="70079-125">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70079-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70079-126">-ResourceGroupName</span></span>
<span data-ttu-id="70079-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="70079-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70079-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70079-128">-ResourceId</span></span>
<span data-ttu-id="70079-129">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="70079-129">The container registry resource id</span></span>

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

### <span data-ttu-id="70079-130">— Tag</span><span class="sxs-lookup"><span data-stu-id="70079-130">-Tag</span></span>
<span data-ttu-id="70079-131">Tagi rejestru Container.</span><span class="sxs-lookup"><span data-stu-id="70079-131">Container Registry Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70079-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="70079-132">-Confirm</span></span>
<span data-ttu-id="70079-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="70079-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70079-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70079-134">-WhatIf</span></span>
<span data-ttu-id="70079-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70079-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70079-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="70079-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70079-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70079-137">CommonParameters</span></span>
<span data-ttu-id="70079-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70079-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70079-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70079-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70079-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70079-140">INPUTS</span></span>

### <span data-ttu-id="70079-141">System.String</span><span class="sxs-lookup"><span data-stu-id="70079-141">System.String</span></span>

## <span data-ttu-id="70079-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70079-142">OUTPUTS</span></span>

### <span data-ttu-id="70079-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="70079-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="70079-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="70079-144">NOTES</span></span>

## <span data-ttu-id="70079-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70079-145">RELATED LINKS</span></span>

[<span data-ttu-id="70079-146">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="70079-146">Get-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="70079-147">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="70079-147">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)