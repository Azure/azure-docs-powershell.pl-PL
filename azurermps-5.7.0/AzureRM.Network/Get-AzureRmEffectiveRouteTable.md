---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
ms.openlocfilehash: 7826dad8b9f19e3fc289ec4b08efa98b8b1ed8a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717486"
---
# <span data-ttu-id="98c4b-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="98c4b-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="98c4b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98c4b-102">SYNOPSIS</span></span>
<span data-ttu-id="98c4b-103">Pobiera efektywną tabelę tras dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="98c4b-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98c4b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98c4b-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98c4b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="98c4b-105">DESCRIPTION</span></span>
<span data-ttu-id="98c4b-106">Polecenie cmdlet **Get-AzureRmEffectiveRouteTable** zwraca tabelę efektywnej trasy zastosowaną na interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="98c4b-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="98c4b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98c4b-107">EXAMPLES</span></span>

### <span data-ttu-id="98c4b-108">Przykład 1: uzyskiwanie efektywnej tabeli routingu na interfejsie sieciowym</span><span class="sxs-lookup"><span data-stu-id="98c4b-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="98c4b-109">To polecenie pobiera efektywną tabelę tras skojarzoną z interfejsem sieciowym o nazwie MyNetworkInterface w grupie zasobów o nazwie Moja zasobów.</span><span class="sxs-lookup"><span data-stu-id="98c4b-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="98c4b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98c4b-110">PARAMETERS</span></span>

### <span data-ttu-id="98c4b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98c4b-111">-AsJob</span></span>
<span data-ttu-id="98c4b-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="98c4b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98c4b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c4b-113">-DefaultProfile</span></span>
<span data-ttu-id="98c4b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="98c4b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98c4b-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="98c4b-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="98c4b-116">Określa nazwę interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="98c4b-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="98c4b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98c4b-117">-ResourceGroupName</span></span>
<span data-ttu-id="98c4b-118">Określa grupę zasobów interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="98c4b-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="98c4b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c4b-119">CommonParameters</span></span>
<span data-ttu-id="98c4b-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98c4b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c4b-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98c4b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c4b-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98c4b-122">INPUTS</span></span>

### <span data-ttu-id="98c4b-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="98c4b-123">None</span></span>
<span data-ttu-id="98c4b-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="98c4b-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="98c4b-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98c4b-125">OUTPUTS</span></span>

### <span data-ttu-id="98c4b-126">Microsoft. Azure. Commands. Network. models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="98c4b-126">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="98c4b-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98c4b-127">NOTES</span></span>

## <span data-ttu-id="98c4b-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98c4b-128">RELATED LINKS</span></span>

[<span data-ttu-id="98c4b-129">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="98c4b-129">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)


