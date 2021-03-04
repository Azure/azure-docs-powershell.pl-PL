---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/test-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
ms.openlocfilehash: 837e0fa40bc07ce5c38d6dfd4b7c86efe2425be9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956330"
---
# <span data-ttu-id="fe0b9-101">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fe0b9-101">Test-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="fe0b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe0b9-102">SYNOPSIS</span></span>
<span data-ttu-id="fe0b9-103">Wyzwala zdarzenie ping webhook.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-103">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="fe0b9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fe0b9-104">SYNTAX</span></span>

### <span data-ttu-id="fe0b9-105">ResourceIdParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="fe0b9-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe0b9-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe0b9-106">NameResourceGroupParameterSet</span></span>
```
Test-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe0b9-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe0b9-107">WebhookObjectParameterSet</span></span>
```
Test-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe0b9-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="fe0b9-108">DESCRIPTION</span></span>
<span data-ttu-id="fe0b9-109">Polecenie cmdlet Test-AzContainerRegistryWebhook wyzwala zdarzenie ping webhook.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-109">The Test-AzContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="fe0b9-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fe0b9-110">EXAMPLES</span></span>

### <span data-ttu-id="fe0b9-111">Przykład 1. Wyzwala zdarzenie ping webhook.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="fe0b9-112">Wyzwala zdarzenie ping webhook.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="fe0b9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe0b9-113">PARAMETERS</span></span>

### <span data-ttu-id="fe0b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe0b9-114">-DefaultProfile</span></span>
<span data-ttu-id="fe0b9-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe0b9-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fe0b9-116">-Name</span></span>
<span data-ttu-id="fe0b9-117">Nazwa przeglądarki Webhook.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-117">Webhook Name.</span></span>

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

### <span data-ttu-id="fe0b9-118">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="fe0b9-118">-RegistryName</span></span>
<span data-ttu-id="fe0b9-119">Container Registry Name (Nazwa rejestru kontenera).</span><span class="sxs-lookup"><span data-stu-id="fe0b9-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="fe0b9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe0b9-120">-ResourceGroupName</span></span>
<span data-ttu-id="fe0b9-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="fe0b9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe0b9-122">-ResourceId</span></span>
<span data-ttu-id="fe0b9-123">Identyfikator zasobu webhook kontenera</span><span class="sxs-lookup"><span data-stu-id="fe0b9-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="fe0b9-124">- Webhook</span><span class="sxs-lookup"><span data-stu-id="fe0b9-124">-Webhook</span></span>
<span data-ttu-id="fe0b9-125">Obiekt Container Registry.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="fe0b9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe0b9-126">CommonParameters</span></span>
<span data-ttu-id="fe0b9-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe0b9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe0b9-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe0b9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe0b9-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe0b9-129">INPUTS</span></span>

### <span data-ttu-id="fe0b9-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fe0b9-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="fe0b9-131">System.String</span><span class="sxs-lookup"><span data-stu-id="fe0b9-131">System.String</span></span>

## <span data-ttu-id="fe0b9-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe0b9-132">OUTPUTS</span></span>

### <span data-ttu-id="fe0b9-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span><span class="sxs-lookup"><span data-stu-id="fe0b9-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="fe0b9-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fe0b9-134">NOTES</span></span>

## <span data-ttu-id="fe0b9-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe0b9-135">RELATED LINKS</span></span>

[<span data-ttu-id="fe0b9-136">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fe0b9-136">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="fe0b9-137">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fe0b9-137">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="fe0b9-138">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fe0b9-138">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="fe0b9-139">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fe0b9-139">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)