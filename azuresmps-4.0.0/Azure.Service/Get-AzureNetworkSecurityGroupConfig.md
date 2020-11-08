---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: FCB3C8EB-EAA6-48E3-A1A5-DB3050821BD8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 402aa39fb1476d6b3bc69902148e71549fccb3fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055299"
---
# <span data-ttu-id="48fb1-101">Get-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="48fb1-101">Get-AzureNetworkSecurityGroupConfig</span></span>

## <span data-ttu-id="48fb1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="48fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="48fb1-103">Pobiera szczegóły grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="48fb1-103">Gets details for a network security group.</span></span>

## <span data-ttu-id="48fb1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="48fb1-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroupConfig [-Detailed] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="48fb1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="48fb1-105">DESCRIPTION</span></span>
<span data-ttu-id="48fb1-106">Polecenie cmdlet **Get-AzureNetworkSecurityGroupConfig** zwraca szczegóły grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="48fb1-106">The **Get-AzureNetworkSecurityGroupConfig** cmdlet returns details for a network security group.</span></span>
<span data-ttu-id="48fb1-107">Określ *szczegółowy* parametr, aby wyświetlić reguły zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="48fb1-107">Specify the *Detailed* parameter to display the network security rules.</span></span>

## <span data-ttu-id="48fb1-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="48fb1-108">EXAMPLES</span></span>

## <span data-ttu-id="48fb1-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="48fb1-109">PARAMETERS</span></span>

### <span data-ttu-id="48fb1-110">— Szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="48fb1-110">-Detailed</span></span>
<span data-ttu-id="48fb1-111">Wskazuje, że w tym poleceniu cmdlet są wyświetlane reguły zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="48fb1-111">Indicates that this cmdlet displays the network security rules.</span></span>

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

### <span data-ttu-id="48fb1-112">-Profile</span><span class="sxs-lookup"><span data-stu-id="48fb1-112">-Profile</span></span>
<span data-ttu-id="48fb1-113">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48fb1-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="48fb1-114">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="48fb1-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="48fb1-115">-VM</span><span class="sxs-lookup"><span data-stu-id="48fb1-115">-VM</span></span>
<span data-ttu-id="48fb1-116">Określa maszynę wirtualną, dla której to polecenie cmdlet pobiera szczegóły grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="48fb1-116">Specifies the virtual machine for which this cmdlet gets the details of a network security group.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48fb1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48fb1-117">CommonParameters</span></span>
<span data-ttu-id="48fb1-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48fb1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48fb1-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48fb1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48fb1-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="48fb1-120">INPUTS</span></span>

## <span data-ttu-id="48fb1-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="48fb1-121">OUTPUTS</span></span>

## <span data-ttu-id="48fb1-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="48fb1-122">NOTES</span></span>

## <span data-ttu-id="48fb1-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="48fb1-123">RELATED LINKS</span></span>

[<span data-ttu-id="48fb1-124">Nowe — AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="48fb1-124">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="48fb1-125">Remove-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="48fb1-125">Remove-AzureNetworkSecurityGroup</span></span>](./Remove-AzureNetworkSecurityGroup.md)


