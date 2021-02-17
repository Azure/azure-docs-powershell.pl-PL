---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: ee249b7e3d811a527a9322e09ba65075883e73b6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198322"
---
# <span data-ttu-id="a6436-101">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="a6436-101">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="a6436-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6436-102">SYNOPSIS</span></span>
<span data-ttu-id="a6436-103">Dodaje zakres oczekiwanego kodu stanu do obiektu profilu lokalnego menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="a6436-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="a6436-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a6436-104">SYNTAX</span></span>

```
Add-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6436-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a6436-105">DESCRIPTION</span></span>
<span data-ttu-id="a6436-106">Polecenie **cmdlet Add-AzTrafficManagerExpectedStatusCodeRange** dodaje zakres kodów stanu do lokalnego obiektu profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="a6436-106">The **Add-AzTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="a6436-107">Profil można uzyskać za pomocą New-AzTrafficManagerProfile lub Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6436-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="a6436-108">To polecenie cmdlet działa na lokalnym obiekcie profilu.</span><span class="sxs-lookup"><span data-stu-id="a6436-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="a6436-109">Zatwierdzanie zmian w profilu menedżera ruchu za pomocą Set-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6436-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="a6436-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a6436-110">EXAMPLES</span></span>

### <span data-ttu-id="a6436-111">Przykład 1. Dodawanie do profilu oczekiwanego zakresu kodów stanu</span><span class="sxs-lookup"><span data-stu-id="a6436-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="a6436-112">Pierwsze polecenie otrzymuje profil usługi Azure Traffic Manager za pomocą polecenia cmdlet **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="a6436-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="a6436-113">Polecenie przechowuje profil lokalny w $TrafficManagerProfile zmienną.</span><span class="sxs-lookup"><span data-stu-id="a6436-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="a6436-114">Drugie polecenie dodaje zakres oczekiwanego kodu stanu do profilu przechowywanego w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="a6436-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="a6436-115">Ostatnie polecenie aktualizuje profil w Menedżerze ruchu, aby dopasować go do wartości lokalnej w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="a6436-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="a6436-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6436-116">PARAMETERS</span></span>

### <span data-ttu-id="a6436-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6436-117">-DefaultProfile</span></span>
<span data-ttu-id="a6436-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a6436-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6436-119">— Maksimum</span><span class="sxs-lookup"><span data-stu-id="a6436-119">-Max</span></span>
<span data-ttu-id="a6436-120">Określa najwyższą wartość w zakresie kodów stanu do dodania.</span><span class="sxs-lookup"><span data-stu-id="a6436-120">Specifies the highest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="a6436-121">— Minimum</span><span class="sxs-lookup"><span data-stu-id="a6436-121">-Min</span></span>
<span data-ttu-id="a6436-122">Określa najniższą wartość w zakresie kodów stanu do dodania.</span><span class="sxs-lookup"><span data-stu-id="a6436-122">Specifies the lowest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="a6436-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a6436-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="a6436-124">Określa lokalny obiekt **TrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="a6436-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="a6436-125">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="a6436-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="a6436-126">Aby uzyskać obiekt **TrafficManagerProfile,** użyj Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6436-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="a6436-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a6436-127">-Confirm</span></span>
<span data-ttu-id="a6436-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a6436-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6436-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6436-129">-WhatIf</span></span>
<span data-ttu-id="a6436-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6436-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6436-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a6436-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6436-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6436-132">CommonParameters</span></span>
<span data-ttu-id="a6436-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6436-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6436-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6436-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6436-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6436-135">INPUTS</span></span>

### <span data-ttu-id="a6436-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a6436-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="a6436-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a6436-137">OUTPUTS</span></span>

### <span data-ttu-id="a6436-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a6436-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="a6436-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a6436-139">NOTES</span></span>

## <span data-ttu-id="a6436-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6436-140">RELATED LINKS</span></span>

[<span data-ttu-id="a6436-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="a6436-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="a6436-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a6436-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="a6436-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a6436-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
