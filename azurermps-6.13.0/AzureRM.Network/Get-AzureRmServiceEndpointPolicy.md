---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: 989b6aa91c0dabec1b72425f214c4097df374041
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541707"
---
# <span data-ttu-id="673ec-101">Get-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="673ec-101">Get-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="673ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="673ec-102">SYNOPSIS</span></span>
<span data-ttu-id="673ec-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="673ec-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="673ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="673ec-104">SYNTAX</span></span>

```
Get-AzureRmServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="673ec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="673ec-105">DESCRIPTION</span></span>
<span data-ttu-id="673ec-106">Polecenie cmdlet **Get-AzureRmServiceEndpointPolicy** pobiera zasadę punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="673ec-106">The **Get-AzureRmServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="673ec-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="673ec-107">EXAMPLES</span></span>

### <span data-ttu-id="673ec-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="673ec-108">Example 1</span></span>
```
$policy = Get-AzureRmServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="673ec-109">To polecenie pobiera zasady punktu końcowego usługi o nazwie ServiceEndpointPolicy1 należące do grupy zasobów o nazwie ResourceGroup01 i zapisuje je w zmiennej $policy.</span><span class="sxs-lookup"><span data-stu-id="673ec-109">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="673ec-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="673ec-110">Example 2</span></span>
```
$policyList = Get-AzureRmServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="673ec-111">To polecenie pobiera listę wszystkich zasad punktu końcowego usługi w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $policyList.</span><span class="sxs-lookup"><span data-stu-id="673ec-111">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

## <span data-ttu-id="673ec-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="673ec-112">PARAMETERS</span></span>

### <span data-ttu-id="673ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="673ec-113">-DefaultProfile</span></span>
<span data-ttu-id="673ec-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="673ec-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="673ec-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="673ec-115">-Name</span></span>
<span data-ttu-id="673ec-116">Nazwa zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="673ec-116">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="673ec-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="673ec-117">-ResourceGroupName</span></span>
<span data-ttu-id="673ec-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="673ec-118">The resource group name.</span></span>

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

### <span data-ttu-id="673ec-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="673ec-119">CommonParameters</span></span>
<span data-ttu-id="673ec-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="673ec-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="673ec-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="673ec-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="673ec-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="673ec-122">INPUTS</span></span>

### <span data-ttu-id="673ec-123">System. String</span><span class="sxs-lookup"><span data-stu-id="673ec-123">System.String</span></span>


## <span data-ttu-id="673ec-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="673ec-124">OUTPUTS</span></span>

### <span data-ttu-id="673ec-125">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="673ec-125">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="673ec-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="673ec-126">NOTES</span></span>

## <span data-ttu-id="673ec-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="673ec-127">RELATED LINKS</span></span>
