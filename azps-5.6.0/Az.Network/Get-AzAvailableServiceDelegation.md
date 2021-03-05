---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azavailableservicedelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceDelegation.md
ms.openlocfilehash: d98b9d2395c0795c37fd9d7cf31dc354bde3b7cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993847"
---
# <span data-ttu-id="de177-101">Get-AzAvailableServiceDelegation</span><span class="sxs-lookup"><span data-stu-id="de177-101">Get-AzAvailableServiceDelegation</span></span>

## <span data-ttu-id="de177-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de177-102">SYNOPSIS</span></span>
<span data-ttu-id="de177-103">Uzyskaj dostępne delegowanie usługi w regionie.</span><span class="sxs-lookup"><span data-stu-id="de177-103">Get available service delegations in the region.</span></span>

## <span data-ttu-id="de177-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="de177-104">SYNTAX</span></span>

```
Get-AzAvailableServiceDelegation -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de177-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="de177-105">DESCRIPTION</span></span>
<span data-ttu-id="de177-106">Polecenie **cmdlet Get-AzAvailableServiceDelegation** umożliwia pobieranie wszystkich dostępnych delegowania usługi do podsieci w podanej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="de177-106">The **Get-AzAvailableServiceDelegation** cmdlet allows you to retrieve all of the available service delegations for a subnet in the provided location.</span></span> <span data-ttu-id="de177-107">To polecenie cmdlet *nie opisuje,* które delegowania mogą istnieć w jednej podsieci.</span><span class="sxs-lookup"><span data-stu-id="de177-107">This cmdlet does *not* describe which delegations may co-exist on a single subnet.</span></span>

## <span data-ttu-id="de177-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="de177-108">EXAMPLES</span></span>

### <span data-ttu-id="de177-109">1. Uzyskiwanie wszystkich dostępnych delegowania usługi</span><span class="sxs-lookup"><span data-stu-id="de177-109">1: Getting all available service delegations</span></span>
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

## <span data-ttu-id="de177-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de177-110">PARAMETERS</span></span>

### <span data-ttu-id="de177-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de177-111">-DefaultProfile</span></span>
<span data-ttu-id="de177-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="de177-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de177-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="de177-113">-Location</span></span>
<span data-ttu-id="de177-114">Lokalizacja.</span><span class="sxs-lookup"><span data-stu-id="de177-114">The location.</span></span>

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

### <span data-ttu-id="de177-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de177-115">CommonParameters</span></span>
<span data-ttu-id="de177-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de177-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de177-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de177-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de177-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de177-118">INPUTS</span></span>

### <span data-ttu-id="de177-119">System.String</span><span class="sxs-lookup"><span data-stu-id="de177-119">System.String</span></span>

## <span data-ttu-id="de177-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de177-120">OUTPUTS</span></span>

### <span data-ttu-id="de177-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span><span class="sxs-lookup"><span data-stu-id="de177-121">Microsoft.Azure.Commands.Network.Models.PSAvailableDelegation</span></span>

## <span data-ttu-id="de177-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="de177-122">NOTES</span></span>

## <span data-ttu-id="de177-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de177-123">RELATED LINKS</span></span>

<span data-ttu-id="de177-124">[Add-azDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="de177-124">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)</span></span>