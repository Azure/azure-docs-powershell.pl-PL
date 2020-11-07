---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectivenetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: 214ab7f91791fa05453e2f4ef4238440d9c78a3d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897973"
---
# <span data-ttu-id="117ad-101">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="117ad-101">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="117ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="117ad-102">SYNOPSIS</span></span>
<span data-ttu-id="117ad-103">Pobiera skuteczną grupę zabezpieczeń sieci interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="117ad-103">Gets the effective network security group of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="117ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="117ad-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="117ad-105">Opis</span><span class="sxs-lookup"><span data-stu-id="117ad-105">DESCRIPTION</span></span>
<span data-ttu-id="117ad-106">Polecenie cmdlet **Get-AzureRmEffectiveNetworkSecurityGroup** zwraca skuteczną grupę zabezpieczeń sieci stosowaną na interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="117ad-106">The **Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="117ad-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="117ad-107">EXAMPLES</span></span>

### <span data-ttu-id="117ad-108">Przykład 1: uzyskiwanie efektywnej grupy zabezpieczeń sieci na interfejsie sieciowym</span><span class="sxs-lookup"><span data-stu-id="117ad-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="117ad-109">To polecenie pobiera wszystkie efektywne reguły zabezpieczeń sieci skojarzone z interfejsem sieciowym o nazwie MyNetworkInterface w grupie zasobów o nazwie moja grupa.</span><span class="sxs-lookup"><span data-stu-id="117ad-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="117ad-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="117ad-110">PARAMETERS</span></span>

### <span data-ttu-id="117ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="117ad-111">-DefaultProfile</span></span>
<span data-ttu-id="117ad-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="117ad-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="117ad-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="117ad-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="117ad-114">Określa nazwę interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="117ad-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="117ad-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="117ad-115">-ResourceGroupName</span></span>
<span data-ttu-id="117ad-116">Określa grupę zasobów interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="117ad-116">Specifies the resource group of a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="117ad-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="117ad-117">CommonParameters</span></span>
<span data-ttu-id="117ad-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="117ad-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="117ad-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="117ad-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="117ad-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="117ad-120">INPUTS</span></span>

## <span data-ttu-id="117ad-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="117ad-121">OUTPUTS</span></span>

### <span data-ttu-id="117ad-122">Microsoft. Azure. Commands. Network. models. PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="117ad-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="117ad-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="117ad-123">NOTES</span></span>

## <span data-ttu-id="117ad-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="117ad-124">RELATED LINKS</span></span>

[<span data-ttu-id="117ad-125">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="117ad-125">Get-AzureRmEffectiveRouteTable</span></span>](./Get-AzureRmEffectiveRouteTable.md)


