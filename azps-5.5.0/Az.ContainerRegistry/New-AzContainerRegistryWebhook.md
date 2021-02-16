---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
ms.openlocfilehash: 8ea10f2acbe69e31bf80e35f0a8ea1577ffac6f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199130"
---
# <span data-ttu-id="7f7f5-101">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7f7f5-101">New-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="7f7f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f7f5-102">SYNOPSIS</span></span>
<span data-ttu-id="7f7f5-103">Tworzy webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="7f7f5-103">Creates a container registry webhook.</span></span>

## <span data-ttu-id="7f7f5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7f7f5-104">SYNTAX</span></span>

### <span data-ttu-id="7f7f5-105">NameResourceGroupParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="7f7f5-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f7f5-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f7f5-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f7f5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f7f5-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f7f5-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7f7f5-108">DESCRIPTION</span></span>
<span data-ttu-id="7f7f5-109">Polecenie New-AzContainerRegistryWebhook cmdlet tworzy webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="7f7f5-109">The New-AzContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="7f7f5-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7f7f5-110">EXAMPLES</span></span>

### <span data-ttu-id="7f7f5-111">Przykład 1. Tworzenie kontenera rejestru webhook.</span><span class="sxs-lookup"><span data-stu-id="7f7f5-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="7f7f5-112">Utwórz webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="7f7f5-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="7f7f5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f7f5-113">PARAMETERS</span></span>

### <span data-ttu-id="7f7f5-114">— akcja</span><span class="sxs-lookup"><span data-stu-id="7f7f5-114">-Action</span></span>
<span data-ttu-id="7f7f5-115">Rozdzielona odstępami lista akcji, które powodują, że aplikacja WebHook może publikować powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="7f7f5-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="7f7f5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f7f5-116">-DefaultProfile</span></span>
<span data-ttu-id="7f7f5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7f7f5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f7f5-118">— Nagłówek</span><span class="sxs-lookup"><span data-stu-id="7f7f5-118">-Header</span></span>
<span data-ttu-id="7f7f5-119">Nagłówki niestandardowe, które zostaną dodane do powiadomień aplikacji WebHook.</span><span class="sxs-lookup"><span data-stu-id="7f7f5-119">Custom headers that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="7f7f5-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7f7f5-120">-Location</span></span>
<span data-ttu-id="7f7f5-121">Lokalizacja w aplikacji Webhook.</span><span class="sxs-lookup"><span data-stu-id="7f7f5-121">Webhook Location.</span></span>
<span data-ttu-id="7f7f5-122">Domyślna lokalizacja rejestru.</span><span class="sxs-lookup"><span data-stu-id="7f7f5-122">Default to the location of the registry.</span></span>

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

### <span data-ttu-id="7f7f5-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7f7f5-123">-Name</span></span>
<span data-ttu-id="7f7f5-124">Nazwa przeglądarki Webhook.</span><span class="sxs-lookup"><span data-stu-id="7f7f5-124">Webhook Name.</span></span>

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

### <span data-ttu-id="7f7f5-125">-Registry</span><span class="sxs-lookup"><span data-stu-id="7f7f5-125">-Registry</span></span>
<span data-ttu-id="7f7f5-126">Obiekt Container Registry.</span><span class="sxs-lookup"><span data-stu-id="7f7f5-126">Container Registry Object.</span></span>

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

### <span data-ttu-id="7f7f5-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="7f7f5-127">-RegistryName</span></span>
<span data-ttu-id="7f7f5-128">Container Registry Name (Nazwa rejestru kontenera).</span><span class="sxs-lookup"><span data-stu-id="7f7f5-128">Container Registry Name.</span></span>

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

### <span data-ttu-id="7f7f5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f7f5-129">-ResourceGroupName</span></span>
<span data-ttu-id="7f7f5-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7f7f5-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="7f7f5-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f7f5-131">-ResourceId</span></span>
<span data-ttu-id="7f7f5-132">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="7f7f5-132">The container registry resource id</span></span>

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

### <span data-ttu-id="7f7f5-133">— Zakres</span><span class="sxs-lookup"><span data-stu-id="7f7f5-133">-Scope</span></span>
<span data-ttu-id="7f7f5-134">Zakres webhook.</span><span class="sxs-lookup"><span data-stu-id="7f7f5-134">Webhook scope.</span></span>

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

### <span data-ttu-id="7f7f5-135">— Status</span><span class="sxs-lookup"><span data-stu-id="7f7f5-135">-Status</span></span>
<span data-ttu-id="7f7f5-136">Stan webhook, wartość domyślna jest włączona</span><span class="sxs-lookup"><span data-stu-id="7f7f5-136">Webhook status, default value is enabled</span></span>

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

### <span data-ttu-id="7f7f5-137">— Tag</span><span class="sxs-lookup"><span data-stu-id="7f7f5-137">-Tag</span></span>
<span data-ttu-id="7f7f5-138">Tagi Webhook.</span><span class="sxs-lookup"><span data-stu-id="7f7f5-138">Webhook tags.</span></span>

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

### <span data-ttu-id="7f7f5-139">-Uri</span><span class="sxs-lookup"><span data-stu-id="7f7f5-139">-Uri</span></span>
<span data-ttu-id="7f7f5-140">The service URI for the webhook to post notifications.</span><span class="sxs-lookup"><span data-stu-id="7f7f5-140">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="7f7f5-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7f7f5-141">-Confirm</span></span>
<span data-ttu-id="7f7f5-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7f7f5-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f7f5-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f7f5-143">-WhatIf</span></span>
<span data-ttu-id="7f7f5-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f7f5-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f7f5-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7f7f5-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f7f5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f7f5-146">CommonParameters</span></span>
<span data-ttu-id="7f7f5-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f7f5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f7f5-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f7f5-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f7f5-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7f7f5-149">INPUTS</span></span>

### <span data-ttu-id="7f7f5-150">System.String</span><span class="sxs-lookup"><span data-stu-id="7f7f5-150">System.String</span></span>

## <span data-ttu-id="7f7f5-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7f7f5-151">OUTPUTS</span></span>

### <span data-ttu-id="7f7f5-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7f7f5-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="7f7f5-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7f7f5-153">NOTES</span></span>

## <span data-ttu-id="7f7f5-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7f7f5-154">RELATED LINKS</span></span>

[<span data-ttu-id="7f7f5-155">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7f7f5-155">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="7f7f5-156">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7f7f5-156">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="7f7f5-157">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7f7f5-157">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="7f7f5-158">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7f7f5-158">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)