---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkavailableendpointservice
schema: 2.0.0
ms.openlocfilehash: ed33d1a683e10e0e39d0b722dec92b7f7ba11254
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897926"
---
# <span data-ttu-id="54bcf-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="54bcf-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="54bcf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="54bcf-102">SYNOPSIS</span></span>
<span data-ttu-id="54bcf-103">Wyświetla listę dostępnych usług punktu końcowego dla lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="54bcf-103">Lists available endpoint services for location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54bcf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="54bcf-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54bcf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="54bcf-105">DESCRIPTION</span></span>
<span data-ttu-id="54bcf-106">Get-AzureRmVirtualNetworkAvailableEndpointService wyświetla listę usług punktu końcowego dostępnych w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="54bcf-106">Get-AzureRmVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="54bcf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="54bcf-107">EXAMPLES</span></span>

### <span data-ttu-id="54bcf-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="54bcf-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="54bcf-109">Pobiera dostępne usługi punktu końcowego w regionie zachód.</span><span class="sxs-lookup"><span data-stu-id="54bcf-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="54bcf-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="54bcf-110">PARAMETERS</span></span>

### <span data-ttu-id="54bcf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54bcf-111">-DefaultProfile</span></span>
<span data-ttu-id="54bcf-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="54bcf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54bcf-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="54bcf-113">-Location</span></span>
<span data-ttu-id="54bcf-114">Lokalizacja, z której mają zostać pobrane usługi punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="54bcf-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="54bcf-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54bcf-115">CommonParameters</span></span>
<span data-ttu-id="54bcf-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54bcf-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54bcf-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54bcf-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54bcf-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54bcf-118">INPUTS</span></span>

### <span data-ttu-id="54bcf-119">System. String</span><span class="sxs-lookup"><span data-stu-id="54bcf-119">System.String</span></span>

## <span data-ttu-id="54bcf-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="54bcf-120">OUTPUTS</span></span>

### <span data-ttu-id="54bcf-121">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Network. MODELES. PSEndpointServiceResult; Microsoft. Azure. Commands. Network, Version = 4.2.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="54bcf-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult, Microsoft.Azure.Commands.Network, Version=4.2.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="54bcf-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="54bcf-122">NOTES</span></span>

## <span data-ttu-id="54bcf-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54bcf-123">RELATED LINKS</span></span>

