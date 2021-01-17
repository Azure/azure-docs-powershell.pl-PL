---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 4795e89013acaadcc08477370441ff5acdded85a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330385"
---
# <span data-ttu-id="b2c4d-101">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="b2c4d-101">Remove-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="b2c4d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b2c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="b2c4d-103">Usuwa punkt końcowy z obiektu profilu lokalnego zarządzania ruchem.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="b2c4d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b2c4d-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2c4d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b2c4d-105">DESCRIPTION</span></span>
<span data-ttu-id="b2c4d-106">Polecenie cmdlet **Remove-AzTrafficManagerEndpointConfig** umożliwia usunięcie punktu końcowego z obiektu profilu lokalnego usługi Azure Endpoint Manager.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-106">The **Remove-AzTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="b2c4d-107">Możesz uzyskać profil przy użyciu Get-AzTrafficManagerProfile polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-107">You can get a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="b2c4d-108">To polecenie cmdlet działa na obiekcie profilu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="b2c4d-109">Zatwierdź zmiany w profilu dla Menedżera ruchu, korzystając z polecenia cmdlet Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="b2c4d-110">Aby usunąć punkt końcowy i przekazać zmiany w ramach jednej operacji, użyj polecenia cmdlet Remove-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="b2c4d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b2c4d-111">EXAMPLES</span></span>

### <span data-ttu-id="b2c4d-112">Przykład 1: Usuwanie punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="b2c4d-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="b2c4d-113">Pierwsze polecenie pobiera profil usługi Azure Traffic Manager przy użyciu polecenia cmdlet **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="b2c4d-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="b2c4d-114">Polecenie zapisuje profil lokalny w zmiennej $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="b2c4d-115">Drugie polecenie usuwa punkt końcowy Azure o nazwie contoso z profilu przechowywanego w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="b2c4d-116">To polecenie powoduje zmianę tylko obiektu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-116">This command changes only the local object.</span></span>

<span data-ttu-id="b2c4d-117">Ostatnie polecenie aktualizuje profil usługi Traffic Manager o nazwie ContosoProfile, aby odpowiadał wartości lokalnej w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="b2c4d-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b2c4d-118">PARAMETERS</span></span>

### <span data-ttu-id="b2c4d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2c4d-119">-DefaultProfile</span></span>
<span data-ttu-id="b2c4d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2c4d-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b2c4d-121">-EndpointName</span></span>
<span data-ttu-id="b2c4d-122">Określa nazwę punktu końcowego usługi Traffic Managera, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b2c4d-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b2c4d-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="b2c4d-124">Określa lokalny obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="b2c4d-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="b2c4d-125">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="b2c4d-126">Aby uzyskać obiekt **TrafficManagerProfile** , użyj polecenia cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="b2c4d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2c4d-127">CommonParameters</span></span>
<span data-ttu-id="b2c4d-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2c4d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2c4d-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2c4d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2c4d-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2c4d-130">INPUTS</span></span>

### <span data-ttu-id="b2c4d-131">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b2c4d-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="b2c4d-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b2c4d-132">OUTPUTS</span></span>

### <span data-ttu-id="b2c4d-133">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b2c4d-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="b2c4d-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b2c4d-134">NOTES</span></span>

## <span data-ttu-id="b2c4d-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2c4d-135">RELATED LINKS</span></span>

[<span data-ttu-id="b2c4d-136">Dodaj-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="b2c4d-136">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="b2c4d-137">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b2c4d-137">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="b2c4d-138">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b2c4d-138">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="b2c4d-139">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b2c4d-139">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


