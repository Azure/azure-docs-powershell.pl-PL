---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceenvironmentinboundservices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironmentInboundServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironmentInboundServices.md
ms.openlocfilehash: 68b2957e959365187ad82980bd2be2f055632a57
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002113"
---
# <span data-ttu-id="4f711-101">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="4f711-101">New-AzAppServiceEnvironmentInboundServices</span></span>

## <span data-ttu-id="4f711-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f711-102">SYNOPSIS</span></span>
<span data-ttu-id="4f711-103">Tworzy usługi przychodzące dla środowiska usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4f711-103">Creates inbound services for App Service Environment.</span></span> <span data-ttu-id="4f711-104">W przypadku protokołu ILB ASEv2 spowoduje to utworzenie prywatnej strefy DNS platformy Azure i rekordów w celu zamapowania ich na wewnętrzny adres IP.</span><span class="sxs-lookup"><span data-stu-id="4f711-104">For ASEv2 ILB, this will create an Azure Private DNS Zone and records to map to the internal IP.</span></span> <span data-ttu-id="4f711-105">W przypadku ustawienia ASEv3 zapewni ono ponadto, że w podsieci podrzędnej zasady sieci są wyłączone, i utworzy prywatny punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="4f711-105">For ASEv3 it will in addition ensure subnet has Network Policy disabled and will create a private endpoint.</span></span>

## <span data-ttu-id="4f711-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4f711-106">SYNTAX</span></span>

### <span data-ttu-id="4f711-107">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f711-107">SubnetNameParameterSet</span></span>
```
New-AzAppServiceEnvironmentInboundServices [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkName <String> -SubnetName <String> [-SkipDns] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f711-108">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f711-108">SubnetIdParameterSet</span></span>
```
New-AzAppServiceEnvironmentInboundServices [-ResourceGroupName] <String> [-Name] <String> -SubnetId <String>
 [-SkipDns] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f711-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="4f711-109">DESCRIPTION</span></span>
<span data-ttu-id="4f711-110">Polecenie **cmdlet New-AzAppServiceEnvironmentInboundServices** umożliwia tworzenie usług przychodzących w środowisku usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4f711-110">The **New-AzAppServiceEnvironmentInboundServices** cmdlet create inbound services for an App Service Environment.</span></span>

## <span data-ttu-id="4f711-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4f711-111">EXAMPLES</span></span>

### <span data-ttu-id="4f711-112">Przykład 1. Tworzenie prywatnej strefy DNS i rekordów dla rekordu ASEv2</span><span class="sxs-lookup"><span data-stu-id="4f711-112">Example 1: Create Private DNS Zone and records for ASEv2</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet
```

<span data-ttu-id="4f711-113">Tworzenie prywatnej strefy DNS i rekordów dla asev2</span><span class="sxs-lookup"><span data-stu-id="4f711-113">Create Private DNS Zone and records for ASEv2</span></span>

### <span data-ttu-id="4f711-114">Przykład 2. Tworzenie prywatnego punktu końcowego, prywatnej strefy DNS i rekordów dla parametru ASEv3</span><span class="sxs-lookup"><span data-stu-id="4f711-114">Example 2: Create private endpoint, Private DNS Zone and records for ASEv3</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet
```

<span data-ttu-id="4f711-115">Tworzenie prywatnego punktu końcowego, prywatnej strefy DNS i rekordów dla rekordu ASEv3</span><span class="sxs-lookup"><span data-stu-id="4f711-115">Create private endpoint, Private DNS Zone and records for ASEv3</span></span>

### <span data-ttu-id="4f711-116">Przykład 3. Tworzenie prywatnego punktu końcowego dla parametru ASEv3</span><span class="sxs-lookup"><span data-stu-id="4f711-116">Example 3: Create private endpoint for ASEv3</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet -SkipDns
```

<span data-ttu-id="4f711-117">Tworzenie prywatnego punktu końcowego dla asev3</span><span class="sxs-lookup"><span data-stu-id="4f711-117">Create private endpoint for ASEv3</span></span>

## <span data-ttu-id="4f711-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f711-118">PARAMETERS</span></span>

### <span data-ttu-id="4f711-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f711-119">-DefaultProfile</span></span>
<span data-ttu-id="4f711-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4f711-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f711-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4f711-121">-Name</span></span>
<span data-ttu-id="4f711-122">Nazwa środowiska usługi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4f711-122">The name of the app service environment.</span></span>

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

### <span data-ttu-id="4f711-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f711-123">-PassThru</span></span>
<span data-ttu-id="4f711-124">Stan zwrotu.</span><span class="sxs-lookup"><span data-stu-id="4f711-124">Return status.</span></span>

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

### <span data-ttu-id="4f711-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f711-125">-ResourceGroupName</span></span>
<span data-ttu-id="4f711-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4f711-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="4f711-127">-SkipDns</span><span class="sxs-lookup"><span data-stu-id="4f711-127">-SkipDns</span></span>
<span data-ttu-id="4f711-128">Nie twórz prywatnej strefy DNS platformy Azure i rekordów.</span><span class="sxs-lookup"><span data-stu-id="4f711-128">Do not create Azure Private DNS Zone and records.</span></span>

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

### <span data-ttu-id="4f711-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4f711-129">-SubnetId</span></span>
<span data-ttu-id="4f711-130">Identyfikator podsieci.</span><span class="sxs-lookup"><span data-stu-id="4f711-130">The subnet id.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f711-131">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="4f711-131">-SubnetName</span></span>
<span data-ttu-id="4f711-132">Nazwa podsieci.</span><span class="sxs-lookup"><span data-stu-id="4f711-132">The subnet name.</span></span> <span data-ttu-id="4f711-133">Używany w połączeniu z wartością -VirtualNetworkName i musi być w tej samej grupie zasobów co ase.</span><span class="sxs-lookup"><span data-stu-id="4f711-133">Used in combination with -VirtualNetworkName and must be in same resource group as ASE.</span></span> <span data-ttu-id="4f711-134">Jeśli nie, użyj funkcji -SubnetId</span><span class="sxs-lookup"><span data-stu-id="4f711-134">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f711-135">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="4f711-135">-VirtualNetworkName</span></span>
<span data-ttu-id="4f711-136">Nazwa sieci vNet.</span><span class="sxs-lookup"><span data-stu-id="4f711-136">The vNet name.</span></span> <span data-ttu-id="4f711-137">Używany w połączeniu z wartością -SubnetName i musi być w tej samej grupie zasobów co ase.</span><span class="sxs-lookup"><span data-stu-id="4f711-137">Used in combination with -SubnetName and must be in same resource group as ASE.</span></span> <span data-ttu-id="4f711-138">Jeśli nie, użyj funkcji -SubnetId</span><span class="sxs-lookup"><span data-stu-id="4f711-138">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f711-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4f711-139">-Confirm</span></span>
<span data-ttu-id="4f711-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4f711-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f711-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f711-141">-WhatIf</span></span>
<span data-ttu-id="4f711-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f711-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f711-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4f711-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f711-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f711-144">CommonParameters</span></span>
<span data-ttu-id="4f711-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f711-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f711-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f711-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f711-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f711-147">INPUTS</span></span>

### <span data-ttu-id="4f711-148">Brak</span><span class="sxs-lookup"><span data-stu-id="4f711-148">None</span></span>

## <span data-ttu-id="4f711-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f711-149">OUTPUTS</span></span>

### <span data-ttu-id="4f711-150">System.Object</span><span class="sxs-lookup"><span data-stu-id="4f711-150">System.Object</span></span>
## <span data-ttu-id="4f711-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4f711-151">NOTES</span></span>

## <span data-ttu-id="4f711-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f711-152">RELATED LINKS</span></span>

[<span data-ttu-id="4f711-153">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="4f711-153">New-AzAppServiceEnvironment</span></span>](./New-AzAppServiceEnvironment.md)

[<span data-ttu-id="4f711-154">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="4f711-154">Get-AzAppServiceEnvironment</span></span>](./Get-AzAppServiceEnvironment.md)

[<span data-ttu-id="4f711-155">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="4f711-155">Remove-AzAppServiceEnvironment</span></span>](./Remove-AzAppServiceEnvironment.md)