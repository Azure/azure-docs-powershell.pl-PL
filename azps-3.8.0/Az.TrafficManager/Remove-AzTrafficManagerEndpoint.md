---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 6f2884a6d4cefaf52b06ec653db85c9e9ae59f54
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895893"
---
# <span data-ttu-id="ab108-101">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ab108-101">Remove-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="ab108-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab108-102">SYNOPSIS</span></span>
<span data-ttu-id="ab108-103">Umożliwia usunięcie punktu końcowego z usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="ab108-103">Removes an endpoint from Traffic Manager.</span></span>

## <span data-ttu-id="ab108-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab108-104">SYNTAX</span></span>

### <span data-ttu-id="ab108-105">Field</span><span class="sxs-lookup"><span data-stu-id="ab108-105">Fields</span></span>
```
Remove-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab108-106">Stream</span><span class="sxs-lookup"><span data-stu-id="ab108-106">Object</span></span>
```
Remove-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab108-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ab108-107">DESCRIPTION</span></span>
<span data-ttu-id="ab108-108">Polecenie cmdlet **Remove-AzTrafficManagerEndpoint** umożliwia usunięcie punktu końcowego z usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="ab108-108">The **Remove-AzTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="ab108-109">To polecenie cmdlet umożliwia przekazanie każdej zmiany do usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="ab108-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="ab108-110">Aby usunąć wiele punktów końcowych z obiektu profilu lokalnego Menedżera ruchu i przekazać zmiany w ramach jednej operacji, użyj polecenia cmdlet Remove-AzTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="ab108-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="ab108-111">Za pomocą operatora potoku możesz przekazać obiekt **TrafficManagerEndpoint** do tego polecenia cmdlet lub określić obiekt **TrafficManagerEndpoint** przy użyciu parametru *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="ab108-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="ab108-112">Możesz też określić nazwę i typ punktu końcowego przy użyciu parametrów *Nazwa* i *Typ* wraz z parametrami *refilename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="ab108-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="ab108-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab108-113">EXAMPLES</span></span>

### <span data-ttu-id="ab108-114">Przykład 1: Usuwanie punktu końcowego z profilu</span><span class="sxs-lookup"><span data-stu-id="ab108-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="ab108-115">To polecenie usuwa punkt końcowy Azure o nazwie contoso z profilu o nazwie ContosoProfile w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ab108-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="ab108-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab108-116">PARAMETERS</span></span>

### <span data-ttu-id="ab108-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab108-117">-DefaultProfile</span></span>
<span data-ttu-id="ab108-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab108-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab108-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ab108-119">-Force</span></span>
<span data-ttu-id="ab108-120">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ab108-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab108-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ab108-121">-Name</span></span>
<span data-ttu-id="ab108-122">Określa nazwę punktu końcowego usługi Traffic Managera, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab108-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab108-123">-Refilename</span><span class="sxs-lookup"><span data-stu-id="ab108-123">-ProfileName</span></span>
<span data-ttu-id="ab108-124">Określa nazwę profilu usługi Traffic Manager, z którego to polecenie cmdlet usuwa punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="ab108-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="ab108-125">Aby uzyskać profil, użyj polecenia cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="ab108-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab108-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab108-126">-ResourceGroupName</span></span>
<span data-ttu-id="ab108-127">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ab108-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ab108-128">To polecenie cmdlet umożliwia usunięcie punktu końcowego usługi Traffic managera z profilu usługi Traffic Manager w grupie, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="ab108-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab108-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ab108-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="ab108-130">Określa punkt końcowy usługi Traffic Managera, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab108-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="ab108-131">Aby uzyskać obiekt **TrafficManagerEndpoint** , użyj polecenia cmdlet Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ab108-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab108-132">-Type</span><span class="sxs-lookup"><span data-stu-id="ab108-132">-Type</span></span>
<span data-ttu-id="ab108-133">Określa typ punktu końcowego, który jest dodawany przez to polecenie cmdlet do profilu usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="ab108-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="ab108-134">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="ab108-134">Valid values are:</span></span> 

- <span data-ttu-id="ab108-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="ab108-135">AzureEndpoints</span></span>
- <span data-ttu-id="ab108-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="ab108-136">ExternalEndpoints</span></span>
- <span data-ttu-id="ab108-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="ab108-137">NestedEndpoints</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab108-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab108-138">-Confirm</span></span>
<span data-ttu-id="ab108-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab108-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab108-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab108-140">-WhatIf</span></span>
<span data-ttu-id="ab108-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab108-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab108-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ab108-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab108-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab108-143">CommonParameters</span></span>
<span data-ttu-id="ab108-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab108-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab108-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab108-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab108-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab108-146">INPUTS</span></span>

### <span data-ttu-id="ab108-147">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ab108-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="ab108-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab108-148">OUTPUTS</span></span>

### <span data-ttu-id="ab108-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab108-149">System.Boolean</span></span>

## <span data-ttu-id="ab108-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab108-150">NOTES</span></span>

## <span data-ttu-id="ab108-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab108-151">RELATED LINKS</span></span>

[<span data-ttu-id="ab108-152">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ab108-152">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="ab108-153">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ab108-153">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="ab108-154">Nowe — AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ab108-154">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="ab108-155">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="ab108-155">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="ab108-156">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ab108-156">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


