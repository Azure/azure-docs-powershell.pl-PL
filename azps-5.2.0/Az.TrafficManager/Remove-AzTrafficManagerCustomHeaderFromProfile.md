---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D343
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
ms.openlocfilehash: 62dbdfe69feddcbd942a51c05c65e486653a2405
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330433"
---
# <span data-ttu-id="23cff-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="23cff-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>

## <span data-ttu-id="23cff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23cff-102">SYNOPSIS</span></span>
<span data-ttu-id="23cff-103">Usuwa informacje z nagłówków niestandardowych z obiektu profilu lokalnego zarządzania ruchem.</span><span class="sxs-lookup"><span data-stu-id="23cff-103">Removes custom header information from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="23cff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23cff-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromProfile -Name <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23cff-105">Opis</span><span class="sxs-lookup"><span data-stu-id="23cff-105">DESCRIPTION</span></span>
<span data-ttu-id="23cff-106">Polecenie cmdlet **Remove-AzTrafficManagerCustomHeaderFromProfile** usuwa niestandardowe informacje nagłówka z obiektu profilu lokalnego usługi Azure Local Manager.</span><span class="sxs-lookup"><span data-stu-id="23cff-106">The **Remove-AzTrafficManagerCustomHeaderFromProfile** cmdlet removes custom header information from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="23cff-107">Możesz uzyskać profil przy użyciu New-AzTrafficManagerProfile lub Get-AzTrafficManagerProfile poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23cff-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="23cff-108">To polecenie cmdlet działa na obiekcie profilu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="23cff-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="23cff-109">Zatwierdź zmiany w profilu dla Menedżera ruchu, korzystając z polecenia cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="23cff-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="23cff-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23cff-110">EXAMPLES</span></span>

### <span data-ttu-id="23cff-111">Przykład 1: usuwanie informacji nagłówka niestandardowego z profilu</span><span class="sxs-lookup"><span data-stu-id="23cff-111">Example 1: Remove custom header information from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerProfile $TrafficManagerProfile -Name "host"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="23cff-112">Pierwsze polecenie pobiera profil usługi Azure Traffic Manager przy użyciu polecenia cmdlet **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="23cff-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="23cff-113">Drugie polecenie usuwa informacje z nagłówków niestandardowych z profilu przechowywanego w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="23cff-113">The second command removes custom header information from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="23cff-114">Ostatnie polecenie aktualizuje profil w usłudze Traffic Manager w celu dopasowania go do wartości lokalnej w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="23cff-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="23cff-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23cff-115">PARAMETERS</span></span>

### <span data-ttu-id="23cff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23cff-116">-DefaultProfile</span></span>
<span data-ttu-id="23cff-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="23cff-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23cff-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="23cff-118">-Name</span></span>
<span data-ttu-id="23cff-119">Określa nazwę informacji nagłówka niestandardowego, które mają zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="23cff-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="23cff-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="23cff-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="23cff-121">Określa lokalny obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="23cff-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="23cff-122">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="23cff-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="23cff-123">Aby uzyskać obiekt **TrafficManagerProfile** , użyj polecenia cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="23cff-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="23cff-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="23cff-124">-Confirm</span></span>
<span data-ttu-id="23cff-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23cff-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23cff-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23cff-126">-WhatIf</span></span>
<span data-ttu-id="23cff-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23cff-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23cff-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="23cff-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23cff-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23cff-129">CommonParameters</span></span>
<span data-ttu-id="23cff-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23cff-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23cff-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23cff-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23cff-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23cff-132">INPUTS</span></span>

### <span data-ttu-id="23cff-133">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="23cff-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="23cff-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23cff-134">OUTPUTS</span></span>

### <span data-ttu-id="23cff-135">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="23cff-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="23cff-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23cff-136">NOTES</span></span>

## <span data-ttu-id="23cff-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23cff-137">RELATED LINKS</span></span>

[<span data-ttu-id="23cff-138">Dodaj-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="23cff-138">Add-AzTrafficManagerCustomHeaderToProfile</span></span>](./Add-AzTrafficManagerCustomHeaderToProfile.md)

[<span data-ttu-id="23cff-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="23cff-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="23cff-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="23cff-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
