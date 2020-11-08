---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: ee249b7e3d811a527a9322e09ba65075883e73b6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225123"
---
# <span data-ttu-id="f79b7-101">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="f79b7-101">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="f79b7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f79b7-102">SYNOPSIS</span></span>
<span data-ttu-id="f79b7-103">Umożliwia dodanie oczekiwanego zakresu kodów statusu do obiektu profilu lokalnego Menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="f79b7-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="f79b7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f79b7-104">SYNTAX</span></span>

```
Add-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f79b7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f79b7-105">DESCRIPTION</span></span>
<span data-ttu-id="f79b7-106">Polecenie cmdlet **Add-AzTrafficManagerExpectedStatusCodeRange** umożliwia dodanie zakresu oczekiwanych kodów stanu do obiektu profilu lokalnego usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="f79b7-106">The **Add-AzTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="f79b7-107">Możesz uzyskać profil przy użyciu New-AzTrafficManagerProfile lub Get-AzTrafficManagerProfile poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f79b7-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="f79b7-108">To polecenie cmdlet działa na obiekcie profilu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="f79b7-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="f79b7-109">Zatwierdź zmiany w profilu dla Menedżera ruchu, korzystając z polecenia cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f79b7-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="f79b7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f79b7-110">EXAMPLES</span></span>

### <span data-ttu-id="f79b7-111">Przykład 1. Dodawanie zakresu do profilu o oczekiwanym kodzie statusu</span><span class="sxs-lookup"><span data-stu-id="f79b7-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="f79b7-112">Pierwsze polecenie pobiera profil usługi Azure Traffic Manager przy użyciu polecenia cmdlet **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="f79b7-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="f79b7-113">Polecenie zapisuje profil lokalny w zmiennej $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f79b7-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="f79b7-114">Drugie polecenie dodaje oczekiwany zakres kodów statusu do profilu przechowywanego w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f79b7-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="f79b7-115">Ostatnie polecenie aktualizuje profil w usłudze Traffic Manager w celu dopasowania go do wartości lokalnej w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f79b7-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="f79b7-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f79b7-116">PARAMETERS</span></span>

### <span data-ttu-id="f79b7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f79b7-117">-DefaultProfile</span></span>
<span data-ttu-id="f79b7-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f79b7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f79b7-119">-Max</span><span class="sxs-lookup"><span data-stu-id="f79b7-119">-Max</span></span>
<span data-ttu-id="f79b7-120">Określa najwyższą wartość w zakresie kodu stanu, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="f79b7-120">Specifies the highest value in the status code range to be added.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79b7-121">-Min</span><span class="sxs-lookup"><span data-stu-id="f79b7-121">-Min</span></span>
<span data-ttu-id="f79b7-122">Określa najniższą wartość w zakresie kodu stanu, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="f79b7-122">Specifies the lowest value in the status code range to be added.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79b7-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f79b7-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="f79b7-124">Określa lokalny obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="f79b7-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="f79b7-125">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="f79b7-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="f79b7-126">Aby uzyskać obiekt **TrafficManagerProfile** , użyj polecenia cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f79b7-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f79b7-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f79b7-127">-Confirm</span></span>
<span data-ttu-id="f79b7-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f79b7-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79b7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f79b7-129">-WhatIf</span></span>
<span data-ttu-id="f79b7-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f79b7-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f79b7-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f79b7-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f79b7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f79b7-132">CommonParameters</span></span>
<span data-ttu-id="f79b7-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f79b7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f79b7-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f79b7-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f79b7-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f79b7-135">INPUTS</span></span>

### <span data-ttu-id="f79b7-136">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f79b7-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f79b7-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f79b7-137">OUTPUTS</span></span>

### <span data-ttu-id="f79b7-138">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f79b7-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f79b7-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f79b7-139">NOTES</span></span>

## <span data-ttu-id="f79b7-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f79b7-140">RELATED LINKS</span></span>

[<span data-ttu-id="f79b7-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="f79b7-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="f79b7-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f79b7-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="f79b7-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f79b7-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
