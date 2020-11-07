---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
ms.openlocfilehash: 8ea10f2acbe69e31bf80e35f0a8ea1577ffac6f5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894845"
---
# <span data-ttu-id="24921-101">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="24921-101">New-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="24921-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="24921-102">SYNOPSIS</span></span>
<span data-ttu-id="24921-103">Tworzy element webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="24921-103">Creates a container registry webhook.</span></span>

## <span data-ttu-id="24921-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="24921-104">SYNTAX</span></span>

### <span data-ttu-id="24921-105">NameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="24921-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24921-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24921-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24921-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24921-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24921-108">Opis</span><span class="sxs-lookup"><span data-stu-id="24921-108">DESCRIPTION</span></span>
<span data-ttu-id="24921-109">Polecenie cmdlet New-AzContainerRegistryWebhook tworzy element webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="24921-109">The New-AzContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="24921-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="24921-110">EXAMPLES</span></span>

### <span data-ttu-id="24921-111">Przykład 1: Tworzenie elementu webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="24921-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="24921-112">Tworzenie elementu webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="24921-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="24921-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="24921-113">PARAMETERS</span></span>

### <span data-ttu-id="24921-114">-Action</span><span class="sxs-lookup"><span data-stu-id="24921-114">-Action</span></span>
<span data-ttu-id="24921-115">Rozdzielana spacjami lista akcji, które powodują, że element webhook ma publikować powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="24921-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24921-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24921-116">-DefaultProfile</span></span>
<span data-ttu-id="24921-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="24921-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24921-118">-Header</span><span class="sxs-lookup"><span data-stu-id="24921-118">-Header</span></span>
<span data-ttu-id="24921-119">Niestandardowe nagłówki, które zostaną dodane do powiadomień elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="24921-119">Custom headers that will be added to the webhook notifications.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: WebhookHeaders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24921-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="24921-120">-Location</span></span>
<span data-ttu-id="24921-121">Lokalizacja elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="24921-121">Webhook Location.</span></span>
<span data-ttu-id="24921-122">Domyślną lokalizacją rejestru.</span><span class="sxs-lookup"><span data-stu-id="24921-122">Default to the location of the registry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24921-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="24921-123">-Name</span></span>
<span data-ttu-id="24921-124">Nazwa elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="24921-124">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24921-125">-Registry</span><span class="sxs-lookup"><span data-stu-id="24921-125">-Registry</span></span>
<span data-ttu-id="24921-126">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="24921-126">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24921-127">-Registryname</span><span class="sxs-lookup"><span data-stu-id="24921-127">-RegistryName</span></span>
<span data-ttu-id="24921-128">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="24921-128">Container Registry Name.</span></span>

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

### <span data-ttu-id="24921-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24921-129">-ResourceGroupName</span></span>
<span data-ttu-id="24921-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="24921-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="24921-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24921-131">-ResourceId</span></span>
<span data-ttu-id="24921-132">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="24921-132">The container registry resource id</span></span>

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

### <span data-ttu-id="24921-133">-Zakres</span><span class="sxs-lookup"><span data-stu-id="24921-133">-Scope</span></span>
<span data-ttu-id="24921-134">Zakres elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="24921-134">Webhook scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookScope

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24921-135">-Status</span><span class="sxs-lookup"><span data-stu-id="24921-135">-Status</span></span>
<span data-ttu-id="24921-136">Stan elementu webhook, wartość domyślna jest włączona</span><span class="sxs-lookup"><span data-stu-id="24921-136">Webhook status, default value is enabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookStatus
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24921-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="24921-137">-Tag</span></span>
<span data-ttu-id="24921-138">Znaczniki elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="24921-138">Webhook tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24921-139">-URI</span><span class="sxs-lookup"><span data-stu-id="24921-139">-Uri</span></span>
<span data-ttu-id="24921-140">Identyfikator URI usługi elementu webhook w celu publikowania powiadomień.</span><span class="sxs-lookup"><span data-stu-id="24921-140">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24921-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="24921-141">-Confirm</span></span>
<span data-ttu-id="24921-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24921-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24921-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24921-143">-WhatIf</span></span>
<span data-ttu-id="24921-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24921-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24921-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="24921-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24921-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24921-146">CommonParameters</span></span>
<span data-ttu-id="24921-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24921-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24921-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24921-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24921-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="24921-149">INPUTS</span></span>

### <span data-ttu-id="24921-150">System. String</span><span class="sxs-lookup"><span data-stu-id="24921-150">System.String</span></span>

## <span data-ttu-id="24921-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="24921-151">OUTPUTS</span></span>

### <span data-ttu-id="24921-152">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="24921-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="24921-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="24921-153">NOTES</span></span>

## <span data-ttu-id="24921-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="24921-154">RELATED LINKS</span></span>

[<span data-ttu-id="24921-155">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="24921-155">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="24921-156">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="24921-156">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="24921-157">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="24921-157">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="24921-158">Test — AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="24921-158">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)