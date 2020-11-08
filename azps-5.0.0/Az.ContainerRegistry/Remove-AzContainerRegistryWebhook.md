---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: 4064728aeffb53fe9f6065d295455738b6a0f046
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224543"
---
# <span data-ttu-id="1fa26-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="1fa26-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="1fa26-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1fa26-102">SYNOPSIS</span></span>
<span data-ttu-id="1fa26-103">Usuwa element webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="1fa26-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="1fa26-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1fa26-104">SYNTAX</span></span>

### <span data-ttu-id="1fa26-105">NameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1fa26-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fa26-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fa26-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fa26-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fa26-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fa26-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1fa26-108">DESCRIPTION</span></span>
<span data-ttu-id="1fa26-109">Polecenie cmdlet Remove-AzContainerRegistryWebhook usuwa element webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="1fa26-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="1fa26-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1fa26-110">EXAMPLES</span></span>

### <span data-ttu-id="1fa26-111">Przykład 1: usunięcie elementu webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="1fa26-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="1fa26-112">Usuwa element webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="1fa26-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="1fa26-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1fa26-113">PARAMETERS</span></span>

### <span data-ttu-id="1fa26-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fa26-114">-DefaultProfile</span></span>
<span data-ttu-id="1fa26-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1fa26-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fa26-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1fa26-116">-Name</span></span>
<span data-ttu-id="1fa26-117">Nazwa elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="1fa26-117">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fa26-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fa26-118">-PassThru</span></span>
<span data-ttu-id="1fa26-119">Wskazuje, że to polecenie cmdlet zwraca wartość PRAWDA, Jeśli usunięcie się powiodło.</span><span class="sxs-lookup"><span data-stu-id="1fa26-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="1fa26-120">-Registryname</span><span class="sxs-lookup"><span data-stu-id="1fa26-120">-RegistryName</span></span>
<span data-ttu-id="1fa26-121">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="1fa26-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="1fa26-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fa26-122">-ResourceGroupName</span></span>
<span data-ttu-id="1fa26-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1fa26-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="1fa26-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fa26-124">-ResourceId</span></span>
<span data-ttu-id="1fa26-125">Identyfikator zasobu elementu webhook rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="1fa26-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="1fa26-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="1fa26-126">-Webhook</span></span>
<span data-ttu-id="1fa26-127">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="1fa26-127">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fa26-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1fa26-128">-Confirm</span></span>
<span data-ttu-id="1fa26-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fa26-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fa26-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fa26-130">-WhatIf</span></span>
<span data-ttu-id="1fa26-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fa26-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fa26-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1fa26-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fa26-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fa26-133">CommonParameters</span></span>
<span data-ttu-id="1fa26-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fa26-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fa26-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1fa26-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fa26-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1fa26-136">INPUTS</span></span>

### <span data-ttu-id="1fa26-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="1fa26-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="1fa26-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1fa26-138">System.String</span></span>

## <span data-ttu-id="1fa26-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1fa26-139">OUTPUTS</span></span>

### <span data-ttu-id="1fa26-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1fa26-140">System.Boolean</span></span>

## <span data-ttu-id="1fa26-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1fa26-141">NOTES</span></span>

## <span data-ttu-id="1fa26-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1fa26-142">RELATED LINKS</span></span>

[<span data-ttu-id="1fa26-143">Nowe — AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="1fa26-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="1fa26-144">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="1fa26-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="1fa26-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="1fa26-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="1fa26-146">Test — AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="1fa26-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)