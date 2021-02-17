---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: e9195a60b06f206a5b3133834f19cfdab68db31b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243571"
---
# <span data-ttu-id="4183d-101">New-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="4183d-101">New-AzFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="4183d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4183d-102">SYNOPSIS</span></span>
<span data-ttu-id="4183d-103">Tworzenie obiektu PSLoadBalancingSetting do tworzenia drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="4183d-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="4183d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4183d-104">SYNTAX</span></span>

```
New-AzFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4183d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4183d-105">DESCRIPTION</span></span>
<span data-ttu-id="4183d-106">Tworzenie obiektu PSLoadBalancingSetting do tworzenia drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="4183d-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="4183d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4183d-107">EXAMPLES</span></span>

### <span data-ttu-id="4183d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4183d-108">Example 1</span></span>
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

<span data-ttu-id="4183d-109">Tworzenie obiektu PSLoadBalancingSetting do tworzenia drzwi frontowych</span><span class="sxs-lookup"><span data-stu-id="4183d-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="4183d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4183d-110">PARAMETERS</span></span>

### <span data-ttu-id="4183d-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="4183d-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="4183d-112">Dodatkowe opóźnienie w milisekundach dla chętnych do zasobnika z najmniejszymi opóźnieniami.</span><span class="sxs-lookup"><span data-stu-id="4183d-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="4183d-113">Wartość domyślna to 0</span><span class="sxs-lookup"><span data-stu-id="4183d-113">Default value is 0</span></span>

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

### <span data-ttu-id="4183d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4183d-114">-DefaultProfile</span></span>
<span data-ttu-id="4183d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4183d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4183d-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4183d-116">-Name</span></span>
<span data-ttu-id="4183d-117">nazwa ustawienia kondycji.</span><span class="sxs-lookup"><span data-stu-id="4183d-117">health probe setting name.</span></span>

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

### <span data-ttu-id="4183d-118">- SampleSize</span><span class="sxs-lookup"><span data-stu-id="4183d-118">-SampleSize</span></span>
<span data-ttu-id="4183d-119">Liczba próbek do rozważenia w celu podejmowania decyzji dotyczących równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4183d-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="4183d-120">Wartość domyślna to 4</span><span class="sxs-lookup"><span data-stu-id="4183d-120">Default value is 4</span></span>

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

### <span data-ttu-id="4183d-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="4183d-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="4183d-122">Liczba próbek w okresie próbek, które muszą osiągnąć sukces Wartość domyślna wynosi 2</span><span class="sxs-lookup"><span data-stu-id="4183d-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

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

### <span data-ttu-id="4183d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4183d-123">CommonParameters</span></span>
<span data-ttu-id="4183d-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4183d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4183d-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4183d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4183d-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4183d-126">INPUTS</span></span>

### <span data-ttu-id="4183d-127">Brak</span><span class="sxs-lookup"><span data-stu-id="4183d-127">None</span></span>

## <span data-ttu-id="4183d-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4183d-128">OUTPUTS</span></span>

### <span data-ttu-id="4183d-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="4183d-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="4183d-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4183d-130">NOTES</span></span>

## <span data-ttu-id="4183d-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4183d-131">RELATED LINKS</span></span>

<span data-ttu-id="4183d-132">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="4183d-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
