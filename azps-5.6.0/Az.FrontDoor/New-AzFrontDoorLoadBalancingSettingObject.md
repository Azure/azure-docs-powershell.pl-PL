---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: 840c4db17e81f93fc40c86f7c22129b570583bd5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970993"
---
# <span data-ttu-id="354f0-101">New-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="354f0-101">New-AzFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="354f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="354f0-102">SYNOPSIS</span></span>
<span data-ttu-id="354f0-103">Tworzenie obiektu PSLoadBalancingSetting do tworzenia drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="354f0-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="354f0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="354f0-104">SYNTAX</span></span>

```
New-AzFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="354f0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="354f0-105">DESCRIPTION</span></span>
<span data-ttu-id="354f0-106">Tworzenie obiektu PSLoadBalancingSetting do tworzenia drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="354f0-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="354f0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="354f0-107">EXAMPLES</span></span>

### <span data-ttu-id="354f0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="354f0-108">Example 1</span></span>
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

<span data-ttu-id="354f0-109">Tworzenie obiektu PSLoadBalancingSetting do tworzenia drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="354f0-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="354f0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="354f0-110">PARAMETERS</span></span>

### <span data-ttu-id="354f0-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="354f0-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="354f0-112">Dodatkowe opóźnienie (w milisekundach) dla chętnych należy do zasobnika z najmniejszymi opóźnieniami.</span><span class="sxs-lookup"><span data-stu-id="354f0-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="354f0-113">Wartość domyślna to 0</span><span class="sxs-lookup"><span data-stu-id="354f0-113">Default value is 0</span></span>

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

### <span data-ttu-id="354f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="354f0-114">-DefaultProfile</span></span>
<span data-ttu-id="354f0-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="354f0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="354f0-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="354f0-116">-Name</span></span>
<span data-ttu-id="354f0-117">nazwa ustawienia kondycji.</span><span class="sxs-lookup"><span data-stu-id="354f0-117">health probe setting name.</span></span>

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

### <span data-ttu-id="354f0-118">- SampleSize</span><span class="sxs-lookup"><span data-stu-id="354f0-118">-SampleSize</span></span>
<span data-ttu-id="354f0-119">Liczba próbek do rozważenia w celu podejmowania decyzji dotyczących równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="354f0-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="354f0-120">Wartość domyślna to 4</span><span class="sxs-lookup"><span data-stu-id="354f0-120">Default value is 4</span></span>

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

### <span data-ttu-id="354f0-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="354f0-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="354f0-122">Liczba próbek w okresie próbek, które muszą zakończyć się powodzeniem Wartość domyślna wynosi 2</span><span class="sxs-lookup"><span data-stu-id="354f0-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

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

### <span data-ttu-id="354f0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="354f0-123">CommonParameters</span></span>
<span data-ttu-id="354f0-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="354f0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="354f0-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="354f0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="354f0-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="354f0-126">INPUTS</span></span>

### <span data-ttu-id="354f0-127">Brak</span><span class="sxs-lookup"><span data-stu-id="354f0-127">None</span></span>

## <span data-ttu-id="354f0-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="354f0-128">OUTPUTS</span></span>

### <span data-ttu-id="354f0-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="354f0-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="354f0-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="354f0-130">NOTES</span></span>

## <span data-ttu-id="354f0-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="354f0-131">RELATED LINKS</span></span>

<span data-ttu-id="354f0-132">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="354f0-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
