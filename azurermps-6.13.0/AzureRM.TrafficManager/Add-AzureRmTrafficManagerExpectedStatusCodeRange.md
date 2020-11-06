---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurertmtrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 32a00a6dce3d6a370f7b7f79f05794a312277a09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524218"
---
# <span data-ttu-id="b391d-101">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="b391d-101">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="b391d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b391d-102">SYNOPSIS</span></span>
<span data-ttu-id="b391d-103">Umożliwia dodanie oczekiwanego zakresu kodów statusu do obiektu profilu lokalnego Menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="b391d-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b391d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b391d-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b391d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b391d-105">DESCRIPTION</span></span>
<span data-ttu-id="b391d-106">Polecenie cmdlet **Add-AzureRmTrafficManagerExpectedStatusCodeRange** umożliwia dodanie zakresu oczekiwanych kodów stanu do obiektu profilu lokalnego usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="b391d-106">The **Add-AzureRmTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="b391d-107">Możesz uzyskać profil przy użyciu New-AzureRmTrafficManagerProfile lub Get-AzureRmTrafficManagerProfile poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b391d-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="b391d-108">To polecenie cmdlet działa na obiekcie profilu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="b391d-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="b391d-109">Zatwierdź zmiany w profilu dla Menedżera ruchu, korzystając z polecenia cmdlet Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="b391d-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="b391d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b391d-110">EXAMPLES</span></span>

### <span data-ttu-id="b391d-111">Przykład 1. Dodawanie zakresu do profilu o oczekiwanym kodzie statusu</span><span class="sxs-lookup"><span data-stu-id="b391d-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="b391d-112">Pierwsze polecenie pobiera profil usługi Azure Traffic Manager przy użyciu polecenia cmdlet **Get-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="b391d-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="b391d-113">Polecenie zapisuje profil lokalny w zmiennej $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="b391d-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="b391d-114">Drugie polecenie dodaje oczekiwany zakres kodów statusu do profilu przechowywanego w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="b391d-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="b391d-115">Ostatnie polecenie aktualizuje profil w usłudze Traffic Manager w celu dopasowania go do wartości lokalnej w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="b391d-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="b391d-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b391d-116">PARAMETERS</span></span>

### <span data-ttu-id="b391d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b391d-117">-DefaultProfile</span></span>
<span data-ttu-id="b391d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b391d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b391d-119">-Max</span><span class="sxs-lookup"><span data-stu-id="b391d-119">-Max</span></span>
<span data-ttu-id="b391d-120">Określa najwyższą wartość w zakresie kodu stanu, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="b391d-120">Specifies the highest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="b391d-121">-Min</span><span class="sxs-lookup"><span data-stu-id="b391d-121">-Min</span></span>
<span data-ttu-id="b391d-122">Określa najniższą wartość w zakresie kodu stanu, który ma zostać dodany.</span><span class="sxs-lookup"><span data-stu-id="b391d-122">Specifies the lowest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="b391d-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b391d-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="b391d-124">Określa lokalny obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="b391d-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="b391d-125">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="b391d-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="b391d-126">Aby uzyskać obiekt **TrafficManagerProfile** , użyj polecenia cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="b391d-126">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="b391d-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b391d-127">-Confirm</span></span>
<span data-ttu-id="b391d-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b391d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b391d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b391d-129">-WhatIf</span></span>
<span data-ttu-id="b391d-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b391d-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b391d-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b391d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b391d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b391d-132">CommonParameters</span></span>
<span data-ttu-id="b391d-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b391d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b391d-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b391d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b391d-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b391d-135">INPUTS</span></span>

### <span data-ttu-id="b391d-136">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b391d-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="b391d-137">To polecenie cmdlet akceptuje obiekt **TrafficManagerProfile** do tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b391d-137">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="b391d-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b391d-138">OUTPUTS</span></span>

### <span data-ttu-id="b391d-139">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b391d-139">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="b391d-140">To polecenie cmdlet zwraca zmodyfikowany obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="b391d-140">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="b391d-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b391d-141">NOTES</span></span>

## <span data-ttu-id="b391d-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b391d-142">RELATED LINKS</span></span>

[<span data-ttu-id="b391d-143">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="b391d-143">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="b391d-144">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b391d-144">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="b391d-145">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b391d-145">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
