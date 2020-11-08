---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
ms.openlocfilehash: 231ff710e2c8c2945947ecf2d09845e635ee6244
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221850"
---
# <span data-ttu-id="d6807-101">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d6807-101">Get-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="d6807-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d6807-102">SYNOPSIS</span></span>
<span data-ttu-id="d6807-103">Pobiera element webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="d6807-103">Gets a container registry webhook.</span></span>

## <span data-ttu-id="d6807-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d6807-104">SYNTAX</span></span>

### <span data-ttu-id="d6807-105">ListWebhookByNameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d6807-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6807-106">ShowWebhookByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6807-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6807-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6807-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6807-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6807-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6807-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6807-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6807-110">Opis</span><span class="sxs-lookup"><span data-stu-id="d6807-110">DESCRIPTION</span></span>
<span data-ttu-id="d6807-111">Polecenie cmdlet Get-AzContainerRegistryWebhook powoduje wyświetlenie określonego elementu webhook rejestru kontenera lub wszystkich obiektów webhook rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="d6807-111">The Get-AzContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="d6807-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d6807-112">EXAMPLES</span></span>

### <span data-ttu-id="d6807-113">Przykład 1: uzyskiwanie określonego elementu webhook rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="d6807-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="d6807-114">Uzyskiwanie określonego elementu webhook rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="d6807-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="d6807-115">Przykład 2: uzyskiwanie wszystkich punktów dostępu do rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="d6807-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="d6807-116">Uzyskiwanie wszystkich punktów dostępu do rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="d6807-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="d6807-117">Przykład 3: uzyskiwanie określonego elementu webhook rejestru kontenera za pomocą szczegółów konfiguracji</span><span class="sxs-lookup"><span data-stu-id="d6807-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="d6807-118">Uzyskiwanie określonego elementu webhook rejestru kontenera wraz ze szczegółami konfiguracji</span><span class="sxs-lookup"><span data-stu-id="d6807-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="d6807-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d6807-119">PARAMETERS</span></span>

### <span data-ttu-id="d6807-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6807-120">-DefaultProfile</span></span>
<span data-ttu-id="d6807-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6807-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6807-122">-IncludeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6807-122">-IncludeConfiguration</span></span>
<span data-ttu-id="d6807-123">Uzyskiwanie informacji o konfiguracji elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="d6807-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="d6807-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d6807-124">-Name</span></span>
<span data-ttu-id="d6807-125">Nazwa elementu webhook.</span><span class="sxs-lookup"><span data-stu-id="d6807-125">Webhook Name.</span></span>

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

### <span data-ttu-id="d6807-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="d6807-126">-Registry</span></span>
<span data-ttu-id="d6807-127">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="d6807-127">Container Registry Object.</span></span>

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

### <span data-ttu-id="d6807-128">-Registryname</span><span class="sxs-lookup"><span data-stu-id="d6807-128">-RegistryName</span></span>
<span data-ttu-id="d6807-129">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="d6807-129">Container Registry Name.</span></span>

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

### <span data-ttu-id="d6807-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6807-130">-ResourceGroupName</span></span>
<span data-ttu-id="d6807-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d6807-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="d6807-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6807-132">-ResourceId</span></span>
<span data-ttu-id="d6807-133">Identyfikator zasobu elementu webhook rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="d6807-133">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="d6807-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6807-134">CommonParameters</span></span>
<span data-ttu-id="d6807-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6807-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6807-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6807-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6807-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6807-137">INPUTS</span></span>

### <span data-ttu-id="d6807-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d6807-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="d6807-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d6807-139">System.String</span></span>

## <span data-ttu-id="d6807-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d6807-140">OUTPUTS</span></span>

### <span data-ttu-id="d6807-141">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d6807-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="d6807-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d6807-142">NOTES</span></span>

## <span data-ttu-id="d6807-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6807-143">RELATED LINKS</span></span>

[<span data-ttu-id="d6807-144">Nowe — AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d6807-144">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="d6807-145">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d6807-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="d6807-146">Remove-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d6807-146">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="d6807-147">Test — AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="d6807-147">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)