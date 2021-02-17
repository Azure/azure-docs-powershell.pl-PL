---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 037a670c0e96d1a9014cd19b32a7d2ba4da282ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198282"
---
# <span data-ttu-id="fbb1d-101">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fbb1d-101">Disable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="fbb1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbb1d-102">SYNOPSIS</span></span>
<span data-ttu-id="fbb1d-103">Wyłącza punkt końcowy w profilu Menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="fbb1d-103">Disables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="fbb1d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fbb1d-104">SYNTAX</span></span>

### <span data-ttu-id="fbb1d-105">Pola</span><span class="sxs-lookup"><span data-stu-id="fbb1d-105">Fields</span></span>
```
Disable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fbb1d-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="fbb1d-106">Object</span></span>
```
Disable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbb1d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="fbb1d-107">DESCRIPTION</span></span>
<span data-ttu-id="fbb1d-108">Polecenie **cmdlet Disable-AzTrafficManagerEndpoint** wyłącza punkt końcowy w profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="fbb1d-108">The **Disable-AzTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="fbb1d-109">Za pomocą operatora potoku można przekazać obiekt **TrafficManagerEndpoint** do tego polecenia cmdlet lub przekazać obiekt **TrafficManagerEndpoint** przy użyciu *parametru TrafficManagerEndpoint.*</span><span class="sxs-lookup"><span data-stu-id="fbb1d-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="fbb1d-110">Możesz również określić nazwę punktu końcowego i typ, używając parametrów *Name* (Nazwa) i *Type* (Typ) wraz z parametrami *ProfileName* (Nazwa_profilu) i *ResourceGroupName (Nazwa* Grupy Zasobów).</span><span class="sxs-lookup"><span data-stu-id="fbb1d-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="fbb1d-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fbb1d-111">EXAMPLES</span></span>

### <span data-ttu-id="fbb1d-112">Przykład 1. Wyłączanie punktu końcowego według nazwy</span><span class="sxs-lookup"><span data-stu-id="fbb1d-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="fbb1d-113">To polecenie wyłącza zewnętrzny punkt końcowy o nazwie contoso w profilu o nazwie ContosoProfile w grupie zasobów ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="fbb1d-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="fbb1d-114">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fbb1d-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="fbb1d-115">Przykład 2. Wyłączanie punktu końcowego przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="fbb1d-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerEndpoint -Force
```

<span data-ttu-id="fbb1d-116">To polecenie pobiera zewnętrzny punkt końcowy o nazwie Contoso z profilu o nazwie ContosoProfile w grupie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="fbb1d-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="fbb1d-117">Następnie polecenie przekazuje ten punkt końcowy do polecenia cmdlet **Disable-AzTrafficManagerEndpoint** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="fbb1d-117">The command then passes that endpoint to the **Disable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fbb1d-118">To polecenie cmdlet wyłącza ten punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="fbb1d-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="fbb1d-119">Polecenie określa parametr *Force.*</span><span class="sxs-lookup"><span data-stu-id="fbb1d-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="fbb1d-120">Dlatego nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fbb1d-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="fbb1d-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbb1d-121">PARAMETERS</span></span>

### <span data-ttu-id="fbb1d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbb1d-122">-DefaultProfile</span></span>
<span data-ttu-id="fbb1d-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fbb1d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbb1d-124">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="fbb1d-124">-Force</span></span>
<span data-ttu-id="fbb1d-125">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fbb1d-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fbb1d-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fbb1d-126">-Name</span></span>
<span data-ttu-id="fbb1d-127">Określa nazwę punktu końcowego Menedżera ruchu, który zostanie wyłączany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbb1d-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="fbb1d-128">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="fbb1d-128">-ProfileName</span></span>
<span data-ttu-id="fbb1d-129">Określa nazwę profilu menedżera ruchu, w którym to polecenie cmdlet wyłącza punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="fbb1d-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="fbb1d-130">Aby uzyskać profil, użyj polecenia cmdlet Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbb1d-130">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="fbb1d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbb1d-131">-ResourceGroupName</span></span>
<span data-ttu-id="fbb1d-132">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fbb1d-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="fbb1d-133">To polecenie cmdlet wyłącza punkt końcowy menedżera ruchu w grupie, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="fbb1d-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fbb1d-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fbb1d-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="fbb1d-135">Określa punkt końcowy Menedżera ruchu, który zostanie wyłączany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbb1d-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="fbb1d-136">Aby uzyskać obiekt **TrafficManagerEndpoint,** użyj Get-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbb1d-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="fbb1d-137">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="fbb1d-137">-Type</span></span>
<span data-ttu-id="fbb1d-138">Określa typ punktu końcowego, który to polecenie cmdlet dodaje do profilu Menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="fbb1d-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="fbb1d-139">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="fbb1d-139">Valid values are:</span></span> 

- <span data-ttu-id="fbb1d-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="fbb1d-140">AzureEndpoints</span></span>
- <span data-ttu-id="fbb1d-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="fbb1d-141">ExternalEndpoints</span></span>
- <span data-ttu-id="fbb1d-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="fbb1d-142">NestedEndpoints</span></span>

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

### <span data-ttu-id="fbb1d-143">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fbb1d-143">-Confirm</span></span>
<span data-ttu-id="fbb1d-144">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fbb1d-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbb1d-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbb1d-145">-WhatIf</span></span>
<span data-ttu-id="fbb1d-146">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbb1d-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbb1d-147">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fbb1d-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbb1d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbb1d-148">CommonParameters</span></span>
<span data-ttu-id="fbb1d-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbb1d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbb1d-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbb1d-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbb1d-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbb1d-151">INPUTS</span></span>

### <span data-ttu-id="fbb1d-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fbb1d-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="fbb1d-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbb1d-153">OUTPUTS</span></span>

### <span data-ttu-id="fbb1d-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fbb1d-154">System.Boolean</span></span>

## <span data-ttu-id="fbb1d-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fbb1d-155">NOTES</span></span>

## <span data-ttu-id="fbb1d-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbb1d-156">RELATED LINKS</span></span>

[<span data-ttu-id="fbb1d-157">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fbb1d-157">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="fbb1d-158">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fbb1d-158">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="fbb1d-159">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fbb1d-159">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="fbb1d-160">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fbb1d-160">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="fbb1d-161">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fbb1d-161">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="fbb1d-162">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fbb1d-162">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="fbb1d-163">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fbb1d-163">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


