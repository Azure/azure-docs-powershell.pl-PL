---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 0000a7a1dba5f175d70fb93631176a49a9da2d13
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052009"
---
# <span data-ttu-id="ce85a-101">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ce85a-101">Set-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="ce85a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ce85a-102">SYNOPSIS</span></span>
<span data-ttu-id="ce85a-103">Aktualizowanie punktu końcowego w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="ce85a-103">Updates a Traffic Manager endpoint.</span></span>

## <span data-ttu-id="ce85a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ce85a-104">SYNTAX</span></span>

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce85a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ce85a-105">DESCRIPTION</span></span>
<span data-ttu-id="ce85a-106">Polecenie cmdlet **Set-AzTrafficManagerEndpoint** umożliwia zaktualizowanie punktu końcowego w usłudze Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="ce85a-106">The **Set-AzTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="ce85a-107">To polecenie cmdlet spowoduje zaktualizowanie ustawień na podstawie obiektu lokalnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="ce85a-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="ce85a-108">Obiekt Endpoint można określić za pomocą parametru *TrafficManagerEndpoint* lub za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="ce85a-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="ce85a-109">Obiekt lokalny reprezentujący punkt końcowy można uzyskać przy użyciu Get-AzTrafficManagerEndpoint polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce85a-109">You can obtain a local object that represents an endpoint by using the Get-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="ce85a-110">Zmodyfikuj obiekt lokalnie, a następnie użyj **Ustawienia Set-AzTrafficManagerEndpoint** w celu zatwierdzenia zmian.</span><span class="sxs-lookup"><span data-stu-id="ce85a-110">Modify the object locally and then use **Set-AzTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="ce85a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ce85a-111">EXAMPLES</span></span>

### <span data-ttu-id="ce85a-112">Przykład 1: aktualizowanie punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="ce85a-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="ce85a-113">Pierwsze polecenie pobiera punkt końcowy usługi Azure Traffic Manager przy użyciu polecenia cmdlet **Get-AzTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="ce85a-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="ce85a-114">Polecenie zapisuje punkt końcowy lokalnie w zmiennej $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ce85a-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="ce85a-115">Drugie polecenie powoduje zmianę lokalnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="ce85a-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="ce85a-116">To polecenie powoduje zmianę wagi punktu końcowego na 20.</span><span class="sxs-lookup"><span data-stu-id="ce85a-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="ce85a-117">W trzecim poleceniu jest aktualizowany punkt końcowy w usłudze Traffic Manager w celu dopasowania go do wartości lokalnej w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ce85a-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="ce85a-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ce85a-118">PARAMETERS</span></span>

### <span data-ttu-id="ce85a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce85a-119">-DefaultProfile</span></span>
<span data-ttu-id="ce85a-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ce85a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce85a-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ce85a-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="ce85a-122">Określa lokalny obiekt **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="ce85a-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="ce85a-123">To polecenie cmdlet umożliwia zaktualizowanie Menedżera ruchu w celu dopasowania go do tego obiektu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="ce85a-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="ce85a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce85a-124">CommonParameters</span></span>
<span data-ttu-id="ce85a-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce85a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce85a-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce85a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce85a-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce85a-127">INPUTS</span></span>

### <span data-ttu-id="ce85a-128">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ce85a-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="ce85a-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ce85a-129">OUTPUTS</span></span>

### <span data-ttu-id="ce85a-130">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ce85a-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="ce85a-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ce85a-131">NOTES</span></span>

## <span data-ttu-id="ce85a-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ce85a-132">RELATED LINKS</span></span>
