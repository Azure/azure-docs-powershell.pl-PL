---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 53d5e15e6354e359461e59728e0776b7d3ec99ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892741"
---
# <span data-ttu-id="bb215-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bb215-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="bb215-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb215-102">SYNOPSIS</span></span>
<span data-ttu-id="bb215-103">Ustawia stan celu dla publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="bb215-103">Sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="bb215-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb215-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb215-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bb215-105">DESCRIPTION</span></span>
<span data-ttu-id="bb215-106">Polecenie cmdlet **Set-AzPublicIpAddress** ustawia stan celu dla publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="bb215-106">The **Set-AzPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="bb215-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb215-107">EXAMPLES</span></span>

### <span data-ttu-id="bb215-108">1: Zmienianie metody przydzielania publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="bb215-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="bb215-109">Pierwsze polecenie pobiera zasób publiczny adres IP z nazwą $publicIPName w grupie zasób $rgName.</span><span class="sxs-lookup"><span data-stu-id="bb215-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="bb215-110">Drugie polecenie ustawia metodę przydziału obiektu publicznego adresu IP na wartość "static".</span><span class="sxs-lookup"><span data-stu-id="bb215-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="bb215-111">Polecenie Set-AzPublicIPAddress powoduje zaktualizowanie zasobu publicznego adresu IP za pomocą zaktualizowanego obiektu i zmodyfikowanie metody alokacji na wartość "static".</span><span class="sxs-lookup"><span data-stu-id="bb215-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="bb215-112">Publiczny adres IP przydzielono natychmiast.</span><span class="sxs-lookup"><span data-stu-id="bb215-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="bb215-113">2: Zmienianie etykiety domeny DNS dla publicznego adresu IP</span><span class="sxs-lookup"><span data-stu-id="bb215-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="bb215-114">Pierwsze polecenie pobiera zasób publiczny adres IP z nazwą $publicIPName w grupie zasób $rgName.</span><span class="sxs-lookup"><span data-stu-id="bb215-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="bb215-115">Drugie polecenie ustawia właściwość DomainNameLabel na wymagany prefiks DNS.</span><span class="sxs-lookup"><span data-stu-id="bb215-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="bb215-116">Polecenie Set-AzPublicIPAddress aktualizuje zasób publiczny adres IP za pomocą zaktualizowanego obiektu.</span><span class="sxs-lookup"><span data-stu-id="bb215-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="bb215-117">DomainNameLabel & FQDN są modyfikowane zgodnie z oczekiwaniami.</span><span class="sxs-lookup"><span data-stu-id="bb215-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="bb215-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb215-118">PARAMETERS</span></span>

### <span data-ttu-id="bb215-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb215-119">-AsJob</span></span>
<span data-ttu-id="bb215-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bb215-120">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb215-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb215-121">-DefaultProfile</span></span>
<span data-ttu-id="bb215-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb215-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb215-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bb215-123">-PublicIpAddress</span></span>
<span data-ttu-id="bb215-124">Określa obiekt **PublicIpAddress** reprezentujący stan celu, do którego powinien być ustawiony publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="bb215-124">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb215-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb215-125">CommonParameters</span></span>
<span data-ttu-id="bb215-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb215-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb215-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb215-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb215-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb215-128">INPUTS</span></span>

### <span data-ttu-id="bb215-129">PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bb215-129">PSPublicIpAddress</span></span>
<span data-ttu-id="bb215-130">Parametr "PublicIpAddress" akceptuje wartość typu "PSPublicIpAddress" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="bb215-130">Parameter 'PublicIpAddress' accepts value of type 'PSPublicIpAddress' from the pipeline</span></span>

## <span data-ttu-id="bb215-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb215-131">OUTPUTS</span></span>

### <span data-ttu-id="bb215-132">Microsoft. Azure. Commands. Network. models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bb215-132">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="bb215-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb215-133">NOTES</span></span>

## <span data-ttu-id="bb215-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb215-134">RELATED LINKS</span></span>

[<span data-ttu-id="bb215-135">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bb215-135">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="bb215-136">Nowe — AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bb215-136">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="bb215-137">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="bb215-137">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


