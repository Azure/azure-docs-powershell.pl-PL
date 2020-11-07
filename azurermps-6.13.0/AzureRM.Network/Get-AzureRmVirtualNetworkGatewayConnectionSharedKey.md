---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: c2a1a63abb18f5f47ed155f24e8ac73a7bae83ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717395"
---
# <span data-ttu-id="e2c30-101">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="e2c30-101">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="e2c30-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2c30-102">SYNOPSIS</span></span>
<span data-ttu-id="e2c30-103">Umożliwia wyświetlenie klucza współużytkowanego dla połączenia.</span><span class="sxs-lookup"><span data-stu-id="e2c30-103">Displays the shared key used for the connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2c30-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2c30-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2c30-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e2c30-105">DESCRIPTION</span></span>
<span data-ttu-id="e2c30-106">Umożliwia wyświetlenie klucza współużytkowanego dla połączenia.</span><span class="sxs-lookup"><span data-stu-id="e2c30-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="e2c30-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2c30-107">EXAMPLES</span></span>

### <span data-ttu-id="e2c30-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e2c30-108">Example 1</span></span>
```
Get-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="e2c30-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2c30-109">PARAMETERS</span></span>

### <span data-ttu-id="e2c30-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2c30-110">-DefaultProfile</span></span>
<span data-ttu-id="e2c30-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2c30-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2c30-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e2c30-112">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2c30-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2c30-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="e2c30-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2c30-114">CommonParameters</span></span>
<span data-ttu-id="e2c30-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2c30-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2c30-116">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2c30-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2c30-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2c30-117">INPUTS</span></span>

### <span data-ttu-id="e2c30-118">System. String</span><span class="sxs-lookup"><span data-stu-id="e2c30-118">System.String</span></span>

## <span data-ttu-id="e2c30-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2c30-119">OUTPUTS</span></span>

### <span data-ttu-id="e2c30-120">System. String</span><span class="sxs-lookup"><span data-stu-id="e2c30-120">System.String</span></span>

## <span data-ttu-id="e2c30-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2c30-121">NOTES</span></span>

## <span data-ttu-id="e2c30-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2c30-122">RELATED LINKS</span></span>
