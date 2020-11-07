---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
ms.openlocfilehash: 169b7c2daffdf2c241a60468e745752ac7582d7d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894574"
---
# <span data-ttu-id="46630-101">Get-AzAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="46630-101">Get-AzAvailableServiceDelegation</span></span>

## <span data-ttu-id="46630-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46630-102">SYNOPSIS</span></span>
<span data-ttu-id="46630-103">Uzyskiwanie dostępnych delegowań usług w regionie.</span><span class="sxs-lookup"><span data-stu-id="46630-103">Get available service delegations in the region.</span></span>

## <span data-ttu-id="46630-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46630-104">SYNTAX</span></span>

```
Get-AzAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46630-105">Opis</span><span class="sxs-lookup"><span data-stu-id="46630-105">DESCRIPTION</span></span>
<span data-ttu-id="46630-106">Polecenie cmdlet **Get-AzAvailableServiceDelegation** umożliwia pobieranie wszystkich dostępnych delegowań usługi dla podsieci w podanej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="46630-106">The **Get-AzAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="46630-107">W tym poleceniu cmdlet *nie* opisano, które delegacje mogą współistnieć w jednej podsieci.</span><span class="sxs-lookup"><span data-stu-id="46630-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="46630-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46630-108">EXAMPLES</span></span>

### <span data-ttu-id="46630-109">1: uzyskiwanie wszystkich dostępnych delegowań usług</span><span class="sxs-lookup"><span data-stu-id="46630-109">1: Getting all available service delegations</span></span>
```powershell
PS C:\> Get-AzAvailableServiceDelegation -Location "westus"

Name        : Microsoft.Web.serverFarms
Id          : /subscriptions/subId/providers/Microsoft.Network/availableDelegations/Microsoft.Web.serverFarms
Type        : Microsoft.Network/availableDelegations
ServiceName : Microsoft.Web/serverFarms
Actions     : {Microsoft.Network/virtualNetworks/subnets/action}

Name        : Microsoft.Sql.servers
Id          : /subscriptions/subId/providers/Microsoft.Network/availableDelegations/Microsoft.Sql.servers
Type        : Microsoft.Network/availableDelegations
ServiceName : Microsoft.Sql/servers
Actions     : {}
```

## <span data-ttu-id="46630-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46630-110">PARAMETERS</span></span>

### <span data-ttu-id="46630-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46630-111">-DefaultProfile</span></span>
<span data-ttu-id="46630-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="46630-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46630-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="46630-113">-Location</span></span>
<span data-ttu-id="46630-114">Lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="46630-114">The location.</span></span>

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

### <span data-ttu-id="46630-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46630-115">CommonParameters</span></span>
<span data-ttu-id="46630-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46630-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46630-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46630-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46630-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46630-118">INPUTS</span></span>

### <span data-ttu-id="46630-119">System. String</span><span class="sxs-lookup"><span data-stu-id="46630-119">System.String</span></span>

## <span data-ttu-id="46630-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46630-120">OUTPUTS</span></span>

### <span data-ttu-id="46630-121">Microsoft. Azure. Commands. Network. models. PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="46630-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="46630-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46630-122">NOTES</span></span>

## <span data-ttu-id="46630-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46630-123">RELATED LINKS</span></span>

<span data-ttu-id="46630-124">[Dodaj-AzDelegation](./Add-AzDelegation.md) 
 [Nowe — AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="46630-124">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)</span></span>