---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
ms.openlocfilehash: f42e378bb0bb5202f9f955dea1b844e343a0e037
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546976"
---
# <span data-ttu-id="633e9-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="633e9-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="633e9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="633e9-102">SYNOPSIS</span></span>
<span data-ttu-id="633e9-103">Pobiera efektywną tabelę tras dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="633e9-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="633e9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="633e9-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="633e9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="633e9-105">DESCRIPTION</span></span>
<span data-ttu-id="633e9-106">Polecenie cmdlet **Get-AzureRmEffectiveRouteTable** zwraca tabelę efektywnej trasy zastosowaną na interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="633e9-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="633e9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="633e9-107">EXAMPLES</span></span>

### <span data-ttu-id="633e9-108">Przykład 1: uzyskiwanie efektywnej tabeli routingu na interfejsie sieciowym</span><span class="sxs-lookup"><span data-stu-id="633e9-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="633e9-109">To polecenie pobiera efektywną tabelę tras skojarzoną z interfejsem sieciowym o nazwie MyNetworkInterface w grupie zasobów o nazwie Moja zasobów.</span><span class="sxs-lookup"><span data-stu-id="633e9-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="633e9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="633e9-110">PARAMETERS</span></span>

### <span data-ttu-id="633e9-111">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="633e9-111">-NetworkInterfaceName</span></span>
<span data-ttu-id="633e9-112">Określa nazwę interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="633e9-112">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="633e9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="633e9-113">-ResourceGroupName</span></span>
<span data-ttu-id="633e9-114">Określa grupę zasobów interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="633e9-114">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="633e9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="633e9-115">-DefaultProfile</span></span>
<span data-ttu-id="633e9-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="633e9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="633e9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="633e9-117">CommonParameters</span></span>
<span data-ttu-id="633e9-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="633e9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="633e9-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="633e9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="633e9-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="633e9-120">INPUTS</span></span>

## <span data-ttu-id="633e9-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="633e9-121">OUTPUTS</span></span>

### <span data-ttu-id="633e9-122">Microsoft. Azure. Commands. Network. models. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="633e9-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="633e9-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="633e9-123">NOTES</span></span>

## <span data-ttu-id="633e9-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="633e9-124">RELATED LINKS</span></span>

[<span data-ttu-id="633e9-125">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="633e9-125">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)


