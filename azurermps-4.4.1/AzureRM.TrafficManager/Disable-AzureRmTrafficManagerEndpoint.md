---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 1481b577e248354eb2fdccbb9d6ecd450ab0cf62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554332"
---
# <span data-ttu-id="3f65d-101">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f65d-101">Disable-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="3f65d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3f65d-102">SYNOPSIS</span></span>
<span data-ttu-id="3f65d-103">Wyłącza punkt końcowy w profilu z menedżerem ruchu.</span><span class="sxs-lookup"><span data-stu-id="3f65d-103">Disables an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f65d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3f65d-104">SYNTAX</span></span>

### <span data-ttu-id="3f65d-105">Field</span><span class="sxs-lookup"><span data-stu-id="3f65d-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f65d-106">Stream</span><span class="sxs-lookup"><span data-stu-id="3f65d-106">Object</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f65d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3f65d-107">DESCRIPTION</span></span>
<span data-ttu-id="3f65d-108">Polecenie cmdlet **disable-AzureRmTrafficManagerEndpoint** wyłącza punkt końcowy w profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="3f65d-108">The **Disable-AzureRmTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="3f65d-109">Za pomocą operatora potoku możesz przekazać obiekt **TrafficManagerEndpoint** do tego polecenia cmdlet lub przekazać obiekt **TrafficManagerEndpoint** przy użyciu parametru *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="3f65d-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="3f65d-110">Możesz też określić nazwę i typ punktu końcowego przy użyciu parametrów *Nazwa* i *Typ* wraz z parametrami *refilename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="3f65d-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="3f65d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3f65d-111">EXAMPLES</span></span>

### <span data-ttu-id="3f65d-112">Przykład 1. Wyłączanie punktu końcowego według nazwy</span><span class="sxs-lookup"><span data-stu-id="3f65d-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="3f65d-113">To polecenie powoduje wyłączenie zewnętrznego punktu końcowego o nazwie contoso w profilu o nazwie ContosoProfile w grupie zasób ResouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3f65d-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="3f65d-114">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3f65d-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="3f65d-115">Przykład 2: wyłączanie punktu końcowego przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="3f65d-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerEndpoint -Force
```

<span data-ttu-id="3f65d-116">To polecenie uzyskuje zewnętrzny punkt końcowy o nazwie contoso z profilu o nazwie ContosoProfile w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3f65d-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="3f65d-117">Następnie polecenie przekazuje ten punkt końcowy do polecenia cmdlet **disable-AzureRmTrafficManagerEndpoint** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="3f65d-117">The command then passes that endpoint to the **Disable-AzureRmTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3f65d-118">To polecenie cmdlet wyłącza ten punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="3f65d-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="3f65d-119">Polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="3f65d-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="3f65d-120">W związku z tym nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="3f65d-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="3f65d-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3f65d-121">PARAMETERS</span></span>

### <span data-ttu-id="3f65d-122">-Force</span><span class="sxs-lookup"><span data-stu-id="3f65d-122">-Force</span></span>
<span data-ttu-id="3f65d-123">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3f65d-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3f65d-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3f65d-124">-Name</span></span>
<span data-ttu-id="3f65d-125">Określa nazwę punktu końcowego usługi Traffic Managera, który wyłączył to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f65d-125">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="3f65d-126">-Refilename</span><span class="sxs-lookup"><span data-stu-id="3f65d-126">-ProfileName</span></span>
<span data-ttu-id="3f65d-127">Określa nazwę profilu usługi Traffic Manager, w którym to polecenie cmdlet wyłącza punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="3f65d-127">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="3f65d-128">Aby uzyskać profil, użyj polecenia cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="3f65d-128">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="3f65d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f65d-129">-ResourceGroupName</span></span>
<span data-ttu-id="3f65d-130">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3f65d-130">Specifies the name of a resource group.</span></span>
<span data-ttu-id="3f65d-131">To polecenie cmdlet wyłącza punkt końcowy usługi Traffic Manager w grupie, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="3f65d-131">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3f65d-132">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f65d-132">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="3f65d-133">Określa punkt końcowy usługi Traffic Managera, który jest wyłączony przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f65d-133">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="3f65d-134">Aby uzyskać obiekt **TrafficManagerEndpoint** , użyj polecenia cmdlet Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="3f65d-134">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="3f65d-135">-Type</span><span class="sxs-lookup"><span data-stu-id="3f65d-135">-Type</span></span>
<span data-ttu-id="3f65d-136">Określa typ punktu końcowego, który jest dodawany przez to polecenie cmdlet do profilu usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="3f65d-136">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="3f65d-137">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="3f65d-137">Valid values are:</span></span> 

- <span data-ttu-id="3f65d-138">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="3f65d-138">AzureEndpoints</span></span>
- <span data-ttu-id="3f65d-139">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="3f65d-139">ExternalEndpoints</span></span>
- <span data-ttu-id="3f65d-140">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="3f65d-140">NestedEndpoints</span></span>

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

### <span data-ttu-id="3f65d-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3f65d-141">-Confirm</span></span>
<span data-ttu-id="3f65d-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f65d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f65d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f65d-143">-WhatIf</span></span>
<span data-ttu-id="3f65d-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f65d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f65d-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3f65d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f65d-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f65d-146">-DefaultProfile</span></span>
<span data-ttu-id="3f65d-147">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3f65d-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f65d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f65d-148">CommonParameters</span></span>
<span data-ttu-id="3f65d-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f65d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f65d-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f65d-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f65d-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f65d-151">INPUTS</span></span>

### <span data-ttu-id="3f65d-152">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f65d-152">TrafficManagerEndpoint</span></span>
<span data-ttu-id="3f65d-153">Parametr "TrafficManagerEndpoint" akceptuje wartość typu "TrafficManagerEndpoint" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="3f65d-153">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="3f65d-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3f65d-154">OUTPUTS</span></span>

### <span data-ttu-id="3f65d-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3f65d-155">System.Boolean</span></span>

## <span data-ttu-id="3f65d-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3f65d-156">NOTES</span></span>

## <span data-ttu-id="3f65d-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f65d-157">RELATED LINKS</span></span>

[<span data-ttu-id="3f65d-158">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f65d-158">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="3f65d-159">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f65d-159">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="3f65d-160">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f65d-160">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="3f65d-161">Nowe — AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f65d-161">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="3f65d-162">Nowe — AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f65d-162">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="3f65d-163">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f65d-163">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="3f65d-164">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f65d-164">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


