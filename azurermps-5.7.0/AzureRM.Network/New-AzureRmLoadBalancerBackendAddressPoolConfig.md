---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: cbac48c8f9f79dc74453222c162fee105cce2fdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548899"
---
# <span data-ttu-id="01a85-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="01a85-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="01a85-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="01a85-102">SYNOPSIS</span></span>
<span data-ttu-id="01a85-103">Tworzy konfigurację puli adresów zaplecza modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="01a85-103">Creates a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01a85-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="01a85-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01a85-105">Opis</span><span class="sxs-lookup"><span data-stu-id="01a85-105">DESCRIPTION</span></span>
<span data-ttu-id="01a85-106">Polecenie cmdlet **New-AzureRmLoadBalancerBackendAddressPoolConfig** umożliwia utworzenie konfiguracji puli adresów zaplecza modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="01a85-106">The **New-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="01a85-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="01a85-107">EXAMPLES</span></span>

### <span data-ttu-id="01a85-108">Przykład 1. Tworzenie konfiguracji puli adresów zaplecza modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="01a85-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="01a85-109">To polecenie tworzy konfigurację puli adresów zaplecza o nazwie BackendAddressPool02 dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="01a85-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="01a85-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="01a85-110">PARAMETERS</span></span>

### <span data-ttu-id="01a85-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01a85-111">-DefaultProfile</span></span>
<span data-ttu-id="01a85-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="01a85-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01a85-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="01a85-113">-Name</span></span>
<span data-ttu-id="01a85-114">Określa nazwę konfiguracji puli adresów do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="01a85-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="01a85-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01a85-115">CommonParameters</span></span>
<span data-ttu-id="01a85-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01a85-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01a85-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01a85-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01a85-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="01a85-118">INPUTS</span></span>

### <span data-ttu-id="01a85-119">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="01a85-119">None</span></span>
<span data-ttu-id="01a85-120">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="01a85-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="01a85-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="01a85-121">OUTPUTS</span></span>

### <span data-ttu-id="01a85-122">Microsoft. Azure. Commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="01a85-122">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="01a85-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="01a85-123">NOTES</span></span>

## <span data-ttu-id="01a85-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="01a85-124">RELATED LINKS</span></span>

[<span data-ttu-id="01a85-125">Dodaj-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="01a85-125">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="01a85-126">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="01a85-126">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="01a85-127">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="01a85-127">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)

