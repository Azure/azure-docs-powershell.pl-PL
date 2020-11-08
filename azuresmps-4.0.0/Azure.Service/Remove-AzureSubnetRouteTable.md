---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AA2F2793-03A5-41D9-8021-D18BE98DB044
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9bf26bd23ecc3dcb9e6973baf4c5eecf3d544402
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055422"
---
# <span data-ttu-id="3227e-101">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="3227e-101">Remove-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="3227e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3227e-102">SYNOPSIS</span></span>
<span data-ttu-id="3227e-103">Usuwa skojarzenie tabeli tras z podsieci.</span><span class="sxs-lookup"><span data-stu-id="3227e-103">Removes a route table association from a subnet.</span></span>

## <span data-ttu-id="3227e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3227e-104">SYNTAX</span></span>

```
Remove-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> [-Force] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3227e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3227e-105">DESCRIPTION</span></span>
<span data-ttu-id="3227e-106">Polecenie cmdlet **Remove-AzureSubnetRouteTable** Usuwa skojarzenie tabeli routingu z podsieci.</span><span class="sxs-lookup"><span data-stu-id="3227e-106">The **Remove-AzureSubnetRouteTable** cmdlet removes a route table association from a subnet.</span></span>

## <span data-ttu-id="3227e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3227e-107">EXAMPLES</span></span>

### <span data-ttu-id="3227e-108">Przykład 1: Usuwanie skojarzenia między tabelą routingu a podsiecią</span><span class="sxs-lookup"><span data-stu-id="3227e-108">Example 1: Remove an association between a route table and a subnet</span></span>
```
PS C:\> Remove-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet"
```

<span data-ttu-id="3227e-109">To polecenie usuwa skojarzenie tabeli routingu o nazwie PublicRouteTable z podsiecią o nazwie ContosoSubnet.</span><span class="sxs-lookup"><span data-stu-id="3227e-109">This command removes the association of the route table named PublicRouteTable to the subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="3227e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3227e-110">PARAMETERS</span></span>

### <span data-ttu-id="3227e-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3227e-111">-Force</span></span>
<span data-ttu-id="3227e-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3227e-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3227e-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3227e-113">-PassThru</span></span>
<span data-ttu-id="3227e-114">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="3227e-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="3227e-115">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="3227e-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3227e-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="3227e-116">-Profile</span></span>
<span data-ttu-id="3227e-117">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3227e-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3227e-118">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="3227e-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3227e-119">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="3227e-119">-SubnetName</span></span>
<span data-ttu-id="3227e-120">Określa podsieć, dla której to polecenie cmdlet usuwa tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="3227e-120">Specifies the subnet for which this cmdlet removes the route table.</span></span>

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

### <span data-ttu-id="3227e-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3227e-121">-VirtualNetworkName</span></span>
<span data-ttu-id="3227e-122">Określa nazwę sieci wirtualnej zawierającej podsieć, dla której to polecenie cmdlet usuwa tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="3227e-122">Specifies the name of a virtual network that contains the subnet for which this cmdlet removes the route table.</span></span>

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

### <span data-ttu-id="3227e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3227e-123">CommonParameters</span></span>
<span data-ttu-id="3227e-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3227e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3227e-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3227e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3227e-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3227e-126">INPUTS</span></span>

## <span data-ttu-id="3227e-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3227e-127">OUTPUTS</span></span>

## <span data-ttu-id="3227e-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3227e-128">NOTES</span></span>

## <span data-ttu-id="3227e-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3227e-129">RELATED LINKS</span></span>

[<span data-ttu-id="3227e-130">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="3227e-130">Get-AzureSubnetRouteTable</span></span>](./Get-AzureSubnetRouteTable.md)

[<span data-ttu-id="3227e-131">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="3227e-131">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


