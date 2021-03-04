---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: 168a1803781748eb81c3a2087876b2a7b18d9d39
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952170"
---
# <span data-ttu-id="d3c51-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="d3c51-101">New-AzNatGateway</span></span>

## <span data-ttu-id="d3c51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3c51-102">SYNOPSIS</span></span>
<span data-ttu-id="d3c51-103">Utwórz nowy zasób bramy nat o właściwościach Publiczny adres IP/prefiks publicznych adresów IP, IdleTimeoutInMinutes i SKU.</span><span class="sxs-lookup"><span data-stu-id="d3c51-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="d3c51-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d3c51-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3c51-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d3c51-105">DESCRIPTION</span></span>
<span data-ttu-id="d3c51-106">Polecenie **cmdlet New-AzNatGateway** tworzy zasób bramy Nat.</span><span class="sxs-lookup"><span data-stu-id="d3c51-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="d3c51-107">Brama natgateway wymaga następujących czynności:</span><span class="sxs-lookup"><span data-stu-id="d3c51-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="d3c51-108">Publiczny adres IP i/lub publiczny prefiks IP</span><span class="sxs-lookup"><span data-stu-id="d3c51-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="d3c51-109">IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="d3c51-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="d3c51-110">SKU</span><span class="sxs-lookup"><span data-stu-id="d3c51-110">Sku</span></span>
- <span data-ttu-id="d3c51-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3c51-111">ResourceGroupName</span></span>
- <span data-ttu-id="d3c51-112">ResourceName</span><span class="sxs-lookup"><span data-stu-id="d3c51-112">ResourceName</span></span>
- <span data-ttu-id="d3c51-113">Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d3c51-113">Location</span></span>

## <span data-ttu-id="d3c51-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d3c51-114">EXAMPLES</span></span>

### <span data-ttu-id="d3c51-115">Przykład 1. Tworzenie bramy nat z publicznym adresem IP</span><span class="sxs-lookup"><span data-stu-id="d3c51-115">Example 1: Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="d3c51-116">Przykład 2. Tworzenie bramy nat z publicznym prefiksem IP</span><span class="sxs-lookup"><span data-stu-id="d3c51-116">Example 2: Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="d3c51-117">Przykład 3. Tworzenie bramy nat z publicznym adresem IP w strefie dostępności 1</span><span class="sxs-lookup"><span data-stu-id="d3c51-117">Example 3: Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="d3c51-118">Pierwsze polecenie tworzy standardowy publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="d3c51-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="d3c51-119">Drugie polecenie tworzy bramę NAT z publicznym adresem IP w strefie dostępności 1.</span><span class="sxs-lookup"><span data-stu-id="d3c51-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="d3c51-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3c51-120">PARAMETERS</span></span>

### <span data-ttu-id="d3c51-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d3c51-121">-AsJob</span></span>
<span data-ttu-id="d3c51-122">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d3c51-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3c51-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3c51-123">-DefaultProfile</span></span>
<span data-ttu-id="d3c51-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d3c51-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3c51-125">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="d3c51-125">-Force</span></span>
<span data-ttu-id="d3c51-126">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="d3c51-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d3c51-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="d3c51-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="d3c51-128">Limit czasu bezczynności bramy nat.</span><span class="sxs-lookup"><span data-stu-id="d3c51-128">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="d3c51-129">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d3c51-129">-Location</span></span>
<span data-ttu-id="d3c51-130">Lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="d3c51-130">The location.</span></span>

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

### <span data-ttu-id="d3c51-131">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d3c51-131">-Name</span></span>
<span data-ttu-id="d3c51-132">Nazwa bramy nat.</span><span class="sxs-lookup"><span data-stu-id="d3c51-132">The name of the nat gateway.</span></span>

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

### <span data-ttu-id="d3c51-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d3c51-133">-PublicIpAddress</span></span>
<span data-ttu-id="d3c51-134">Tablica publicznych adresów IP skojarzonych z zasobem bramy nat.</span><span class="sxs-lookup"><span data-stu-id="d3c51-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="d3c51-135">- PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d3c51-135">-PublicIpPrefix</span></span>
<span data-ttu-id="d3c51-136">Tablica publicznych prefiksów IP skojarzonych z zasobem bramy nat.</span><span class="sxs-lookup"><span data-stu-id="d3c51-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="d3c51-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3c51-137">-ResourceGroupName</span></span>
<span data-ttu-id="d3c51-138">Nazwa grupy zasobów bramy nat.</span><span class="sxs-lookup"><span data-stu-id="d3c51-138">The resource group name of the nat gateway.</span></span>

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

### <span data-ttu-id="d3c51-139">- SKU</span><span class="sxs-lookup"><span data-stu-id="d3c51-139">-Sku</span></span>
<span data-ttu-id="d3c51-140">Nazwa sku bramy NAT.</span><span class="sxs-lookup"><span data-stu-id="d3c51-140">Name of a NAT gateway SKU.</span></span>

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

### <span data-ttu-id="d3c51-141">— Tag</span><span class="sxs-lookup"><span data-stu-id="d3c51-141">-Tag</span></span>
<span data-ttu-id="d3c51-142">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="d3c51-142">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d3c51-143">— Strefa</span><span class="sxs-lookup"><span data-stu-id="d3c51-143">-Zone</span></span>
<span data-ttu-id="d3c51-144">Lista stref dostępności oznaczających strefę, w której należy wdrożyć bramę nat.</span><span class="sxs-lookup"><span data-stu-id="d3c51-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

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

### <span data-ttu-id="d3c51-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d3c51-145">-Confirm</span></span>
<span data-ttu-id="d3c51-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d3c51-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3c51-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3c51-147">-WhatIf</span></span>
<span data-ttu-id="d3c51-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3c51-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3c51-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d3c51-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3c51-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3c51-150">CommonParameters</span></span>
<span data-ttu-id="d3c51-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3c51-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3c51-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3c51-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3c51-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3c51-153">INPUTS</span></span>

### <span data-ttu-id="d3c51-154">System.String</span><span class="sxs-lookup"><span data-stu-id="d3c51-154">System.String</span></span>

### <span data-ttu-id="d3c51-155">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d3c51-155">System.Int32</span></span>

### <span data-ttu-id="d3c51-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d3c51-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d3c51-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="d3c51-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="d3c51-158">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3c51-158">OUTPUTS</span></span>

### <span data-ttu-id="d3c51-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="d3c51-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="d3c51-160">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d3c51-160">NOTES</span></span>

## <span data-ttu-id="d3c51-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3c51-161">RELATED LINKS</span></span>
