---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: 8f774ab221160a94ee4e8b5f13780b7e3131f252
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182562"
---
# <span data-ttu-id="de94f-101">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="de94f-101">Set-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="de94f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de94f-102">SYNOPSIS</span></span>
<span data-ttu-id="de94f-103">Aktualizuje profil Menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="de94f-103">Updates a Traffic Manager profile.</span></span>

## <span data-ttu-id="de94f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="de94f-104">SYNTAX</span></span>

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de94f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="de94f-105">DESCRIPTION</span></span>
<span data-ttu-id="de94f-106">Polecenie **cmdlet Set-AzTrafficManagerProfile** aktualizuje profil usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="de94f-106">The **Set-AzTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="de94f-107">To polecenie cmdlet aktualizuje ustawienia profilu z lokalnego obiektu profilu.</span><span class="sxs-lookup"><span data-stu-id="de94f-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="de94f-108">Obiekt profilu można określić za pomocą parametru *TrafficManagerProfile* lub potoku.</span><span class="sxs-lookup"><span data-stu-id="de94f-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="de94f-109">Obiekt lokalny reprezentujący profil można uzyskać za pomocą Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de94f-109">You can obtain a local object that represents a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="de94f-110">Zmodyfikuj obiekt lokalnie, a następnie **użyj set-azTrafficManagerProfile,** aby zatwierdzić zmiany.</span><span class="sxs-lookup"><span data-stu-id="de94f-110">Modify the object locally and then use **Set-AzTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="de94f-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="de94f-111">EXAMPLES</span></span>

### <span data-ttu-id="de94f-112">Przykład 1. Aktualizowanie profilu</span><span class="sxs-lookup"><span data-stu-id="de94f-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="de94f-113">Pierwsze polecenie otrzymuje profil usługi Azure Traffic Manager przy użyciu Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de94f-113">The first command gets an Azure Traffic Manager profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="de94f-114">Polecenie przechowuje profil lokalnie w $TrafficManagerProfile zmienną.</span><span class="sxs-lookup"><span data-stu-id="de94f-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="de94f-115">Drugie polecenie zmienia profil lokalnie.</span><span class="sxs-lookup"><span data-stu-id="de94f-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="de94f-116">To polecenie wyłącza profil.</span><span class="sxs-lookup"><span data-stu-id="de94f-116">This command disables the profile.</span></span>

<span data-ttu-id="de94f-117">Trzecie polecenie aktualizuje profil menedżera ruchu o nazwie ContosoProfile, aby dopasować go do wartości lokalnej w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="de94f-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="de94f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de94f-118">PARAMETERS</span></span>

### <span data-ttu-id="de94f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de94f-119">-DefaultProfile</span></span>
<span data-ttu-id="de94f-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="de94f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de94f-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="de94f-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="de94f-122">Określa lokalny obiekt **TrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="de94f-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="de94f-123">To polecenie cmdlet aktualizuje Menedżera ruchu w celu dopasowania tego obiektu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="de94f-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="de94f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de94f-124">CommonParameters</span></span>
<span data-ttu-id="de94f-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de94f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de94f-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de94f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de94f-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de94f-127">INPUTS</span></span>

### <span data-ttu-id="de94f-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="de94f-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="de94f-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de94f-129">OUTPUTS</span></span>

### <span data-ttu-id="de94f-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="de94f-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="de94f-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="de94f-131">NOTES</span></span>

## <span data-ttu-id="de94f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de94f-132">RELATED LINKS</span></span>

[<span data-ttu-id="de94f-133">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="de94f-133">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="de94f-134">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="de94f-134">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="de94f-135">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="de94f-135">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="de94f-136">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="de94f-136">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="de94f-137">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="de94f-137">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)


