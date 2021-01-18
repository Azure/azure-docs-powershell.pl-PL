---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 5d7ef8e2fd778b5bcaaea1413bddd85eceb0582c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501275"
---
# <span data-ttu-id="dd846-101">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd846-101">Enable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="dd846-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd846-102">SYNOPSIS</span></span>
<span data-ttu-id="dd846-103">Umożliwia punktowi końcowemu w profilu w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="dd846-103">Enables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="dd846-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd846-104">SYNTAX</span></span>

### <span data-ttu-id="dd846-105">Field</span><span class="sxs-lookup"><span data-stu-id="dd846-105">Fields</span></span>
```
Enable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd846-106">Stream</span><span class="sxs-lookup"><span data-stu-id="dd846-106">Object</span></span>
```
Enable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd846-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dd846-107">DESCRIPTION</span></span>
<span data-ttu-id="dd846-108">Polecenie cmdlet **enable-AzTrafficManagerEndpoint** włącza punkt końcowy w profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="dd846-108">The **Enable-AzTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="dd846-109">Za pomocą operatora potoku możesz przekazać obiekt **TrafficManagerEndpoint** do tego polecenia cmdlet lub określić obiekt **TrafficManagerEndpoint** przy użyciu parametru *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="dd846-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="dd846-110">Możesz też określić nazwę i typ punktu końcowego przy użyciu parametrów *Nazwa* i *Typ* wraz z parametrami *refilename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="dd846-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="dd846-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd846-111">EXAMPLES</span></span>

### <span data-ttu-id="dd846-112">Przykład 1. Włączanie punktu końcowego z profilu</span><span class="sxs-lookup"><span data-stu-id="dd846-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="dd846-113">To polecenie umożliwia włączenie zewnętrznego punktu końcowego o nazwie contoso w profilu o nazwie ContosoProfile w grupie zasób ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="dd846-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>

### <span data-ttu-id="dd846-114">Przykład 2: Włączanie punktu końcowego za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="dd846-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerEndpoint
```

<span data-ttu-id="dd846-115">To polecenie uzyskuje zewnętrzny punkt końcowy o nazwie contoso z profilu o nazwie ContosoProfile w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="dd846-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="dd846-116">Następnie polecenie przekazuje ten punkt końcowy do polecenia cmdlet **enable-AzTrafficManagerEndpoint** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="dd846-116">The command then passes that endpoint to the **Enable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="dd846-117">To polecenie cmdlet umożliwia włączenie tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="dd846-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="dd846-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd846-118">PARAMETERS</span></span>

### <span data-ttu-id="dd846-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd846-119">-DefaultProfile</span></span>
<span data-ttu-id="dd846-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd846-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd846-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dd846-121">-Name</span></span>
<span data-ttu-id="dd846-122">Określa nazwę punktu końcowego usługi Traffic Managera, który włącza to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd846-122">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="dd846-123">-Refilename</span><span class="sxs-lookup"><span data-stu-id="dd846-123">-ProfileName</span></span>
<span data-ttu-id="dd846-124">Określa nazwę profilu usługi Traffic Manager, w którym to polecenie cmdlet włącza punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="dd846-124">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="dd846-125">Aby uzyskać profil, użyj polecenia cmdlet Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="dd846-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="dd846-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd846-126">-ResourceGroupName</span></span>
<span data-ttu-id="dd846-127">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dd846-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="dd846-128">To polecenie cmdlet umożliwia włączenie punktu końcowego usługi Traffic Manager w grupie, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="dd846-128">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="dd846-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd846-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="dd846-130">Określa punkt końcowy usługi Traffic Managera, który włącza to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd846-130">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="dd846-131">Aby uzyskać obiekt **TrafficManagerEndpoint** , użyj polecenia cmdlet Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="dd846-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="dd846-132">-Type</span><span class="sxs-lookup"><span data-stu-id="dd846-132">-Type</span></span>
<span data-ttu-id="dd846-133">Określa typ punktu końcowego, który ten aplet polecenia wyłącza w profilu usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="dd846-133">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="dd846-134">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="dd846-134">Valid values are:</span></span> 

- <span data-ttu-id="dd846-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="dd846-135">AzureEndpoints</span></span>
- <span data-ttu-id="dd846-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="dd846-136">ExternalEndpoints</span></span>
- <span data-ttu-id="dd846-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="dd846-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="dd846-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd846-138">CommonParameters</span></span>
<span data-ttu-id="dd846-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd846-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd846-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd846-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd846-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd846-141">INPUTS</span></span>

### <span data-ttu-id="dd846-142">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd846-142">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="dd846-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd846-143">OUTPUTS</span></span>

### <span data-ttu-id="dd846-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd846-144">System.Boolean</span></span>

## <span data-ttu-id="dd846-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd846-145">NOTES</span></span>

## <span data-ttu-id="dd846-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd846-146">RELATED LINKS</span></span>

[<span data-ttu-id="dd846-147">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd846-147">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="dd846-148">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd846-148">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="dd846-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="dd846-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="dd846-150">Nowe — AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd846-150">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="dd846-151">Nowe — AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="dd846-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="dd846-152">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd846-152">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="dd846-153">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="dd846-153">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


