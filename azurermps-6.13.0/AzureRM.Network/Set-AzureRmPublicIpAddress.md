---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
ms.openlocfilehash: ed3b2de22c5f71c0782724f99c8325de4dea98b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543595"
---
# <span data-ttu-id="a5d1e-101">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a5d1e-101">Set-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="a5d1e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a5d1e-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d1e-103">Ustawia stan celu dla publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="a5d1e-103">Sets the goal state for a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5d1e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a5d1e-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5d1e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a5d1e-105">DESCRIPTION</span></span>
<span data-ttu-id="a5d1e-106">Polecenie cmdlet **Set-AzureRmPublicIpAddress** ustawia stan celu dla publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="a5d1e-106">The **Set-AzureRmPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="a5d1e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a5d1e-107">EXAMPLES</span></span>

### <span data-ttu-id="a5d1e-108">1: Zmienianie metody przydzielania publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="a5d1e-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="a5d1e-109">Pierwsze polecenie pobiera zasób publiczny adres IP z nazwą $publicIPName w grupie zasób $rgName.</span><span class="sxs-lookup"><span data-stu-id="a5d1e-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="a5d1e-110">Drugie polecenie ustawia metodę przydziału obiektu publicznego adresu IP na wartość "static".</span><span class="sxs-lookup"><span data-stu-id="a5d1e-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="a5d1e-111">Polecenie Set-AzureRmPublicIPAddress powoduje zaktualizowanie zasobu publicznego adresu IP za pomocą zaktualizowanego obiektu i zmodyfikowanie metody alokacji na wartość "static".</span><span class="sxs-lookup"><span data-stu-id="a5d1e-111">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="a5d1e-112">Publiczny adres IP przydzielono natychmiast.</span><span class="sxs-lookup"><span data-stu-id="a5d1e-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="a5d1e-113">2: Zmienianie etykiety domeny DNS dla publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="a5d1e-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="a5d1e-114">Pierwsze polecenie pobiera zasób publiczny adres IP z nazwą $publicIPName w grupie zasób $rgName.</span><span class="sxs-lookup"><span data-stu-id="a5d1e-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="a5d1e-115">Drugie polecenie ustawia właściwość DomainNameLabel na wymagany prefiks DNS.</span><span class="sxs-lookup"><span data-stu-id="a5d1e-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="a5d1e-116">Polecenie Set-AzureRmPublicIPAddress aktualizuje zasób publiczny adres IP za pomocą zaktualizowanego obiektu.</span><span class="sxs-lookup"><span data-stu-id="a5d1e-116">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="a5d1e-117">DomainNameLabel & FQDN są modyfikowane zgodnie z oczekiwaniami.</span><span class="sxs-lookup"><span data-stu-id="a5d1e-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="a5d1e-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a5d1e-118">PARAMETERS</span></span>

### <span data-ttu-id="a5d1e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5d1e-119">-AsJob</span></span>
<span data-ttu-id="a5d1e-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a5d1e-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5d1e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d1e-121">-DefaultProfile</span></span>
<span data-ttu-id="a5d1e-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a5d1e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5d1e-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a5d1e-123">-PublicIpAddress</span></span>
<span data-ttu-id="a5d1e-124">Określa obiekt **PublicIpAddress** reprezentujący stan celu, do którego powinien być ustawiony publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="a5d1e-124">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="a5d1e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d1e-125">CommonParameters</span></span>
<span data-ttu-id="a5d1e-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5d1e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d1e-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5d1e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d1e-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5d1e-128">INPUTS</span></span>

### <span data-ttu-id="a5d1e-129">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a5d1e-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>
<span data-ttu-id="a5d1e-130">Parametry: PublicIpAddress (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a5d1e-130">Parameters: PublicIpAddress (ByValue)</span></span>

## <span data-ttu-id="a5d1e-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a5d1e-131">OUTPUTS</span></span>

### <span data-ttu-id="a5d1e-132">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a5d1e-132">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="a5d1e-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a5d1e-133">NOTES</span></span>

## <span data-ttu-id="a5d1e-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5d1e-134">RELATED LINKS</span></span>

[<span data-ttu-id="a5d1e-135">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a5d1e-135">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="a5d1e-136">Nowe — AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a5d1e-136">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="a5d1e-137">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a5d1e-137">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)


