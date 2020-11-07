---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurertmtrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: a00eb5977ad1a58b12ad3f326d36dba8d083d718
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719053"
---
# <span data-ttu-id="bd65f-101">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd65f-101">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="bd65f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd65f-102">SYNOPSIS</span></span>
<span data-ttu-id="bd65f-103">Dodaje niestandardowe informacje nagłówka do obiektu punktu końcowego lokalnego zarządzania ruchem.</span><span class="sxs-lookup"><span data-stu-id="bd65f-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd65f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd65f-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd65f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bd65f-105">DESCRIPTION</span></span>
<span data-ttu-id="bd65f-106">Polecenie cmdlet **Add-AzureRmTrafficManagerCustomHeaderToEndpoint** dodaje niestandardowe informacje nagłówka do obiektu punktu końcowego usługi Azure Local Manager.</span><span class="sxs-lookup"><span data-stu-id="bd65f-106">The **Add-AzureRmTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="bd65f-107">Punkt końcowy można uzyskać przy użyciu New-AzureRmTrafficManagerEndpoint lub Get-AzureRmTrafficManagerEndpoint poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd65f-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="bd65f-108">To polecenie cmdlet działa w obiekcie lokalnego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="bd65f-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="bd65f-109">Zatwierdź zmiany w punkcie końcowym w usłudze Traffic Manager przy użyciu polecenia cmdlet Set-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="bd65f-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="bd65f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd65f-110">EXAMPLES</span></span>

### <span data-ttu-id="bd65f-111">Przykład 1: Dodawanie niestandardowych informacji nagłówka do punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="bd65f-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzureRmTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="bd65f-112">Pierwsze polecenie tworzy punkt końcowy usługi Azure Traffic Manager przy użyciu polecenia cmdlet **New-AzureRmTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="bd65f-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzureRmTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="bd65f-113">Polecenie zapisuje lokalny punkt końcowy w zmiennej $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="bd65f-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="bd65f-114">Drugie polecenie dodaje niestandardowe informacje nagłówka do punktu końcowego przechowywanego w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="bd65f-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="bd65f-115">Polecenie ostatnie powoduje zaktualizowanie punktu końcowego w usłudze Traffic Manager w celu dopasowania go do wartości lokalnej w $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="bd65f-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="bd65f-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd65f-116">PARAMETERS</span></span>

### <span data-ttu-id="bd65f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd65f-117">-DefaultProfile</span></span>
<span data-ttu-id="bd65f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd65f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd65f-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bd65f-119">-Name</span></span>
<span data-ttu-id="bd65f-120">Określa nazwę informacji nagłówka niestandardowego, które mają zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="bd65f-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="bd65f-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd65f-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="bd65f-122">Określa lokalny obiekt **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="bd65f-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="bd65f-123">To polecenie cmdlet modyfikuje ten obiekt lokalny.</span><span class="sxs-lookup"><span data-stu-id="bd65f-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="bd65f-124">Aby uzyskać obiekt **TrafficManagerEndpoint** , użyj polecenia cmdlet Get-AzureRmTrafficManagerEndpoint lub New-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="bd65f-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="bd65f-125">-Value</span><span class="sxs-lookup"><span data-stu-id="bd65f-125">-Value</span></span>
<span data-ttu-id="bd65f-126">Określa wartość niestandardowych informacji nagłówka, które mają zostać dodane.</span><span class="sxs-lookup"><span data-stu-id="bd65f-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="bd65f-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bd65f-127">-Confirm</span></span>
<span data-ttu-id="bd65f-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd65f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd65f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd65f-129">-WhatIf</span></span>
<span data-ttu-id="bd65f-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd65f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd65f-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bd65f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd65f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd65f-132">CommonParameters</span></span>
<span data-ttu-id="bd65f-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd65f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd65f-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd65f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd65f-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd65f-135">INPUTS</span></span>

### <span data-ttu-id="bd65f-136">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd65f-136">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="bd65f-137">To polecenie cmdlet akceptuje obiekt **TrafficManagerEndpoint** do tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd65f-137">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="bd65f-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd65f-138">OUTPUTS</span></span>

### <span data-ttu-id="bd65f-139">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd65f-139">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="bd65f-140">To polecenie cmdlet zwraca zmodyfikowany obiekt **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="bd65f-140">This cmdlet returns a modified **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="bd65f-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd65f-141">NOTES</span></span>

## <span data-ttu-id="bd65f-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd65f-142">RELATED LINKS</span></span>

[<span data-ttu-id="bd65f-143">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd65f-143">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="bd65f-144">Nowe — AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd65f-144">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="bd65f-145">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bd65f-145">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="bd65f-146">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd65f-146">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
