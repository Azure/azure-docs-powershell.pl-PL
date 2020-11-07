---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
ms.openlocfilehash: 4479cad8117c078c3d863b58cd764a388f78cd28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707390"
---
# <span data-ttu-id="f09d4-101">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="f09d4-101">Add-AzTrafficManagerCustomHeaderToProfile</span></span>

## <span data-ttu-id="f09d4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f09d4-102">SYNOPSIS</span></span>
<span data-ttu-id="f09d4-103">Dodaje informacje nagłówka niestandardowego do obiektu profilu lokalnego w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="f09d4-103">Adds custom header information to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="f09d4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f09d4-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToProfile -Name <String> -Value <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f09d4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f09d4-105">DESCRIPTION</span></span>
<span data-ttu-id="f09d4-106">Polecenie cmdlet **Add-AzTrafficManagerCustomHeaderToProfile** dodaje niestandardowe informacje nagłówka do obiektu profilu lokalnego usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="f09d4-106">The **Add-AzTrafficManagerCustomHeaderToProfile** cmdlet adds custom header information to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="f09d4-107">Możesz uzyskać profil przy użyciu New-AzTrafficManagerProfile lub Get-AzTrafficManagerProfile poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f09d4-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="f09d4-108">To polecenie cmdlet działa na obiekcie profilu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="f09d4-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="f09d4-109">Zatwierdź zmiany w profilu dla Menedżera ruchu, korzystając z polecenia cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f09d4-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="f09d4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f09d4-110">EXAMPLES</span></span>

### <span data-ttu-id="f09d4-111">Przykład 1: Dodawanie niestandardowych informacji nagłówka do profilu</span><span class="sxs-lookup"><span data-stu-id="f09d4-111">Example 1: Add custom header information to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerCustomHeaderToProfile -TrafficManagerProfile $TrafficManagerProfile -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="f09d4-112">Pierwsze polecenie pobiera profil usługi Azure Traffic Manager przy użyciu polecenia cmdlet **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="f09d4-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="f09d4-113">Polecenie zapisuje profil lokalny w zmiennej $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f09d4-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="f09d4-114">Drugie polecenie dodaje niestandardowe informacje nagłówka do profilu przechowywanego w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f09d4-114">The second command adds custom header information to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="f09d4-115">Ostatnie polecenie aktualizuje profil w usłudze Traffic Manager w celu dopasowania go do wartości lokalnej w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f09d4-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="f09d4-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f09d4-116">PARAMETERS</span></span>

### <span data-ttu-id="f09d4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f09d4-117">-DefaultProfile</span></span>
<span data-ttu-id="f09d4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f09d4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f09d4-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f09d4-119">-Name</span></span>
<span data-ttu-id="f09d4-120">Określa nazwę informacji nagłówka niestandardowego, które mają zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="f09d4-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="f09d4-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f09d4-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="f09d4-122">Określa lokalny obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="f09d4-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="f09d4-123">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="f09d4-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="f09d4-124">Aby uzyskać obiekt **TrafficManagerProfile** , użyj polecenia cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f09d4-124">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="f09d4-125">-Value</span><span class="sxs-lookup"><span data-stu-id="f09d4-125">-Value</span></span>
<span data-ttu-id="f09d4-126">Określa wartość niestandardowych informacji nagłówka, które mają zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="f09d4-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="f09d4-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f09d4-127">-Confirm</span></span>
<span data-ttu-id="f09d4-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f09d4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f09d4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f09d4-129">-WhatIf</span></span>
<span data-ttu-id="f09d4-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f09d4-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f09d4-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f09d4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f09d4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f09d4-132">CommonParameters</span></span>
<span data-ttu-id="f09d4-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f09d4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f09d4-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f09d4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f09d4-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f09d4-135">INPUTS</span></span>

### <span data-ttu-id="f09d4-136">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f09d4-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f09d4-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f09d4-137">OUTPUTS</span></span>

### <span data-ttu-id="f09d4-138">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f09d4-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f09d4-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f09d4-139">NOTES</span></span>

## <span data-ttu-id="f09d4-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f09d4-140">RELATED LINKS</span></span>

[<span data-ttu-id="f09d4-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="f09d4-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>](./Remove-AzTrafficManagerCustomHeaderFromProfile.md)

[<span data-ttu-id="f09d4-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f09d4-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="f09d4-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f09d4-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)