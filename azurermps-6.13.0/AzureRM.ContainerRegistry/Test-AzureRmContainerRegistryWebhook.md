---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 0a5894a411f4ffb5b3bde28db68961d321584e1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716784"
---
# <span data-ttu-id="fc602-101">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fc602-101">Test-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="fc602-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fc602-102">SYNOPSIS</span></span>
<span data-ttu-id="fc602-103">Wyzwala zdarzenie ping elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="fc602-103">Triggers a webhook ping event.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc602-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fc602-104">SYNTAX</span></span>

### <span data-ttu-id="fc602-105">ResourceIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fc602-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzureRmContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc602-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc602-106">NameResourceGroupParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc602-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc602-107">WebhookObjectParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc602-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fc602-108">DESCRIPTION</span></span>
<span data-ttu-id="fc602-109">Polecenie cmdlet Test-AzureRmContainerRegistryWebhook wyzwala zdarzenie ping elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="fc602-109">The Test-AzureRmContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="fc602-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fc602-110">EXAMPLES</span></span>

### <span data-ttu-id="fc602-111">Przykład 1. wyzwala zdarzenie ping elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="fc602-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="fc602-112">Wyzwala zdarzenie ping elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="fc602-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="fc602-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fc602-113">PARAMETERS</span></span>

### <span data-ttu-id="fc602-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc602-114">-DefaultProfile</span></span>
<span data-ttu-id="fc602-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fc602-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc602-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fc602-116">-Name</span></span>
<span data-ttu-id="fc602-117">Nazwa elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="fc602-117">Webhook Name.</span></span>

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

### <span data-ttu-id="fc602-118">-Registryname</span><span class="sxs-lookup"><span data-stu-id="fc602-118">-RegistryName</span></span>
<span data-ttu-id="fc602-119">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="fc602-119">Container Registry Name.</span></span>

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

### <span data-ttu-id="fc602-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc602-120">-ResourceGroupName</span></span>
<span data-ttu-id="fc602-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc602-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="fc602-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc602-122">-ResourceId</span></span>
<span data-ttu-id="fc602-123">Identyfikator zasobu elementu webhook rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="fc602-123">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="fc602-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="fc602-124">-Webhook</span></span>
<span data-ttu-id="fc602-125">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="fc602-125">Container Registry Object.</span></span>

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

### <span data-ttu-id="fc602-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc602-126">CommonParameters</span></span>
<span data-ttu-id="fc602-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc602-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc602-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc602-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc602-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc602-129">INPUTS</span></span>

### <span data-ttu-id="fc602-130">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fc602-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="fc602-131">Parametry: webhook (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fc602-131">Parameters: Webhook (ByValue)</span></span>

### <span data-ttu-id="fc602-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fc602-132">System.String</span></span>

## <span data-ttu-id="fc602-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fc602-133">OUTPUTS</span></span>

### <span data-ttu-id="fc602-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryEventInfo</span><span class="sxs-lookup"><span data-stu-id="fc602-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryEventInfo</span></span>

## <span data-ttu-id="fc602-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fc602-135">NOTES</span></span>

## <span data-ttu-id="fc602-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc602-136">RELATED LINKS</span></span>

[<span data-ttu-id="fc602-137">Nowe — AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fc602-137">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="fc602-138">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fc602-138">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="fc602-139">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fc602-139">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="fc602-140">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="fc602-140">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)
