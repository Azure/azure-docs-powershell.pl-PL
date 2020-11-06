---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 0971a4b8d485c1590794de6f1b6c2d4d9d21da4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525921"
---
# <span data-ttu-id="78955-101">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="78955-101">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="78955-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78955-102">SYNOPSIS</span></span>
<span data-ttu-id="78955-103">Usuwa oczekiwany zakres kodów statusu z obiektu profilu lokalnego Menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="78955-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78955-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78955-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78955-105">Opis</span><span class="sxs-lookup"><span data-stu-id="78955-105">DESCRIPTION</span></span>
<span data-ttu-id="78955-106">Polecenie cmdlet **Remove-AzureRmTrafficManagerExpectedStatusCodeRange** umożliwia usunięcie zakresu oczekiwanych kodów stanu z obiektu profilu lokalnego usługi Azure Local Manager.</span><span class="sxs-lookup"><span data-stu-id="78955-106">The **Remove-AzureRmTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="78955-107">Możesz uzyskać profil przy użyciu New-AzureRmTrafficManagerProfile lub Get-AzureRmTrafficManagerProfile poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78955-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="78955-108">To polecenie cmdlet działa na obiekcie profilu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="78955-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="78955-109">Zatwierdź zmiany w profilu dla Menedżera ruchu, korzystając z polecenia cmdlet Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="78955-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="78955-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78955-110">EXAMPLES</span></span>

### <span data-ttu-id="78955-111">Przykład 1: usuwanie oczekiwanego zakresu kodów statusu z profilu</span><span class="sxs-lookup"><span data-stu-id="78955-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="78955-112">Pierwsze polecenie pobiera profil usługi Azure Traffic Manager przy użyciu polecenia cmdlet **Get-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="78955-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="78955-113">Drugie polecenie usuwa oczekiwany zakres kodów statusu z profilu przechowywanego w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="78955-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="78955-114">Ostatnie polecenie aktualizuje profil w usłudze Traffic Manager w celu dopasowania go do wartości lokalnej w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="78955-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="78955-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78955-115">PARAMETERS</span></span>

### <span data-ttu-id="78955-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78955-116">-DefaultProfile</span></span>
<span data-ttu-id="78955-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="78955-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78955-118">-Min</span><span class="sxs-lookup"><span data-stu-id="78955-118">-Min</span></span>
<span data-ttu-id="78955-119">Określa najniższą wartość w zakresie kodu stanu, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="78955-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="78955-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="78955-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="78955-121">Określa lokalny obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="78955-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="78955-122">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="78955-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="78955-123">Aby uzyskać obiekt **TrafficManagerProfile** , użyj polecenia cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="78955-123">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="78955-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="78955-124">-Confirm</span></span>
<span data-ttu-id="78955-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78955-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78955-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78955-126">-WhatIf</span></span>
<span data-ttu-id="78955-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78955-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78955-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="78955-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78955-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78955-129">CommonParameters</span></span>
<span data-ttu-id="78955-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78955-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78955-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78955-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78955-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78955-132">INPUTS</span></span>

### <span data-ttu-id="78955-133">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="78955-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="78955-134">To polecenie cmdlet akceptuje obiekt **TrafficManagerProfile** do tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78955-134">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="78955-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78955-135">OUTPUTS</span></span>

### <span data-ttu-id="78955-136">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="78955-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="78955-137">To polecenie cmdlet zwraca zmodyfikowany obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="78955-137">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="78955-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78955-138">NOTES</span></span>

## <span data-ttu-id="78955-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78955-139">RELATED LINKS</span></span>

[<span data-ttu-id="78955-140">Dodaj-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="78955-140">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzureRmTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="78955-141">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="78955-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="78955-142">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="78955-142">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
