---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 037a670c0e96d1a9014cd19b32a7d2ba4da282ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050612"
---
# <span data-ttu-id="25689-101">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="25689-101">Disable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="25689-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25689-102">SYNOPSIS</span></span>
<span data-ttu-id="25689-103">Wyłącza punkt końcowy w profilu z menedżerem ruchu.</span><span class="sxs-lookup"><span data-stu-id="25689-103">Disables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="25689-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25689-104">SYNTAX</span></span>

### <span data-ttu-id="25689-105">Field</span><span class="sxs-lookup"><span data-stu-id="25689-105">Fields</span></span>
```
Disable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25689-106">Stream</span><span class="sxs-lookup"><span data-stu-id="25689-106">Object</span></span>
```
Disable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25689-107">Opis</span><span class="sxs-lookup"><span data-stu-id="25689-107">DESCRIPTION</span></span>
<span data-ttu-id="25689-108">Polecenie cmdlet **disable-AzTrafficManagerEndpoint** wyłącza punkt końcowy w profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="25689-108">The **Disable-AzTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="25689-109">Za pomocą operatora potoku możesz przekazać obiekt **TrafficManagerEndpoint** do tego polecenia cmdlet lub przekazać obiekt **TrafficManagerEndpoint** przy użyciu parametru *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="25689-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="25689-110">Możesz też określić nazwę i typ punktu końcowego przy użyciu parametrów *Nazwa* i *Typ* wraz z parametrami *refilename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="25689-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="25689-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25689-111">EXAMPLES</span></span>

### <span data-ttu-id="25689-112">Przykład 1. Wyłączanie punktu końcowego według nazwy</span><span class="sxs-lookup"><span data-stu-id="25689-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="25689-113">To polecenie powoduje wyłączenie zewnętrznego punktu końcowego o nazwie contoso w profilu o nazwie ContosoProfile w grupie zasób ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="25689-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="25689-114">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="25689-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="25689-115">Przykład 2: wyłączanie punktu końcowego przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="25689-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerEndpoint -Force
```

<span data-ttu-id="25689-116">To polecenie uzyskuje zewnętrzny punkt końcowy o nazwie contoso z profilu o nazwie ContosoProfile w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="25689-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="25689-117">Następnie polecenie przekazuje ten punkt końcowy do polecenia cmdlet **disable-AzTrafficManagerEndpoint** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="25689-117">The command then passes that endpoint to the **Disable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="25689-118">To polecenie cmdlet wyłącza ten punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="25689-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="25689-119">Polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="25689-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="25689-120">W związku z tym nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="25689-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="25689-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25689-121">PARAMETERS</span></span>

### <span data-ttu-id="25689-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25689-122">-DefaultProfile</span></span>
<span data-ttu-id="25689-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="25689-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25689-124">-Force</span><span class="sxs-lookup"><span data-stu-id="25689-124">-Force</span></span>
<span data-ttu-id="25689-125">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="25689-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="25689-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="25689-126">-Name</span></span>
<span data-ttu-id="25689-127">Określa nazwę punktu końcowego usługi Traffic Managera, który wyłączył to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25689-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="25689-128">-Refilename</span><span class="sxs-lookup"><span data-stu-id="25689-128">-ProfileName</span></span>
<span data-ttu-id="25689-129">Określa nazwę profilu usługi Traffic Manager, w którym to polecenie cmdlet wyłącza punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="25689-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="25689-130">Aby uzyskać profil, użyj polecenia cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="25689-130">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="25689-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25689-131">-ResourceGroupName</span></span>
<span data-ttu-id="25689-132">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="25689-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="25689-133">To polecenie cmdlet wyłącza punkt końcowy usługi Traffic Manager w grupie, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="25689-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="25689-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="25689-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="25689-135">Określa punkt końcowy usługi Traffic Managera, który jest wyłączony przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25689-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="25689-136">Aby uzyskać obiekt **TrafficManagerEndpoint** , użyj polecenia cmdlet Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="25689-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="25689-137">-Type</span><span class="sxs-lookup"><span data-stu-id="25689-137">-Type</span></span>
<span data-ttu-id="25689-138">Określa typ punktu końcowego, który jest dodawany przez to polecenie cmdlet do profilu usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="25689-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="25689-139">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="25689-139">Valid values are:</span></span> 

- <span data-ttu-id="25689-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="25689-140">AzureEndpoints</span></span>
- <span data-ttu-id="25689-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="25689-141">ExternalEndpoints</span></span>
- <span data-ttu-id="25689-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="25689-142">NestedEndpoints</span></span>

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

### <span data-ttu-id="25689-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="25689-143">-Confirm</span></span>
<span data-ttu-id="25689-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25689-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25689-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25689-145">-WhatIf</span></span>
<span data-ttu-id="25689-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25689-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25689-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="25689-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25689-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25689-148">CommonParameters</span></span>
<span data-ttu-id="25689-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25689-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25689-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25689-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25689-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25689-151">INPUTS</span></span>

### <span data-ttu-id="25689-152">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="25689-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="25689-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25689-153">OUTPUTS</span></span>

### <span data-ttu-id="25689-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25689-154">System.Boolean</span></span>

## <span data-ttu-id="25689-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25689-155">NOTES</span></span>

## <span data-ttu-id="25689-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25689-156">RELATED LINKS</span></span>

[<span data-ttu-id="25689-157">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="25689-157">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="25689-158">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="25689-158">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="25689-159">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="25689-159">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="25689-160">Nowe — AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="25689-160">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="25689-161">Nowe — AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="25689-161">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="25689-162">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="25689-162">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="25689-163">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="25689-163">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


