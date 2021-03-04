---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/enable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 5ab6ba03b9803cc8726eff458776f8ee40d48793
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950794"
---
# <span data-ttu-id="85882-101">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="85882-101">Enable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="85882-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85882-102">SYNOPSIS</span></span>
<span data-ttu-id="85882-103">Włącza punkt końcowy w profilu Menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="85882-103">Enables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="85882-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="85882-104">SYNTAX</span></span>

### <span data-ttu-id="85882-105">Pola</span><span class="sxs-lookup"><span data-stu-id="85882-105">Fields</span></span>
```
Enable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85882-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="85882-106">Object</span></span>
```
Enable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85882-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="85882-107">DESCRIPTION</span></span>
<span data-ttu-id="85882-108">Polecenie **cmdlet Enable-AzTrafficManagerEndpoint** umożliwia obsługę punktu końcowego w profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="85882-108">The **Enable-AzTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="85882-109">Za pomocą operatora potoku można przekazać obiekt **TrafficManagerEndpoint** do tego polecenia cmdlet lub określić obiekt **TrafficManagerEndpoint** przy użyciu *parametru TrafficManagerEndpoint.*</span><span class="sxs-lookup"><span data-stu-id="85882-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="85882-110">Możesz również określić nazwę punktu końcowego i typ, używając parametrów *Name* (Nazwa) i *Type* (Typ) wraz z parametrami *ProfileName* (Nazwa_profilu) i *ResourceGroupName (Nazwa* Grupy Zasobów).</span><span class="sxs-lookup"><span data-stu-id="85882-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="85882-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="85882-111">EXAMPLES</span></span>

### <span data-ttu-id="85882-112">Przykład 1. Włączanie punktu końcowego z profilu</span><span class="sxs-lookup"><span data-stu-id="85882-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="85882-113">To polecenie włącza zewnętrzny punkt końcowy o nazwie contoso w profilu o nazwie ContosoProfile w grupie zasobów ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="85882-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>

### <span data-ttu-id="85882-114">Przykład 2. Włączanie punktu końcowego przy użyciu potoku</span><span class="sxs-lookup"><span data-stu-id="85882-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerEndpoint
```

<span data-ttu-id="85882-115">To polecenie pobiera zewnętrzny punkt końcowy o nazwie Contoso z profilu o nazwie ContosoProfile w grupie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="85882-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="85882-116">Następnie polecenie przekazuje ten punkt końcowy do polecenia cmdlet **Enable-AzTrafficManagerEndpoint** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="85882-116">The command then passes that endpoint to the **Enable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="85882-117">To polecenie cmdlet umożliwia korzystanie z tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="85882-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="85882-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85882-118">PARAMETERS</span></span>

### <span data-ttu-id="85882-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85882-119">-DefaultProfile</span></span>
<span data-ttu-id="85882-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="85882-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85882-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="85882-121">-Name</span></span>
<span data-ttu-id="85882-122">Określa nazwę punktu końcowego menedżera ruchu, który jest włączany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85882-122">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="85882-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="85882-123">-ProfileName</span></span>
<span data-ttu-id="85882-124">Określa nazwę profilu menedżera ruchu, w którym to polecenie cmdlet włącza punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="85882-124">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="85882-125">Aby uzyskać profil, użyj polecenia cmdlet Get-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85882-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="85882-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85882-126">-ResourceGroupName</span></span>
<span data-ttu-id="85882-127">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="85882-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="85882-128">To polecenie cmdlet umożliwia włączenie punktu końcowego Menedżera ruchu w grupie, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="85882-128">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="85882-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="85882-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="85882-130">Określa punkt końcowy Menedżera ruchu, który włącza to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85882-130">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="85882-131">Aby uzyskać obiekt **TrafficManagerEndpoint,** użyj Get-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85882-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="85882-132">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="85882-132">-Type</span></span>
<span data-ttu-id="85882-133">Określa typ punktu końcowego, który to polecenie cmdlet wyłącza w profilu Menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="85882-133">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="85882-134">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="85882-134">Valid values are:</span></span> 

- <span data-ttu-id="85882-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="85882-135">AzureEndpoints</span></span>
- <span data-ttu-id="85882-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="85882-136">ExternalEndpoints</span></span>
- <span data-ttu-id="85882-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="85882-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="85882-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85882-138">CommonParameters</span></span>
<span data-ttu-id="85882-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85882-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85882-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85882-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85882-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85882-141">INPUTS</span></span>

### <span data-ttu-id="85882-142">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="85882-142">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="85882-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85882-143">OUTPUTS</span></span>

### <span data-ttu-id="85882-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="85882-144">System.Boolean</span></span>

## <span data-ttu-id="85882-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="85882-145">NOTES</span></span>

## <span data-ttu-id="85882-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85882-146">RELATED LINKS</span></span>

[<span data-ttu-id="85882-147">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="85882-147">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="85882-148">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="85882-148">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="85882-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="85882-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="85882-150">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="85882-150">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="85882-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="85882-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="85882-152">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="85882-152">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="85882-153">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="85882-153">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


