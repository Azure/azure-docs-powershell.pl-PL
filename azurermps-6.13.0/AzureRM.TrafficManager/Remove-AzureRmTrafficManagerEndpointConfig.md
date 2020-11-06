---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: 3468730caa727c7c8cde46ddbf431c374361b8fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525925"
---
# <span data-ttu-id="1dc99-101">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="1dc99-101">Remove-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="1dc99-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1dc99-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc99-103">Usuwa punkt końcowy z obiektu profilu lokalnego zarządzania ruchem.</span><span class="sxs-lookup"><span data-stu-id="1dc99-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dc99-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1dc99-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerEndpointConfig -EndpointName <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dc99-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1dc99-105">DESCRIPTION</span></span>
<span data-ttu-id="1dc99-106">Polecenie cmdlet **Remove-AzureRmTrafficManagerEndpointConfig** umożliwia usunięcie punktu końcowego z obiektu profilu lokalnego usługi Azure Endpoint Manager.</span><span class="sxs-lookup"><span data-stu-id="1dc99-106">The **Remove-AzureRmTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="1dc99-107">Możesz uzyskać profil przy użyciu Get-AzureRmTrafficManagerProfile polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dc99-107">You can get a profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="1dc99-108">To polecenie cmdlet działa na obiekcie profilu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="1dc99-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="1dc99-109">Zatwierdź zmiany w profilu dla Menedżera ruchu, korzystając z polecenia cmdlet Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="1dc99-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="1dc99-110">Aby usunąć punkt końcowy i przekazać zmiany w ramach jednej operacji, użyj polecenia cmdlet Remove-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="1dc99-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="1dc99-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1dc99-111">EXAMPLES</span></span>

### <span data-ttu-id="1dc99-112">Przykład 1: Usuwanie punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="1dc99-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="1dc99-113">Pierwsze polecenie pobiera profil usługi Azure Traffic Manager przy użyciu polecenia cmdlet **Get-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="1dc99-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="1dc99-114">Polecenie zapisuje profil lokalny w zmiennej $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="1dc99-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="1dc99-115">Drugie polecenie usuwa punkt końcowy Azure o nazwie contoso z profilu przechowywanego w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="1dc99-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="1dc99-116">To polecenie powoduje zmianę tylko obiektu lokalnego.</span><span class="sxs-lookup"><span data-stu-id="1dc99-116">This command changes only the local object.</span></span>

<span data-ttu-id="1dc99-117">Ostatnie polecenie aktualizuje profil usługi Traffic Manager o nazwie ContosoProfile, aby odpowiadał wartości lokalnej w $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="1dc99-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="1dc99-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1dc99-118">PARAMETERS</span></span>

### <span data-ttu-id="1dc99-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc99-119">-DefaultProfile</span></span>
<span data-ttu-id="1dc99-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1dc99-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dc99-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1dc99-121">-EndpointName</span></span>
<span data-ttu-id="1dc99-122">Określa nazwę punktu końcowego usługi Traffic Managera, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dc99-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1dc99-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1dc99-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="1dc99-124">Określa lokalny obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="1dc99-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="1dc99-125">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="1dc99-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="1dc99-126">Aby uzyskać obiekt **TrafficManagerProfile** , użyj polecenia cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="1dc99-126">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="1dc99-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc99-127">CommonParameters</span></span>
<span data-ttu-id="1dc99-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dc99-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc99-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dc99-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc99-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1dc99-130">INPUTS</span></span>

### <span data-ttu-id="1dc99-131">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1dc99-131">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="1dc99-132">To polecenie cmdlet akceptuje obiekt **TrafficManagerProfile** do tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dc99-132">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="1dc99-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1dc99-133">OUTPUTS</span></span>

### <span data-ttu-id="1dc99-134">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1dc99-134">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="1dc99-135">To polecenie cmdlet zwraca zmodyfikowany obiekt TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="1dc99-135">This cmdlet returns a modified TrafficManagerProfile object.</span></span>

## <span data-ttu-id="1dc99-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1dc99-136">NOTES</span></span>

## <span data-ttu-id="1dc99-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1dc99-137">RELATED LINKS</span></span>

[<span data-ttu-id="1dc99-138">Dodaj-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="1dc99-138">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="1dc99-139">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1dc99-139">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="1dc99-140">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1dc99-140">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="1dc99-141">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1dc99-141">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


