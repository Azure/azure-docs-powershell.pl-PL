---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 4cb7d3a48d1783e834b9ecdd53d86969b4e1e6cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364007"
---
# <span data-ttu-id="d5152-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d5152-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="d5152-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d5152-102">SYNOPSIS</span></span>
<span data-ttu-id="d5152-103">Aktualizuje publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="d5152-103">Updates a public IP address.</span></span>

## <span data-ttu-id="d5152-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d5152-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5152-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d5152-105">DESCRIPTION</span></span>
<span data-ttu-id="d5152-106">Polecenie cmdlet **Set-AzPublicIpAddress** aktualizuje publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="d5152-106">The **Set-AzPublicIpAddress** cmdlet updates a public IP address.</span></span>

## <span data-ttu-id="d5152-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d5152-107">EXAMPLES</span></span>

### <span data-ttu-id="d5152-108">1: Zmienianie metody przydzielania publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="d5152-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="d5152-109">Pierwsze polecenie pobiera zasób publiczny adres IP z nazwą $publicIPName w grupie zasób $rgName.</span><span class="sxs-lookup"><span data-stu-id="d5152-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="d5152-110">Drugie polecenie ustawia metodę przydziału obiektu publicznego adresu IP na wartość "static".</span><span class="sxs-lookup"><span data-stu-id="d5152-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="d5152-111">Polecenie Set-AzPublicIPAddress powoduje zaktualizowanie zasobu publicznego adresu IP za pomocą zaktualizowanego obiektu i zmodyfikowanie metody alokacji na wartość "static".</span><span class="sxs-lookup"><span data-stu-id="d5152-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="d5152-112">Publiczny adres IP przydzielono natychmiast.</span><span class="sxs-lookup"><span data-stu-id="d5152-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="d5152-113">2: Dodawanie etykiety domeny DNS dla publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="d5152-113">2: Add DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="d5152-114">Pierwsze polecenie pobiera zasób publiczny adres IP z nazwą $publicIPName w grupie zasób $rgName.</span><span class="sxs-lookup"><span data-stu-id="d5152-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="d5152-115">Drugie polecenie ustawia właściwość DomainNameLabel na wymagany prefiks DNS.</span><span class="sxs-lookup"><span data-stu-id="d5152-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="d5152-116">Polecenie Set-AzPublicIPAddress aktualizuje zasób publiczny adres IP za pomocą zaktualizowanego obiektu.</span><span class="sxs-lookup"><span data-stu-id="d5152-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="d5152-117">DomainNameLabel & FQDN są modyfikowane zgodnie z oczekiwaniami.</span><span class="sxs-lookup"><span data-stu-id="d5152-117">DomainNameLabel & Fqdn are modified as expected.</span></span>
    
### <span data-ttu-id="d5152-118">3: Zmienianie etykiety domeny DNS dla publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="d5152-118">3: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="d5152-119">Pierwsze polecenie pobiera zasób publiczny adres IP z nazwą $publicIPName w grupie zasób $rgName.</span><span class="sxs-lookup"><span data-stu-id="d5152-119">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="d5152-120">Drugie polecenie ustawia właściwość DomainNameLabel na wymagany prefiks DNS.</span><span class="sxs-lookup"><span data-stu-id="d5152-120">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="d5152-121">Polecenie Set-AzPublicIPAddress aktualizuje zasób publiczny adres IP za pomocą zaktualizowanego obiektu.</span><span class="sxs-lookup"><span data-stu-id="d5152-121">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="d5152-122">DomainNameLabel & FQDN są modyfikowane zgodnie z oczekiwaniami.</span><span class="sxs-lookup"><span data-stu-id="d5152-122">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="d5152-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d5152-123">PARAMETERS</span></span>

### <span data-ttu-id="d5152-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5152-124">-AsJob</span></span>
<span data-ttu-id="d5152-125">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d5152-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d5152-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5152-126">-DefaultProfile</span></span>
<span data-ttu-id="d5152-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5152-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5152-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d5152-128">-PublicIpAddress</span></span>
<span data-ttu-id="d5152-129">Określa publiczny obiekt adresu IP reprezentujący stan, w którym powinien być ustawiony publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="d5152-129">Specifies a public IP address object representing the state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="d5152-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5152-130">CommonParameters</span></span>
<span data-ttu-id="d5152-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5152-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5152-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5152-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5152-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5152-133">INPUTS</span></span>

### <span data-ttu-id="d5152-134">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d5152-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="d5152-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d5152-135">OUTPUTS</span></span>

### <span data-ttu-id="d5152-136">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d5152-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="d5152-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d5152-137">NOTES</span></span>

## <span data-ttu-id="d5152-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5152-138">RELATED LINKS</span></span>

[<span data-ttu-id="d5152-139">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d5152-139">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="d5152-140">Nowe — AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d5152-140">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="d5152-141">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d5152-141">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


