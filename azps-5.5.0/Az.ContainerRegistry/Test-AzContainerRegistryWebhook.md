---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
ms.openlocfilehash: 1245c92e13af691b0b439d6745a35a917bdf4d89
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243939"
---
# <span data-ttu-id="0ca4e-101">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0ca4e-101">Test-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="0ca4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ca4e-102">SYNOPSIS</span></span>
<span data-ttu-id="0ca4e-103">Wyzwala zdarzenie ping webhook.</span><span class="sxs-lookup"><span data-stu-id="0ca4e-103">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="0ca4e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0ca4e-104">SYNTAX</span></span>

### <span data-ttu-id="0ca4e-105">ResourceIdParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="0ca4e-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ca4e-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ca4e-106">NameResourceGroupParameterSet</span></span>
```
Test-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ca4e-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ca4e-107">WebhookObjectParameterSet</span></span>
```
Test-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ca4e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="0ca4e-108">DESCRIPTION</span></span>
<span data-ttu-id="0ca4e-109">Polecenie cmdlet Test-AzContainerRegistryWebhook wyzwala zdarzenie ping webhook.</span><span class="sxs-lookup"><span data-stu-id="0ca4e-109">The Test-AzContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="0ca4e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0ca4e-110">EXAMPLES</span></span>

### <span data-ttu-id="0ca4e-111">Przykład 1. Wyzwala zdarzenie ping webhook.</span><span class="sxs-lookup"><span data-stu-id="0ca4e-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="0ca4e-112">Wyzwala zdarzenie ping webhook.</span><span class="sxs-lookup"><span data-stu-id="0ca4e-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="0ca4e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ca4e-113">PARAMETERS</span></span>

### <span data-ttu-id="0ca4e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ca4e-114">-DefaultProfile</span></span>
<span data-ttu-id="0ca4e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ca4e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ca4e-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0ca4e-116">-Name</span></span>
<span data-ttu-id="0ca4e-117">Nazwa przeglądarki Webhook.</span><span class="sxs-lookup"><span data-stu-id="0ca4e-117">Webhook Name.</span></span>

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

### <span data-ttu-id="0ca4e-118">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="0ca4e-118">-RegistryName</span></span>
<span data-ttu-id="0ca4e-119">Container Registry Name (Nazwa rejestru kontenera).</span><span class="sxs-lookup"><span data-stu-id="0ca4e-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="0ca4e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ca4e-120">-ResourceGroupName</span></span>
<span data-ttu-id="0ca4e-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0ca4e-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="0ca4e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ca4e-122">-ResourceId</span></span>
<span data-ttu-id="0ca4e-123">Identyfikator zasobu webhook kontenera</span><span class="sxs-lookup"><span data-stu-id="0ca4e-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="0ca4e-124">- Webhook</span><span class="sxs-lookup"><span data-stu-id="0ca4e-124">-Webhook</span></span>
<span data-ttu-id="0ca4e-125">Obiekt Container Registry.</span><span class="sxs-lookup"><span data-stu-id="0ca4e-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="0ca4e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ca4e-126">CommonParameters</span></span>
<span data-ttu-id="0ca4e-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ca4e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ca4e-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ca4e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ca4e-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ca4e-129">INPUTS</span></span>

### <span data-ttu-id="0ca4e-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0ca4e-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="0ca4e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="0ca4e-131">System.String</span></span>

## <span data-ttu-id="0ca4e-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ca4e-132">OUTPUTS</span></span>

### <span data-ttu-id="0ca4e-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span><span class="sxs-lookup"><span data-stu-id="0ca4e-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="0ca4e-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0ca4e-134">NOTES</span></span>

## <span data-ttu-id="0ca4e-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ca4e-135">RELATED LINKS</span></span>

[<span data-ttu-id="0ca4e-136">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0ca4e-136">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="0ca4e-137">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0ca4e-137">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="0ca4e-138">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0ca4e-138">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="0ca4e-139">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="0ca4e-139">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)