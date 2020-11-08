---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AEFC9094-144F-4E29-AC5A-DBFDA175A920
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8e56496c1fdf04b5227121f5ac39193938a2214e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054508"
---
# <span data-ttu-id="a6f1a-101">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6f1a-101">Get-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="a6f1a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a6f1a-102">SYNOPSIS</span></span>
<span data-ttu-id="a6f1a-103">Pobiera tabelę tras dla podsieci.</span><span class="sxs-lookup"><span data-stu-id="a6f1a-103">Gets a route table for a subnet.</span></span>

## <span data-ttu-id="a6f1a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a6f1a-104">SYNTAX</span></span>

```
Get-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a6f1a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a6f1a-105">DESCRIPTION</span></span>
<span data-ttu-id="a6f1a-106">Polecenie cmdlet **Get-AzureSubnetRouteTable** pobiera tabelę tras, która jest skojarzona z podsiecią.</span><span class="sxs-lookup"><span data-stu-id="a6f1a-106">The **Get-AzureSubnetRouteTable** cmdlet gets the route table that is associated with a subnet.</span></span>

## <span data-ttu-id="a6f1a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a6f1a-107">EXAMPLES</span></span>

### <span data-ttu-id="a6f1a-108">Przykład 1. Wyświetl trasy dla podsieci</span><span class="sxs-lookup"><span data-stu-id="a6f1a-108">Example 1: Display routes for a subnet</span></span>
```
PS C:\> Get-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet" -Detailed
Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{internetroute}               PublicRT                      Central US                    Sample RT in Central US
```

<span data-ttu-id="a6f1a-109">To polecenie wyświetla trasy w nazwie tabeli routingu skojarzonej z podsiecią o nazwie ContosoSubnet.</span><span class="sxs-lookup"><span data-stu-id="a6f1a-109">This command displays the routes in the route table name that is associated with subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="a6f1a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a6f1a-110">PARAMETERS</span></span>

### <span data-ttu-id="a6f1a-111">— Szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="a6f1a-111">-Detailed</span></span>
<span data-ttu-id="a6f1a-112">Wskazuje, że w tym poleceniu cmdlet są wyświetlane trasy w tabeli tras, która jest skojarzona z podsiecią.</span><span class="sxs-lookup"><span data-stu-id="a6f1a-112">Indicates that this cmdlet displays the routes in the route table that is associated with the subnet.</span></span>

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

### <span data-ttu-id="a6f1a-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="a6f1a-113">-Profile</span></span>
<span data-ttu-id="a6f1a-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6f1a-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a6f1a-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="a6f1a-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a6f1a-116">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="a6f1a-116">-SubnetName</span></span>
<span data-ttu-id="a6f1a-117">Określa podsieć, dla której to polecenie cmdlet pobiera tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="a6f1a-117">Specifies the subnet for which this cmdlet gets the route table.</span></span>

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

### <span data-ttu-id="a6f1a-118">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a6f1a-118">-VirtualNetworkName</span></span>
<span data-ttu-id="a6f1a-119">Określa nazwę sieci wirtualnej zawierającej podsieć, dla której to polecenie cmdlet pobiera tabelę tras.</span><span class="sxs-lookup"><span data-stu-id="a6f1a-119">Specifies the name of a virtual network that contains the subnet for which this cmdlet gets the route table.</span></span>

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

### <span data-ttu-id="a6f1a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6f1a-120">CommonParameters</span></span>
<span data-ttu-id="a6f1a-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6f1a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6f1a-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6f1a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6f1a-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6f1a-123">INPUTS</span></span>

## <span data-ttu-id="a6f1a-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a6f1a-124">OUTPUTS</span></span>

## <span data-ttu-id="a6f1a-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a6f1a-125">NOTES</span></span>

## <span data-ttu-id="a6f1a-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6f1a-126">RELATED LINKS</span></span>

[<span data-ttu-id="a6f1a-127">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6f1a-127">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)

[<span data-ttu-id="a6f1a-128">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="a6f1a-128">Set-AzureSubnetRouteTable</span></span>](./Set-AzureSubnetRouteTable.md)


