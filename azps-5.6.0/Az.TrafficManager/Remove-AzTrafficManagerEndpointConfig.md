---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 1dac991645d6f57ba4fe30a82955531b7fdb3f5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987267"
---
# <span data-ttu-id="2957a-101">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="2957a-101">Remove-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="2957a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2957a-102">SYNOPSIS</span></span>
<span data-ttu-id="2957a-103">Usuwa punkt końcowy z obiektu profilu lokalnego menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="2957a-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="2957a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2957a-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2957a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2957a-105">DESCRIPTION</span></span>
<span data-ttu-id="2957a-106">Polecenie **cmdlet Remove-AzTrafficManagerEndpointConfig** usuwa punkt końcowy z lokalnego obiektu profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="2957a-106">The **Remove-AzTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="2957a-107">Profil możesz uzyskać za pomocą polecenia cmdlet Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2957a-107">You can get a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="2957a-108">To polecenie cmdlet działa na lokalnym obiekcie profilu.</span><span class="sxs-lookup"><span data-stu-id="2957a-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="2957a-109">Zatwierdzanie zmian w profilu menedżera ruchu za pomocą Set-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2957a-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="2957a-110">Aby usunąć punkt końcowy i zatwierdzić zmiany w jednej operacji, użyj Remove-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2957a-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="2957a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2957a-111">EXAMPLES</span></span>

### <span data-ttu-id="2957a-112">Przykład 1. Usuwanie punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="2957a-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="2957a-113">Pierwsze polecenie otrzymuje profil usługi Azure Traffic Manager za pomocą polecenia cmdlet **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="2957a-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="2957a-114">Polecenie przechowuje profil lokalny w $TrafficManagerProfile zmienną.</span><span class="sxs-lookup"><span data-stu-id="2957a-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="2957a-115">Drugie polecenie usuwa punkt końcowy platformy Azure o nazwie contoso z profilu przechowywanego w usłudze $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="2957a-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="2957a-116">To polecenie zmienia tylko obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="2957a-116">This command changes only the local object.</span></span>

<span data-ttu-id="2957a-117">Ostatnie polecenie aktualizuje profil menedżera ruchu o nazwie ContosoProfile, aby dopasować go do wartości lokalnej w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="2957a-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="2957a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2957a-118">PARAMETERS</span></span>

### <span data-ttu-id="2957a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2957a-119">-DefaultProfile</span></span>
<span data-ttu-id="2957a-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2957a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2957a-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2957a-121">-EndpointName</span></span>
<span data-ttu-id="2957a-122">Określa nazwę punktu końcowego menedżera ruchu, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2957a-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2957a-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2957a-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="2957a-124">Określa lokalny obiekt **TrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="2957a-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="2957a-125">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="2957a-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="2957a-126">Aby uzyskać obiekt **TrafficManagerProfile,** użyj Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2957a-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="2957a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2957a-127">CommonParameters</span></span>
<span data-ttu-id="2957a-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2957a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2957a-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2957a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2957a-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2957a-130">INPUTS</span></span>

### <span data-ttu-id="2957a-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2957a-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="2957a-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2957a-132">OUTPUTS</span></span>

### <span data-ttu-id="2957a-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2957a-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="2957a-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2957a-134">NOTES</span></span>

## <span data-ttu-id="2957a-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2957a-135">RELATED LINKS</span></span>

[<span data-ttu-id="2957a-136">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="2957a-136">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="2957a-137">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2957a-137">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="2957a-138">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2957a-138">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="2957a-139">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2957a-139">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


