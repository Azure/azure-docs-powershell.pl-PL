---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
ms.openlocfilehash: 231ff710e2c8c2945947ecf2d09845e635ee6244
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181467"
---
# <span data-ttu-id="6de9c-101">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="6de9c-101">Get-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="6de9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6de9c-102">SYNOPSIS</span></span>
<span data-ttu-id="6de9c-103">Pobiera webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="6de9c-103">Gets a container registry webhook.</span></span>

## <span data-ttu-id="6de9c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6de9c-104">SYNTAX</span></span>

### <span data-ttu-id="6de9c-105">ListWebhookByNameResourceGroupParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="6de9c-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6de9c-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="6de9c-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6de9c-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6de9c-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6de9c-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6de9c-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6de9c-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6de9c-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6de9c-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="6de9c-110">DESCRIPTION</span></span>
<span data-ttu-id="6de9c-111">Polecenie Get-AzContainerRegistryWebhook pobiera określony webhook rejestru kontenera lub cały webhoox rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="6de9c-111">The Get-AzContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="6de9c-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6de9c-112">EXAMPLES</span></span>

### <span data-ttu-id="6de9c-113">Przykład 1. Uzyskiwanie określonego webhook rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="6de9c-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="6de9c-114">Uzyskiwanie określonego webhook rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="6de9c-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="6de9c-115">Przykład 2. Uzyskiwanie wszystkich składników Webhoox rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="6de9c-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="6de9c-116">Pobierz całą witrynę internetową rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="6de9c-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="6de9c-117">Przykład 3. Uzyskiwanie określonego webhook rejestru kontenera ze szczegółami konfiguracji</span><span class="sxs-lookup"><span data-stu-id="6de9c-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="6de9c-118">Uzyskiwanie określonego webhook rejestru kontenera ze szczegółami konfiguracji</span><span class="sxs-lookup"><span data-stu-id="6de9c-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="6de9c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6de9c-119">PARAMETERS</span></span>

### <span data-ttu-id="6de9c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6de9c-120">-DefaultProfile</span></span>
<span data-ttu-id="6de9c-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6de9c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6de9c-122">- IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="6de9c-122">-IncludeConfiguration</span></span>
<span data-ttu-id="6de9c-123">Uzyskaj informacje o konfiguracji dla sieci Web.</span><span class="sxs-lookup"><span data-stu-id="6de9c-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="6de9c-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6de9c-124">-Name</span></span>
<span data-ttu-id="6de9c-125">Nazwa przeglądarki Webhook.</span><span class="sxs-lookup"><span data-stu-id="6de9c-125">Webhook Name.</span></span>

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

### <span data-ttu-id="6de9c-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="6de9c-126">-Registry</span></span>
<span data-ttu-id="6de9c-127">Obiekt Container Registry.</span><span class="sxs-lookup"><span data-stu-id="6de9c-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="6de9c-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="6de9c-128">-RegistryName</span></span>
<span data-ttu-id="6de9c-129">Container Registry Name (Nazwa rejestru kontenera).</span><span class="sxs-lookup"><span data-stu-id="6de9c-129">Container Registry Name.</span></span>

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

### <span data-ttu-id="6de9c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6de9c-130">-ResourceGroupName</span></span>
<span data-ttu-id="6de9c-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6de9c-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="6de9c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6de9c-132">-ResourceId</span></span>
<span data-ttu-id="6de9c-133">Identyfikator zasobu webhook kontenera</span><span class="sxs-lookup"><span data-stu-id="6de9c-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="6de9c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6de9c-134">CommonParameters</span></span>
<span data-ttu-id="6de9c-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6de9c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6de9c-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6de9c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6de9c-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6de9c-137">INPUTS</span></span>

### <span data-ttu-id="6de9c-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6de9c-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="6de9c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6de9c-139">System.String</span></span>

## <span data-ttu-id="6de9c-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6de9c-140">OUTPUTS</span></span>

### <span data-ttu-id="6de9c-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="6de9c-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="6de9c-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6de9c-142">NOTES</span></span>

## <span data-ttu-id="6de9c-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6de9c-143">RELATED LINKS</span></span>

[<span data-ttu-id="6de9c-144">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="6de9c-144">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="6de9c-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="6de9c-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="6de9c-146">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="6de9c-146">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="6de9c-147">Test-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="6de9c-147">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)