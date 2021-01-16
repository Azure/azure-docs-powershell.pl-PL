---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: 0855ba4e7e16503045d13c370838cd5d3fffb033
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344818"
---
# <span data-ttu-id="885e9-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="885e9-101">New-AzNatGateway</span></span>

## <span data-ttu-id="885e9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="885e9-102">SYNOPSIS</span></span>
<span data-ttu-id="885e9-103">Tworzenie nowego zasobu bramy NAT z właściwościami publiczny adres IP/publiczny prefiks IP, IdleTimeoutInMinutes i SKU.</span><span class="sxs-lookup"><span data-stu-id="885e9-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="885e9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="885e9-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="885e9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="885e9-105">DESCRIPTION</span></span>
<span data-ttu-id="885e9-106">Polecenie cmdlet **New-AzNatGateway** tworzy zasób bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="885e9-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="885e9-107">Natgateway wymaga następujących czynności:</span><span class="sxs-lookup"><span data-stu-id="885e9-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="885e9-108">Publiczny adres IP i/lub prefiks publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="885e9-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="885e9-109">IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="885e9-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="885e9-110">Zapas</span><span class="sxs-lookup"><span data-stu-id="885e9-110">Sku</span></span>
- <span data-ttu-id="885e9-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="885e9-111">ResourceGroupName</span></span>
- <span data-ttu-id="885e9-112">Source</span><span class="sxs-lookup"><span data-stu-id="885e9-112">ResourceName</span></span>
- <span data-ttu-id="885e9-113">Pozycję</span><span class="sxs-lookup"><span data-stu-id="885e9-113">Location</span></span>

## <span data-ttu-id="885e9-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="885e9-114">EXAMPLES</span></span>

### <span data-ttu-id="885e9-115">Przykład 1: Tworzenie bramy NAT z publicznym adresem IP</span><span class="sxs-lookup"><span data-stu-id="885e9-115">Example 1: Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="885e9-116">Przykład 2: Tworzenie bramy NAT z publicznym prefiksem IP</span><span class="sxs-lookup"><span data-stu-id="885e9-116">Example 2: Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="885e9-117">Przykład 3: Tworzenie bramy NAT z publicznym adresem IP w strefie dostępności 1</span><span class="sxs-lookup"><span data-stu-id="885e9-117">Example 3: Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="885e9-118">Pierwsze polecenie tworzy standardowy publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="885e9-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="885e9-119">Drugie polecenie tworzy bramę NAT z publicznym adresem IP w strefie dostępności 1.</span><span class="sxs-lookup"><span data-stu-id="885e9-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="885e9-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="885e9-120">PARAMETERS</span></span>

### <span data-ttu-id="885e9-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="885e9-121">-AsJob</span></span>
<span data-ttu-id="885e9-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="885e9-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="885e9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="885e9-123">-DefaultProfile</span></span>
<span data-ttu-id="885e9-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="885e9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="885e9-125">-Force</span><span class="sxs-lookup"><span data-stu-id="885e9-125">-Force</span></span>
<span data-ttu-id="885e9-126">Nie pytaj o potwierdzenie zamiaru zastąpienia zasobu</span><span class="sxs-lookup"><span data-stu-id="885e9-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="885e9-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="885e9-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="885e9-128">Limit czasu bezczynności bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="885e9-128">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="885e9-129">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="885e9-129">-Location</span></span>
<span data-ttu-id="885e9-130">Lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="885e9-130">The location.</span></span>

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

### <span data-ttu-id="885e9-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="885e9-131">-Name</span></span>
<span data-ttu-id="885e9-132">Nazwa bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="885e9-132">The name of the nat gateway.</span></span>

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

### <span data-ttu-id="885e9-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="885e9-133">-PublicIpAddress</span></span>
<span data-ttu-id="885e9-134">Tablica publicznych adresów IP skojarzonych z zasobem bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="885e9-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="885e9-135">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="885e9-135">-PublicIpPrefix</span></span>
<span data-ttu-id="885e9-136">Tablica prefiksów publicznych adresów IP skojarzonych z zasobem bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="885e9-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="885e9-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="885e9-137">-ResourceGroupName</span></span>
<span data-ttu-id="885e9-138">Nazwa grupy zasobów bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="885e9-138">The resource group name of the nat gateway.</span></span>

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

### <span data-ttu-id="885e9-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="885e9-139">-Sku</span></span>
<span data-ttu-id="885e9-140">Nazwa jednostki SKU bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="885e9-140">Name of a NAT gateway SKU.</span></span>

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

### <span data-ttu-id="885e9-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="885e9-141">-Tag</span></span>
<span data-ttu-id="885e9-142">Obiekt Hashtable reprezentujący znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="885e9-142">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="885e9-143">-Zone</span><span class="sxs-lookup"><span data-stu-id="885e9-143">-Zone</span></span>
<span data-ttu-id="885e9-144">Lista stref dostępności oznaczająca strefę, w której należy wdrożyć bramę NAT.</span><span class="sxs-lookup"><span data-stu-id="885e9-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

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

### <span data-ttu-id="885e9-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="885e9-145">-Confirm</span></span>
<span data-ttu-id="885e9-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="885e9-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="885e9-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="885e9-147">-WhatIf</span></span>
<span data-ttu-id="885e9-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="885e9-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="885e9-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="885e9-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="885e9-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="885e9-150">CommonParameters</span></span>
<span data-ttu-id="885e9-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="885e9-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="885e9-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="885e9-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="885e9-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="885e9-153">INPUTS</span></span>

### <span data-ttu-id="885e9-154">System. String</span><span class="sxs-lookup"><span data-stu-id="885e9-154">System.String</span></span>

### <span data-ttu-id="885e9-155">System. Int32</span><span class="sxs-lookup"><span data-stu-id="885e9-155">System.Int32</span></span>

### <span data-ttu-id="885e9-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="885e9-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="885e9-157">Microsoft. Azure. Commands. Network. models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="885e9-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="885e9-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="885e9-158">OUTPUTS</span></span>

### <span data-ttu-id="885e9-159">Microsoft. Azure. Commands. Network. models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="885e9-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="885e9-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="885e9-160">NOTES</span></span>

## <span data-ttu-id="885e9-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="885e9-161">RELATED LINKS</span></span>
