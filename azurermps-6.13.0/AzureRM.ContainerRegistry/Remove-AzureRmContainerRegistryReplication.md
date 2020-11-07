---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 7dfb080ae20c583467add8ce298b03199a4f89dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718345"
---
# <span data-ttu-id="eb97f-101">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="eb97f-101">Remove-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="eb97f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eb97f-102">SYNOPSIS</span></span>
<span data-ttu-id="eb97f-103">Usuwa replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="eb97f-103">Removes a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb97f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eb97f-104">SYNTAX</span></span>

### <span data-ttu-id="eb97f-105">NameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="eb97f-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String>
 [-RegistryName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eb97f-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb97f-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -Replicatoin <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb97f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb97f-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb97f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="eb97f-108">DESCRIPTION</span></span>
<span data-ttu-id="eb97f-109">Polecenie cmdlet Remove-AzureRmContainerRegistryReplication usuwa replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="eb97f-109">The Remove-AzureRmContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="eb97f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eb97f-110">EXAMPLES</span></span>

### <span data-ttu-id="eb97f-111">Przykład 1: usunięcie replikacji rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="eb97f-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="eb97f-112">Usuwa replikację rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="eb97f-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="eb97f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eb97f-113">PARAMETERS</span></span>

### <span data-ttu-id="eb97f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb97f-114">-DefaultProfile</span></span>
<span data-ttu-id="eb97f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eb97f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb97f-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eb97f-116">-Name</span></span>
<span data-ttu-id="eb97f-117">Nazwa replikacji rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="eb97f-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="eb97f-118">Domyślnie jest to nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="eb97f-118">Default to the location name.</span></span>

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

### <span data-ttu-id="eb97f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb97f-119">-PassThru</span></span>
<span data-ttu-id="eb97f-120">Wskazuje, że to polecenie cmdlet zwraca wartość PRAWDA, Jeśli usunięcie się powiodło.</span><span class="sxs-lookup"><span data-stu-id="eb97f-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="eb97f-121">-Registryname</span><span class="sxs-lookup"><span data-stu-id="eb97f-121">-RegistryName</span></span>
<span data-ttu-id="eb97f-122">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="eb97f-122">Container Registry Name.</span></span>

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

### <span data-ttu-id="eb97f-123">-Replicatoin</span><span class="sxs-lookup"><span data-stu-id="eb97f-123">-Replicatoin</span></span>
<span data-ttu-id="eb97f-124">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="eb97f-124">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb97f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb97f-125">-ResourceGroupName</span></span>
<span data-ttu-id="eb97f-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="eb97f-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="eb97f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb97f-127">-ResourceId</span></span>
<span data-ttu-id="eb97f-128">Identyfikator zasobu replikacji rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="eb97f-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="eb97f-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eb97f-129">-Confirm</span></span>
<span data-ttu-id="eb97f-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb97f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb97f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb97f-131">-WhatIf</span></span>
<span data-ttu-id="eb97f-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb97f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb97f-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eb97f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb97f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb97f-134">CommonParameters</span></span>
<span data-ttu-id="eb97f-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb97f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb97f-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb97f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb97f-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb97f-137">INPUTS</span></span>

### <span data-ttu-id="eb97f-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="eb97f-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>
<span data-ttu-id="eb97f-139">Parametry: Replicatoin (ByValue)</span><span class="sxs-lookup"><span data-stu-id="eb97f-139">Parameters: Replicatoin (ByValue)</span></span>

### <span data-ttu-id="eb97f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="eb97f-140">System.String</span></span>

## <span data-ttu-id="eb97f-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eb97f-141">OUTPUTS</span></span>

### <span data-ttu-id="eb97f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eb97f-142">System.Boolean</span></span>

## <span data-ttu-id="eb97f-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eb97f-143">NOTES</span></span>

## <span data-ttu-id="eb97f-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb97f-144">RELATED LINKS</span></span>

[<span data-ttu-id="eb97f-145">Nowe — AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="eb97f-145">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="eb97f-146">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="eb97f-146">Get-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)

