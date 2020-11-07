---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: 37c9827f2af970c0c376c31f4d67ba7723e02e99
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890833"
---
# <span data-ttu-id="79a4d-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="79a4d-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="79a4d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="79a4d-103">Pobiera efektywną tabelę tras dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="79a4d-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="79a4d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79a4d-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79a4d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="79a4d-105">DESCRIPTION</span></span>
<span data-ttu-id="79a4d-106">Polecenie cmdlet **Get-AzEffectiveRouteTable** zwraca tabelę efektywnej trasy zastosowaną na interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="79a4d-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="79a4d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79a4d-107">EXAMPLES</span></span>

### <span data-ttu-id="79a4d-108">Przykład 1: uzyskiwanie efektywnej tabeli routingu na interfejsie sieciowym</span><span class="sxs-lookup"><span data-stu-id="79a4d-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="79a4d-109">To polecenie pobiera efektywną tabelę tras skojarzoną z interfejsem sieciowym o nazwie MyNetworkInterface w grupie zasobów o nazwie Moja zasobów.</span><span class="sxs-lookup"><span data-stu-id="79a4d-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="79a4d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79a4d-110">PARAMETERS</span></span>

### <span data-ttu-id="79a4d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79a4d-111">-AsJob</span></span>
<span data-ttu-id="79a4d-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="79a4d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79a4d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79a4d-113">-DefaultProfile</span></span>
<span data-ttu-id="79a4d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="79a4d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79a4d-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="79a4d-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="79a4d-116">Określa nazwę interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="79a4d-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="79a4d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79a4d-117">-ResourceGroupName</span></span>
<span data-ttu-id="79a4d-118">Określa grupę zasobów interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="79a4d-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="79a4d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a4d-119">CommonParameters</span></span>
<span data-ttu-id="79a4d-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79a4d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a4d-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79a4d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a4d-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79a4d-122">INPUTS</span></span>

## <span data-ttu-id="79a4d-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79a4d-123">OUTPUTS</span></span>

### <span data-ttu-id="79a4d-124">Microsoft. Azure. Commands. Network. models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="79a4d-124">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="79a4d-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79a4d-125">NOTES</span></span>

## <span data-ttu-id="79a4d-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79a4d-126">RELATED LINKS</span></span>

[<span data-ttu-id="79a4d-127">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="79a4d-127">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


