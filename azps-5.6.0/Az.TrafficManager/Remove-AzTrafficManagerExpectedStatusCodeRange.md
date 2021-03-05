---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 8e79fe1a0d0cc1c681c88cb3d5dfdd8d48dfd26b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987260"
---
# <span data-ttu-id="4944c-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="4944c-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="4944c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4944c-102">SYNOPSIS</span></span>
<span data-ttu-id="4944c-103">Usuwa zakres oczekiwanego kodu stanu z lokalnego obiektu profilu menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="4944c-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="4944c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4944c-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4944c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4944c-105">DESCRIPTION</span></span>
<span data-ttu-id="4944c-106">Polecenie **cmdlet Remove-AzTrafficManagerExpectedStatusCodeRange** usuwa zakres kodów stanu z lokalnego obiektu profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="4944c-106">The **Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="4944c-107">Profil można uzyskać za pomocą New-AzTrafficManagerProfile lub Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4944c-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="4944c-108">To polecenie cmdlet działa na lokalnym obiekcie profilu.</span><span class="sxs-lookup"><span data-stu-id="4944c-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="4944c-109">Zatwierdzanie zmian w profilu menedżera ruchu za pomocą Set-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4944c-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="4944c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4944c-110">EXAMPLES</span></span>

### <span data-ttu-id="4944c-111">Przykład 1. Usuwanie z profilu oczekiwanego zakresu kodów stanu</span><span class="sxs-lookup"><span data-stu-id="4944c-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="4944c-112">Pierwsze polecenie otrzymuje profil usługi Azure Traffic Manager za pomocą polecenia cmdlet **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="4944c-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="4944c-113">Drugie polecenie usuwa zakres oczekiwanego kodu stanu z profilu przechowywanego w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="4944c-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="4944c-114">Ostatnie polecenie aktualizuje profil w Menedżerze ruchu, aby dopasować go do wartości lokalnej w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="4944c-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="4944c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4944c-115">PARAMETERS</span></span>

### <span data-ttu-id="4944c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4944c-116">-DefaultProfile</span></span>
<span data-ttu-id="4944c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4944c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4944c-118">— Minimum</span><span class="sxs-lookup"><span data-stu-id="4944c-118">-Min</span></span>
<span data-ttu-id="4944c-119">Określa najniższą wartość w zakresie kodów stanu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="4944c-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="4944c-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4944c-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="4944c-121">Określa lokalny obiekt **TrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="4944c-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="4944c-122">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="4944c-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="4944c-123">Aby uzyskać obiekt **TrafficManagerProfile,** użyj Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4944c-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="4944c-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4944c-124">-Confirm</span></span>
<span data-ttu-id="4944c-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4944c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4944c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4944c-126">-WhatIf</span></span>
<span data-ttu-id="4944c-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4944c-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4944c-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4944c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4944c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4944c-129">CommonParameters</span></span>
<span data-ttu-id="4944c-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4944c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4944c-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4944c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4944c-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4944c-132">INPUTS</span></span>

### <span data-ttu-id="4944c-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4944c-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="4944c-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4944c-134">OUTPUTS</span></span>

### <span data-ttu-id="4944c-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4944c-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="4944c-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4944c-136">NOTES</span></span>

## <span data-ttu-id="4944c-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4944c-137">RELATED LINKS</span></span>

[<span data-ttu-id="4944c-138">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="4944c-138">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="4944c-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4944c-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="4944c-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4944c-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
