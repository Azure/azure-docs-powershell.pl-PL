---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
ms.openlocfilehash: da7a024c526baca5f8e41e288d7159c8872cd667
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710135"
---
# <span data-ttu-id="8616b-101">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8616b-101">Update-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="8616b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8616b-102">SYNOPSIS</span></span>
<span data-ttu-id="8616b-103">Umożliwia zaktualizowanie elementu webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="8616b-103">Updates a container registry webhook.</span></span>

## <span data-ttu-id="8616b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8616b-104">SYNTAX</span></span>

### <span data-ttu-id="8616b-105">ResourceIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8616b-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>]
 [-Status <String>] [-Scope <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8616b-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="8616b-106">NameResourceGroupParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8616b-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8616b-107">WebhookObjectParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8616b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8616b-108">DESCRIPTION</span></span>
<span data-ttu-id="8616b-109">Polecenie cmdlet Update-AzContainerRegistryWebhook aktualizuje element webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="8616b-109">The Update-AzContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="8616b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8616b-110">EXAMPLES</span></span>

### <span data-ttu-id="8616b-111">Przykład 1: Aktualizowanie istniejącego elementu webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="8616b-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="8616b-112">Aktualizowanie istniejącego elementu webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="8616b-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="8616b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8616b-113">PARAMETERS</span></span>

### <span data-ttu-id="8616b-114">-Action</span><span class="sxs-lookup"><span data-stu-id="8616b-114">-Action</span></span>
<span data-ttu-id="8616b-115">Rozdzielana spacjami lista akcji, które powodują, że element webhook ma publikować powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="8616b-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="8616b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8616b-116">-DefaultProfile</span></span>
<span data-ttu-id="8616b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8616b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8616b-118">-Header</span><span class="sxs-lookup"><span data-stu-id="8616b-118">-Header</span></span>
<span data-ttu-id="8616b-119">Rozdzielone spacje nagłówki niestandardowe w \[ formacie "klucz = wartość \] ", które zostaną dodane do powiadomień elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="8616b-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="8616b-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8616b-120">-Name</span></span>
<span data-ttu-id="8616b-121">Nazwa elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="8616b-121">Webhook Name.</span></span>

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

### <span data-ttu-id="8616b-122">-Registryname</span><span class="sxs-lookup"><span data-stu-id="8616b-122">-RegistryName</span></span>
<span data-ttu-id="8616b-123">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="8616b-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="8616b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8616b-124">-ResourceGroupName</span></span>
<span data-ttu-id="8616b-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8616b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="8616b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8616b-126">-ResourceId</span></span>
<span data-ttu-id="8616b-127">Identyfikator zasobu elementu webhook rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="8616b-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="8616b-128">-Zakres</span><span class="sxs-lookup"><span data-stu-id="8616b-128">-Scope</span></span>
<span data-ttu-id="8616b-129">Zakres elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="8616b-129">Webhook scope.</span></span>

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

### <span data-ttu-id="8616b-130">-Status</span><span class="sxs-lookup"><span data-stu-id="8616b-130">-Status</span></span>
<span data-ttu-id="8616b-131">Stan elementu webhook</span><span class="sxs-lookup"><span data-stu-id="8616b-131">Webhook status</span></span>

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

### <span data-ttu-id="8616b-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="8616b-132">-Tag</span></span>
<span data-ttu-id="8616b-133">Znaczniki oddzielone spacjami w \[ formacie "klucz = wartość \] ".</span><span class="sxs-lookup"><span data-stu-id="8616b-133">Space separated tags in 'key\[=value\]' format.</span></span>

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

### <span data-ttu-id="8616b-134">-URI</span><span class="sxs-lookup"><span data-stu-id="8616b-134">-Uri</span></span>
<span data-ttu-id="8616b-135">Identyfikator URI usługi elementu webhook w celu publikowania powiadomień.</span><span class="sxs-lookup"><span data-stu-id="8616b-135">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="8616b-136">-Webhook</span><span class="sxs-lookup"><span data-stu-id="8616b-136">-Webhook</span></span>
<span data-ttu-id="8616b-137">Obiekt webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="8616b-137">Container Registry Webhook Object.</span></span>

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

### <span data-ttu-id="8616b-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8616b-138">-Confirm</span></span>
<span data-ttu-id="8616b-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8616b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8616b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8616b-140">-WhatIf</span></span>
<span data-ttu-id="8616b-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8616b-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8616b-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8616b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8616b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8616b-143">CommonParameters</span></span>
<span data-ttu-id="8616b-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8616b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8616b-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8616b-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8616b-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8616b-146">INPUTS</span></span>

### <span data-ttu-id="8616b-147">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8616b-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="8616b-148">System. String</span><span class="sxs-lookup"><span data-stu-id="8616b-148">System.String</span></span>

## <span data-ttu-id="8616b-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8616b-149">OUTPUTS</span></span>

### <span data-ttu-id="8616b-150">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8616b-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="8616b-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8616b-151">NOTES</span></span>

## <span data-ttu-id="8616b-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8616b-152">RELATED LINKS</span></span>

[<span data-ttu-id="8616b-153">Nowe — AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8616b-153">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="8616b-154">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8616b-154">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="8616b-155">Test — AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8616b-155">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)

[<span data-ttu-id="8616b-156">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="8616b-156">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)