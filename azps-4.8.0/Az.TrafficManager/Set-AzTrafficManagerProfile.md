---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: 8f774ab221160a94ee4e8b5f13780b7e3131f252
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222408"
---
# <span data-ttu-id="7ed80-101">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7ed80-101">Set-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="7ed80-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7ed80-102">SYNOPSIS</span></span>
<span data-ttu-id="7ed80-103">Aktualizuje profil w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="7ed80-103">Updates a Traffic Manager profile.</span></span>

## <span data-ttu-id="7ed80-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7ed80-104">SYNTAX</span></span>

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ed80-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7ed80-105">DESCRIPTION</span></span>
<span data-ttu-id="7ed80-106">Polecenie cmdlet **Set-AzTrafficManagerProfile** aktualizuje profil usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="7ed80-106">The **Set-AzTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="7ed80-107">To polecenie cmdlet umożliwia zaktualizowanie ustawień profilu z obiektu profilu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="7ed80-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="7ed80-108">Obiekt profile można określić przy użyciu parametru *TrafficManagerProfile* lub za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="7ed80-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="7ed80-109">Obiekt lokalny przedstawiający profil można uzyskać przy użyciu Get-AzTrafficManagerProfile polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ed80-109">You can obtain a local object that represents a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="7ed80-110">Zmodyfikuj obiekt lokalnie, a następnie użyj **Ustawienia Set-AzTrafficManagerProfile** w celu zatwierdzenia zmian.</span><span class="sxs-lookup"><span data-stu-id="7ed80-110">Modify the object locally and then use **Set-AzTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="7ed80-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7ed80-111">EXAMPLES</span></span>

### <span data-ttu-id="7ed80-112">Przykład 1: aktualizowanie profilu</span><span class="sxs-lookup"><span data-stu-id="7ed80-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="7ed80-113">Pierwsze polecenie pobiera profil usługi Azure Traffic Manager przy użyciu polecenia cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="7ed80-113">The first command gets an Azure Traffic Manager profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="7ed80-114">Polecenie zapisuje profil lokalnie w zmiennej $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="7ed80-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="7ed80-115">Drugie polecenie powoduje zmianę lokalnego profilu.</span><span class="sxs-lookup"><span data-stu-id="7ed80-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="7ed80-116">To polecenie wyłącza profil.</span><span class="sxs-lookup"><span data-stu-id="7ed80-116">This command disables the profile.</span></span>

<span data-ttu-id="7ed80-117">Trzecie polecenie aktualizuje profil usługi Traffic Manager o nazwie ContosoProfile, aby odpowiadał wartości lokalnej w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="7ed80-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="7ed80-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7ed80-118">PARAMETERS</span></span>

### <span data-ttu-id="7ed80-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ed80-119">-DefaultProfile</span></span>
<span data-ttu-id="7ed80-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7ed80-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ed80-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7ed80-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="7ed80-122">Określa lokalny obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="7ed80-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="7ed80-123">To polecenie cmdlet umożliwia zaktualizowanie Menedżera ruchu w celu dopasowania go do tego obiektu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="7ed80-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="7ed80-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ed80-124">CommonParameters</span></span>
<span data-ttu-id="7ed80-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ed80-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ed80-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ed80-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ed80-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7ed80-127">INPUTS</span></span>

### <span data-ttu-id="7ed80-128">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7ed80-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="7ed80-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7ed80-129">OUTPUTS</span></span>

### <span data-ttu-id="7ed80-130">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7ed80-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="7ed80-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7ed80-131">NOTES</span></span>

## <span data-ttu-id="7ed80-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7ed80-132">RELATED LINKS</span></span>

[<span data-ttu-id="7ed80-133">Dodaj-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="7ed80-133">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="7ed80-134">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7ed80-134">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="7ed80-135">Nowe — AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7ed80-135">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="7ed80-136">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="7ed80-136">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="7ed80-137">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7ed80-137">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)


