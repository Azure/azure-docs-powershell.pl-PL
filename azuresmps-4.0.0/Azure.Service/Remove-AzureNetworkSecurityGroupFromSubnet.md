---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BABA5142-541F-40C8-AFF5-20E4283BE147
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a718e2f675b4a5e204610a2d4f1fb1aac4c5478
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055116"
---
# <span data-ttu-id="d0f49-101">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="d0f49-101">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>

## <span data-ttu-id="d0f49-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0f49-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f49-103">Deskojarzenie grupy zabezpieczeń sieci z podsieci.</span><span class="sxs-lookup"><span data-stu-id="d0f49-103">Dissociates a network security group from a subnet.</span></span>

## <span data-ttu-id="d0f49-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0f49-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityGroupFromSubnet -Name <String> -VirtualNetworkName <String> -SubnetName <String>
 [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d0f49-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d0f49-105">DESCRIPTION</span></span>
<span data-ttu-id="d0f49-106">Polecenie cmdlet **Remove-AzureNetworkSecurityGroupFromSubnet** umożliwia skojarzenie grupy zabezpieczeń sieci Azure z podsieci.</span><span class="sxs-lookup"><span data-stu-id="d0f49-106">The **Remove-AzureNetworkSecurityGroupFromSubnet** cmdlet dissociates an Azure network security group from a subnet.</span></span>

## <span data-ttu-id="d0f49-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0f49-107">EXAMPLES</span></span>

## <span data-ttu-id="d0f49-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0f49-108">PARAMETERS</span></span>

### <span data-ttu-id="d0f49-109">-Force</span><span class="sxs-lookup"><span data-stu-id="d0f49-109">-Force</span></span>
<span data-ttu-id="d0f49-110">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d0f49-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d0f49-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d0f49-111">-Name</span></span>
<span data-ttu-id="d0f49-112">Określa nazwę grupy zabezpieczeń sieci, którą to polecenie cmdlet ma skojarzenie z podsiecią.</span><span class="sxs-lookup"><span data-stu-id="d0f49-112">Specifies the name of the network security group that this cmdlet dissociates from a subnet.</span></span>

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

### <span data-ttu-id="d0f49-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0f49-113">-PassThru</span></span>
<span data-ttu-id="d0f49-114">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="d0f49-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="d0f49-115">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d0f49-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d0f49-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="d0f49-116">-Profile</span></span>
<span data-ttu-id="d0f49-117">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0f49-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d0f49-118">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="d0f49-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d0f49-119">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="d0f49-119">-SubnetName</span></span>
<span data-ttu-id="d0f49-120">Określa nazwę podsieci, z której to polecenie cmdlet powoduje skojarzenie grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="d0f49-120">Specifies the name of a subnet from which this cmdlet dissociates a network security group.</span></span>

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

### <span data-ttu-id="d0f49-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d0f49-121">-VirtualNetworkName</span></span>
<span data-ttu-id="d0f49-122">Określa nazwę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d0f49-122">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="d0f49-123">To polecenie cmdlet powoduje odkojarzenie grupy zabezpieczeń sieci z podsieci w sieci wirtualnej, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="d0f49-123">This cmdlet disassociates a network security group from a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="d0f49-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f49-124">CommonParameters</span></span>
<span data-ttu-id="d0f49-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0f49-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f49-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0f49-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0f49-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0f49-127">INPUTS</span></span>

## <span data-ttu-id="d0f49-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0f49-128">OUTPUTS</span></span>

## <span data-ttu-id="d0f49-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0f49-129">NOTES</span></span>

## <span data-ttu-id="d0f49-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0f49-130">RELATED LINKS</span></span>

[<span data-ttu-id="d0f49-131">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="d0f49-131">Get-AzureNetworkSecurityGroupForSubnet</span></span>](./Get-AzureNetworkSecurityGroupForSubnet.md)

[<span data-ttu-id="d0f49-132">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="d0f49-132">Set-AzureNetworkSecurityGroupToSubnet</span></span>](./Set-AzureNetworkSecurityGroupToSubnet.md)


