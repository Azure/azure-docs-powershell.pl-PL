---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryWebhook.md
ms.openlocfilehash: 1245c92e13af691b0b439d6745a35a917bdf4d89
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223601"
---
# <span data-ttu-id="a1f77-101">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a1f77-101">Test-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="a1f77-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a1f77-102">SYNOPSIS</span></span>
<span data-ttu-id="a1f77-103">Wyzwala zdarzenie ping elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="a1f77-103">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="a1f77-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a1f77-104">SYNTAX</span></span>

### <span data-ttu-id="a1f77-105">ResourceIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a1f77-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1f77-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1f77-106">NameResourceGroupParameterSet</span></span>
```
Test-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1f77-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1f77-107">WebhookObjectParameterSet</span></span>
```
Test-AzContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1f77-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a1f77-108">DESCRIPTION</span></span>
<span data-ttu-id="a1f77-109">Polecenie cmdlet Test-AzContainerRegistryWebhook wyzwala zdarzenie ping elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="a1f77-109">The Test-AzContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="a1f77-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a1f77-110">EXAMPLES</span></span>

### <span data-ttu-id="a1f77-111">Przykład 1. wyzwala zdarzenie ping elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="a1f77-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="a1f77-112">Wyzwala zdarzenie ping elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="a1f77-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="a1f77-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a1f77-113">PARAMETERS</span></span>

### <span data-ttu-id="a1f77-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1f77-114">-DefaultProfile</span></span>
<span data-ttu-id="a1f77-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1f77-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1f77-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a1f77-116">-Name</span></span>
<span data-ttu-id="a1f77-117">Nazwa elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="a1f77-117">Webhook Name.</span></span>

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

### <span data-ttu-id="a1f77-118">-Registryname</span><span class="sxs-lookup"><span data-stu-id="a1f77-118">-RegistryName</span></span>
<span data-ttu-id="a1f77-119">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="a1f77-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="a1f77-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1f77-120">-ResourceGroupName</span></span>
<span data-ttu-id="a1f77-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a1f77-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="a1f77-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1f77-122">-ResourceId</span></span>
<span data-ttu-id="a1f77-123">Identyfikator zasobu elementu webhook rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="a1f77-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="a1f77-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="a1f77-124">-Webhook</span></span>
<span data-ttu-id="a1f77-125">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="a1f77-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="a1f77-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1f77-126">CommonParameters</span></span>
<span data-ttu-id="a1f77-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1f77-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1f77-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1f77-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1f77-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1f77-129">INPUTS</span></span>

### <span data-ttu-id="a1f77-130">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a1f77-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="a1f77-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a1f77-131">System.String</span></span>

## <span data-ttu-id="a1f77-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a1f77-132">OUTPUTS</span></span>

### <span data-ttu-id="a1f77-133">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryEventInfo</span><span class="sxs-lookup"><span data-stu-id="a1f77-133">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="a1f77-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a1f77-134">NOTES</span></span>

## <span data-ttu-id="a1f77-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1f77-135">RELATED LINKS</span></span>

[<span data-ttu-id="a1f77-136">Nowe — AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a1f77-136">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="a1f77-137">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a1f77-137">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="a1f77-138">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a1f77-138">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="a1f77-139">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="a1f77-139">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)