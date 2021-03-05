---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D343
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
ms.openlocfilehash: 1026f5e34c2b8efc17503a81a521a0ceb3d92060
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991838"
---
# <span data-ttu-id="87eba-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="87eba-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>

## <span data-ttu-id="87eba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87eba-102">SYNOPSIS</span></span>
<span data-ttu-id="87eba-103">Usuwa niestandardowe informacje nagłówka z obiektu profilu lokalnego menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="87eba-103">Removes custom header information from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="87eba-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="87eba-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromProfile -Name <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87eba-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="87eba-105">DESCRIPTION</span></span>
<span data-ttu-id="87eba-106">Polecenie **cmdlet Remove-AzTrafficManagerCustomHeaderFromProfile** usuwa niestandardowe informacje nagłówka z lokalnego obiektu profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="87eba-106">The **Remove-AzTrafficManagerCustomHeaderFromProfile** cmdlet removes custom header information from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="87eba-107">Profil można uzyskać za pomocą New-AzTrafficManagerProfile lub Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87eba-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="87eba-108">To polecenie cmdlet działa na lokalnym obiekcie profilu.</span><span class="sxs-lookup"><span data-stu-id="87eba-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="87eba-109">Zatwierdzanie zmian w profilu menedżera ruchu za pomocą Set-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87eba-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="87eba-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="87eba-110">EXAMPLES</span></span>

### <span data-ttu-id="87eba-111">Przykład 1. Usuwanie niestandardowych informacji nagłówka z profilu</span><span class="sxs-lookup"><span data-stu-id="87eba-111">Example 1: Remove custom header information from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerProfile $TrafficManagerProfile -Name "host"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="87eba-112">Pierwsze polecenie otrzymuje profil usługi Azure Traffic Manager za pomocą polecenia cmdlet **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="87eba-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="87eba-113">Drugie polecenie usuwa niestandardowe informacje nagłówka z profilu przechowywanego w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="87eba-113">The second command removes custom header information from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="87eba-114">Ostatnie polecenie aktualizuje profil w Menedżerze ruchu, aby dopasować go do wartości lokalnej w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="87eba-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="87eba-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87eba-115">PARAMETERS</span></span>

### <span data-ttu-id="87eba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87eba-116">-DefaultProfile</span></span>
<span data-ttu-id="87eba-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="87eba-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87eba-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="87eba-118">-Name</span></span>
<span data-ttu-id="87eba-119">Określa nazwę nagłówka niestandardowego do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="87eba-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="87eba-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="87eba-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="87eba-121">Określa lokalny obiekt **TrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="87eba-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="87eba-122">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="87eba-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="87eba-123">Aby uzyskać obiekt **TrafficManagerProfile,** użyj Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87eba-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="87eba-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="87eba-124">-Confirm</span></span>
<span data-ttu-id="87eba-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="87eba-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87eba-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87eba-126">-WhatIf</span></span>
<span data-ttu-id="87eba-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87eba-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87eba-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="87eba-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87eba-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87eba-129">CommonParameters</span></span>
<span data-ttu-id="87eba-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87eba-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87eba-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87eba-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87eba-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87eba-132">INPUTS</span></span>

### <span data-ttu-id="87eba-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="87eba-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="87eba-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87eba-134">OUTPUTS</span></span>

### <span data-ttu-id="87eba-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="87eba-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="87eba-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="87eba-136">NOTES</span></span>

## <span data-ttu-id="87eba-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87eba-137">RELATED LINKS</span></span>

[<span data-ttu-id="87eba-138">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="87eba-138">Add-AzTrafficManagerCustomHeaderToProfile</span></span>](./Add-AzTrafficManagerCustomHeaderToProfile.md)

[<span data-ttu-id="87eba-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="87eba-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="87eba-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="87eba-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
