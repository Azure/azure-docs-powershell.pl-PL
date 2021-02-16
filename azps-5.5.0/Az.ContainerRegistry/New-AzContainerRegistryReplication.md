---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
ms.openlocfilehash: aadac0f7d408efd5f635d77d14f9afabfbd444d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199146"
---
# <span data-ttu-id="0d68c-101">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="0d68c-101">New-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="0d68c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d68c-102">SYNOPSIS</span></span>
<span data-ttu-id="0d68c-103">Tworzy replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="0d68c-103">Creates a container registry replication.</span></span>

## <span data-ttu-id="0d68c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0d68c-104">SYNTAX</span></span>

### <span data-ttu-id="0d68c-105">NameResourceGroupParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="0d68c-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String> -Location <String>
 [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d68c-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d68c-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d68c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d68c-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d68c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0d68c-108">DESCRIPTION</span></span>
<span data-ttu-id="0d68c-109">Polecenie New-AzContainerRegistryReplication cmdlet tworzy nową replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="0d68c-109">The New-AzContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="0d68c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0d68c-110">EXAMPLES</span></span>

### <span data-ttu-id="0d68c-111">Przykład 1. Tworzenie nowego kontenera replikacji rejestru.</span><span class="sxs-lookup"><span data-stu-id="0d68c-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="0d68c-112">Utwórz nową replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="0d68c-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="0d68c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d68c-113">PARAMETERS</span></span>

### <span data-ttu-id="0d68c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d68c-114">-DefaultProfile</span></span>
<span data-ttu-id="0d68c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0d68c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d68c-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0d68c-116">-Location</span></span>
<span data-ttu-id="0d68c-117">Container Registry Location (Lokalizacja rejestru kontenerów).</span><span class="sxs-lookup"><span data-stu-id="0d68c-117">Container Registry Location.</span></span>
<span data-ttu-id="0d68c-118">Domyślna lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0d68c-118">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="0d68c-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0d68c-119">-Name</span></span>
<span data-ttu-id="0d68c-120">Nazwa replikacji rejestru kontenerów.</span><span class="sxs-lookup"><span data-stu-id="0d68c-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="0d68c-121">Domyślnie jest to nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="0d68c-121">Default to the location name.</span></span>

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

### <span data-ttu-id="0d68c-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="0d68c-122">-Registry</span></span>
<span data-ttu-id="0d68c-123">Obiekt Container Registry.</span><span class="sxs-lookup"><span data-stu-id="0d68c-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="0d68c-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="0d68c-124">-RegistryName</span></span>
<span data-ttu-id="0d68c-125">Container Registry Name (Nazwa rejestru kontenera).</span><span class="sxs-lookup"><span data-stu-id="0d68c-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="0d68c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d68c-126">-ResourceGroupName</span></span>
<span data-ttu-id="0d68c-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0d68c-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="0d68c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d68c-128">-ResourceId</span></span>
<span data-ttu-id="0d68c-129">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="0d68c-129">The container registry resource id</span></span>

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

### <span data-ttu-id="0d68c-130">— Tag</span><span class="sxs-lookup"><span data-stu-id="0d68c-130">-Tag</span></span>
<span data-ttu-id="0d68c-131">Tagi rejestru Container.</span><span class="sxs-lookup"><span data-stu-id="0d68c-131">Container Registry Tags.</span></span>

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

### <span data-ttu-id="0d68c-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0d68c-132">-Confirm</span></span>
<span data-ttu-id="0d68c-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0d68c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d68c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d68c-134">-WhatIf</span></span>
<span data-ttu-id="0d68c-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d68c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d68c-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0d68c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d68c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d68c-137">CommonParameters</span></span>
<span data-ttu-id="0d68c-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d68c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d68c-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d68c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d68c-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d68c-140">INPUTS</span></span>

### <span data-ttu-id="0d68c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0d68c-141">System.String</span></span>

## <span data-ttu-id="0d68c-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0d68c-142">OUTPUTS</span></span>

### <span data-ttu-id="0d68c-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="0d68c-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="0d68c-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0d68c-144">NOTES</span></span>

## <span data-ttu-id="0d68c-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d68c-145">RELATED LINKS</span></span>

[<span data-ttu-id="0d68c-146">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="0d68c-146">Get-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="0d68c-147">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="0d68c-147">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)