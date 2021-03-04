---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: c72c4ad67f6096f5ba86924219670be53a725d26
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953898"
---
# <span data-ttu-id="0506a-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0506a-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="0506a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0506a-102">SYNOPSIS</span></span>
<span data-ttu-id="0506a-103">Tworzy publiczny prefiks IP</span><span class="sxs-lookup"><span data-stu-id="0506a-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="0506a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0506a-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>]
 [-Zone <String[]>] [-CustomIpPrefix <PSCustomIpPrefix>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0506a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0506a-105">DESCRIPTION</span></span>
<span data-ttu-id="0506a-106">Polecenie **cmdlet New-AzPublicIpPrefix** tworzy publiczny prefiks IP.</span><span class="sxs-lookup"><span data-stu-id="0506a-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="0506a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0506a-107">EXAMPLES</span></span>

### <span data-ttu-id="0506a-108">Przykład 1. Tworzenie nowego publicznego prefiksu IP</span><span class="sxs-lookup"><span data-stu-id="0506a-108">Example 1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="0506a-109">To polecenie tworzy nowy publiczny zasób prefiksu IP.</span><span class="sxs-lookup"><span data-stu-id="0506a-109">This command creates a new public IP prefix resource.</span></span> 

### <span data-ttu-id="0506a-110">Przykład 2. Tworzenie nowego globalnego prefiksu IP</span><span class="sxs-lookup"><span data-stu-id="0506a-110">Example 2: Create a new global public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -ResourceGroupName $rgname -name $rname -location $location -Tier Global -PrefixLength 30
```

<span data-ttu-id="0506a-111">To polecenie tworzy nowy globalny publiczny zasób prefiksu IP.</span><span class="sxs-lookup"><span data-stu-id="0506a-111">This command creates a new global public IP prefix resource.</span></span> 

## <span data-ttu-id="0506a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0506a-112">PARAMETERS</span></span>

### <span data-ttu-id="0506a-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="0506a-113">-AsJob</span></span>
<span data-ttu-id="0506a-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0506a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0506a-115">- CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0506a-115">-CustomIpPrefix</span></span>
<span data-ttu-id="0506a-116">The CustomIpPrefix that this PublicIpPrefix will be associated with</span><span class="sxs-lookup"><span data-stu-id="0506a-116">The CustomIpPrefix that this PublicIpPrefix will be associated with</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0506a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0506a-117">-DefaultProfile</span></span>
<span data-ttu-id="0506a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0506a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0506a-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="0506a-119">-Force</span></span>
<span data-ttu-id="0506a-120">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="0506a-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="0506a-121">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="0506a-121">-IpAddressVersion</span></span>
<span data-ttu-id="0506a-122">Wersja publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="0506a-122">The public IP address version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0506a-123">-IpTag</span><span class="sxs-lookup"><span data-stu-id="0506a-123">-IpTag</span></span>
<span data-ttu-id="0506a-124">Lista tagów IP.</span><span class="sxs-lookup"><span data-stu-id="0506a-124">IpTag List.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0506a-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0506a-125">-Location</span></span>
<span data-ttu-id="0506a-126">Lokalizacja publicznego prefiksu IP.</span><span class="sxs-lookup"><span data-stu-id="0506a-126">The public IP prefix location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0506a-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="0506a-127">-Name</span></span>
<span data-ttu-id="0506a-128">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="0506a-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0506a-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="0506a-129">-PrefixLength</span></span>
<span data-ttu-id="0506a-130">Długość publicznej poprawki publicznej (PublicIPPrefix)</span><span class="sxs-lookup"><span data-stu-id="0506a-130">The PublicIPPrefix length</span></span>

```yaml
Type: System.UInt16
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0506a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0506a-131">-ResourceGroupName</span></span>
<span data-ttu-id="0506a-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0506a-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0506a-133">- SKU</span><span class="sxs-lookup"><span data-stu-id="0506a-133">-Sku</span></span>
<span data-ttu-id="0506a-134">Nazwa publicznego prefiksu IP SKU.</span><span class="sxs-lookup"><span data-stu-id="0506a-134">The public IP Prefix Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0506a-135">— Tag</span><span class="sxs-lookup"><span data-stu-id="0506a-135">-Tag</span></span>
<span data-ttu-id="0506a-136">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="0506a-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="0506a-137">- Warstwa</span><span class="sxs-lookup"><span data-stu-id="0506a-137">-Tier</span></span>
<span data-ttu-id="0506a-138">Publiczna warstwa SKU prefiksu IP.</span><span class="sxs-lookup"><span data-stu-id="0506a-138">The public IP Prefix Sku tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Regional, Global

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0506a-139">— Strefa</span><span class="sxs-lookup"><span data-stu-id="0506a-139">-Zone</span></span>
<span data-ttu-id="0506a-140">Lista stref dostępności oznaczających adresy IP przydzielone do zasobu.</span><span class="sxs-lookup"><span data-stu-id="0506a-140">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0506a-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0506a-141">-Confirm</span></span>
<span data-ttu-id="0506a-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0506a-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0506a-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0506a-143">-WhatIf</span></span>
<span data-ttu-id="0506a-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0506a-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0506a-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0506a-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0506a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0506a-146">CommonParameters</span></span>
<span data-ttu-id="0506a-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0506a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0506a-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0506a-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0506a-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0506a-149">INPUTS</span></span>

### <span data-ttu-id="0506a-150">System.String</span><span class="sxs-lookup"><span data-stu-id="0506a-150">System.String</span></span>

### <span data-ttu-id="0506a-151">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="0506a-151">System.UInt16</span></span>

### <span data-ttu-id="0506a-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span><span class="sxs-lookup"><span data-stu-id="0506a-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="0506a-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="0506a-153">System.String[]</span></span>

### <span data-ttu-id="0506a-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0506a-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0506a-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0506a-155">OUTPUTS</span></span>

### <span data-ttu-id="0506a-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0506a-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="0506a-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0506a-157">NOTES</span></span>

## <span data-ttu-id="0506a-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0506a-158">RELATED LINKS</span></span>

[<span data-ttu-id="0506a-159">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0506a-159">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="0506a-160">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0506a-160">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="0506a-161">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0506a-161">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
