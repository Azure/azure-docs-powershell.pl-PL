---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4D75240C-F2B5-4273-848C-107308DD6837
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d56de5b27565f7bfdd90198ad45e2766da521f4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054604"
---
# <span data-ttu-id="6db1b-101">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="6db1b-101">Get-AzureNetworkSecurityGroupForSubnet</span></span>

## <span data-ttu-id="6db1b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6db1b-102">SYNOPSIS</span></span>
<span data-ttu-id="6db1b-103">Pobiera grupę zabezpieczeń sieci dla podsieci.</span><span class="sxs-lookup"><span data-stu-id="6db1b-103">Gets the network security group for a subnet.</span></span>

## <span data-ttu-id="6db1b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6db1b-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroupForSubnet -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6db1b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6db1b-105">DESCRIPTION</span></span>
<span data-ttu-id="6db1b-106">Polecenie cmdlet **Get-AzureNetworkSecurityGroupForSubnet** pobiera grupę zabezpieczeń sieci skojarzoną z podsiecią.</span><span class="sxs-lookup"><span data-stu-id="6db1b-106">The **Get-AzureNetworkSecurityGroupForSubnet** cmdlet gets the network security group that is associated to a subnet.</span></span>

## <span data-ttu-id="6db1b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6db1b-107">EXAMPLES</span></span>

## <span data-ttu-id="6db1b-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6db1b-108">PARAMETERS</span></span>

### <span data-ttu-id="6db1b-109">— Szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="6db1b-109">-Detailed</span></span>
<span data-ttu-id="6db1b-110">Wskazuje, że w tym poleceniu cmdlet są wyświetlane reguły zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="6db1b-110">Indicates that this cmdlet displays the network security rules.</span></span>

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

### <span data-ttu-id="6db1b-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="6db1b-111">-Profile</span></span>
<span data-ttu-id="6db1b-112">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6db1b-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6db1b-113">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="6db1b-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6db1b-114">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="6db1b-114">-SubnetName</span></span>
<span data-ttu-id="6db1b-115">Określa nazwę podsieci, dla której to polecenie cmdlet pobiera grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="6db1b-115">Specifies the name of a subnet for which this cmdlet gets a network security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6db1b-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="6db1b-116">-VirtualNetworkName</span></span>
<span data-ttu-id="6db1b-117">Określa nazwę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6db1b-117">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="6db1b-118">To polecenie cmdlet pobiera grupę zabezpieczeń sieci dla podsieci w sieci wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="6db1b-118">This cmdlet gets a network security group for a subnet in the virtual network that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6db1b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6db1b-119">CommonParameters</span></span>
<span data-ttu-id="6db1b-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6db1b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6db1b-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6db1b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6db1b-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6db1b-122">INPUTS</span></span>

## <span data-ttu-id="6db1b-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6db1b-123">OUTPUTS</span></span>

## <span data-ttu-id="6db1b-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6db1b-124">NOTES</span></span>

## <span data-ttu-id="6db1b-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6db1b-125">RELATED LINKS</span></span>

[<span data-ttu-id="6db1b-126">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="6db1b-126">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>](./Remove-AzureNetworkSecurityGroupFromSubnet.md)

[<span data-ttu-id="6db1b-127">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="6db1b-127">Set-AzureNetworkSecurityGroupToSubnet</span></span>](./Set-AzureNetworkSecurityGroupToSubnet.md)
