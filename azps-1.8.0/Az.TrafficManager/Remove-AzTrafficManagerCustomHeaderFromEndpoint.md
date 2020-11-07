---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: f1575de761180c6ce17bcd6af1186d3e5bff60ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707363"
---
# <span data-ttu-id="6ffdd-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ffdd-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="6ffdd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ffdd-102">SYNOPSIS</span></span>
<span data-ttu-id="6ffdd-103">Usuwa informacje z nagłówków niestandardowych z obiektu punktu końcowego lokalnego zarządzania ruchem.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="6ffdd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ffdd-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromEndpoint -Name <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ffdd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6ffdd-105">DESCRIPTION</span></span>
<span data-ttu-id="6ffdd-106">Polecenie cmdlet **Remove-AzTrafficManagerCustomHeaderFromEndpoint** powoduje usunięcie niestandardowych informacji nagłówka z obiektu punktu końcowego usługi Azure Local Manager.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-106">The **Remove-AzTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="6ffdd-107">Punkt końcowy można uzyskać przy użyciu New-AzTrafficManagerEndpoint lub Get-AzTrafficManagerEndpoint poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="6ffdd-108">To polecenie cmdlet działa w obiekcie lokalnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="6ffdd-109">Zatwierdź zmiany w punkcie końcowym w usłudze Traffic Manager przy użyciu polecenia cmdlet Set-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="6ffdd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ffdd-110">EXAMPLES</span></span>

### <span data-ttu-id="6ffdd-111">Przykład 1: usuwanie niestandardowych informacji o podsieciie z punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="6ffdd-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="6ffdd-112">Pierwsze polecenie uzyskuje punkt końcowy Azure o nazwie contoso z profilu o nazwie ContosoProfile w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="6ffdd-113">Drugie polecenie usuwa informacje z nagłówków niestandardowych z punktu końcowego przechowywanego w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="6ffdd-114">Polecenie ostatnie powoduje zaktualizowanie punktu końcowego w usłudze Traffic Manager w celu dopasowania go do wartości lokalnej w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="6ffdd-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ffdd-115">PARAMETERS</span></span>

### <span data-ttu-id="6ffdd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ffdd-116">-DefaultProfile</span></span>
<span data-ttu-id="6ffdd-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ffdd-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6ffdd-118">-Name</span></span>
<span data-ttu-id="6ffdd-119">Określa nazwę informacji nagłówka niestandardowego, które mają zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="6ffdd-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ffdd-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="6ffdd-121">Określa lokalny obiekt **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="6ffdd-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="6ffdd-122">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="6ffdd-123">Aby uzyskać obiekt **TrafficManagerEndpoint** , użyj polecenia cmdlet Get-AzTrafficManagerEndpoint lub New-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="6ffdd-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ffdd-124">-Confirm</span></span>
<span data-ttu-id="6ffdd-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ffdd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ffdd-126">-WhatIf</span></span>
<span data-ttu-id="6ffdd-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ffdd-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ffdd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ffdd-129">CommonParameters</span></span>
<span data-ttu-id="6ffdd-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ffdd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ffdd-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ffdd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ffdd-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ffdd-132">INPUTS</span></span>

### <span data-ttu-id="6ffdd-133">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ffdd-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="6ffdd-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ffdd-134">OUTPUTS</span></span>

### <span data-ttu-id="6ffdd-135">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ffdd-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="6ffdd-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ffdd-136">NOTES</span></span>

## <span data-ttu-id="6ffdd-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ffdd-137">RELATED LINKS</span></span>

[<span data-ttu-id="6ffdd-138">Dodaj-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ffdd-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="6ffdd-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6ffdd-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="6ffdd-140">Nowe — AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ffdd-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="6ffdd-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ffdd-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)