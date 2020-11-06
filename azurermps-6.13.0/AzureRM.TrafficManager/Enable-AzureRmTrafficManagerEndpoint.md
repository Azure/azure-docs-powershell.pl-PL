---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/enable-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 2556715c321ddcc3f8acbc518ddbe6a3048353af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544731"
---
# <span data-ttu-id="0c7ca-101">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0c7ca-101">Enable-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="0c7ca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0c7ca-102">SYNOPSIS</span></span>
<span data-ttu-id="0c7ca-103">Umożliwia punktowi końcowemu w profilu w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="0c7ca-103">Enables an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c7ca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0c7ca-104">SYNTAX</span></span>

### <span data-ttu-id="0c7ca-105">Field</span><span class="sxs-lookup"><span data-stu-id="0c7ca-105">Fields</span></span>
```
Enable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c7ca-106">Stream</span><span class="sxs-lookup"><span data-stu-id="0c7ca-106">Object</span></span>
```
Enable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c7ca-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0c7ca-107">DESCRIPTION</span></span>
<span data-ttu-id="0c7ca-108">Polecenie cmdlet **enable-AzureRmTrafficManagerEndpoint** włącza punkt końcowy w profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="0c7ca-108">The **Enable-AzureRmTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="0c7ca-109">Za pomocą operatora potoku możesz przekazać obiekt **TrafficManagerEndpoint** do tego polecenia cmdlet lub określić obiekt **TrafficManagerEndpoint** przy użyciu parametru *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="0c7ca-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="0c7ca-110">Możesz też określić nazwę i typ punktu końcowego przy użyciu parametrów *Nazwa* i *Typ* wraz z parametrami *refilename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="0c7ca-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="0c7ca-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0c7ca-111">EXAMPLES</span></span>

### <span data-ttu-id="0c7ca-112">Przykład 1. Włączanie punktu końcowego z profilu</span><span class="sxs-lookup"><span data-stu-id="0c7ca-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="0c7ca-113">To polecenie umożliwia włączenie zewnętrznego punktu końcowego o nazwie contoso w profilu o nazwie ContosoProfile w grupie zasób ResouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0c7ca-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>

### <span data-ttu-id="0c7ca-114">Przykład 2: Włączanie punktu końcowego za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="0c7ca-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerEndpoint
```

<span data-ttu-id="0c7ca-115">To polecenie uzyskuje zewnętrzny punkt końcowy o nazwie contoso z profilu o nazwie ContosoProfile w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0c7ca-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="0c7ca-116">Następnie polecenie przekazuje ten punkt końcowy do polecenia cmdlet **enable-AzureRmTrafficManagerEndpoint** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="0c7ca-116">The command then passes that endpoint to the **Enable-AzureRmTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0c7ca-117">To polecenie cmdlet umożliwia włączenie tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="0c7ca-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="0c7ca-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c7ca-118">PARAMETERS</span></span>

### <span data-ttu-id="0c7ca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c7ca-119">-DefaultProfile</span></span>
<span data-ttu-id="0c7ca-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c7ca-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c7ca-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0c7ca-121">-Name</span></span>
<span data-ttu-id="0c7ca-122">Określa nazwę punktu końcowego usługi Traffic Managera, który włącza to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c7ca-122">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="0c7ca-123">-Refilename</span><span class="sxs-lookup"><span data-stu-id="0c7ca-123">-ProfileName</span></span>
<span data-ttu-id="0c7ca-124">Określa nazwę profilu usługi Traffic Manager, w którym to polecenie cmdlet włącza punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="0c7ca-124">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="0c7ca-125">Aby uzyskać profil, użyj polecenia cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="0c7ca-125">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="0c7ca-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c7ca-126">-ResourceGroupName</span></span>
<span data-ttu-id="0c7ca-127">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0c7ca-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="0c7ca-128">To polecenie cmdlet umożliwia włączenie punktu końcowego usługi Traffic Manager w grupie, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="0c7ca-128">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0c7ca-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0c7ca-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="0c7ca-130">Określa punkt końcowy usługi Traffic Managera, który włącza to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c7ca-130">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="0c7ca-131">Aby uzyskać obiekt **TrafficManagerEndpoint** , użyj polecenia cmdlet Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0c7ca-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="0c7ca-132">-Type</span><span class="sxs-lookup"><span data-stu-id="0c7ca-132">-Type</span></span>
<span data-ttu-id="0c7ca-133">Określa typ punktu końcowego, który ten aplet polecenia wyłącza w profilu usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="0c7ca-133">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="0c7ca-134">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="0c7ca-134">Valid values are:</span></span> 

- <span data-ttu-id="0c7ca-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="0c7ca-135">AzureEndpoints</span></span>
- <span data-ttu-id="0c7ca-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="0c7ca-136">ExternalEndpoints</span></span>
- <span data-ttu-id="0c7ca-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="0c7ca-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="0c7ca-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c7ca-138">CommonParameters</span></span>
<span data-ttu-id="0c7ca-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c7ca-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c7ca-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c7ca-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c7ca-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c7ca-141">INPUTS</span></span>

### <span data-ttu-id="0c7ca-142">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0c7ca-142">TrafficManagerEndpoint</span></span>
<span data-ttu-id="0c7ca-143">Parametr "TrafficManagerEndpoint" akceptuje wartość typu "TrafficManagerEndpoint" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="0c7ca-143">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="0c7ca-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0c7ca-144">OUTPUTS</span></span>

### <span data-ttu-id="0c7ca-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0c7ca-145">System.Boolean</span></span>

## <span data-ttu-id="0c7ca-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0c7ca-146">NOTES</span></span>

## <span data-ttu-id="0c7ca-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c7ca-147">RELATED LINKS</span></span>

[<span data-ttu-id="0c7ca-148">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0c7ca-148">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="0c7ca-149">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0c7ca-149">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="0c7ca-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0c7ca-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="0c7ca-151">Nowe — AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0c7ca-151">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="0c7ca-152">Nowe — AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0c7ca-152">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="0c7ca-153">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0c7ca-153">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="0c7ca-154">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0c7ca-154">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


