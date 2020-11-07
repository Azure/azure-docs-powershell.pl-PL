---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: e9195a60b06f206a5b3133834f19cfdab68db31b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894650"
---
# <span data-ttu-id="3132e-101">New-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="3132e-101">New-AzFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="3132e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3132e-102">SYNOPSIS</span></span>
<span data-ttu-id="3132e-103">Tworzenie obiektu PSLoadBalancingSetting na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="3132e-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="3132e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3132e-104">SYNTAX</span></span>

```
New-AzFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3132e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3132e-105">DESCRIPTION</span></span>
<span data-ttu-id="3132e-106">Tworzenie obiektu PSLoadBalancingSetting na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="3132e-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="3132e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3132e-107">EXAMPLES</span></span>

### <span data-ttu-id="3132e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3132e-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorLoadBalancingSettingObject -Name "loadbalancingsetting1"


SampleSize                    : 4
AdditionalLatencyMilliseconds : 0
SuccessfulSamplesRequired     : 2
ResourceState                 :
Id                            :
Name                          : loadbalancingsetting1
Type                          :
```

<span data-ttu-id="3132e-109">Tworzenie obiektu PSLoadBalancingSetting na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="3132e-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="3132e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3132e-110">PARAMETERS</span></span>

### <span data-ttu-id="3132e-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="3132e-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="3132e-112">Dodatkowe opóźnienie w milisekundach na potrzeby sondowania w celu uwzględnienia najniższego zasobnika czasu oczekiwania.</span><span class="sxs-lookup"><span data-stu-id="3132e-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="3132e-113">Wartość domyślna to 0</span><span class="sxs-lookup"><span data-stu-id="3132e-113">Default value is 0</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3132e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3132e-114">-DefaultProfile</span></span>
<span data-ttu-id="3132e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3132e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3132e-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3132e-116">-Name</span></span>
<span data-ttu-id="3132e-117">Nazwa ustawienia badania kondycji.</span><span class="sxs-lookup"><span data-stu-id="3132e-117">health probe setting name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3132e-118">-SampleSize</span><span class="sxs-lookup"><span data-stu-id="3132e-118">-SampleSize</span></span>
<span data-ttu-id="3132e-119">Liczba próbek do uwzględnienia w decyzjach dotyczących równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="3132e-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="3132e-120">Wartość domyślna to 4</span><span class="sxs-lookup"><span data-stu-id="3132e-120">Default value is 4</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3132e-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="3132e-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="3132e-122">Liczba próbek w okresie próbkowania, które muszą się zakończyć, musi być wartością domyślną 2.</span><span class="sxs-lookup"><span data-stu-id="3132e-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3132e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3132e-123">CommonParameters</span></span>
<span data-ttu-id="3132e-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3132e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3132e-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3132e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3132e-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3132e-126">INPUTS</span></span>

### <span data-ttu-id="3132e-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3132e-127">None</span></span>

## <span data-ttu-id="3132e-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3132e-128">OUTPUTS</span></span>

### <span data-ttu-id="3132e-129">Microsoft. Azure. Commands. FrontDoor. models. PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="3132e-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="3132e-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3132e-130">NOTES</span></span>

## <span data-ttu-id="3132e-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3132e-131">RELATED LINKS</span></span>

<span data-ttu-id="3132e-132">[Nowe — AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="3132e-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
