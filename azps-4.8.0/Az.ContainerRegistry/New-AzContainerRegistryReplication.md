---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
ms.openlocfilehash: aadac0f7d408efd5f635d77d14f9afabfbd444d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221361"
---
# <span data-ttu-id="fab16-101">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="fab16-101">New-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="fab16-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fab16-102">SYNOPSIS</span></span>
<span data-ttu-id="fab16-103">Tworzy replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="fab16-103">Creates a container registry replication.</span></span>

## <span data-ttu-id="fab16-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fab16-104">SYNTAX</span></span>

### <span data-ttu-id="fab16-105">NameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fab16-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String> -Location <String>
 [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fab16-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fab16-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fab16-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fab16-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fab16-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fab16-108">DESCRIPTION</span></span>
<span data-ttu-id="fab16-109">Polecenie cmdlet New-AzContainerRegistryReplication tworzy nową replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="fab16-109">The New-AzContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="fab16-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fab16-110">EXAMPLES</span></span>

### <span data-ttu-id="fab16-111">Przykład 1: Tworzenie nowej replikacji rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="fab16-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="fab16-112">Tworzenie nowej replikacji rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="fab16-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="fab16-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fab16-113">PARAMETERS</span></span>

### <span data-ttu-id="fab16-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fab16-114">-DefaultProfile</span></span>
<span data-ttu-id="fab16-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fab16-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fab16-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fab16-116">-Location</span></span>
<span data-ttu-id="fab16-117">Lokalizacja rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="fab16-117">Container Registry Location.</span></span>
<span data-ttu-id="fab16-118">Domyślnie jest to lokalizacja grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fab16-118">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="fab16-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fab16-119">-Name</span></span>
<span data-ttu-id="fab16-120">Nazwa replikacji rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="fab16-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="fab16-121">Domyślnie jest to nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="fab16-121">Default to the location name.</span></span>

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

### <span data-ttu-id="fab16-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="fab16-122">-Registry</span></span>
<span data-ttu-id="fab16-123">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="fab16-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="fab16-124">-Registryname</span><span class="sxs-lookup"><span data-stu-id="fab16-124">-RegistryName</span></span>
<span data-ttu-id="fab16-125">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="fab16-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="fab16-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fab16-126">-ResourceGroupName</span></span>
<span data-ttu-id="fab16-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fab16-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="fab16-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fab16-128">-ResourceId</span></span>
<span data-ttu-id="fab16-129">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="fab16-129">The container registry resource id</span></span>

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

### <span data-ttu-id="fab16-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="fab16-130">-Tag</span></span>
<span data-ttu-id="fab16-131">Znaczniki rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="fab16-131">Container Registry Tags.</span></span>

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

### <span data-ttu-id="fab16-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fab16-132">-Confirm</span></span>
<span data-ttu-id="fab16-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fab16-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fab16-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fab16-134">-WhatIf</span></span>
<span data-ttu-id="fab16-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fab16-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fab16-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fab16-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fab16-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fab16-137">CommonParameters</span></span>
<span data-ttu-id="fab16-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fab16-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fab16-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fab16-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fab16-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fab16-140">INPUTS</span></span>

### <span data-ttu-id="fab16-141">System. String</span><span class="sxs-lookup"><span data-stu-id="fab16-141">System.String</span></span>

## <span data-ttu-id="fab16-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fab16-142">OUTPUTS</span></span>

### <span data-ttu-id="fab16-143">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="fab16-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="fab16-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fab16-144">NOTES</span></span>

## <span data-ttu-id="fab16-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fab16-145">RELATED LINKS</span></span>

[<span data-ttu-id="fab16-146">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="fab16-146">Get-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="fab16-147">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="fab16-147">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)