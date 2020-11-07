---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 31201d607d1b9f0825236fe162bf86028b148193
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888477"
---
# <span data-ttu-id="9258c-101">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9258c-101">Set-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="9258c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9258c-102">SYNOPSIS</span></span>
<span data-ttu-id="9258c-103">Aktualizowanie punktu końcowego w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="9258c-103">Updates a Traffic Manager endpoint.</span></span>

## <span data-ttu-id="9258c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9258c-104">SYNTAX</span></span>

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9258c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9258c-105">DESCRIPTION</span></span>
<span data-ttu-id="9258c-106">Polecenie cmdlet **Set-AzTrafficManagerEndpoint** umożliwia zaktualizowanie punktu końcowego w usłudze Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="9258c-106">The **Set-AzTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="9258c-107">To polecenie cmdlet spowoduje zaktualizowanie ustawień na podstawie obiektu lokalnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="9258c-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="9258c-108">Obiekt Endpoint można określić za pomocą parametru *TrafficManagerEndpoint* lub za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="9258c-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="9258c-109">Obiekt lokalny reprezentujący punkt końcowy można uzyskać przy użyciu Get-AzTrafficManagerEndpoint polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9258c-109">You can obtain a local object that represents an endpoint by using the Get-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="9258c-110">Zmodyfikuj obiekt lokalnie, a następnie użyj **Ustawienia Set-AzTrafficManagerEndpoint** w celu zatwierdzenia zmian.</span><span class="sxs-lookup"><span data-stu-id="9258c-110">Modify the object locally and then use **Set-AzTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="9258c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9258c-111">EXAMPLES</span></span>

### <span data-ttu-id="9258c-112">Przykład 1: aktualizowanie punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="9258c-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="9258c-113">Pierwsze polecenie pobiera punkt końcowy usługi Azure Traffic Manager przy użyciu polecenia cmdlet **Get-AzTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="9258c-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="9258c-114">Polecenie zapisuje punkt końcowy lokalnie w zmiennej $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="9258c-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="9258c-115">Drugie polecenie powoduje zmianę lokalnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="9258c-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="9258c-116">To polecenie powoduje zmianę wagi punktu końcowego na 20.</span><span class="sxs-lookup"><span data-stu-id="9258c-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="9258c-117">W trzecim poleceniu jest aktualizowany punkt końcowy w usłudze Traffic Manager w celu dopasowania go do wartości lokalnej w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="9258c-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="9258c-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9258c-118">PARAMETERS</span></span>

### <span data-ttu-id="9258c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9258c-119">-DefaultProfile</span></span>
<span data-ttu-id="9258c-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9258c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9258c-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9258c-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="9258c-122">Określa lokalny obiekt **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="9258c-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="9258c-123">To polecenie cmdlet umożliwia zaktualizowanie Menedżera ruchu w celu dopasowania go do tego obiektu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="9258c-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="9258c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9258c-124">CommonParameters</span></span>
<span data-ttu-id="9258c-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9258c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9258c-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9258c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9258c-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9258c-127">INPUTS</span></span>

### <span data-ttu-id="9258c-128">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9258c-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="9258c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9258c-129">OUTPUTS</span></span>

### <span data-ttu-id="9258c-130">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9258c-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="9258c-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9258c-131">NOTES</span></span>

## <span data-ttu-id="9258c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9258c-132">RELATED LINKS</span></span>
