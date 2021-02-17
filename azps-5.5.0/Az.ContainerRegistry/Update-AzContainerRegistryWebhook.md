---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
ms.openlocfilehash: 2343b58891109d829a37131dff084b2b51e7f8ad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177323"
---
# <span data-ttu-id="8f2bf-101">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8f2bf-101">Update-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="8f2bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f2bf-102">SYNOPSIS</span></span>
<span data-ttu-id="8f2bf-103">Aktualizuje webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-103">Updates a container registry webhook.</span></span>

## <span data-ttu-id="8f2bf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8f2bf-104">SYNTAX</span></span>

### <span data-ttu-id="8f2bf-105">ResourceIdParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="8f2bf-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>]
 [-Status <String>] [-Scope <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f2bf-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f2bf-106">NameResourceGroupParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f2bf-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f2bf-107">WebhookObjectParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f2bf-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="8f2bf-108">DESCRIPTION</span></span>
<span data-ttu-id="8f2bf-109">Polecenie Update-AzContainerRegistryWebhook cmdlet aktualizuje webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-109">The Update-AzContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="8f2bf-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8f2bf-110">EXAMPLES</span></span>

### <span data-ttu-id="8f2bf-111">Przykład 1. Aktualizowanie istniejącego kontenera rejestru webhook.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="8f2bf-112">Aktualizowanie istniejącego kontenera rejestru webhook.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="8f2bf-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f2bf-113">PARAMETERS</span></span>

### <span data-ttu-id="8f2bf-114">— Akcja</span><span class="sxs-lookup"><span data-stu-id="8f2bf-114">-Action</span></span>
<span data-ttu-id="8f2bf-115">Rozdzielona odstępami lista akcji, które powodują, że aplikacja WebHook może publikować powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f2bf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f2bf-116">-DefaultProfile</span></span>
<span data-ttu-id="8f2bf-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f2bf-118">— Nagłówek</span><span class="sxs-lookup"><span data-stu-id="8f2bf-118">-Header</span></span>
<span data-ttu-id="8f2bf-119">Nagłówki niestandardowe oddzielone spacjami w formacie "key \[ \] =value", które zostaną dodane do powiadomień aplikacji WebHook.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="8f2bf-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8f2bf-120">-Name</span></span>
<span data-ttu-id="8f2bf-121">Nazwa przeglądarki Webhook.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-121">Webhook Name.</span></span>

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

### <span data-ttu-id="8f2bf-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="8f2bf-122">-RegistryName</span></span>
<span data-ttu-id="8f2bf-123">Container Registry Name (Nazwa rejestru kontenera).</span><span class="sxs-lookup"><span data-stu-id="8f2bf-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="8f2bf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f2bf-124">-ResourceGroupName</span></span>
<span data-ttu-id="8f2bf-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="8f2bf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f2bf-126">-ResourceId</span></span>
<span data-ttu-id="8f2bf-127">Identyfikator zasobu webhook kontenera</span><span class="sxs-lookup"><span data-stu-id="8f2bf-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="8f2bf-128">— Zakres</span><span class="sxs-lookup"><span data-stu-id="8f2bf-128">-Scope</span></span>
<span data-ttu-id="8f2bf-129">Zakres webhook.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-129">Webhook scope.</span></span>

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

### <span data-ttu-id="8f2bf-130">— Status</span><span class="sxs-lookup"><span data-stu-id="8f2bf-130">-Status</span></span>
<span data-ttu-id="8f2bf-131">Stan aplikacji Webhook</span><span class="sxs-lookup"><span data-stu-id="8f2bf-131">Webhook status</span></span>

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

### <span data-ttu-id="8f2bf-132">— Tag</span><span class="sxs-lookup"><span data-stu-id="8f2bf-132">-Tag</span></span>
<span data-ttu-id="8f2bf-133">Tagi oddzielone spacjami w \[ formacie "key \] =value".</span><span class="sxs-lookup"><span data-stu-id="8f2bf-133">Space separated tags in 'key\[=value\]' format.</span></span>

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

### <span data-ttu-id="8f2bf-134">-Uri</span><span class="sxs-lookup"><span data-stu-id="8f2bf-134">-Uri</span></span>
<span data-ttu-id="8f2bf-135">The service URI for the webhook to post notifications.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-135">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f2bf-136">- Webhook</span><span class="sxs-lookup"><span data-stu-id="8f2bf-136">-Webhook</span></span>
<span data-ttu-id="8f2bf-137">Container Registry Webhook Object.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-137">Container Registry Webhook Object.</span></span>

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

### <span data-ttu-id="8f2bf-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8f2bf-138">-Confirm</span></span>
<span data-ttu-id="8f2bf-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f2bf-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f2bf-140">-WhatIf</span></span>
<span data-ttu-id="8f2bf-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f2bf-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f2bf-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f2bf-143">CommonParameters</span></span>
<span data-ttu-id="8f2bf-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f2bf-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f2bf-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f2bf-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f2bf-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f2bf-146">INPUTS</span></span>

### <span data-ttu-id="8f2bf-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8f2bf-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="8f2bf-148">System.String</span><span class="sxs-lookup"><span data-stu-id="8f2bf-148">System.String</span></span>

## <span data-ttu-id="8f2bf-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8f2bf-149">OUTPUTS</span></span>

### <span data-ttu-id="8f2bf-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8f2bf-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="8f2bf-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8f2bf-151">NOTES</span></span>

## <span data-ttu-id="8f2bf-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f2bf-152">RELATED LINKS</span></span>

[<span data-ttu-id="8f2bf-153">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8f2bf-153">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="8f2bf-154">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8f2bf-154">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="8f2bf-155">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8f2bf-155">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)

[<span data-ttu-id="8f2bf-156">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8f2bf-156">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)