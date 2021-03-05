---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
ms.openlocfilehash: 36bc713561c739804b358e4b778e17740bd9fb6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977473"
---
# <span data-ttu-id="f1d3d-101">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f1d3d-101">Get-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="f1d3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1d3d-102">SYNOPSIS</span></span>
<span data-ttu-id="f1d3d-103">Pobiera webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-103">Gets a container registry webhook.</span></span>

## <span data-ttu-id="f1d3d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f1d3d-104">SYNTAX</span></span>

### <span data-ttu-id="f1d3d-105">ListWebhookByNameResourceGroupParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f1d3d-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1d3d-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1d3d-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1d3d-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1d3d-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1d3d-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1d3d-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1d3d-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1d3d-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1d3d-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="f1d3d-110">DESCRIPTION</span></span>
<span data-ttu-id="f1d3d-111">Polecenie Get-AzContainerRegistryWebhook pobiera określony webhook rejestru kontenera lub cały webhoox rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-111">The Get-AzContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="f1d3d-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f1d3d-112">EXAMPLES</span></span>

### <span data-ttu-id="f1d3d-113">Przykład 1. Uzyskiwanie określonego webhook rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="f1d3d-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="f1d3d-114">Uzyskiwanie określonego webhook rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="f1d3d-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="f1d3d-115">Przykład 2. Uzyskiwanie wszystkich składników Webhoox rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="f1d3d-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="f1d3d-116">Pobierz całą witrynę internetową rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="f1d3d-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="f1d3d-117">Przykład 3. Uzyskiwanie określonego webhook rejestru kontenera ze szczegółami konfiguracji</span><span class="sxs-lookup"><span data-stu-id="f1d3d-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="f1d3d-118">Uzyskiwanie określonego webhook rejestru kontenera ze szczegółami konfiguracji</span><span class="sxs-lookup"><span data-stu-id="f1d3d-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="f1d3d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1d3d-119">PARAMETERS</span></span>

### <span data-ttu-id="f1d3d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1d3d-120">-DefaultProfile</span></span>
<span data-ttu-id="f1d3d-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1d3d-122">- IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1d3d-122">-IncludeConfiguration</span></span>
<span data-ttu-id="f1d3d-123">Uzyskaj informacje o konfiguracji dla sieci Web.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-123">Get the configuration information for a webhook.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d3d-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f1d3d-124">-Name</span></span>
<span data-ttu-id="f1d3d-125">Nazwa przeglądarki Webhook.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-125">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShowWebhookByNameResourceGroupParameterSet, ShowWebhookByRegistryObjectParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d3d-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="f1d3d-126">-Registry</span></span>
<span data-ttu-id="f1d3d-127">Obiekt Container Registry.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-127">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: ShowWebhookByRegistryObjectParameterSet, ListWebhookByRegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1d3d-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="f1d3d-128">-RegistryName</span></span>
<span data-ttu-id="f1d3d-129">Container Registry Name (Nazwa rejestru kontenera).</span><span class="sxs-lookup"><span data-stu-id="f1d3d-129">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d3d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1d3d-130">-ResourceGroupName</span></span>
<span data-ttu-id="f1d3d-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1d3d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1d3d-132">-ResourceId</span></span>
<span data-ttu-id="f1d3d-133">Identyfikator zasobu webhook kontenera</span><span class="sxs-lookup"><span data-stu-id="f1d3d-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="f1d3d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1d3d-134">CommonParameters</span></span>
<span data-ttu-id="f1d3d-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1d3d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1d3d-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1d3d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1d3d-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1d3d-137">INPUTS</span></span>

### <span data-ttu-id="f1d3d-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f1d3d-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="f1d3d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f1d3d-139">System.String</span></span>

## <span data-ttu-id="f1d3d-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1d3d-140">OUTPUTS</span></span>

### <span data-ttu-id="f1d3d-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f1d3d-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="f1d3d-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f1d3d-142">NOTES</span></span>

## <span data-ttu-id="f1d3d-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1d3d-143">RELATED LINKS</span></span>

[<span data-ttu-id="f1d3d-144">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f1d3d-144">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="f1d3d-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f1d3d-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="f1d3d-146">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f1d3d-146">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="f1d3d-147">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f1d3d-147">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)