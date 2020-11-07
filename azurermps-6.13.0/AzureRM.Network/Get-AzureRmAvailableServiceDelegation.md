---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmAvailableServiceDelegation.md
ms.openlocfilehash: bc5c09913209713df192603aff7ea7646e651699
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717914"
---
# <span data-ttu-id="ddbd0-101">Get-AzureRmAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="ddbd0-101">Get-AzureRmAvailableServiceDelegation</span></span>

## <span data-ttu-id="ddbd0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ddbd0-102">SYNOPSIS</span></span>
<span data-ttu-id="ddbd0-103">Uzyskiwanie dostępnych delegowań usług w regionie.</span><span class="sxs-lookup"><span data-stu-id="ddbd0-103">Get available service delegations in the region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddbd0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ddbd0-104">SYNTAX</span></span>

```
Get-AzureRmAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ddbd0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ddbd0-105">DESCRIPTION</span></span>
<span data-ttu-id="ddbd0-106">Polecenie cmdlet **Get-AzureRmAvailableServiceDelegation** umożliwia pobieranie wszystkich dostępnych delegowań usługi dla podsieci w podanej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="ddbd0-106">The **Get-AzureRmAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="ddbd0-107">W tym poleceniu cmdlet *nie* opisano, które delegacje mogą współistnieć w jednej podsieci.</span><span class="sxs-lookup"><span data-stu-id="ddbd0-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="ddbd0-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ddbd0-108">EXAMPLES</span></span>

### <span data-ttu-id="ddbd0-109">1: uzyskiwanie wszystkich dostępnych delegowań usług</span><span class="sxs-lookup"><span data-stu-id="ddbd0-109">1: Getting all available service delegations</span></span>
```powershell
PS C:\> Get-AzureRmAvailableServiceDelegation -Location "westus"

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

## <span data-ttu-id="ddbd0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ddbd0-110">PARAMETERS</span></span>

### <span data-ttu-id="ddbd0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddbd0-111">-DefaultProfile</span></span>
<span data-ttu-id="ddbd0-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ddbd0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddbd0-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ddbd0-113">-Location</span></span>
<span data-ttu-id="ddbd0-114">Lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="ddbd0-114">The location.</span></span>

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

### <span data-ttu-id="ddbd0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddbd0-115">CommonParameters</span></span>
<span data-ttu-id="ddbd0-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddbd0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ddbd0-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddbd0-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddbd0-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ddbd0-118">INPUTS</span></span>

### <span data-ttu-id="ddbd0-119">System. String</span><span class="sxs-lookup"><span data-stu-id="ddbd0-119">System.String</span></span>

## <span data-ttu-id="ddbd0-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ddbd0-120">OUTPUTS</span></span>

### <span data-ttu-id="ddbd0-121">Microsoft. Azure. Commands. Network. models. PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="ddbd0-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="ddbd0-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ddbd0-122">NOTES</span></span>

## <span data-ttu-id="ddbd0-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ddbd0-123">RELATED LINKS</span></span>
<span data-ttu-id="ddbd0-124">[Dodaj-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [Nowe — AzureRmDelegation](./New-AzureRmDelegation.md) 
 [Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmDelegation](./Get-AzureRmDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="ddbd0-124">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)</span></span>
