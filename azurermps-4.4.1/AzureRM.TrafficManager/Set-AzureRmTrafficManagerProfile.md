---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: e8baf033131442f23a0db63339673018b209f140
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717550"
---
# <span data-ttu-id="f1cb3-101">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f1cb3-101">Set-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="f1cb3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f1cb3-102">SYNOPSIS</span></span>
<span data-ttu-id="f1cb3-103">Aktualizuje profil w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="f1cb3-103">Updates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1cb3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f1cb3-104">SYNTAX</span></span>

```
Set-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1cb3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f1cb3-105">DESCRIPTION</span></span>
<span data-ttu-id="f1cb3-106">Polecenie cmdlet **Set-AzureRmTrafficManagerProfile** aktualizuje profil usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="f1cb3-106">The **Set-AzureRmTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="f1cb3-107">To polecenie cmdlet umożliwia zaktualizowanie ustawień profilu z obiektu profilu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="f1cb3-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="f1cb3-108">Obiekt profile można określić przy użyciu parametru *TrafficManagerProfile* lub za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="f1cb3-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="f1cb3-109">Obiekt lokalny przedstawiający profil można uzyskać przy użyciu Get-AzureRmTrafficManagerProfile polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1cb3-109">You can obtain a local object that represents a profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="f1cb3-110">Zmodyfikuj obiekt lokalnie, a następnie użyj **Ustawienia Set-AzureRmTrafficManagerProfile** w celu zatwierdzenia zmian.</span><span class="sxs-lookup"><span data-stu-id="f1cb3-110">Modify the object locally and then use **Set-AzureRmTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="f1cb3-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f1cb3-111">EXAMPLES</span></span>

### <span data-ttu-id="f1cb3-112">Przykład 1: aktualizowanie profilu</span><span class="sxs-lookup"><span data-stu-id="f1cb3-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="f1cb3-113">Pierwsze polecenie pobiera profil usługi Azure Traffic Manager przy użyciu polecenia cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f1cb3-113">The first command gets an Azure Traffic Manager profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="f1cb3-114">Polecenie zapisuje profil lokalnie w zmiennej $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f1cb3-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="f1cb3-115">Drugie polecenie powoduje zmianę lokalnego profilu.</span><span class="sxs-lookup"><span data-stu-id="f1cb3-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="f1cb3-116">To polecenie wyłącza profil.</span><span class="sxs-lookup"><span data-stu-id="f1cb3-116">This command disables the profile.</span></span>

<span data-ttu-id="f1cb3-117">Trzecie polecenie aktualizuje profil usługi Traffic Manager o nazwie ContosoProfile, aby odpowiadał wartości lokalnej w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f1cb3-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="f1cb3-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f1cb3-118">PARAMETERS</span></span>

### <span data-ttu-id="f1cb3-119">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f1cb3-119">-TrafficManagerProfile</span></span>
<span data-ttu-id="f1cb3-120">Określa lokalny obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="f1cb3-120">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="f1cb3-121">To polecenie cmdlet umożliwia zaktualizowanie Menedżera ruchu w celu dopasowania go do tego obiektu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="f1cb3-121">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="f1cb3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1cb3-122">-DefaultProfile</span></span>
<span data-ttu-id="f1cb3-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f1cb3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1cb3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1cb3-124">CommonParameters</span></span>
<span data-ttu-id="f1cb3-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1cb3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1cb3-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1cb3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1cb3-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1cb3-127">INPUTS</span></span>

### <span data-ttu-id="f1cb3-128">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f1cb3-128">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="f1cb3-129">To polecenie cmdlet akceptuje obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="f1cb3-129">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="f1cb3-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f1cb3-130">OUTPUTS</span></span>

### <span data-ttu-id="f1cb3-131">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f1cb3-131">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="f1cb3-132">To polecenie cmdlet zwraca obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="f1cb3-132">This cmdlet returns a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="f1cb3-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f1cb3-133">NOTES</span></span>

## <span data-ttu-id="f1cb3-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1cb3-134">RELATED LINKS</span></span>

[<span data-ttu-id="f1cb3-135">Dodaj-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f1cb3-135">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="f1cb3-136">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f1cb3-136">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="f1cb3-137">Nowe — AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f1cb3-137">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="f1cb3-138">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f1cb3-138">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="f1cb3-139">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f1cb3-139">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)


