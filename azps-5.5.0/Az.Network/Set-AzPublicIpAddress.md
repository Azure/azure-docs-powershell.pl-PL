---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 4cb7d3a48d1783e834b9ecdd53d86969b4e1e6cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193354"
---
# <span data-ttu-id="fb4ec-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fb4ec-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="fb4ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb4ec-102">SYNOPSIS</span></span>
<span data-ttu-id="fb4ec-103">Aktualizuje publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-103">Updates a public IP address.</span></span>

## <span data-ttu-id="fb4ec-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fb4ec-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb4ec-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fb4ec-105">DESCRIPTION</span></span>
<span data-ttu-id="fb4ec-106">Polecenie **cmdlet Set-AzPublicIpAddress** aktualizuje publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-106">The **Set-AzPublicIpAddress** cmdlet updates a public IP address.</span></span>

## <span data-ttu-id="fb4ec-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fb4ec-107">EXAMPLES</span></span>

### <span data-ttu-id="fb4ec-108">1. Zmienianie metody alokacji publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="fb4ec-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="fb4ec-109">Pierwsze polecenie pobiera publiczny zasób adresu IP z $publicIPName nazwami w grupie zasobów $rgName.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="fb4ec-110">Drugie polecenie ustawia metodę alokacji publicznego obiektu adresu IP na "Statyczny".</span><span class="sxs-lookup"><span data-stu-id="fb4ec-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="fb4ec-111">Set-AzPublicIPAddress aktualizuje zasób publicznego adresu IP zaktualizowanym obiektem i modyfikuje metodę alokacji na "Statyczną".</span><span class="sxs-lookup"><span data-stu-id="fb4ec-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="fb4ec-112">Publiczny adres IP jest przydzielany natychmiast.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="fb4ec-113">2. Dodawanie etykiety domeny DNS publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="fb4ec-113">2: Add DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="fb4ec-114">Pierwsze polecenie pobiera publiczny zasób adresu IP z $publicIPName nazwami w grupie zasobów $rgName.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="fb4ec-115">Drugie polecenie ustawia właściwość DomainNameLabel na wymagany prefiks dns.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="fb4ec-116">Set-AzPublicIPAddress aktualizuje publiczny zasób adresu IP zaktualizowanym obiektem.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="fb4ec-117">NazwaNazwa_domeny & nazwy Fqdn są modyfikowane zgodnie z oczekiwaniami.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-117">DomainNameLabel & Fqdn are modified as expected.</span></span>
    
### <span data-ttu-id="fb4ec-118">3. Zmienianie etykiety domeny DNS publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="fb4ec-118">3: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="fb4ec-119">Pierwsze polecenie pobiera publiczny zasób adresu IP z $publicIPName nazwami w grupie zasobów $rgName.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-119">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="fb4ec-120">Drugie polecenie ustawia właściwość DomainNameLabel na wymagany prefiks dns.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-120">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="fb4ec-121">Set-AzPublicIPAddress aktualizuje publiczny zasób adresu IP zaktualizowanym obiektem.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-121">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="fb4ec-122">NazwaNazwa_domeny & nazwy Fqdn są modyfikowane zgodnie z oczekiwaniami.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-122">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="fb4ec-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb4ec-123">PARAMETERS</span></span>

### <span data-ttu-id="fb4ec-124">— AsJob</span><span class="sxs-lookup"><span data-stu-id="fb4ec-124">-AsJob</span></span>
<span data-ttu-id="fb4ec-125">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fb4ec-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb4ec-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb4ec-126">-DefaultProfile</span></span>
<span data-ttu-id="fb4ec-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb4ec-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fb4ec-128">-PublicIpAddress</span></span>
<span data-ttu-id="fb4ec-129">Określa publiczny obiekt adresu IP reprezentujący stan, dla którego należy ustawić publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-129">Specifies a public IP address object representing the state to which the public IP address should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb4ec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb4ec-130">CommonParameters</span></span>
<span data-ttu-id="fb4ec-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb4ec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb4ec-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb4ec-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb4ec-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb4ec-133">INPUTS</span></span>

### <span data-ttu-id="fb4ec-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fb4ec-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="fb4ec-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fb4ec-135">OUTPUTS</span></span>

### <span data-ttu-id="fb4ec-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fb4ec-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="fb4ec-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fb4ec-137">NOTES</span></span>

## <span data-ttu-id="fb4ec-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb4ec-138">RELATED LINKS</span></span>

[<span data-ttu-id="fb4ec-139">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fb4ec-139">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="fb4ec-140">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fb4ec-140">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="fb4ec-141">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fb4ec-141">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


