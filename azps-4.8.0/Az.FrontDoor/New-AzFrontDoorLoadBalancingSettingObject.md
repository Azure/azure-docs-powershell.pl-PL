---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: e9195a60b06f206a5b3133834f19cfdab68db31b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062744"
---
# <span data-ttu-id="23cb8-101">New-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="23cb8-101">New-AzFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="23cb8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23cb8-102">SYNOPSIS</span></span>
<span data-ttu-id="23cb8-103">Tworzenie obiektu PSLoadBalancingSetting na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="23cb8-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="23cb8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23cb8-104">SYNTAX</span></span>

```
New-AzFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23cb8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="23cb8-105">DESCRIPTION</span></span>
<span data-ttu-id="23cb8-106">Tworzenie obiektu PSLoadBalancingSetting na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="23cb8-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="23cb8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23cb8-107">EXAMPLES</span></span>

### <span data-ttu-id="23cb8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="23cb8-108">Example 1</span></span>
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

<span data-ttu-id="23cb8-109">Tworzenie obiektu PSLoadBalancingSetting na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="23cb8-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="23cb8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23cb8-110">PARAMETERS</span></span>

### <span data-ttu-id="23cb8-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="23cb8-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="23cb8-112">Dodatkowe opóźnienie w milisekundach na potrzeby sondowania w celu uwzględnienia najniższego zasobnika czasu oczekiwania.</span><span class="sxs-lookup"><span data-stu-id="23cb8-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="23cb8-113">Wartość domyślna to 0</span><span class="sxs-lookup"><span data-stu-id="23cb8-113">Default value is 0</span></span>

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

### <span data-ttu-id="23cb8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23cb8-114">-DefaultProfile</span></span>
<span data-ttu-id="23cb8-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="23cb8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23cb8-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="23cb8-116">-Name</span></span>
<span data-ttu-id="23cb8-117">Nazwa ustawienia badania kondycji.</span><span class="sxs-lookup"><span data-stu-id="23cb8-117">health probe setting name.</span></span>

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

### <span data-ttu-id="23cb8-118">-SampleSize</span><span class="sxs-lookup"><span data-stu-id="23cb8-118">-SampleSize</span></span>
<span data-ttu-id="23cb8-119">Liczba próbek do uwzględnienia w decyzjach dotyczących równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="23cb8-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="23cb8-120">Wartość domyślna to 4</span><span class="sxs-lookup"><span data-stu-id="23cb8-120">Default value is 4</span></span>

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

### <span data-ttu-id="23cb8-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="23cb8-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="23cb8-122">Liczba próbek w okresie próbkowania, które muszą się zakończyć, musi być wartością domyślną 2.</span><span class="sxs-lookup"><span data-stu-id="23cb8-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

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

### <span data-ttu-id="23cb8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23cb8-123">CommonParameters</span></span>
<span data-ttu-id="23cb8-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23cb8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23cb8-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23cb8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23cb8-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23cb8-126">INPUTS</span></span>

### <span data-ttu-id="23cb8-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="23cb8-127">None</span></span>

## <span data-ttu-id="23cb8-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23cb8-128">OUTPUTS</span></span>

### <span data-ttu-id="23cb8-129">Microsoft. Azure. Commands. FrontDoor. models. PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="23cb8-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="23cb8-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23cb8-130">NOTES</span></span>

## <span data-ttu-id="23cb8-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23cb8-131">RELATED LINKS</span></span>

<span data-ttu-id="23cb8-132">[Nowe — AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="23cb8-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
