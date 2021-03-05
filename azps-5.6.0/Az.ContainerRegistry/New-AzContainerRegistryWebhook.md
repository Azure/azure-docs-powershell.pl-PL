---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/new-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
ms.openlocfilehash: 10acca5a89c4ea84d475e5eea2e89e18942116f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975457"
---
# <span data-ttu-id="e6fec-101">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e6fec-101">New-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="e6fec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6fec-102">SYNOPSIS</span></span>
<span data-ttu-id="e6fec-103">Tworzy webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="e6fec-103">Creates a container registry webhook.</span></span>

## <span data-ttu-id="e6fec-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e6fec-104">SYNTAX</span></span>

### <span data-ttu-id="e6fec-105">NameResourceGroupParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e6fec-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6fec-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6fec-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6fec-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6fec-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6fec-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e6fec-108">DESCRIPTION</span></span>
<span data-ttu-id="e6fec-109">Polecenie New-AzContainerRegistryWebhook cmdlet tworzy webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="e6fec-109">The New-AzContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="e6fec-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e6fec-110">EXAMPLES</span></span>

### <span data-ttu-id="e6fec-111">Przykład 1. Tworzenie kontenera rejestru webhook.</span><span class="sxs-lookup"><span data-stu-id="e6fec-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="e6fec-112">Utwórz webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="e6fec-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="e6fec-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6fec-113">PARAMETERS</span></span>

### <span data-ttu-id="e6fec-114">— Akcja</span><span class="sxs-lookup"><span data-stu-id="e6fec-114">-Action</span></span>
<span data-ttu-id="e6fec-115">Rozdzielona odstępami lista akcji, które powodują, że aplikacja WebHook może publikować powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="e6fec-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="e6fec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6fec-116">-DefaultProfile</span></span>
<span data-ttu-id="e6fec-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6fec-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6fec-118">— Nagłówek</span><span class="sxs-lookup"><span data-stu-id="e6fec-118">-Header</span></span>
<span data-ttu-id="e6fec-119">Nagłówki niestandardowe, które zostaną dodane do powiadomień aplikacji WebHook.</span><span class="sxs-lookup"><span data-stu-id="e6fec-119">Custom headers that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="e6fec-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e6fec-120">-Location</span></span>
<span data-ttu-id="e6fec-121">Lokalizacja w aplikacji Webhook.</span><span class="sxs-lookup"><span data-stu-id="e6fec-121">Webhook Location.</span></span>
<span data-ttu-id="e6fec-122">Domyślna lokalizacja rejestru.</span><span class="sxs-lookup"><span data-stu-id="e6fec-122">Default to the location of the registry.</span></span>

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

### <span data-ttu-id="e6fec-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e6fec-123">-Name</span></span>
<span data-ttu-id="e6fec-124">Nazwa przeglądarki Webhook.</span><span class="sxs-lookup"><span data-stu-id="e6fec-124">Webhook Name.</span></span>

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

### <span data-ttu-id="e6fec-125">-Registry</span><span class="sxs-lookup"><span data-stu-id="e6fec-125">-Registry</span></span>
<span data-ttu-id="e6fec-126">Obiekt Container Registry.</span><span class="sxs-lookup"><span data-stu-id="e6fec-126">Container Registry Object.</span></span>

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

### <span data-ttu-id="e6fec-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="e6fec-127">-RegistryName</span></span>
<span data-ttu-id="e6fec-128">Container Registry Name (Nazwa rejestru kontenera).</span><span class="sxs-lookup"><span data-stu-id="e6fec-128">Container Registry Name.</span></span>

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

### <span data-ttu-id="e6fec-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6fec-129">-ResourceGroupName</span></span>
<span data-ttu-id="e6fec-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e6fec-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="e6fec-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6fec-131">-ResourceId</span></span>
<span data-ttu-id="e6fec-132">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="e6fec-132">The container registry resource id</span></span>

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

### <span data-ttu-id="e6fec-133">— Zakres</span><span class="sxs-lookup"><span data-stu-id="e6fec-133">-Scope</span></span>
<span data-ttu-id="e6fec-134">Zakres webhook.</span><span class="sxs-lookup"><span data-stu-id="e6fec-134">Webhook scope.</span></span>

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

### <span data-ttu-id="e6fec-135">— Status</span><span class="sxs-lookup"><span data-stu-id="e6fec-135">-Status</span></span>
<span data-ttu-id="e6fec-136">Stan webhook, wartość domyślna jest włączona</span><span class="sxs-lookup"><span data-stu-id="e6fec-136">Webhook status, default value is enabled</span></span>

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

### <span data-ttu-id="e6fec-137">— Tag</span><span class="sxs-lookup"><span data-stu-id="e6fec-137">-Tag</span></span>
<span data-ttu-id="e6fec-138">Tagi Webhook.</span><span class="sxs-lookup"><span data-stu-id="e6fec-138">Webhook tags.</span></span>

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

### <span data-ttu-id="e6fec-139">-Uri</span><span class="sxs-lookup"><span data-stu-id="e6fec-139">-Uri</span></span>
<span data-ttu-id="e6fec-140">The service URI for the webhook to post notifications.</span><span class="sxs-lookup"><span data-stu-id="e6fec-140">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="e6fec-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e6fec-141">-Confirm</span></span>
<span data-ttu-id="e6fec-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e6fec-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6fec-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6fec-143">-WhatIf</span></span>
<span data-ttu-id="e6fec-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6fec-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6fec-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e6fec-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6fec-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6fec-146">CommonParameters</span></span>
<span data-ttu-id="e6fec-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6fec-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6fec-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6fec-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6fec-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6fec-149">INPUTS</span></span>

### <span data-ttu-id="e6fec-150">System.String</span><span class="sxs-lookup"><span data-stu-id="e6fec-150">System.String</span></span>

## <span data-ttu-id="e6fec-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6fec-151">OUTPUTS</span></span>

### <span data-ttu-id="e6fec-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e6fec-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="e6fec-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e6fec-153">NOTES</span></span>

## <span data-ttu-id="e6fec-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6fec-154">RELATED LINKS</span></span>

[<span data-ttu-id="e6fec-155">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e6fec-155">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="e6fec-156">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e6fec-156">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="e6fec-157">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e6fec-157">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="e6fec-158">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e6fec-158">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)