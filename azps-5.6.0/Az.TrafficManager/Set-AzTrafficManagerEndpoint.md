---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 8f8ba0297ac0302e50dfdfdc25ddc3941fb10e34
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987239"
---
# <span data-ttu-id="4b9ac-101">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b9ac-101">Set-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="4b9ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b9ac-102">SYNOPSIS</span></span>
<span data-ttu-id="4b9ac-103">Aktualizuje punkt końcowy Menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-103">Updates a Traffic Manager endpoint.</span></span>

## <span data-ttu-id="4b9ac-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4b9ac-104">SYNTAX</span></span>

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b9ac-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4b9ac-105">DESCRIPTION</span></span>
<span data-ttu-id="4b9ac-106">Polecenie **cmdlet Set-AzTrafficManagerEndpoint** aktualizuje punkt końcowy w usłudze Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-106">The **Set-AzTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="4b9ac-107">To polecenie cmdlet aktualizuje ustawienia z lokalnego obiektu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="4b9ac-108">Obiekt punktu końcowego można określić za pomocą *parametru TrafficManagerEndpoint* lub potoku.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="4b9ac-109">Za pomocą polecenia cmdlet można uzyskać obiekt lokalny reprezentujący punkt Get-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-109">You can obtain a local object that represents an endpoint by using the Get-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="4b9ac-110">Zmodyfikuj obiekt lokalnie, a następnie **użyj ustawienia Set-AzTrafficManagerEndpoint,** aby zatwierdzić zmiany.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-110">Modify the object locally and then use **Set-AzTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="4b9ac-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4b9ac-111">EXAMPLES</span></span>

### <span data-ttu-id="4b9ac-112">Przykład 1. Aktualizowanie punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="4b9ac-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="4b9ac-113">Pierwsze polecenie uzyskuje punkt końcowy usługi Azure Traffic Manager za pomocą polecenia cmdlet **Get-AzTrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="4b9ac-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="4b9ac-114">Polecenie przechowuje punkt końcowy lokalnie w $TrafficManagerEndpoint zmienną.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="4b9ac-115">Drugie polecenie zmienia ten punkt końcowy lokalnie.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="4b9ac-116">To polecenie zmienia wagę punktu końcowego na 20.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="4b9ac-117">Trzecie polecenie aktualizuje punkt końcowy w Menedżerze ruchu, aby dopasować wartość lokalną w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="4b9ac-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b9ac-118">PARAMETERS</span></span>

### <span data-ttu-id="4b9ac-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b9ac-119">-DefaultProfile</span></span>
<span data-ttu-id="4b9ac-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b9ac-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b9ac-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="4b9ac-122">Określa lokalny obiekt **TrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="4b9ac-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="4b9ac-123">To polecenie cmdlet aktualizuje Menedżera ruchu w celu dopasowania tego obiektu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b9ac-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b9ac-124">CommonParameters</span></span>
<span data-ttu-id="4b9ac-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b9ac-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b9ac-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b9ac-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b9ac-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b9ac-127">INPUTS</span></span>

### <span data-ttu-id="4b9ac-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b9ac-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="4b9ac-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4b9ac-129">OUTPUTS</span></span>

### <span data-ttu-id="4b9ac-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b9ac-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="4b9ac-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4b9ac-131">NOTES</span></span>

## <span data-ttu-id="4b9ac-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4b9ac-132">RELATED LINKS</span></span>
