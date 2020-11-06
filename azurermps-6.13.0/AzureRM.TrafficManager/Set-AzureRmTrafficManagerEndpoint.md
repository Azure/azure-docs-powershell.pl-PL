---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: a6a5b9ed5dbf1faa4a2be345039e53bb3daae291
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525913"
---
# <span data-ttu-id="19fbc-101">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="19fbc-101">Set-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="19fbc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="19fbc-102">SYNOPSIS</span></span>
<span data-ttu-id="19fbc-103">Aktualizowanie punktu końcowego w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="19fbc-103">Updates a Traffic Manager endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19fbc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="19fbc-104">SYNTAX</span></span>

```
Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19fbc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="19fbc-105">DESCRIPTION</span></span>
<span data-ttu-id="19fbc-106">Polecenie cmdlet **Set-AzureRmTrafficManagerEndpoint** umożliwia zaktualizowanie punktu końcowego w usłudze Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="19fbc-106">The **Set-AzureRmTrafficManagerEndpoint** cmdlet updates an endpoint in Azure Traffic Manager.</span></span>
<span data-ttu-id="19fbc-107">To polecenie cmdlet spowoduje zaktualizowanie ustawień na podstawie obiektu lokalnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="19fbc-107">This cmdlet updates the settings from a local endpoint object.</span></span>
<span data-ttu-id="19fbc-108">Obiekt Endpoint można określić za pomocą parametru *TrafficManagerEndpoint* lub za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="19fbc-108">You can specify the endpoint object either by using the *TrafficManagerEndpoint* parameter or by using the pipeline.</span></span>

<span data-ttu-id="19fbc-109">Obiekt lokalny reprezentujący punkt końcowy można uzyskać przy użyciu Get-AzureRmTrafficManagerEndpoint polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19fbc-109">You can obtain a local object that represents an endpoint by using the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="19fbc-110">Zmodyfikuj obiekt lokalnie, a następnie użyj **Ustawienia Set-AzureRmTrafficManagerEndpoint** w celu zatwierdzenia zmian.</span><span class="sxs-lookup"><span data-stu-id="19fbc-110">Modify the object locally and then use **Set-AzureRmTrafficManagerEndpoint** to commit your changes.</span></span>

## <span data-ttu-id="19fbc-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="19fbc-111">EXAMPLES</span></span>

### <span data-ttu-id="19fbc-112">Przykład 1: aktualizowanie punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="19fbc-112">Example 1: Update an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="19fbc-113">Pierwsze polecenie pobiera punkt końcowy usługi Azure Traffic Manager przy użyciu polecenia cmdlet **Get-AzureRmTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="19fbc-113">The first command gets an Azure Traffic Manager endpoint by using the **Get-AzureRmTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="19fbc-114">Polecenie zapisuje punkt końcowy lokalnie w zmiennej $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="19fbc-114">The command stores the endpoint locally in the $TrafficManagerEndpoint variable.</span></span>

<span data-ttu-id="19fbc-115">Drugie polecenie powoduje zmianę lokalnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="19fbc-115">The second command changes that endpoint locally.</span></span>
<span data-ttu-id="19fbc-116">To polecenie powoduje zmianę wagi punktu końcowego na 20.</span><span class="sxs-lookup"><span data-stu-id="19fbc-116">This command changes the endpoint weight to 20.</span></span>

<span data-ttu-id="19fbc-117">W trzecim poleceniu jest aktualizowany punkt końcowy w usłudze Traffic Manager w celu dopasowania go do wartości lokalnej w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="19fbc-117">The third command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="19fbc-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="19fbc-118">PARAMETERS</span></span>

### <span data-ttu-id="19fbc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19fbc-119">-DefaultProfile</span></span>
<span data-ttu-id="19fbc-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="19fbc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19fbc-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="19fbc-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="19fbc-122">Określa lokalny obiekt **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="19fbc-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="19fbc-123">To polecenie cmdlet umożliwia zaktualizowanie Menedżera ruchu w celu dopasowania go do tego obiektu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="19fbc-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="19fbc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19fbc-124">CommonParameters</span></span>
<span data-ttu-id="19fbc-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19fbc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19fbc-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19fbc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19fbc-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19fbc-127">INPUTS</span></span>

### <span data-ttu-id="19fbc-128">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="19fbc-128">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="19fbc-129">To polecenie cmdlet akceptuje obiekt **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="19fbc-129">This cmdlet accepts a **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="19fbc-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="19fbc-130">OUTPUTS</span></span>

### <span data-ttu-id="19fbc-131">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="19fbc-131">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="19fbc-132">To polecenie cmdlet zwraca obiekt **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="19fbc-132">This cmdlet returns a **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="19fbc-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="19fbc-133">NOTES</span></span>

## <span data-ttu-id="19fbc-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19fbc-134">RELATED LINKS</span></span>
