---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: 452e252b7bf9368ea89e81f2d37fd5a80ab079b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525926"
---
# <span data-ttu-id="e6264-101">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6264-101">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="e6264-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e6264-102">SYNOPSIS</span></span>
<span data-ttu-id="e6264-103">Usuwa informacje z nagłówków niestandardowych z obiektu punktu końcowego lokalnego zarządzania ruchem.</span><span class="sxs-lookup"><span data-stu-id="e6264-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6264-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e6264-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -Name <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6264-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e6264-105">DESCRIPTION</span></span>
<span data-ttu-id="e6264-106">Polecenie cmdlet **Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint** powoduje usunięcie niestandardowych informacji nagłówka z obiektu punktu końcowego usługi Azure Local Manager.</span><span class="sxs-lookup"><span data-stu-id="e6264-106">The **Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="e6264-107">Punkt końcowy można uzyskać przy użyciu New-AzureRmTrafficManagerEndpoint lub Get-AzureRmTrafficManagerEndpoint poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6264-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="e6264-108">To polecenie cmdlet działa w obiekcie lokalnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="e6264-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="e6264-109">Zatwierdź zmiany w punkcie końcowym w usłudze Traffic Manager przy użyciu polecenia cmdlet Set-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e6264-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="e6264-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e6264-110">EXAMPLES</span></span>

### <span data-ttu-id="e6264-111">Przykład 1: usuwanie niestandardowych informacji o podsieciie z punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="e6264-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="e6264-112">Pierwsze polecenie uzyskuje punkt końcowy Azure o nazwie contoso z profilu o nazwie ContosoProfile w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e6264-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="e6264-113">Drugie polecenie usuwa informacje z nagłówków niestandardowych z punktu końcowego przechowywanego w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e6264-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="e6264-114">Polecenie ostatnie powoduje zaktualizowanie punktu końcowego w usłudze Traffic Manager w celu dopasowania go do wartości lokalnej w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e6264-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="e6264-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e6264-115">PARAMETERS</span></span>

### <span data-ttu-id="e6264-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6264-116">-DefaultProfile</span></span>
<span data-ttu-id="e6264-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6264-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6264-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e6264-118">-Name</span></span>
<span data-ttu-id="e6264-119">Określa nazwę informacji nagłówka niestandardowego, które mają zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="e6264-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="e6264-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6264-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="e6264-121">Określa lokalny obiekt **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="e6264-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="e6264-122">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="e6264-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="e6264-123">Aby uzyskać obiekt **TrafficManagerEndpoint** , użyj polecenia cmdlet Get-AzureRmTrafficManagerEndpoint lub New-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e6264-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6264-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e6264-124">-Confirm</span></span>
<span data-ttu-id="e6264-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6264-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6264-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6264-126">-WhatIf</span></span>
<span data-ttu-id="e6264-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6264-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6264-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e6264-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6264-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6264-129">CommonParameters</span></span>
<span data-ttu-id="e6264-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6264-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6264-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6264-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6264-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6264-132">INPUTS</span></span>

### <span data-ttu-id="e6264-133">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6264-133">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="e6264-134">To polecenie cmdlet akceptuje obiekt **TrafficManagerEndpoint** do tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6264-134">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="e6264-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e6264-135">OUTPUTS</span></span>

### <span data-ttu-id="e6264-136">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6264-136">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="e6264-137">To polecenie cmdlet zwraca zmodyfikowany obiekt TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e6264-137">This cmdlet returns a modified TrafficManagerEndpoint object.</span></span>

## <span data-ttu-id="e6264-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e6264-138">NOTES</span></span>

## <span data-ttu-id="e6264-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6264-139">RELATED LINKS</span></span>

[<span data-ttu-id="e6264-140">Dodaj-AzureRmTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6264-140">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="e6264-141">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e6264-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="e6264-142">Nowe — AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6264-142">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="e6264-143">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6264-143">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
