---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33F
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
ms.openlocfilehash: 8421027f751aab64f5a9e63e08dafca4471d3169
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987400"
---
# <span data-ttu-id="f423e-101">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="f423e-101">Add-AzTrafficManagerCustomHeaderToProfile</span></span>

## <span data-ttu-id="f423e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f423e-102">SYNOPSIS</span></span>
<span data-ttu-id="f423e-103">Dodaje niestandardowe informacje nagłówka do obiektu profilu lokalnego menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="f423e-103">Adds custom header information to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="f423e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f423e-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToProfile -Name <String> -Value <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f423e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f423e-105">DESCRIPTION</span></span>
<span data-ttu-id="f423e-106">Polecenie **cmdlet Add-AzTrafficManagerCustomHeaderToProfile** dodaje niestandardowe informacje nagłówka do lokalnego obiektu profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="f423e-106">The **Add-AzTrafficManagerCustomHeaderToProfile** cmdlet adds custom header information to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="f423e-107">Profil można uzyskać za pomocą New-AzTrafficManagerProfile lub Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f423e-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="f423e-108">To polecenie cmdlet działa na lokalnym obiekcie profilu.</span><span class="sxs-lookup"><span data-stu-id="f423e-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="f423e-109">Zatwierdzanie zmian w profilu menedżera ruchu za pomocą Set-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f423e-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="f423e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f423e-110">EXAMPLES</span></span>

### <span data-ttu-id="f423e-111">Przykład 1. Dodawanie do profilu niestandardowych informacji nagłówka</span><span class="sxs-lookup"><span data-stu-id="f423e-111">Example 1: Add custom header information to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerCustomHeaderToProfile -TrafficManagerProfile $TrafficManagerProfile -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="f423e-112">Pierwsze polecenie otrzymuje profil usługi Azure Traffic Manager za pomocą polecenia cmdlet **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="f423e-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="f423e-113">Polecenie przechowuje profil lokalny w $TrafficManagerProfile zmienną.</span><span class="sxs-lookup"><span data-stu-id="f423e-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="f423e-114">Drugie polecenie dodaje niestandardowe informacje nagłówka do profilu przechowywanego w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f423e-114">The second command adds custom header information to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="f423e-115">Ostatnie polecenie aktualizuje profil w Menedżerze ruchu, aby dopasować go do wartości lokalnej w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f423e-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="f423e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f423e-116">PARAMETERS</span></span>

### <span data-ttu-id="f423e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f423e-117">-DefaultProfile</span></span>
<span data-ttu-id="f423e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f423e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f423e-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f423e-119">-Name</span></span>
<span data-ttu-id="f423e-120">Określa nazwę nagłówka niestandardowego do dodania.</span><span class="sxs-lookup"><span data-stu-id="f423e-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="f423e-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f423e-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="f423e-122">Określa lokalny obiekt **TrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="f423e-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="f423e-123">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="f423e-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="f423e-124">Aby uzyskać obiekt **TrafficManagerProfile,** użyj Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f423e-124">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="f423e-125">— Wartość</span><span class="sxs-lookup"><span data-stu-id="f423e-125">-Value</span></span>
<span data-ttu-id="f423e-126">Określa wartość dodawanych informacji nagłówka niestandardowego.</span><span class="sxs-lookup"><span data-stu-id="f423e-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="f423e-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f423e-127">-Confirm</span></span>
<span data-ttu-id="f423e-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f423e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f423e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f423e-129">-WhatIf</span></span>
<span data-ttu-id="f423e-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f423e-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f423e-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f423e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f423e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f423e-132">CommonParameters</span></span>
<span data-ttu-id="f423e-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f423e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f423e-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f423e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f423e-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f423e-135">INPUTS</span></span>

### <span data-ttu-id="f423e-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f423e-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f423e-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f423e-137">OUTPUTS</span></span>

### <span data-ttu-id="f423e-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f423e-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f423e-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f423e-139">NOTES</span></span>

## <span data-ttu-id="f423e-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f423e-140">RELATED LINKS</span></span>

[<span data-ttu-id="f423e-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="f423e-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>](./Remove-AzTrafficManagerCustomHeaderFromProfile.md)

[<span data-ttu-id="f423e-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f423e-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="f423e-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f423e-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
