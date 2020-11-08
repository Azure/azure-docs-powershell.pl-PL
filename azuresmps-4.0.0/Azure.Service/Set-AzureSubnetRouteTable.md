---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 7E40C4A2-8B9A-47E8-82AB-19208247349C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 893e03f8e59b3cd01e7d96ca2d04119ee6fb4c66
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054778"
---
# <span data-ttu-id="ece69-101">Set-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="ece69-101">Set-AzureSubnetRouteTable</span></span>

## <span data-ttu-id="ece69-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ece69-102">SYNOPSIS</span></span>
<span data-ttu-id="ece69-103">Umożliwia skojarzenie tabeli routingu z podsiecią.</span><span class="sxs-lookup"><span data-stu-id="ece69-103">Associates a route table to a subnet.</span></span>

## <span data-ttu-id="ece69-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ece69-104">SYNTAX</span></span>

```
Set-AzureSubnetRouteTable -VirtualNetworkName <String> -SubnetName <String> -RouteTableName <String>
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ece69-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ece69-105">DESCRIPTION</span></span>
<span data-ttu-id="ece69-106">Polecenie cmdlet **Set-AzureSubnetRouteTable** kojarzy tabelę tras z podsiecią.</span><span class="sxs-lookup"><span data-stu-id="ece69-106">The **Set-AzureSubnetRouteTable** cmdlet associates a route table to a subnet.</span></span>

## <span data-ttu-id="ece69-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ece69-107">EXAMPLES</span></span>

### <span data-ttu-id="ece69-108">Przykład 1: Kojarzenie tabeli tras z podsiecią</span><span class="sxs-lookup"><span data-stu-id="ece69-108">Example 1: Associate a route table to a subnet</span></span>
```
PS C:\> Set-AzureSubnetRouteTable -VirtualNetworkName "VNetUSCentral" -SubnetName "ContosoSubnet" -RouteTableName "PublicRouteTable"
```

<span data-ttu-id="ece69-109">To polecenie kojarzy tabelę routingu o nazwie PublicRouteTable z podsiecią o nazwie ContosoSubnet.</span><span class="sxs-lookup"><span data-stu-id="ece69-109">This command associates the route table named PublicRouteTable to the subnet named ContosoSubnet.</span></span>

## <span data-ttu-id="ece69-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ece69-110">PARAMETERS</span></span>

### <span data-ttu-id="ece69-111">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ece69-111">-PassThru</span></span>
<span data-ttu-id="ece69-112">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="ece69-112">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ece69-113">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="ece69-113">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ece69-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="ece69-114">-Profile</span></span>
<span data-ttu-id="ece69-115">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ece69-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ece69-116">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="ece69-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ece69-117">-RouteTableName</span><span class="sxs-lookup"><span data-stu-id="ece69-117">-RouteTableName</span></span>
<span data-ttu-id="ece69-118">Określa nazwę tabeli tras, którą to polecenie cmdlet kojarzy z podsiecią.</span><span class="sxs-lookup"><span data-stu-id="ece69-118">Specifies the name of the route table that this cmdlet associates with a subnet.</span></span>

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

### <span data-ttu-id="ece69-119">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="ece69-119">-SubnetName</span></span>
<span data-ttu-id="ece69-120">Określa podsieć, do której to polecenie cmdlet kojarzy tabelę routingu.</span><span class="sxs-lookup"><span data-stu-id="ece69-120">Specifies the subnet to which this cmdlet associates the route table.</span></span>

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

### <span data-ttu-id="ece69-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ece69-121">-VirtualNetworkName</span></span>
<span data-ttu-id="ece69-122">Określa nazwę sieci wirtualnej zawierającej podsieć, do której to polecenie cmdlet kojarzy tabelę routingu.</span><span class="sxs-lookup"><span data-stu-id="ece69-122">Specifies the name of a virtual network that contains the subnet to which this cmdlet associates the route table.</span></span>

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

### <span data-ttu-id="ece69-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece69-123">CommonParameters</span></span>
<span data-ttu-id="ece69-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ece69-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece69-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ece69-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece69-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ece69-126">INPUTS</span></span>

## <span data-ttu-id="ece69-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ece69-127">OUTPUTS</span></span>

## <span data-ttu-id="ece69-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ece69-128">NOTES</span></span>

## <span data-ttu-id="ece69-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ece69-129">RELATED LINKS</span></span>

[<span data-ttu-id="ece69-130">Get-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="ece69-130">Get-AzureSubnetRouteTable</span></span>](./Get-AzureSubnetRouteTable.md)

[<span data-ttu-id="ece69-131">Remove-AzureSubnetRouteTable</span><span class="sxs-lookup"><span data-stu-id="ece69-131">Remove-AzureSubnetRouteTable</span></span>](./Remove-AzureSubnetRouteTable.md)
