---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: d8f4b5e069ef273dedc8e2e5a1f929d1649aefdb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888474"
---
# <span data-ttu-id="0decc-101">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0decc-101">Set-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="0decc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0decc-102">SYNOPSIS</span></span>
<span data-ttu-id="0decc-103">Aktualizuje profil w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="0decc-103">Updates a Traffic Manager profile.</span></span>

## <span data-ttu-id="0decc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0decc-104">SYNTAX</span></span>

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0decc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0decc-105">DESCRIPTION</span></span>
<span data-ttu-id="0decc-106">Polecenie cmdlet **Set-AzTrafficManagerProfile** aktualizuje profil usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="0decc-106">The **Set-AzTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="0decc-107">To polecenie cmdlet umożliwia zaktualizowanie ustawień profilu z obiektu profilu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="0decc-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="0decc-108">Obiekt profile można określić przy użyciu parametru *TrafficManagerProfile* lub za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="0decc-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="0decc-109">Obiekt lokalny przedstawiający profil można uzyskać przy użyciu Get-AzTrafficManagerProfile polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0decc-109">You can obtain a local object that represents a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="0decc-110">Zmodyfikuj obiekt lokalnie, a następnie użyj **Ustawienia Set-AzTrafficManagerProfile** w celu zatwierdzenia zmian.</span><span class="sxs-lookup"><span data-stu-id="0decc-110">Modify the object locally and then use **Set-AzTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="0decc-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0decc-111">EXAMPLES</span></span>

### <span data-ttu-id="0decc-112">Przykład 1: aktualizowanie profilu</span><span class="sxs-lookup"><span data-stu-id="0decc-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="0decc-113">Pierwsze polecenie pobiera profil usługi Azure Traffic Manager przy użyciu polecenia cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="0decc-113">The first command gets an Azure Traffic Manager profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="0decc-114">Polecenie zapisuje profil lokalnie w zmiennej $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="0decc-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="0decc-115">Drugie polecenie powoduje zmianę lokalnego profilu.</span><span class="sxs-lookup"><span data-stu-id="0decc-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="0decc-116">To polecenie wyłącza profil.</span><span class="sxs-lookup"><span data-stu-id="0decc-116">This command disables the profile.</span></span>

<span data-ttu-id="0decc-117">Trzecie polecenie aktualizuje profil usługi Traffic Manager o nazwie ContosoProfile, aby odpowiadał wartości lokalnej w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="0decc-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="0decc-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0decc-118">PARAMETERS</span></span>

### <span data-ttu-id="0decc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0decc-119">-DefaultProfile</span></span>
<span data-ttu-id="0decc-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0decc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0decc-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0decc-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="0decc-122">Określa lokalny obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="0decc-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="0decc-123">To polecenie cmdlet umożliwia zaktualizowanie Menedżera ruchu w celu dopasowania go do tego obiektu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="0decc-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="0decc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0decc-124">CommonParameters</span></span>
<span data-ttu-id="0decc-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0decc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0decc-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0decc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0decc-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0decc-127">INPUTS</span></span>

### <span data-ttu-id="0decc-128">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0decc-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="0decc-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0decc-129">OUTPUTS</span></span>

### <span data-ttu-id="0decc-130">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0decc-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="0decc-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0decc-131">NOTES</span></span>

## <span data-ttu-id="0decc-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0decc-132">RELATED LINKS</span></span>

[<span data-ttu-id="0decc-133">Dodaj-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="0decc-133">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="0decc-134">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0decc-134">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="0decc-135">Nowe — AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0decc-135">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="0decc-136">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="0decc-136">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="0decc-137">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0decc-137">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)


