---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
ms.openlocfilehash: 717e1ecd7b2242ee5643ca80883e472f5ea4a3c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706083"
---
# <span data-ttu-id="4b05f-101">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4b05f-101">Remove-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="4b05f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4b05f-102">SYNOPSIS</span></span>
<span data-ttu-id="4b05f-103">Usuwa replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="4b05f-103">Removes a container registry replication.</span></span>

## <span data-ttu-id="4b05f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4b05f-104">SYNTAX</span></span>

### <span data-ttu-id="4b05f-105">NameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4b05f-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b05f-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b05f-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -Replication <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b05f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b05f-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b05f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4b05f-108">DESCRIPTION</span></span>
<span data-ttu-id="4b05f-109">Polecenie cmdlet Remove-AzContainerRegistryReplication usuwa replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="4b05f-109">The Remove-AzContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="4b05f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4b05f-110">EXAMPLES</span></span>

### <span data-ttu-id="4b05f-111">Przykład 1: usunięcie replikacji rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="4b05f-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="4b05f-112">Usuwa replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="4b05f-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="4b05f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4b05f-113">PARAMETERS</span></span>

### <span data-ttu-id="4b05f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b05f-114">-DefaultProfile</span></span>
<span data-ttu-id="4b05f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4b05f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b05f-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4b05f-116">-Name</span></span>
<span data-ttu-id="4b05f-117">Nazwa replikacji rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="4b05f-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="4b05f-118">Domyślnie jest to nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="4b05f-118">Default to the location name.</span></span>

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

### <span data-ttu-id="4b05f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b05f-119">-PassThru</span></span>
<span data-ttu-id="4b05f-120">Wskazuje, że to polecenie cmdlet zwraca wartość PRAWDA, Jeśli usunięcie się powiodło.</span><span class="sxs-lookup"><span data-stu-id="4b05f-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="4b05f-121">-Registryname</span><span class="sxs-lookup"><span data-stu-id="4b05f-121">-RegistryName</span></span>
<span data-ttu-id="4b05f-122">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="4b05f-122">Container Registry Name.</span></span>

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

### <span data-ttu-id="4b05f-123">— Replikacja</span><span class="sxs-lookup"><span data-stu-id="4b05f-123">-Replication</span></span>
<span data-ttu-id="4b05f-124">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="4b05f-124">Container Registry Object.</span></span>

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

### <span data-ttu-id="4b05f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b05f-125">-ResourceGroupName</span></span>
<span data-ttu-id="4b05f-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4b05f-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="4b05f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b05f-127">-ResourceId</span></span>
<span data-ttu-id="4b05f-128">Identyfikator zasobu replikacji rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="4b05f-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="4b05f-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4b05f-129">-Confirm</span></span>
<span data-ttu-id="4b05f-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b05f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b05f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b05f-131">-WhatIf</span></span>
<span data-ttu-id="4b05f-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b05f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b05f-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4b05f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b05f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b05f-134">CommonParameters</span></span>
<span data-ttu-id="4b05f-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b05f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b05f-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b05f-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b05f-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b05f-137">INPUTS</span></span>

### <span data-ttu-id="4b05f-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4b05f-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

### <span data-ttu-id="4b05f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4b05f-139">System.String</span></span>

## <span data-ttu-id="4b05f-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4b05f-140">OUTPUTS</span></span>

### <span data-ttu-id="4b05f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4b05f-141">System.Boolean</span></span>

## <span data-ttu-id="4b05f-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4b05f-142">NOTES</span></span>

## <span data-ttu-id="4b05f-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4b05f-143">RELATED LINKS</span></span>

[<span data-ttu-id="4b05f-144">Nowe — AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4b05f-144">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="4b05f-145">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="4b05f-145">Get-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)
