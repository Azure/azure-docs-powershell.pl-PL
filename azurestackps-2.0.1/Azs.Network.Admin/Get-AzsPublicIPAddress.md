---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
schema: 2.0.0
ms.openlocfilehash: d63133d082af8a9938b2e39318d05ec4ba0d0eb3
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054170"
---
# <span data-ttu-id="3bba5-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="3bba5-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="3bba5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3bba5-102">SYNOPSIS</span></span>
<span data-ttu-id="3bba5-103">Lista publicznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="3bba5-103">List of public ip addresses.</span></span>

## <span data-ttu-id="3bba5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3bba5-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3bba5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3bba5-105">DESCRIPTION</span></span>
<span data-ttu-id="3bba5-106">Lista publicznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="3bba5-106">List of public ip addresses.</span></span>

## <span data-ttu-id="3bba5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3bba5-107">EXAMPLES</span></span>

### <span data-ttu-id="3bba5-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3bba5-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsPublicIPAddress
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
```

<span data-ttu-id="3bba5-109">Pobierz listę publicznych adresów IP, przydzielonych lub nieprzydzielonych.</span><span class="sxs-lookup"><span data-stu-id="3bba5-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="3bba5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3bba5-110">PARAMETERS</span></span>

### <span data-ttu-id="3bba5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bba5-111">-DefaultProfile</span></span>
<span data-ttu-id="3bba5-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3bba5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3bba5-113">-Filter</span><span class="sxs-lookup"><span data-stu-id="3bba5-113">-Filter</span></span>
<span data-ttu-id="3bba5-114">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="3bba5-114">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3bba5-115">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="3bba5-115">-InlineCount</span></span>
<span data-ttu-id="3bba5-116">Parametr liczby w tekście OData.</span><span class="sxs-lookup"><span data-stu-id="3bba5-116">OData inline count parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3bba5-117">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="3bba5-117">-OrderBy</span></span>
<span data-ttu-id="3bba5-118">Parametr orderBy OData.</span><span class="sxs-lookup"><span data-stu-id="3bba5-118">OData orderBy parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3bba5-119">-Skip</span><span class="sxs-lookup"><span data-stu-id="3bba5-119">-Skip</span></span>
<span data-ttu-id="3bba5-120">Parametr pomijania OData.</span><span class="sxs-lookup"><span data-stu-id="3bba5-120">OData skip parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3bba5-121">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3bba5-121">-SubscriptionId</span></span>
<span data-ttu-id="3bba5-122">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3bba5-122">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3bba5-123">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="3bba5-123">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3bba5-124">-Początek</span><span class="sxs-lookup"><span data-stu-id="3bba5-124">-Top</span></span>
<span data-ttu-id="3bba5-125">Parametr najwyższy OData.</span><span class="sxs-lookup"><span data-stu-id="3bba5-125">OData top parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3bba5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bba5-126">CommonParameters</span></span>
<span data-ttu-id="3bba5-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bba5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bba5-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3bba5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bba5-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3bba5-129">INPUTS</span></span>

## <span data-ttu-id="3bba5-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3bba5-130">OUTPUTS</span></span>

### <span data-ttu-id="3bba5-131">Microsoft. Azure. PowerShell. polecenia. NetworkAdmin. models. Api20150615. IPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="3bba5-131">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IPublicIPAddress</span></span>



## <span data-ttu-id="3bba5-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3bba5-132">NOTES</span></span>

## <span data-ttu-id="3bba5-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3bba5-133">RELATED LINKS</span></span>

