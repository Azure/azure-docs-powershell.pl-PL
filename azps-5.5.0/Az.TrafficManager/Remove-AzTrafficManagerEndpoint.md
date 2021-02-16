---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 6f2884a6d4cefaf52b06ec653db85c9e9ae59f54
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182579"
---
# <span data-ttu-id="d8d4e-101">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d8d4e-101">Remove-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="d8d4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8d4e-102">SYNOPSIS</span></span>
<span data-ttu-id="d8d4e-103">Usuwa punkt końcowy z Menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="d8d4e-103">Removes an endpoint from Traffic Manager.</span></span>

## <span data-ttu-id="d8d4e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d8d4e-104">SYNTAX</span></span>

### <span data-ttu-id="d8d4e-105">Pola</span><span class="sxs-lookup"><span data-stu-id="d8d4e-105">Fields</span></span>
```
Remove-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8d4e-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="d8d4e-106">Object</span></span>
```
Remove-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8d4e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d8d4e-107">DESCRIPTION</span></span>
<span data-ttu-id="d8d4e-108">Polecenie **cmdlet Remove-AzTrafficManagerEndpoint** usuwa punkt końcowy z usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="d8d4e-108">The **Remove-AzTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="d8d4e-109">To polecenie cmdlet zatwierdza każdą zmianę w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="d8d4e-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="d8d4e-110">Aby usunąć wiele punktów końcowych z lokalnego obiektu profilu usługi Traffic Manager i zatwierdzić zmiany w ramach jednej operacji, użyj Remove-AzTrafficManagerEndpointConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8d4e-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="d8d4e-111">Za pomocą operatora potoku można przekazać obiekt **TrafficManagerEndpoint** do tego polecenia cmdlet lub określić obiekt **TrafficManagerEndpoint** przy użyciu *parametru TrafficManagerEndpoint.*</span><span class="sxs-lookup"><span data-stu-id="d8d4e-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="d8d4e-112">Możesz również określić nazwę punktu końcowego i typ, używając parametrów *Name* (Nazwa) i *Type* (Typ) wraz z parametrami *ProfileName* (Nazwa_profilu) i *ResourceGroupName (Nazwa* Grupy Zasobów).</span><span class="sxs-lookup"><span data-stu-id="d8d4e-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="d8d4e-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d8d4e-113">EXAMPLES</span></span>

### <span data-ttu-id="d8d4e-114">Przykład 1. Usuwanie punktu końcowego z profilu</span><span class="sxs-lookup"><span data-stu-id="d8d4e-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="d8d4e-115">To polecenie usuwa punkt końcowy platformy Azure o nazwie contoso z profilu o nazwie ContosoProfile w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d8d4e-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="d8d4e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8d4e-116">PARAMETERS</span></span>

### <span data-ttu-id="d8d4e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8d4e-117">-DefaultProfile</span></span>
<span data-ttu-id="d8d4e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8d4e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8d4e-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="d8d4e-119">-Force</span></span>
<span data-ttu-id="d8d4e-120">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d8d4e-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d8d4e-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d8d4e-121">-Name</span></span>
<span data-ttu-id="d8d4e-122">Określa nazwę punktu końcowego Menedżera ruchu, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8d4e-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d8d4e-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="d8d4e-123">-ProfileName</span></span>
<span data-ttu-id="d8d4e-124">Określa nazwę profilu menedżera ruchu, z którego to polecenie cmdlet usuwa punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="d8d4e-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="d8d4e-125">Aby uzyskać profil, użyj polecenia cmdlet Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8d4e-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="d8d4e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8d4e-126">-ResourceGroupName</span></span>
<span data-ttu-id="d8d4e-127">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d8d4e-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="d8d4e-128">To polecenie cmdlet usuwa punkt końcowy Menedżera ruchu z profilu Menedżera ruchu w grupie, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="d8d4e-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d8d4e-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d8d4e-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="d8d4e-130">Określa punkt końcowy Menedżera ruchu, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8d4e-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="d8d4e-131">Aby uzyskać obiekt **TrafficManagerEndpoint,** użyj Get-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8d4e-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="d8d4e-132">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="d8d4e-132">-Type</span></span>
<span data-ttu-id="d8d4e-133">Określa typ punktu końcowego, który to polecenie cmdlet dodaje do profilu Menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="d8d4e-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="d8d4e-134">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="d8d4e-134">Valid values are:</span></span> 

- <span data-ttu-id="d8d4e-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="d8d4e-135">AzureEndpoints</span></span>
- <span data-ttu-id="d8d4e-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="d8d4e-136">ExternalEndpoints</span></span>
- <span data-ttu-id="d8d4e-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="d8d4e-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="d8d4e-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d8d4e-138">-Confirm</span></span>
<span data-ttu-id="d8d4e-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d8d4e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8d4e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8d4e-140">-WhatIf</span></span>
<span data-ttu-id="d8d4e-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8d4e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8d4e-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d8d4e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8d4e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d4e-143">CommonParameters</span></span>
<span data-ttu-id="d8d4e-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8d4e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d4e-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8d4e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d4e-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8d4e-146">INPUTS</span></span>

### <span data-ttu-id="d8d4e-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d8d4e-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="d8d4e-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d8d4e-148">OUTPUTS</span></span>

### <span data-ttu-id="d8d4e-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d8d4e-149">System.Boolean</span></span>

## <span data-ttu-id="d8d4e-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d8d4e-150">NOTES</span></span>

## <span data-ttu-id="d8d4e-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8d4e-151">RELATED LINKS</span></span>

[<span data-ttu-id="d8d4e-152">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d8d4e-152">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="d8d4e-153">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d8d4e-153">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="d8d4e-154">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d8d4e-154">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="d8d4e-155">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="d8d4e-155">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="d8d4e-156">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d8d4e-156">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


