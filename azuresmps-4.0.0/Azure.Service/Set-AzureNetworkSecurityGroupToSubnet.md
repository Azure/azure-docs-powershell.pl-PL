---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A14F9105-1422-4073-96CF-E75CFC039E05
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7eaf1af2efe3f93f4e0a44d54e1f07ea52166942
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054795"
---
# <span data-ttu-id="4ab06-101">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="4ab06-101">Set-AzureNetworkSecurityGroupToSubnet</span></span>

## <span data-ttu-id="4ab06-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ab06-102">SYNOPSIS</span></span>
<span data-ttu-id="4ab06-103">Kojarzy grupę zabezpieczeń sieci z podsiecią.</span><span class="sxs-lookup"><span data-stu-id="4ab06-103">Associates a network security group to a subnet.</span></span>

## <span data-ttu-id="4ab06-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ab06-104">SYNTAX</span></span>

```
Set-AzureNetworkSecurityGroupToSubnet -Name <String> -VirtualNetworkName <String> -SubnetName <String> [-Force]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4ab06-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4ab06-105">DESCRIPTION</span></span>
<span data-ttu-id="4ab06-106">Polecenie cmdlet **Set-AzureNetworkSecurityGroupToSubnet** kojarzy grupę zabezpieczeń sieci Azure z podsiecią.</span><span class="sxs-lookup"><span data-stu-id="4ab06-106">The **Set-AzureNetworkSecurityGroupToSubnet** cmdlet associates an Azure network security group to a subnet.</span></span>

## <span data-ttu-id="4ab06-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ab06-107">EXAMPLES</span></span>

## <span data-ttu-id="4ab06-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ab06-108">PARAMETERS</span></span>

### <span data-ttu-id="4ab06-109">-Force</span><span class="sxs-lookup"><span data-stu-id="4ab06-109">-Force</span></span>
<span data-ttu-id="4ab06-110">Wskazuje, że to polecenie cmdlet nie wyświetla monitu o potwierdzenie usunięcia poprzedniej grupy zabezpieczeń sieci z podsieci.</span><span class="sxs-lookup"><span data-stu-id="4ab06-110">Indicates that this cmdlet does not prompt you to confirm the removal of a previous network security group from the subnet.</span></span>

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

### <span data-ttu-id="4ab06-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4ab06-111">-Name</span></span>
<span data-ttu-id="4ab06-112">Określa nazwę grupy zabezpieczeń sieci, którą to polecenie cmdlet skojarzy z podsiecią.</span><span class="sxs-lookup"><span data-stu-id="4ab06-112">Specifies the name of the network security group that this cmdlet associates to a subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ab06-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ab06-113">-PassThru</span></span>
<span data-ttu-id="4ab06-114">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="4ab06-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="4ab06-115">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="4ab06-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4ab06-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="4ab06-116">-Profile</span></span>
<span data-ttu-id="4ab06-117">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ab06-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="4ab06-118">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="4ab06-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4ab06-119">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="4ab06-119">-SubnetName</span></span>
<span data-ttu-id="4ab06-120">Określa nazwę podsieci, do której to polecenie cmdlet kojarzy grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="4ab06-120">Specifies the name of a subnet to which this cmdlet associates a network security group.</span></span>

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

### <span data-ttu-id="4ab06-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="4ab06-121">-VirtualNetworkName</span></span>
<span data-ttu-id="4ab06-122">Określa nazwę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4ab06-122">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="4ab06-123">To polecenie cmdlet kojarzy grupę zabezpieczeń sieci z podsiecią w sieci wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="4ab06-123">This cmdlet associates a network security group to a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="4ab06-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ab06-124">CommonParameters</span></span>
<span data-ttu-id="4ab06-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ab06-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ab06-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ab06-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ab06-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ab06-127">INPUTS</span></span>

## <span data-ttu-id="4ab06-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ab06-128">OUTPUTS</span></span>

## <span data-ttu-id="4ab06-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ab06-129">NOTES</span></span>

## <span data-ttu-id="4ab06-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ab06-130">RELATED LINKS</span></span>

[<span data-ttu-id="4ab06-131">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="4ab06-131">Get-AzureNetworkSecurityGroupForSubnet</span></span>](./Get-AzureNetworkSecurityGroupForSubnet.md)

[<span data-ttu-id="4ab06-132">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="4ab06-132">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>](./Remove-AzureNetworkSecurityGroupFromSubnet.md)


