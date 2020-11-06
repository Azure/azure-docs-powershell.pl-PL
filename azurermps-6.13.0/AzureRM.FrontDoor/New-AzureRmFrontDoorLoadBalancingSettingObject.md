---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: de13a33aeaf60dbd83fcacebb8380bee27c18c46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541715"
---
# <span data-ttu-id="de926-101">New-AzureRmFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="de926-101">New-AzureRmFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="de926-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="de926-102">SYNOPSIS</span></span>
<span data-ttu-id="de926-103">Tworzenie obiektu PSLoadBalancingSetting na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="de926-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de926-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="de926-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de926-105">Opis</span><span class="sxs-lookup"><span data-stu-id="de926-105">DESCRIPTION</span></span>
<span data-ttu-id="de926-106">Tworzenie obiektu PSLoadBalancingSetting na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="de926-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="de926-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="de926-107">EXAMPLES</span></span>

### <span data-ttu-id="de926-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="de926-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorLoadBalancingSettingObject -Name "loadbalancingsetting1"


SampleSize                    : 4
AdditionalLatencyMilliseconds : 0
SuccessfulSamplesRequired     : 2
ResourceState                 :
Id                            :
Name                          : loadbalancingsetting1
Type                          :
```

<span data-ttu-id="de926-109">Tworzenie obiektu PSLoadBalancingSetting na potrzeby tworzenia przednich drzwi</span><span class="sxs-lookup"><span data-stu-id="de926-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="de926-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="de926-110">PARAMETERS</span></span>

### <span data-ttu-id="de926-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="de926-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="de926-112">Dodatkowe opóźnienie w milisekundach na potrzeby sondowania w celu uwzględnienia najniższego zasobnika czasu oczekiwania.</span><span class="sxs-lookup"><span data-stu-id="de926-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="de926-113">Wartość domyślna to 0</span><span class="sxs-lookup"><span data-stu-id="de926-113">Default value is 0</span></span>

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

### <span data-ttu-id="de926-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de926-114">-DefaultProfile</span></span>
<span data-ttu-id="de926-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="de926-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de926-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="de926-116">-Name</span></span>
<span data-ttu-id="de926-117">Nazwa ustawienia badania kondycji.</span><span class="sxs-lookup"><span data-stu-id="de926-117">health probe setting name.</span></span>

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

### <span data-ttu-id="de926-118">-SampleSize</span><span class="sxs-lookup"><span data-stu-id="de926-118">-SampleSize</span></span>
<span data-ttu-id="de926-119">Liczba próbek do uwzględnienia w decyzjach dotyczących równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="de926-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="de926-120">Wartość domyślna to 4</span><span class="sxs-lookup"><span data-stu-id="de926-120">Default value is 4</span></span>

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

### <span data-ttu-id="de926-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="de926-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="de926-122">Liczba próbek w okresie próbkowania, które muszą się zakończyć, musi być wartością domyślną 2.</span><span class="sxs-lookup"><span data-stu-id="de926-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

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

### <span data-ttu-id="de926-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de926-123">CommonParameters</span></span>
<span data-ttu-id="de926-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de926-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de926-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de926-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de926-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de926-126">INPUTS</span></span>

### <span data-ttu-id="de926-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="de926-127">None</span></span>

## <span data-ttu-id="de926-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="de926-128">OUTPUTS</span></span>

### <span data-ttu-id="de926-129">Microsoft. Azure. Commands. FrontDoor. models. PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="de926-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="de926-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="de926-130">NOTES</span></span>

## <span data-ttu-id="de926-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de926-131">RELATED LINKS</span></span>

<span data-ttu-id="de926-132">[Nowe — AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="de926-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
