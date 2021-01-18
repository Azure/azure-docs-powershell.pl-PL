---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: 0855ba4e7e16503045d13c370838cd5d3fffb033
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501258"
---
# <span data-ttu-id="d3abb-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d3abb-101">New-AzNatGateway</span></span>

## <span data-ttu-id="d3abb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d3abb-102">SYNOPSIS</span></span>
<span data-ttu-id="d3abb-103">Tworzenie nowego zasobu bramy NAT z właściwościami publiczny adres IP/publiczny prefiks IP, IdleTimeoutInMinutes i SKU.</span><span class="sxs-lookup"><span data-stu-id="d3abb-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="d3abb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d3abb-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3abb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d3abb-105">DESCRIPTION</span></span>
<span data-ttu-id="d3abb-106">Polecenie cmdlet **New-AzNatGateway** tworzy zasób bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="d3abb-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="d3abb-107">Natgateway wymaga następujących czynności:</span><span class="sxs-lookup"><span data-stu-id="d3abb-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="d3abb-108">Publiczny adres IP i/lub prefiks publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="d3abb-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="d3abb-109">IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="d3abb-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="d3abb-110">Zapas</span><span class="sxs-lookup"><span data-stu-id="d3abb-110">Sku</span></span>
- <span data-ttu-id="d3abb-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3abb-111">ResourceGroupName</span></span>
- <span data-ttu-id="d3abb-112">Source</span><span class="sxs-lookup"><span data-stu-id="d3abb-112">ResourceName</span></span>
- <span data-ttu-id="d3abb-113">Pozycję</span><span class="sxs-lookup"><span data-stu-id="d3abb-113">Location</span></span>

## <span data-ttu-id="d3abb-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d3abb-114">EXAMPLES</span></span>

### <span data-ttu-id="d3abb-115">Przykład 1: Tworzenie bramy NAT z publicznym adresem IP</span><span class="sxs-lookup"><span data-stu-id="d3abb-115">Example 1: Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="d3abb-116">Przykład 2: Tworzenie bramy NAT z publicznym prefiksem IP</span><span class="sxs-lookup"><span data-stu-id="d3abb-116">Example 2: Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="d3abb-117">Przykład 3: Tworzenie bramy NAT z publicznym adresem IP w strefie dostępności 1</span><span class="sxs-lookup"><span data-stu-id="d3abb-117">Example 3: Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="d3abb-118">Pierwsze polecenie tworzy standardowy publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="d3abb-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="d3abb-119">Drugie polecenie tworzy bramę NAT z publicznym adresem IP w strefie dostępności 1.</span><span class="sxs-lookup"><span data-stu-id="d3abb-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="d3abb-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d3abb-120">PARAMETERS</span></span>

### <span data-ttu-id="d3abb-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3abb-121">-AsJob</span></span>
<span data-ttu-id="d3abb-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d3abb-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3abb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3abb-123">-DefaultProfile</span></span>
<span data-ttu-id="d3abb-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d3abb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3abb-125">-Force</span><span class="sxs-lookup"><span data-stu-id="d3abb-125">-Force</span></span>
<span data-ttu-id="d3abb-126">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="d3abb-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d3abb-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="d3abb-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="d3abb-128">Limit czasu bezczynności bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="d3abb-128">The idle timeout of the nat gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3abb-129">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d3abb-129">-Location</span></span>
<span data-ttu-id="d3abb-130">Lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="d3abb-130">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3abb-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d3abb-131">-Name</span></span>
<span data-ttu-id="d3abb-132">Nazwa bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="d3abb-132">The name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3abb-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d3abb-133">-PublicIpAddress</span></span>
<span data-ttu-id="d3abb-134">Tablica publicznych adresów IP skojarzonych z zasobem bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="d3abb-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3abb-135">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d3abb-135">-PublicIpPrefix</span></span>
<span data-ttu-id="d3abb-136">Tablica prefiksów publicznych adresów IP skojarzonych z zasobem bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="d3abb-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3abb-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3abb-137">-ResourceGroupName</span></span>
<span data-ttu-id="d3abb-138">Nazwa grupy zasobów bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="d3abb-138">The resource group name of the nat gateway.</span></span>

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

### <span data-ttu-id="d3abb-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="d3abb-139">-Sku</span></span>
<span data-ttu-id="d3abb-140">Nazwa jednostki SKU bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="d3abb-140">Name of a NAT gateway SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3abb-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="d3abb-141">-Tag</span></span>
<span data-ttu-id="d3abb-142">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="d3abb-142">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3abb-143">-Zone</span><span class="sxs-lookup"><span data-stu-id="d3abb-143">-Zone</span></span>
<span data-ttu-id="d3abb-144">Lista stref dostępności oznaczająca strefę, w której należy wdrożyć bramę NAT.</span><span class="sxs-lookup"><span data-stu-id="d3abb-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3abb-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d3abb-145">-Confirm</span></span>
<span data-ttu-id="d3abb-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3abb-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3abb-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3abb-147">-WhatIf</span></span>
<span data-ttu-id="d3abb-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3abb-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3abb-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d3abb-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3abb-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3abb-150">CommonParameters</span></span>
<span data-ttu-id="d3abb-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3abb-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3abb-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3abb-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3abb-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3abb-153">INPUTS</span></span>

### <span data-ttu-id="d3abb-154">System. String</span><span class="sxs-lookup"><span data-stu-id="d3abb-154">System.String</span></span>

### <span data-ttu-id="d3abb-155">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d3abb-155">System.Int32</span></span>

### <span data-ttu-id="d3abb-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d3abb-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d3abb-157">Microsoft. Azure. Commands. Network. models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="d3abb-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="d3abb-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d3abb-158">OUTPUTS</span></span>

### <span data-ttu-id="d3abb-159">Microsoft. Azure. Commands. Network. models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="d3abb-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="d3abb-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d3abb-160">NOTES</span></span>

## <span data-ttu-id="d3abb-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3abb-161">RELATED LINKS</span></span>
