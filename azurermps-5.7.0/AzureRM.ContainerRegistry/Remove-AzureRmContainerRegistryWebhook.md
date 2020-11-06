---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/remove-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Remove-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 058c923528227e05a4c8b8078f4495c56edfe20c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526901"
---
# <span data-ttu-id="e2856-101">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e2856-101">Remove-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="e2856-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2856-102">SYNOPSIS</span></span>
<span data-ttu-id="e2856-103">Usuwa element webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="e2856-103">Removes a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2856-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2856-104">SYNTAX</span></span>

### <span data-ttu-id="e2856-105">NameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e2856-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2856-106">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2856-106">WebhookObjectParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -Webhook <PSContainerRegistryWebhook> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2856-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2856-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmContainerRegistryWebhook -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2856-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e2856-108">DESCRIPTION</span></span>
<span data-ttu-id="e2856-109">Polecenie cmdlet Remove-AzureRmContainerRegistryWebhook usuwa element webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="e2856-109">The Remove-AzureRmContainerRegistryWebhook cmdlet removes a container registry webhook.</span></span>

## <span data-ttu-id="e2856-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2856-110">EXAMPLES</span></span>

### <span data-ttu-id="e2856-111">Przykład 1: usunięcie elementu webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="e2856-111">Example 1: Remove a container registry webhook.</span></span>
```powershell
PS C:\> Remove-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"
```

<span data-ttu-id="e2856-112">Usuwa element webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="e2856-112">Removes a container registry webhook.</span></span>

## <span data-ttu-id="e2856-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2856-113">PARAMETERS</span></span>

### <span data-ttu-id="e2856-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e2856-114">-Confirm</span></span>
<span data-ttu-id="e2856-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2856-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2856-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2856-116">-DefaultProfile</span></span>
<span data-ttu-id="e2856-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2856-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2856-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e2856-118">-Name</span></span>
<span data-ttu-id="e2856-119">Nazwa elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="e2856-119">Webhook Name.</span></span>

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

### <span data-ttu-id="e2856-120">-Registryname</span><span class="sxs-lookup"><span data-stu-id="e2856-120">-RegistryName</span></span>
<span data-ttu-id="e2856-121">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="e2856-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="e2856-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2856-122">-ResourceGroupName</span></span>
<span data-ttu-id="e2856-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e2856-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="e2856-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2856-124">-ResourceId</span></span>
<span data-ttu-id="e2856-125">Identyfikator zasobu elementu webhook rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="e2856-125">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="e2856-126">-Webhook</span><span class="sxs-lookup"><span data-stu-id="e2856-126">-Webhook</span></span>
<span data-ttu-id="e2856-127">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="e2856-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="e2856-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2856-128">-WhatIf</span></span>
<span data-ttu-id="e2856-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2856-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2856-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e2856-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2856-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2856-131">-PassThru</span></span>
<span data-ttu-id="e2856-132">Wskazuje, że to polecenie cmdlet zwraca wartość PRAWDA, Jeśli usunięcie się powiodło.</span><span class="sxs-lookup"><span data-stu-id="e2856-132">Indicates that this cmdlet returns true if the removal was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2856-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2856-133">CommonParameters</span></span>
<span data-ttu-id="e2856-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2856-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2856-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2856-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2856-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2856-136">INPUTS</span></span>

### <span data-ttu-id="e2856-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e2856-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="e2856-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e2856-138">System.String</span></span>

## <span data-ttu-id="e2856-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2856-139">OUTPUTS</span></span>

### <span data-ttu-id="e2856-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="e2856-140">System.Object</span></span>

## <span data-ttu-id="e2856-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2856-141">NOTES</span></span>

## <span data-ttu-id="e2856-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2856-142">RELATED LINKS</span></span>

[<span data-ttu-id="e2856-143">Nowe — AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e2856-143">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="e2856-144">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e2856-144">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="e2856-145">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e2856-145">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="e2856-146">Test — AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e2856-146">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
