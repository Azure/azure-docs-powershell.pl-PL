---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
ms.openlocfilehash: 8095e2ebd1d9e55e8f5bc847f4a72277363e197a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552700"
---
# <span data-ttu-id="a90c6-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="a90c6-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="a90c6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a90c6-102">SYNOPSIS</span></span>
<span data-ttu-id="a90c6-103">Pobiera efektywną tabelę tras dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="a90c6-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a90c6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a90c6-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a90c6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a90c6-105">DESCRIPTION</span></span>
<span data-ttu-id="a90c6-106">Polecenie cmdlet **Get-AzureRmEffectiveRouteTable** zwraca tabelę efektywnej trasy zastosowaną na interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="a90c6-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="a90c6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a90c6-107">EXAMPLES</span></span>

### <span data-ttu-id="a90c6-108">Przykład 1: uzyskiwanie efektywnej tabeli routingu na interfejsie sieciowym</span><span class="sxs-lookup"><span data-stu-id="a90c6-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="a90c6-109">To polecenie pobiera efektywną tabelę tras skojarzoną z interfejsem sieciowym o nazwie MyNetworkInterface w grupie zasobów o nazwie Moja zasobów.</span><span class="sxs-lookup"><span data-stu-id="a90c6-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="a90c6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a90c6-110">PARAMETERS</span></span>

### <span data-ttu-id="a90c6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a90c6-111">-AsJob</span></span>
<span data-ttu-id="a90c6-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a90c6-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a90c6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a90c6-113">-DefaultProfile</span></span>
<span data-ttu-id="a90c6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a90c6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a90c6-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="a90c6-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="a90c6-116">Określa nazwę interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="a90c6-116">Specified the name of a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a90c6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a90c6-117">-ResourceGroupName</span></span>
<span data-ttu-id="a90c6-118">Określa grupę zasobów interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="a90c6-118">Specifies the resource group of a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a90c6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a90c6-119">CommonParameters</span></span>
<span data-ttu-id="a90c6-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a90c6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a90c6-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a90c6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a90c6-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a90c6-122">INPUTS</span></span>

### <span data-ttu-id="a90c6-123">System. String</span><span class="sxs-lookup"><span data-stu-id="a90c6-123">System.String</span></span>

## <span data-ttu-id="a90c6-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a90c6-124">OUTPUTS</span></span>

### <span data-ttu-id="a90c6-125">Microsoft. Azure. Commands. Network. models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="a90c6-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="a90c6-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a90c6-126">NOTES</span></span>

## <span data-ttu-id="a90c6-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a90c6-127">RELATED LINKS</span></span>

[<span data-ttu-id="a90c6-128">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a90c6-128">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)


