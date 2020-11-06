---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 25b4adeb2d62f1e66bd30cd990db27eadb41b405
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523841"
---
# <span data-ttu-id="df9eb-101">New-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="df9eb-101">New-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="df9eb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df9eb-102">SYNOPSIS</span></span>
<span data-ttu-id="df9eb-103">Tworzy usługę w topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="df9eb-103">Creates a service in a service topology.</span></span>

## <span data-ttu-id="df9eb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df9eb-104">SYNTAX</span></span>

### <span data-ttu-id="df9eb-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="df9eb-105">Interactive (Default)</span></span>
```
New-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 -Name <String> -Location <String> -TargetLocation <String> -TargetSubscriptionId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df9eb-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="df9eb-106">ByServiceTopologyObject</span></span>
```
New-AzureRmDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopology] <PSServiceTopologyResource>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df9eb-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="df9eb-107">ByServiceTopologyResourceId</span></span>
```
New-AzureRmDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df9eb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="df9eb-108">DESCRIPTION</span></span>
<span data-ttu-id="df9eb-109">Polecenie cmdlet **New-AzureRmDeploymentManagerService** tworzy usługę w ramach topologii usług i zwraca obiekt reprezentujący tę usługę.</span><span class="sxs-lookup"><span data-stu-id="df9eb-109">The **New-AzureRmDeploymentManagerService** cmdlet creates a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="df9eb-110">Określ usługę za pomocą jej nazwy, topologii usługi i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="df9eb-110">Specify the service by its name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="df9eb-111">Polecenie cmdlet zwraca obiekt usługi.</span><span class="sxs-lookup"><span data-stu-id="df9eb-111">The cmdlet returns a Service object.</span></span> <span data-ttu-id="df9eb-112">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany w usłudze za pomocą polecenia cmdlet Set-AzureRmDeploymentManagerService.</span><span class="sxs-lookup"><span data-stu-id="df9eb-112">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="df9eb-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df9eb-113">EXAMPLES</span></span>

### <span data-ttu-id="df9eb-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="df9eb-114">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1 -Location "Central US" -TargetLocation "East US" -TargetSubscriptionId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="df9eb-115">Tworzy nową usługę o nazwie ContosoService1 w obszarze Topologia usługi ContosoServiceTopology w grupie zasobów ContosoResourceGroup w lokalizacji Centrala amerykańska.</span><span class="sxs-lookup"><span data-stu-id="df9eb-115">Creates a new service with name ContosoService1 under service topology ContosoServiceTopology in Resource Group ContosoResourceGroup, in the location Central US.</span></span> <span data-ttu-id="df9eb-116">Właściwość TargetLocation wskazuje, że usługa ContosoService1 usługi powinna zostać wdrożona w regionie Stanów Zjednoczonych w określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="df9eb-116">The TargetLocation property indicates that the service ContosoService1 should be deployed to the East US region in the subscription specified.</span></span>

## <span data-ttu-id="df9eb-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df9eb-117">PARAMETERS</span></span>

### <span data-ttu-id="df9eb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df9eb-118">-DefaultProfile</span></span>
<span data-ttu-id="df9eb-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="df9eb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df9eb-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="df9eb-120">-Location</span></span>
<span data-ttu-id="df9eb-121">Lokalizacja zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="df9eb-121">The location of the service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9eb-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="df9eb-122">-Name</span></span>
<span data-ttu-id="df9eb-123">Nazwa usługi.</span><span class="sxs-lookup"><span data-stu-id="df9eb-123">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9eb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df9eb-124">-ResourceGroupName</span></span>
<span data-ttu-id="df9eb-125">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="df9eb-125">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9eb-126">-Servicetopology</span><span class="sxs-lookup"><span data-stu-id="df9eb-126">-ServiceTopology</span></span>
<span data-ttu-id="df9eb-127">Obiekt z topologią usług, w którym ma zostać utworzona usługa.</span><span class="sxs-lookup"><span data-stu-id="df9eb-127">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9eb-128">-ServiceTopologyId</span><span class="sxs-lookup"><span data-stu-id="df9eb-128">-ServiceTopologyId</span></span>
<span data-ttu-id="df9eb-129">Identyfikator zasobu topologii usług, w którym ma zostać utworzona usługa.</span><span class="sxs-lookup"><span data-stu-id="df9eb-129">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9eb-130">-Servicetopologyname</span><span class="sxs-lookup"><span data-stu-id="df9eb-130">-ServiceTopologyName</span></span>
<span data-ttu-id="df9eb-131">Nazwa topologii usług, do której należy ta usługa.</span><span class="sxs-lookup"><span data-stu-id="df9eb-131">The name of the service topology this service belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9eb-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="df9eb-132">-Tag</span></span>
<span data-ttu-id="df9eb-133">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="df9eb-133">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df9eb-134">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="df9eb-134">-TargetLocation</span></span>
<span data-ttu-id="df9eb-135">Określa lokalizację, do której będą wdrażane zasoby w ramach usługi.</span><span class="sxs-lookup"><span data-stu-id="df9eb-135">Determines the location where resources under the service would be deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9eb-136">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="df9eb-136">-TargetSubscriptionId</span></span>
<span data-ttu-id="df9eb-137">Określa abonament, na który zostaną wdrożone zasoby w ramach usługi.</span><span class="sxs-lookup"><span data-stu-id="df9eb-137">Determines the subscription to which resources under the service would be deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9eb-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="df9eb-138">-Confirm</span></span>
<span data-ttu-id="df9eb-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df9eb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df9eb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df9eb-140">-WhatIf</span></span>
<span data-ttu-id="df9eb-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df9eb-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df9eb-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="df9eb-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df9eb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df9eb-143">CommonParameters</span></span>
<span data-ttu-id="df9eb-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df9eb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df9eb-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df9eb-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df9eb-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df9eb-146">INPUTS</span></span>

### <span data-ttu-id="df9eb-147">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="df9eb-147">None</span></span>

## <span data-ttu-id="df9eb-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df9eb-148">OUTPUTS</span></span>

### <span data-ttu-id="df9eb-149">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="df9eb-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="df9eb-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df9eb-150">NOTES</span></span>

## <span data-ttu-id="df9eb-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df9eb-151">RELATED LINKS</span></span>

[<span data-ttu-id="df9eb-152">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="df9eb-152">Get-AzureRmDeploymentManagerService</span></span>](./Get-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="df9eb-153">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="df9eb-153">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="df9eb-154">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="df9eb-154">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)