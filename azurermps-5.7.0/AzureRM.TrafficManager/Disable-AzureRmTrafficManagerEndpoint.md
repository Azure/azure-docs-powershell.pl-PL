---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/disable-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 13b798da7b35a4721b35d2375cf4e25bb47fbb98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717674"
---
# <span data-ttu-id="6062e-101">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6062e-101">Disable-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="6062e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6062e-102">SYNOPSIS</span></span>
<span data-ttu-id="6062e-103">Wyłącza punkt końcowy w profilu z menedżerem ruchu.</span><span class="sxs-lookup"><span data-stu-id="6062e-103">Disables an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6062e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6062e-104">SYNTAX</span></span>

### <span data-ttu-id="6062e-105">Field</span><span class="sxs-lookup"><span data-stu-id="6062e-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6062e-106">Stream</span><span class="sxs-lookup"><span data-stu-id="6062e-106">Object</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6062e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6062e-107">DESCRIPTION</span></span>
<span data-ttu-id="6062e-108">Polecenie cmdlet **disable-AzureRmTrafficManagerEndpoint** wyłącza punkt końcowy w profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="6062e-108">The **Disable-AzureRmTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="6062e-109">Za pomocą operatora potoku możesz przekazać obiekt **TrafficManagerEndpoint** do tego polecenia cmdlet lub przekazać obiekt **TrafficManagerEndpoint** przy użyciu parametru *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="6062e-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="6062e-110">Możesz też określić nazwę i typ punktu końcowego przy użyciu parametrów *Nazwa* i *Typ* wraz z parametrami *refilename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="6062e-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="6062e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6062e-111">EXAMPLES</span></span>

### <span data-ttu-id="6062e-112">Przykład 1. Wyłączanie punktu końcowego według nazwy</span><span class="sxs-lookup"><span data-stu-id="6062e-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="6062e-113">To polecenie powoduje wyłączenie zewnętrznego punktu końcowego o nazwie contoso w profilu o nazwie ContosoProfile w grupie zasób ResouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="6062e-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="6062e-114">Polecenie wyświetli monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6062e-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="6062e-115">Przykład 2: wyłączanie punktu końcowego przy użyciu rurociągu</span><span class="sxs-lookup"><span data-stu-id="6062e-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerEndpoint -Force
```

<span data-ttu-id="6062e-116">To polecenie uzyskuje zewnętrzny punkt końcowy o nazwie contoso z profilu o nazwie ContosoProfile w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="6062e-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="6062e-117">Następnie polecenie przekazuje ten punkt końcowy do polecenia cmdlet **disable-AzureRmTrafficManagerEndpoint** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="6062e-117">The command then passes that endpoint to the **Disable-AzureRmTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6062e-118">To polecenie cmdlet wyłącza ten punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="6062e-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="6062e-119">Polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="6062e-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="6062e-120">W związku z tym nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6062e-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6062e-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6062e-121">PARAMETERS</span></span>

### <span data-ttu-id="6062e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6062e-122">-DefaultProfile</span></span>
<span data-ttu-id="6062e-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6062e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6062e-124">-Force</span><span class="sxs-lookup"><span data-stu-id="6062e-124">-Force</span></span>
<span data-ttu-id="6062e-125">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6062e-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6062e-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6062e-126">-Name</span></span>
<span data-ttu-id="6062e-127">Określa nazwę punktu końcowego usługi Traffic Managera, który wyłączył to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6062e-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6062e-128">-Refilename</span><span class="sxs-lookup"><span data-stu-id="6062e-128">-ProfileName</span></span>
<span data-ttu-id="6062e-129">Określa nazwę profilu usługi Traffic Manager, w którym to polecenie cmdlet wyłącza punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="6062e-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="6062e-130">Aby uzyskać profil, użyj polecenia cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="6062e-130">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6062e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6062e-131">-ResourceGroupName</span></span>
<span data-ttu-id="6062e-132">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6062e-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="6062e-133">To polecenie cmdlet wyłącza punkt końcowy usługi Traffic Manager w grupie, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="6062e-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6062e-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6062e-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="6062e-135">Określa punkt końcowy usługi Traffic Managera, który jest wyłączony przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6062e-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="6062e-136">Aby uzyskać obiekt **TrafficManagerEndpoint** , użyj polecenia cmdlet Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6062e-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: TrafficManagerEndpoint
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6062e-137">-Type</span><span class="sxs-lookup"><span data-stu-id="6062e-137">-Type</span></span>
<span data-ttu-id="6062e-138">Określa typ punktu końcowego, który jest dodawany przez to polecenie cmdlet do profilu usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="6062e-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="6062e-139">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="6062e-139">Valid values are:</span></span> 

- <span data-ttu-id="6062e-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="6062e-140">AzureEndpoints</span></span>
- <span data-ttu-id="6062e-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="6062e-141">ExternalEndpoints</span></span>
- <span data-ttu-id="6062e-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="6062e-142">NestedEndpoints</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6062e-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6062e-143">-Confirm</span></span>
<span data-ttu-id="6062e-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6062e-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6062e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6062e-145">-WhatIf</span></span>
<span data-ttu-id="6062e-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6062e-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6062e-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6062e-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6062e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6062e-148">CommonParameters</span></span>
<span data-ttu-id="6062e-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6062e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6062e-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6062e-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6062e-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6062e-151">INPUTS</span></span>

### <span data-ttu-id="6062e-152">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6062e-152">TrafficManagerEndpoint</span></span>
<span data-ttu-id="6062e-153">Parametr "TrafficManagerEndpoint" akceptuje wartość typu "TrafficManagerEndpoint" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="6062e-153">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="6062e-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6062e-154">OUTPUTS</span></span>

### <span data-ttu-id="6062e-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6062e-155">System.Boolean</span></span>

## <span data-ttu-id="6062e-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6062e-156">NOTES</span></span>

## <span data-ttu-id="6062e-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6062e-157">RELATED LINKS</span></span>

[<span data-ttu-id="6062e-158">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6062e-158">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="6062e-159">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6062e-159">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="6062e-160">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6062e-160">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="6062e-161">Nowe — AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6062e-161">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="6062e-162">Nowe — AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6062e-162">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="6062e-163">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6062e-163">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="6062e-164">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6062e-164">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


