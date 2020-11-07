---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 7515046ed6e9fd6ba5c64b8123f8113b28b53f9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717216"
---
# <span data-ttu-id="69efb-101">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="69efb-101">Update-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="69efb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="69efb-102">SYNOPSIS</span></span>
<span data-ttu-id="69efb-103">Umożliwia zaktualizowanie elementu webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="69efb-103">Updates a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69efb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="69efb-104">SYNTAX</span></span>

### <span data-ttu-id="69efb-105">ResourceIdParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="69efb-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69efb-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="69efb-106">NameResourceGroupParameterSet</span></span>
```
Update-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69efb-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69efb-107">WebhookObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69efb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="69efb-108">DESCRIPTION</span></span>
<span data-ttu-id="69efb-109">Polecenie cmdlet Update-AzureRmContainerRegistryWebhook aktualizuje element webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="69efb-109">The Update-AzureRmContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="69efb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="69efb-110">EXAMPLES</span></span>

### <span data-ttu-id="69efb-111">Przykład 1: Aktualizowanie istniejącego elementu webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="69efb-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="69efb-112">Aktualizowanie istniejącego elementu webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="69efb-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="69efb-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69efb-113">PARAMETERS</span></span>

### <span data-ttu-id="69efb-114">-Action</span><span class="sxs-lookup"><span data-stu-id="69efb-114">-Action</span></span>
<span data-ttu-id="69efb-115">Rozdzielana spacjami lista akcji, które powodują, że element webhook ma publikować powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="69efb-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69efb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69efb-116">-DefaultProfile</span></span>
<span data-ttu-id="69efb-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="69efb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69efb-118">-Header</span><span class="sxs-lookup"><span data-stu-id="69efb-118">-Header</span></span>
<span data-ttu-id="69efb-119">Rozdzielone spacje nagłówki niestandardowe w \[ formacie "klucz = wartość \] ", które zostaną dodane do powiadomień elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="69efb-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: WebhookHeaders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69efb-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="69efb-120">-Name</span></span>
<span data-ttu-id="69efb-121">Nazwa elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="69efb-121">Webhook Name.</span></span>

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

### <span data-ttu-id="69efb-122">-Registryname</span><span class="sxs-lookup"><span data-stu-id="69efb-122">-RegistryName</span></span>
<span data-ttu-id="69efb-123">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="69efb-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="69efb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69efb-124">-ResourceGroupName</span></span>
<span data-ttu-id="69efb-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="69efb-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="69efb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69efb-126">-ResourceId</span></span>
<span data-ttu-id="69efb-127">Identyfikator zasobu elementu webhook rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="69efb-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="69efb-128">-Zakres</span><span class="sxs-lookup"><span data-stu-id="69efb-128">-Scope</span></span>
<span data-ttu-id="69efb-129">Zakres elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="69efb-129">Webhook scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookScope

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69efb-130">-Status</span><span class="sxs-lookup"><span data-stu-id="69efb-130">-Status</span></span>
<span data-ttu-id="69efb-131">Stan elementu webhook</span><span class="sxs-lookup"><span data-stu-id="69efb-131">Webhook status</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookStatus
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69efb-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="69efb-132">-Tag</span></span>
<span data-ttu-id="69efb-133">Znaczniki oddzielone spacjami w \[ formacie "klucz = wartość \] ".</span><span class="sxs-lookup"><span data-stu-id="69efb-133">Space separated tags in 'key\[=value\]' format.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69efb-134">-URI</span><span class="sxs-lookup"><span data-stu-id="69efb-134">-Uri</span></span>
<span data-ttu-id="69efb-135">Identyfikator URI usługi elementu webhook w celu publikowania powiadomień.</span><span class="sxs-lookup"><span data-stu-id="69efb-135">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69efb-136">-Webhook</span><span class="sxs-lookup"><span data-stu-id="69efb-136">-Webhook</span></span>
<span data-ttu-id="69efb-137">Obiekt webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="69efb-137">Container Registry Webhook Object.</span></span>

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

### <span data-ttu-id="69efb-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69efb-138">-Confirm</span></span>
<span data-ttu-id="69efb-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69efb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69efb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69efb-140">-WhatIf</span></span>
<span data-ttu-id="69efb-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69efb-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69efb-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="69efb-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69efb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69efb-143">CommonParameters</span></span>
<span data-ttu-id="69efb-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69efb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69efb-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69efb-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69efb-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69efb-146">INPUTS</span></span>

### <span data-ttu-id="69efb-147">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="69efb-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="69efb-148">System. String</span><span class="sxs-lookup"><span data-stu-id="69efb-148">System.String</span></span>

## <span data-ttu-id="69efb-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="69efb-149">OUTPUTS</span></span>

### <span data-ttu-id="69efb-150">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="69efb-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="69efb-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="69efb-151">NOTES</span></span>

## <span data-ttu-id="69efb-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69efb-152">RELATED LINKS</span></span>

[<span data-ttu-id="69efb-153">Nowe — AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="69efb-153">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="69efb-154">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="69efb-154">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="69efb-155">Test — AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="69efb-155">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="69efb-156">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="69efb-156">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)
