---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 6d8ea34de1520326ead270ffa44837388729bc5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868116"
---
# <span data-ttu-id="790c9-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="790c9-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="790c9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="790c9-102">SYNOPSIS</span></span>
<span data-ttu-id="790c9-103">Pobiera metryki przydziału dla IotHub.</span><span class="sxs-lookup"><span data-stu-id="790c9-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="790c9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="790c9-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="790c9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="790c9-105">DESCRIPTION</span></span>
<span data-ttu-id="790c9-106">Pobiera metryki przydziału dla IotHub.</span><span class="sxs-lookup"><span data-stu-id="790c9-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="790c9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="790c9-107">EXAMPLES</span></span>

### <span data-ttu-id="790c9-108">Przykład 1 pobieranie metryki przydziału</span><span class="sxs-lookup"><span data-stu-id="790c9-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="790c9-109">Pobiera informacje metryki przydziału dla IotHub o nazwie "myiothub".</span><span class="sxs-lookup"><span data-stu-id="790c9-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="790c9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="790c9-110">PARAMETERS</span></span>

### <span data-ttu-id="790c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="790c9-111">-DefaultProfile</span></span>
<span data-ttu-id="790c9-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="790c9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="790c9-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="790c9-113">-Name</span></span>
<span data-ttu-id="790c9-114">Nazwa Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="790c9-114">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="790c9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="790c9-115">-ResourceGroupName</span></span>
<span data-ttu-id="790c9-116">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="790c9-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="790c9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="790c9-117">CommonParameters</span></span>
<span data-ttu-id="790c9-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="790c9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="790c9-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="790c9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="790c9-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="790c9-120">INPUTS</span></span>

### <span data-ttu-id="790c9-121">System. String</span><span class="sxs-lookup"><span data-stu-id="790c9-121">System.String</span></span>

## <span data-ttu-id="790c9-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="790c9-122">OUTPUTS</span></span>

### <span data-ttu-id="790c9-123">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="790c9-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="790c9-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="790c9-124">NOTES</span></span>

## <span data-ttu-id="790c9-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="790c9-125">RELATED LINKS</span></span>
