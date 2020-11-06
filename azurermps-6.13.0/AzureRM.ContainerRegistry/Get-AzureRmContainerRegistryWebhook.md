---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: d2fee7d402ddf25a2bcc4b32528e31e44f500618
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552168"
---
# <span data-ttu-id="b77d3-101">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b77d3-101">Get-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="b77d3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b77d3-102">SYNOPSIS</span></span>
<span data-ttu-id="b77d3-103">Pobiera element webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="b77d3-103">Gets a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b77d3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b77d3-104">SYNTAX</span></span>

### <span data-ttu-id="b77d3-105">ListWebhookByNameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b77d3-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b77d3-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="b77d3-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b77d3-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b77d3-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b77d3-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b77d3-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b77d3-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b77d3-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b77d3-110">Opis</span><span class="sxs-lookup"><span data-stu-id="b77d3-110">DESCRIPTION</span></span>
<span data-ttu-id="b77d3-111">Polecenie cmdlet Get-AzureRmContainerRegistryWebhook powoduje wyświetlenie określonego elementu webhook rejestru kontenera lub wszystkich obiektów webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="b77d3-111">The Get-AzureRmContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="b77d3-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b77d3-112">EXAMPLES</span></span>

### <span data-ttu-id="b77d3-113">Przykład 1: uzyskiwanie określonego elementu webhook rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="b77d3-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="b77d3-114">Uzyskiwanie określonego elementu webhook rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="b77d3-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="b77d3-115">Przykład 2: uzyskiwanie wszystkich punktów dostępu do rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="b77d3-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="b77d3-116">Uzyskiwanie wszystkich punktów dostępu do rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="b77d3-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="b77d3-117">Przykład 3: uzyskiwanie określonego elementu webhook rejestru kontenera za pomocą szczegółów konfiguracji</span><span class="sxs-lookup"><span data-stu-id="b77d3-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="b77d3-118">Uzyskiwanie określonego elementu webhook rejestru kontenera wraz ze szczegółami konfiguracji</span><span class="sxs-lookup"><span data-stu-id="b77d3-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="b77d3-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b77d3-119">PARAMETERS</span></span>

### <span data-ttu-id="b77d3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b77d3-120">-DefaultProfile</span></span>
<span data-ttu-id="b77d3-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b77d3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b77d3-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="b77d3-122">-IncludeConfiguration</span></span>
<span data-ttu-id="b77d3-123">Uzyskiwanie informacji o konfiguracji elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="b77d3-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="b77d3-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b77d3-124">-Name</span></span>
<span data-ttu-id="b77d3-125">Nazwa elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="b77d3-125">Webhook Name.</span></span>

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

### <span data-ttu-id="b77d3-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="b77d3-126">-Registry</span></span>
<span data-ttu-id="b77d3-127">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="b77d3-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="b77d3-128">-Registryname</span><span class="sxs-lookup"><span data-stu-id="b77d3-128">-RegistryName</span></span>
<span data-ttu-id="b77d3-129">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="b77d3-129">Container Registry Name.</span></span>

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

### <span data-ttu-id="b77d3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b77d3-130">-ResourceGroupName</span></span>
<span data-ttu-id="b77d3-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b77d3-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="b77d3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b77d3-132">-ResourceId</span></span>
<span data-ttu-id="b77d3-133">Identyfikator zasobu elementu webhook rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="b77d3-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="b77d3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b77d3-134">CommonParameters</span></span>
<span data-ttu-id="b77d3-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b77d3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b77d3-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b77d3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b77d3-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b77d3-137">INPUTS</span></span>

### <span data-ttu-id="b77d3-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b77d3-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="b77d3-139">Parametry: Registry (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b77d3-139">Parameters: Registry (ByValue)</span></span>

### <span data-ttu-id="b77d3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b77d3-140">System.String</span></span>

## <span data-ttu-id="b77d3-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b77d3-141">OUTPUTS</span></span>

### <span data-ttu-id="b77d3-142">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b77d3-142">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="b77d3-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b77d3-143">NOTES</span></span>

## <span data-ttu-id="b77d3-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b77d3-144">RELATED LINKS</span></span>

[<span data-ttu-id="b77d3-145">Nowe — AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b77d3-145">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="b77d3-146">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b77d3-146">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="b77d3-147">Remove-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b77d3-147">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="b77d3-148">Test — AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="b77d3-148">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)
