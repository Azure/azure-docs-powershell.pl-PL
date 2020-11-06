---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 02d16be7c41a95c32d4aa7b6f3231b68c0ba7244
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546808"
---
# <span data-ttu-id="02ee5-101">Test-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="02ee5-101">Test-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="02ee5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02ee5-102">SYNOPSIS</span></span>
<span data-ttu-id="02ee5-103">Wyzwala zdarzenie ping elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="02ee5-103">Triggers a webhook ping event.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02ee5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02ee5-104">SYNTAX</span></span>

### <span data-ttu-id="02ee5-105">ResourceIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="02ee5-105">ResourceIdParameterSet (Default)</span></span>
```
Test-AzureRmContainerRegistryWebhook -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="02ee5-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="02ee5-106">NameResourceGroupParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02ee5-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02ee5-107">WebhookObjectParameterSet</span></span>
```
Test-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02ee5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="02ee5-108">DESCRIPTION</span></span>
<span data-ttu-id="02ee5-109">Polecenie cmdlet Test-AzureRmContainerRegistryWebhook wyzwala zdarzenie ping elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="02ee5-109">The Test-AzureRmContainerRegistryWebhook cmdlet triggers a webhook ping event.</span></span>

## <span data-ttu-id="02ee5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02ee5-110">EXAMPLES</span></span>

### <span data-ttu-id="02ee5-111">Przykład 1. wyzwala zdarzenie ping elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="02ee5-111">Example 1: Triggers a webhook ping event.</span></span>
```powershell
PS C:\> Test-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Id
--
c5950af0-c8d0-4924-9873-1ba7da5cbf83
```

<span data-ttu-id="02ee5-112">Wyzwala zdarzenie ping elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="02ee5-112">Triggers a webhook ping event.</span></span>

## <span data-ttu-id="02ee5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02ee5-113">PARAMETERS</span></span>

### <span data-ttu-id="02ee5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02ee5-114">-DefaultProfile</span></span>
<span data-ttu-id="02ee5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="02ee5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ee5-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="02ee5-116">-Name</span></span>
<span data-ttu-id="02ee5-117">Nazwa elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="02ee5-117">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ee5-118">-Registryname</span><span class="sxs-lookup"><span data-stu-id="02ee5-118">-RegistryName</span></span>
<span data-ttu-id="02ee5-119">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="02ee5-119">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ee5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02ee5-120">-ResourceGroupName</span></span>
<span data-ttu-id="02ee5-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="02ee5-121">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ee5-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02ee5-122">-ResourceId</span></span>
<span data-ttu-id="02ee5-123">Identyfikator zasobu elementu webhook rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="02ee5-123">The container registry Webhook resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02ee5-124">-Webhook</span><span class="sxs-lookup"><span data-stu-id="02ee5-124">-Webhook</span></span>
<span data-ttu-id="02ee5-125">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="02ee5-125">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02ee5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02ee5-126">CommonParameters</span></span>
<span data-ttu-id="02ee5-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02ee5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02ee5-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02ee5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02ee5-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02ee5-129">INPUTS</span></span>

### <span data-ttu-id="02ee5-130">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="02ee5-130">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="02ee5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="02ee5-131">System.String</span></span>

## <span data-ttu-id="02ee5-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02ee5-132">OUTPUTS</span></span>

### <span data-ttu-id="02ee5-133">Microsoft. Azure. Management. ContainerRegistry. MODELES. EventInfo</span><span class="sxs-lookup"><span data-stu-id="02ee5-133">Microsoft.Azure.Management.ContainerRegistry.Models.EventInfo</span></span>

## <span data-ttu-id="02ee5-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02ee5-134">NOTES</span></span>

## <span data-ttu-id="02ee5-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02ee5-135">RELATED LINKS</span></span>

[<span data-ttu-id="02ee5-136">Nowe — AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="02ee5-136">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="02ee5-137">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="02ee5-137">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="02ee5-138">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="02ee5-138">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="02ee5-139">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="02ee5-139">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)
