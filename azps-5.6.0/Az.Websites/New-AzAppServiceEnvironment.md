---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironment.md
ms.openlocfilehash: a922958ec2e15ea9cb4a3b0189f74dda6d71eab2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011137"
---
# <span data-ttu-id="e8ceb-101">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="e8ceb-101">New-AzAppServiceEnvironment</span></span>

## <span data-ttu-id="e8ceb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8ceb-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ceb-103">Tworzy środowisko usługi aplikacji, w tym zalecaną tabelę trasy i grupę zabezpieczeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="e8ceb-103">Creates an App Service Environment including the recommended Route Table and Network Security Group</span></span>

## <span data-ttu-id="e8ceb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e8ceb-104">SYNTAX</span></span>

### <span data-ttu-id="e8ceb-105">ASEv2SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8ceb-105">ASEv2SubnetNameParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -VirtualNetworkName <String> -SubnetName <String> -LoadBalancerMode <String>
 [-SkipRouteTable] [-SkipNetworkSecurityGroup] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8ceb-106">ASEv3SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8ceb-106">ASEv3SubnetNameParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -VirtualNetworkName <String> -SubnetName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8ceb-107">ASEv2SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8ceb-107">ASEv2SubnetIdParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -SubnetId <String> -LoadBalancerMode <String> [-SkipRouteTable] [-SkipNetworkSecurityGroup]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8ceb-108">ASEv3SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8ceb-108">ASEv3SubnetIdParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -SubnetId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8ceb-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="e8ceb-109">DESCRIPTION</span></span>
<span data-ttu-id="e8ceb-110">Polecenie **cmdlet New-AzAppServiceEnvironment** tworzy środowisko usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e8ceb-110">The **New-AzAppServiceEnvironment** cmdlet creates an App Service Environment.</span></span>

## <span data-ttu-id="e8ceb-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e8ceb-111">EXAMPLES</span></span>

### <span data-ttu-id="e8ceb-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e8ceb-112">Example 1</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseV2 -Location WestEurope 
        -VirtualNetworkName MyVirtualNetwork -SubnetName AseSubnet -LoadBalancerMode Internal
```

<span data-ttu-id="e8ceb-113">Tworzenie środowiska usługi aplikacji o nazwie MyAseV2 z uwzględnieniem zalecanej tabeli trasy i grupy zabezpieczeń sieciowych</span><span class="sxs-lookup"><span data-stu-id="e8ceb-113">Create App Service Environment named MyAseV2 including recommended Route Table and Network Security Group</span></span>

### <span data-ttu-id="e8ceb-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e8ceb-114">Example 2</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseV2 -Location WestEurope 
        -VirtualNetworkName MyVirtualNetwork -SubnetName AseSubnet -LoadBalancerMode Internal
        -SkipRouteTable -SkipNetworkSecurityGroup
```

<span data-ttu-id="e8ceb-115">Utwórz środowisko usługi aplikacji o nazwie MyAseV2 bez zalecanej tabeli trasy i grupy zabezpieczeń sieciowych.</span><span class="sxs-lookup"><span data-stu-id="e8ceb-115">Create App Service Environment named MyAseV2 without recommended Route Table and Network Security Group.</span></span>
<span data-ttu-id="e8ceb-116">Należy je utworzyć przed lub bezpośrednio po inicjowaniu obsługi administracyjnej środowiska usługi aplikacji, aby zapewnić wystąpienie funkcjonalności.</span><span class="sxs-lookup"><span data-stu-id="e8ceb-116">These should be create before or right after provisioning the App Service Environment to ensure a functional instance.</span></span>

## <span data-ttu-id="e8ceb-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8ceb-117">PARAMETERS</span></span>

### <span data-ttu-id="e8ceb-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="e8ceb-118">-AsJob</span></span>
<span data-ttu-id="e8ceb-119">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="e8ceb-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e8ceb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ceb-120">-DefaultProfile</span></span>
<span data-ttu-id="e8ceb-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8ceb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8ceb-122">— Rodzaj</span><span class="sxs-lookup"><span data-stu-id="e8ceb-122">-Kind</span></span>
<span data-ttu-id="e8ceb-123">Wersja środowiska usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e8ceb-123">The version of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ASEv2, ASEv3

Required: False
Position: 3
Default value: ASEv2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ceb-124">-LoadBalancerMode</span><span class="sxs-lookup"><span data-stu-id="e8ceb-124">-LoadBalancerMode</span></span>
<span data-ttu-id="e8ceb-125">Tryb równoważenia obciążenia środowiska usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e8ceb-125">Load balancer mode of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:
Accepted values: Internal, External

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ceb-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e8ceb-126">-Location</span></span>
<span data-ttu-id="e8ceb-127">Lokalizacja środowiska usługi aplikacji, na przykład: Europa Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="e8ceb-127">The Location of the app service environment eg: West Europe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ceb-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e8ceb-128">-Name</span></span>
<span data-ttu-id="e8ceb-129">Nazwa środowiska usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e8ceb-129">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ceb-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8ceb-130">-PassThru</span></span>
<span data-ttu-id="e8ceb-131">Zwróć obiekt środowiska usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e8ceb-131">Return the app service environment object.</span></span>

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

### <span data-ttu-id="e8ceb-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8ceb-132">-ResourceGroupName</span></span>
<span data-ttu-id="e8ceb-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e8ceb-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="e8ceb-134">-SkipNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e8ceb-134">-SkipNetworkSecurityGroup</span></span>
<span data-ttu-id="e8ceb-135">Nie należy tworzyć zalecanej grupy zabezpieczeń sieciowych w ramach środowiska usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e8ceb-135">Do not create the recommended network security group as part of the app service environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ceb-136">-SkipRouteTable</span><span class="sxs-lookup"><span data-stu-id="e8ceb-136">-SkipRouteTable</span></span>
<span data-ttu-id="e8ceb-137">Nie należy tworzyć tabeli zalecanej trasy w ramach środowiska usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e8ceb-137">Do not create the recommended route table as part of the app service environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ceb-138">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e8ceb-138">-SubnetId</span></span>
<span data-ttu-id="e8ceb-139">Identyfikator podsieci.</span><span class="sxs-lookup"><span data-stu-id="e8ceb-139">The subnet id.</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetIdParameterSet, ASEv3SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ceb-140">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="e8ceb-140">-SubnetName</span></span>
<span data-ttu-id="e8ceb-141">Nazwa podsieci.</span><span class="sxs-lookup"><span data-stu-id="e8ceb-141">The subnet name.</span></span> <span data-ttu-id="e8ceb-142">Używany w połączeniu z wartością -VirtualNetworkName i musi być w tej samej grupie zasobów co ase.</span><span class="sxs-lookup"><span data-stu-id="e8ceb-142">Used in combination with -VirtualNetworkName and must be in same resource group as ASE.</span></span> <span data-ttu-id="e8ceb-143">Jeśli nie, użyj funkcji -SubnetId</span><span class="sxs-lookup"><span data-stu-id="e8ceb-143">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv3SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ceb-144">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e8ceb-144">-VirtualNetworkName</span></span>
<span data-ttu-id="e8ceb-145">Nazwa sieci vNet.</span><span class="sxs-lookup"><span data-stu-id="e8ceb-145">The vNet name.</span></span> <span data-ttu-id="e8ceb-146">Używany w połączeniu z wartością -SubnetName i musi być w tej samej grupie zasobów co ase.</span><span class="sxs-lookup"><span data-stu-id="e8ceb-146">Used in combination with -SubnetName and must be in same resource group as ASE.</span></span> <span data-ttu-id="e8ceb-147">Jeśli nie, użyj funkcji -SubnetId</span><span class="sxs-lookup"><span data-stu-id="e8ceb-147">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv3SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ceb-148">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8ceb-148">-Confirm</span></span>
<span data-ttu-id="e8ceb-149">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e8ceb-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8ceb-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8ceb-150">-WhatIf</span></span>
<span data-ttu-id="e8ceb-151">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8ceb-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8ceb-152">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e8ceb-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8ceb-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ceb-153">CommonParameters</span></span>
<span data-ttu-id="e8ceb-154">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8ceb-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ceb-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8ceb-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ceb-156">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8ceb-156">INPUTS</span></span>

### <span data-ttu-id="e8ceb-157">Brak</span><span class="sxs-lookup"><span data-stu-id="e8ceb-157">None</span></span>

## <span data-ttu-id="e8ceb-158">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8ceb-158">OUTPUTS</span></span>

### <span data-ttu-id="e8ceb-159">System.Object</span><span class="sxs-lookup"><span data-stu-id="e8ceb-159">System.Object</span></span>
## <span data-ttu-id="e8ceb-160">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e8ceb-160">NOTES</span></span>

## <span data-ttu-id="e8ceb-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8ceb-161">RELATED LINKS</span></span>

[<span data-ttu-id="e8ceb-162">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="e8ceb-162">Get-AzAppServiceEnvironment</span></span>](./Get-AzAppServiceEnvironment.md)

[<span data-ttu-id="e8ceb-163">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="e8ceb-163">New-AzAppServiceEnvironmentInboundServices</span></span>](./New-AzAppServiceEnvironmentInboundServices.md)

[<span data-ttu-id="e8ceb-164">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="e8ceb-164">Remove-AzAppServiceEnvironment</span></span>](./Remove-AzAppServiceEnvironment.md)
