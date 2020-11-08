---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: 49a6a7d817a6b84626b200faada5c36525dc1c91
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052071"
---
# <span data-ttu-id="f38b1-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f38b1-101">New-AzNatGateway</span></span>

## <span data-ttu-id="f38b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f38b1-102">SYNOPSIS</span></span>
<span data-ttu-id="f38b1-103">Tworzenie nowego zasobu bramy NAT z właściwościami publiczny adres IP/publiczny prefiks IP, IdleTimeoutInMinutes i SKU.</span><span class="sxs-lookup"><span data-stu-id="f38b1-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="f38b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f38b1-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f38b1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f38b1-105">DESCRIPTION</span></span>
<span data-ttu-id="f38b1-106">Polecenie cmdlet **New-AzNatGateway** tworzy zasób bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="f38b1-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="f38b1-107">Natgateway wymaga następujących czynności:</span><span class="sxs-lookup"><span data-stu-id="f38b1-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="f38b1-108">Publiczny adres IP i/lub prefiks publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="f38b1-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="f38b1-109">IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f38b1-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="f38b1-110">Zapas</span><span class="sxs-lookup"><span data-stu-id="f38b1-110">Sku</span></span>
- <span data-ttu-id="f38b1-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f38b1-111">ResourceGroupName</span></span>
- <span data-ttu-id="f38b1-112">Source</span><span class="sxs-lookup"><span data-stu-id="f38b1-112">ResourceName</span></span>
- <span data-ttu-id="f38b1-113">Pozycję</span><span class="sxs-lookup"><span data-stu-id="f38b1-113">Location</span></span>

## <span data-ttu-id="f38b1-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f38b1-114">EXAMPLES</span></span>

### <span data-ttu-id="f38b1-115">Przykład 1: Tworzenie bramy NAT z publicznym adresem IP</span><span class="sxs-lookup"><span data-stu-id="f38b1-115">Example 1 : Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="f38b1-116">Przykład 2: Tworzenie bramy NAT z publicznym prefiksem IP</span><span class="sxs-lookup"><span data-stu-id="f38b1-116">Example 2 : Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="f38b1-117">Przykład 3: Tworzenie bramy NAT z publicznym adresem IP w strefie dostępności 1</span><span class="sxs-lookup"><span data-stu-id="f38b1-117">Example 3 : Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="f38b1-118">Pierwsze polecenie tworzy standardowy publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="f38b1-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="f38b1-119">Drugie polecenie tworzy bramę NAT z publicznym adresem IP w strefie dostępności 1.</span><span class="sxs-lookup"><span data-stu-id="f38b1-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="f38b1-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f38b1-120">PARAMETERS</span></span>

### <span data-ttu-id="f38b1-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f38b1-121">-AsJob</span></span>
<span data-ttu-id="f38b1-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f38b1-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f38b1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f38b1-123">-DefaultProfile</span></span>
<span data-ttu-id="f38b1-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f38b1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f38b1-125">-Force</span><span class="sxs-lookup"><span data-stu-id="f38b1-125">-Force</span></span>
<span data-ttu-id="f38b1-126">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="f38b1-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f38b1-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f38b1-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="f38b1-128">Limit czasu bezczynności bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="f38b1-128">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="f38b1-129">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f38b1-129">-Location</span></span>
<span data-ttu-id="f38b1-130">Lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="f38b1-130">The location.</span></span>

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

### <span data-ttu-id="f38b1-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f38b1-131">-Name</span></span>
<span data-ttu-id="f38b1-132">Nazwa bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="f38b1-132">The name of the nat gateway.</span></span>

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

### <span data-ttu-id="f38b1-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f38b1-133">-PublicIpAddress</span></span>
<span data-ttu-id="f38b1-134">Tablica publicznych adresów IP skojarzonych z zasobem bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="f38b1-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="f38b1-135">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f38b1-135">-PublicIpPrefix</span></span>
<span data-ttu-id="f38b1-136">Tablica prefiksów publicznych adresów IP skojarzonych z zasobem bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="f38b1-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="f38b1-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f38b1-137">-ResourceGroupName</span></span>
<span data-ttu-id="f38b1-138">Nazwa grupy zasobów bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="f38b1-138">The resource group name of the nat gateway.</span></span>

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

### <span data-ttu-id="f38b1-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="f38b1-139">-Sku</span></span>
<span data-ttu-id="f38b1-140">Nazwa jednostki SKU bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="f38b1-140">Name of a NAT gateway SKU.</span></span>

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

### <span data-ttu-id="f38b1-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="f38b1-141">-Tag</span></span>
<span data-ttu-id="f38b1-142">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="f38b1-142">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f38b1-143">-Zone</span><span class="sxs-lookup"><span data-stu-id="f38b1-143">-Zone</span></span>
<span data-ttu-id="f38b1-144">Lista stref dostępności oznaczająca strefę, w której należy wdrożyć bramę NAT.</span><span class="sxs-lookup"><span data-stu-id="f38b1-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

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

### <span data-ttu-id="f38b1-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f38b1-145">-Confirm</span></span>
<span data-ttu-id="f38b1-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f38b1-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f38b1-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f38b1-147">-WhatIf</span></span>
<span data-ttu-id="f38b1-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f38b1-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f38b1-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f38b1-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f38b1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f38b1-150">CommonParameters</span></span>
<span data-ttu-id="f38b1-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f38b1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f38b1-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f38b1-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f38b1-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f38b1-153">INPUTS</span></span>

### <span data-ttu-id="f38b1-154">System. String</span><span class="sxs-lookup"><span data-stu-id="f38b1-154">System.String</span></span>

### <span data-ttu-id="f38b1-155">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f38b1-155">System.Int32</span></span>

### <span data-ttu-id="f38b1-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f38b1-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f38b1-157">Microsoft. Azure. Commands. Network. models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="f38b1-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="f38b1-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f38b1-158">OUTPUTS</span></span>

### <span data-ttu-id="f38b1-159">Microsoft. Azure. Commands. Network. models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="f38b1-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="f38b1-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f38b1-160">NOTES</span></span>

## <span data-ttu-id="f38b1-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f38b1-161">RELATED LINKS</span></span>
