---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: fdada94847fdf2f83141f7cca63da61ead6fcd2c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232914"
---
# <span data-ttu-id="02d9d-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="02d9d-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="02d9d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="02d9d-103">Usuwa oczekiwany zakres kodów statusu z obiektu profilu lokalnego Menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="02d9d-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="02d9d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02d9d-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02d9d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="02d9d-105">DESCRIPTION</span></span>
<span data-ttu-id="02d9d-106">Polecenie cmdlet **Remove-AzTrafficManagerExpectedStatusCodeRange** umożliwia usunięcie zakresu oczekiwanych kodów stanu z obiektu profilu lokalnego usługi Azure Local Manager.</span><span class="sxs-lookup"><span data-stu-id="02d9d-106">The **Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="02d9d-107">Możesz uzyskać profil przy użyciu New-AzTrafficManagerProfile lub Get-AzTrafficManagerProfile poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02d9d-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="02d9d-108">To polecenie cmdlet działa na obiekcie profilu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="02d9d-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="02d9d-109">Zatwierdź zmiany w profilu dla Menedżera ruchu, korzystając z polecenia cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="02d9d-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="02d9d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02d9d-110">EXAMPLES</span></span>

### <span data-ttu-id="02d9d-111">Przykład 1: usuwanie oczekiwanego zakresu kodów statusu z profilu</span><span class="sxs-lookup"><span data-stu-id="02d9d-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="02d9d-112">Pierwsze polecenie pobiera profil usługi Azure Traffic Manager przy użyciu polecenia cmdlet **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="02d9d-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="02d9d-113">Drugie polecenie usuwa oczekiwany zakres kodów statusu z profilu przechowywanego w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="02d9d-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="02d9d-114">Ostatnie polecenie aktualizuje profil w usłudze Traffic Manager w celu dopasowania go do wartości lokalnej w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="02d9d-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="02d9d-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02d9d-115">PARAMETERS</span></span>

### <span data-ttu-id="02d9d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02d9d-116">-DefaultProfile</span></span>
<span data-ttu-id="02d9d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="02d9d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02d9d-118">-Min</span><span class="sxs-lookup"><span data-stu-id="02d9d-118">-Min</span></span>
<span data-ttu-id="02d9d-119">Określa najniższą wartość w zakresie kodu stanu, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="02d9d-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="02d9d-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="02d9d-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="02d9d-121">Określa lokalny obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="02d9d-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="02d9d-122">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="02d9d-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="02d9d-123">Aby uzyskać obiekt **TrafficManagerProfile** , użyj polecenia cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="02d9d-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="02d9d-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="02d9d-124">-Confirm</span></span>
<span data-ttu-id="02d9d-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02d9d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02d9d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02d9d-126">-WhatIf</span></span>
<span data-ttu-id="02d9d-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02d9d-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02d9d-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="02d9d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02d9d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02d9d-129">CommonParameters</span></span>
<span data-ttu-id="02d9d-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02d9d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02d9d-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02d9d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02d9d-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02d9d-132">INPUTS</span></span>

### <span data-ttu-id="02d9d-133">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="02d9d-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="02d9d-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02d9d-134">OUTPUTS</span></span>

### <span data-ttu-id="02d9d-135">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="02d9d-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="02d9d-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02d9d-136">NOTES</span></span>

## <span data-ttu-id="02d9d-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02d9d-137">RELATED LINKS</span></span>

[<span data-ttu-id="02d9d-138">Dodaj-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="02d9d-138">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="02d9d-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="02d9d-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="02d9d-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="02d9d-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
