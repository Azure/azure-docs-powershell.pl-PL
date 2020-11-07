---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: f40587460cf5e4a1d7f06bfb88229f6e4e3f7975
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888454"
---
# <span data-ttu-id="22762-101">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="22762-101">Remove-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="22762-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22762-102">SYNOPSIS</span></span>
<span data-ttu-id="22762-103">Usuwa punkt końcowy z obiektu profilu lokalnego zarządzania ruchem.</span><span class="sxs-lookup"><span data-stu-id="22762-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="22762-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22762-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22762-105">Opis</span><span class="sxs-lookup"><span data-stu-id="22762-105">DESCRIPTION</span></span>
<span data-ttu-id="22762-106">Polecenie cmdlet **Remove-AzTrafficManagerEndpointConfig** umożliwia usunięcie punktu końcowego z obiektu profilu lokalnego usługi Azure Endpoint Manager.</span><span class="sxs-lookup"><span data-stu-id="22762-106">The **Remove-AzTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="22762-107">Możesz uzyskać profil przy użyciu Get-AzTrafficManagerProfile polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22762-107">You can get a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="22762-108">To polecenie cmdlet działa na obiekcie profilu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="22762-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="22762-109">Zatwierdź zmiany w profilu dla Menedżera ruchu, korzystając z polecenia cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="22762-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="22762-110">Aby usunąć punkt końcowy i przekazać zmiany w ramach jednej operacji, użyj polecenia cmdlet Remove-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="22762-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="22762-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22762-111">EXAMPLES</span></span>

### <span data-ttu-id="22762-112">Przykład 1: Usuwanie punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="22762-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="22762-113">Pierwsze polecenie pobiera profil usługi Azure Traffic Manager przy użyciu polecenia cmdlet **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="22762-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="22762-114">Polecenie zapisuje profil lokalny w zmiennej $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="22762-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="22762-115">Drugie polecenie usuwa punkt końcowy Azure o nazwie contoso z profilu przechowywanego w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="22762-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="22762-116">To polecenie powoduje zmianę tylko obiektu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="22762-116">This command changes only the local object.</span></span>

<span data-ttu-id="22762-117">Ostatnie polecenie aktualizuje profil usługi Traffic Manager o nazwie ContosoProfile, aby odpowiadał wartości lokalnej w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="22762-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="22762-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22762-118">PARAMETERS</span></span>

### <span data-ttu-id="22762-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22762-119">-DefaultProfile</span></span>
<span data-ttu-id="22762-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="22762-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22762-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="22762-121">-EndpointName</span></span>
<span data-ttu-id="22762-122">Określa nazwę punktu końcowego usługi Traffic Managera, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22762-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="22762-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="22762-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="22762-124">Określa lokalny obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="22762-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="22762-125">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="22762-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="22762-126">Aby uzyskać obiekt **TrafficManagerProfile** , użyj polecenia cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="22762-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="22762-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22762-127">CommonParameters</span></span>
<span data-ttu-id="22762-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22762-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22762-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22762-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22762-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22762-130">INPUTS</span></span>

### <span data-ttu-id="22762-131">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="22762-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="22762-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22762-132">OUTPUTS</span></span>

### <span data-ttu-id="22762-133">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="22762-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="22762-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22762-134">NOTES</span></span>

## <span data-ttu-id="22762-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22762-135">RELATED LINKS</span></span>

[<span data-ttu-id="22762-136">Dodaj-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="22762-136">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="22762-137">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="22762-137">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="22762-138">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="22762-138">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="22762-139">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="22762-139">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


