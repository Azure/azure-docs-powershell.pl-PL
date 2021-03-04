---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryWebhook.md
ms.openlocfilehash: e189be8f04081bbc51c5cc19b981c164ce4e9c2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956394"
---
# <span data-ttu-id="def9c-101">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="def9c-101">Remove-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="def9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="def9c-102">SYNOPSIS</span></span>
<span data-ttu-id="def9c-103">Usuwa webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="def9c-103">Removes a container registry webhook.</span></span>

## <span data-ttu-id="def9c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="def9c-104">SYNTAX</span></span>

### <span data-ttu-id="def9c-105">NameResourceGroupParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="def9c-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="def9c-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="def9c-106">WebhookObjectParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="def9c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="def9c-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryWebhook -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="def9c-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="def9c-108">DESCRIPTION</span></span>
<span data-ttu-id="def9c-109">Polecenie Remove-AzContainerRegistryWebhook cmdlet usuwa webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="def9c-109">The Remove-AzContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="def9c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="def9c-110">EXAMPLES</span></span>

### <span data-ttu-id="def9c-111">Przykład 1. Usunięcie kontenera rejestru webhook.</span><span class="sxs-lookup"><span data-stu-id="def9c-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="def9c-112">Usuwa webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="def9c-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="def9c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="def9c-113">PARAMETERS</span></span>

### <span data-ttu-id="def9c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="def9c-114">-DefaultProfile</span></span>
<span data-ttu-id="def9c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="def9c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="def9c-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="def9c-116">-Name</span></span>
<span data-ttu-id="def9c-117">Nazwa przeglądarki Webhook.</span><span class="sxs-lookup"><span data-stu-id="def9c-117">Webhook Name.</span></span>

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

### <span data-ttu-id="def9c-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="def9c-118">-PassThru</span></span>
<span data-ttu-id="def9c-119">Wskazuje, że to polecenie cmdlet zwraca wartość prawda, jeśli usunięcie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="def9c-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="def9c-120">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="def9c-120">-RegistryName</span></span>
<span data-ttu-id="def9c-121">Container Registry Name (Nazwa rejestru kontenera).</span><span class="sxs-lookup"><span data-stu-id="def9c-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="def9c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="def9c-122">-ResourceGroupName</span></span>
<span data-ttu-id="def9c-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="def9c-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="def9c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="def9c-124">-ResourceId</span></span>
<span data-ttu-id="def9c-125">Identyfikator zasobu webhook kontenera</span><span class="sxs-lookup"><span data-stu-id="def9c-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="def9c-126">- Webhook</span><span class="sxs-lookup"><span data-stu-id="def9c-126">-Webhook</span></span>
<span data-ttu-id="def9c-127">Obiekt Container Registry.</span><span class="sxs-lookup"><span data-stu-id="def9c-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="def9c-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="def9c-128">-Confirm</span></span>
<span data-ttu-id="def9c-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="def9c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="def9c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="def9c-130">-WhatIf</span></span>
<span data-ttu-id="def9c-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="def9c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="def9c-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="def9c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="def9c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="def9c-133">CommonParameters</span></span>
<span data-ttu-id="def9c-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="def9c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="def9c-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="def9c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="def9c-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="def9c-136">INPUTS</span></span>

### <span data-ttu-id="def9c-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="def9c-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="def9c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="def9c-138">System.String</span></span>

## <span data-ttu-id="def9c-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="def9c-139">OUTPUTS</span></span>

### <span data-ttu-id="def9c-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="def9c-140">System.Boolean</span></span>

## <span data-ttu-id="def9c-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="def9c-141">NOTES</span></span>

## <span data-ttu-id="def9c-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="def9c-142">RELATED LINKS</span></span>

[<span data-ttu-id="def9c-143">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="def9c-143">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="def9c-144">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="def9c-144">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="def9c-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="def9c-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="def9c-146">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="def9c-146">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)