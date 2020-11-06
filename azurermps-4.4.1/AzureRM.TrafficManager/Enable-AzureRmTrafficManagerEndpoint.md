---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 64fdd0cb3c2fa31396d9e917dcd7c2e26730c755
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525473"
---
# <span data-ttu-id="923bd-101">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="923bd-101">Enable-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="923bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="923bd-102">SYNOPSIS</span></span>
<span data-ttu-id="923bd-103">Umożliwia punktowi końcowemu w profilu w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="923bd-103">Enables an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="923bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="923bd-104">SYNTAX</span></span>

### <span data-ttu-id="923bd-105">Field</span><span class="sxs-lookup"><span data-stu-id="923bd-105">Fields</span></span>
```
Enable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="923bd-106">Stream</span><span class="sxs-lookup"><span data-stu-id="923bd-106">Object</span></span>
```
Enable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="923bd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="923bd-107">DESCRIPTION</span></span>
<span data-ttu-id="923bd-108">Polecenie cmdlet **enable-AzureRmTrafficManagerEndpoint** włącza punkt końcowy w profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="923bd-108">The **Enable-AzureRmTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="923bd-109">Za pomocą operatora potoku możesz przekazać obiekt **TrafficManagerEndpoint** do tego polecenia cmdlet lub określić obiekt **TrafficManagerEndpoint** przy użyciu parametru *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="923bd-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="923bd-110">Możesz też określić nazwę i typ punktu końcowego przy użyciu parametrów *Nazwa* i *Typ* wraz z parametrami *refilename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="923bd-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="923bd-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="923bd-111">EXAMPLES</span></span>

### <span data-ttu-id="923bd-112">Przykład 1. Włączanie punktu końcowego z profilu</span><span class="sxs-lookup"><span data-stu-id="923bd-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="923bd-113">To polecenie umożliwia włączenie zewnętrznego punktu końcowego o nazwie contoso w profilu o nazwie ContosoProfile w grupie zasób ResouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="923bd-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>

### <span data-ttu-id="923bd-114">Przykład 2: Włączanie punktu końcowego za pomocą potoku</span><span class="sxs-lookup"><span data-stu-id="923bd-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerEndpoint
```

<span data-ttu-id="923bd-115">To polecenie uzyskuje zewnętrzny punkt końcowy o nazwie contoso z profilu o nazwie ContosoProfile w ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="923bd-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="923bd-116">Następnie polecenie przekazuje ten punkt końcowy do polecenia cmdlet **enable-AzureRmTrafficManagerEndpoint** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="923bd-116">The command then passes that endpoint to the **Enable-AzureRmTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="923bd-117">To polecenie cmdlet umożliwia włączenie tego punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="923bd-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="923bd-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="923bd-118">PARAMETERS</span></span>

### <span data-ttu-id="923bd-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="923bd-119">-Name</span></span>
<span data-ttu-id="923bd-120">Określa nazwę punktu końcowego usługi Traffic Managera, który włącza to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="923bd-120">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="923bd-121">-Refilename</span><span class="sxs-lookup"><span data-stu-id="923bd-121">-ProfileName</span></span>
<span data-ttu-id="923bd-122">Określa nazwę profilu usługi Traffic Manager, w którym to polecenie cmdlet włącza punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="923bd-122">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="923bd-123">Aby uzyskać profil, użyj polecenia cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="923bd-123">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="923bd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="923bd-124">-ResourceGroupName</span></span>
<span data-ttu-id="923bd-125">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="923bd-125">Specifies the name of a resource group.</span></span>
<span data-ttu-id="923bd-126">To polecenie cmdlet umożliwia włączenie punktu końcowego usługi Traffic Manager w grupie, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="923bd-126">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="923bd-127">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="923bd-127">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="923bd-128">Określa punkt końcowy usługi Traffic Managera, który włącza to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="923bd-128">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="923bd-129">Aby uzyskać obiekt **TrafficManagerEndpoint** , użyj polecenia cmdlet Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="923bd-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="923bd-130">-Type</span><span class="sxs-lookup"><span data-stu-id="923bd-130">-Type</span></span>
<span data-ttu-id="923bd-131">Określa typ punktu końcowego, który ten aplet polecenia wyłącza w profilu usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="923bd-131">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="923bd-132">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="923bd-132">Valid values are:</span></span> 

- <span data-ttu-id="923bd-133">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="923bd-133">AzureEndpoints</span></span>
- <span data-ttu-id="923bd-134">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="923bd-134">ExternalEndpoints</span></span>
- <span data-ttu-id="923bd-135">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="923bd-135">NestedEndpoints</span></span>

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

### <span data-ttu-id="923bd-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="923bd-136">-DefaultProfile</span></span>
<span data-ttu-id="923bd-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="923bd-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="923bd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="923bd-138">CommonParameters</span></span>
<span data-ttu-id="923bd-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="923bd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="923bd-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="923bd-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="923bd-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="923bd-141">INPUTS</span></span>

### <span data-ttu-id="923bd-142">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="923bd-142">TrafficManagerEndpoint</span></span>
<span data-ttu-id="923bd-143">Parametr "TrafficManagerEndpoint" akceptuje wartość typu "TrafficManagerEndpoint" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="923bd-143">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="923bd-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="923bd-144">OUTPUTS</span></span>

### <span data-ttu-id="923bd-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="923bd-145">System.Boolean</span></span>

## <span data-ttu-id="923bd-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="923bd-146">NOTES</span></span>

## <span data-ttu-id="923bd-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="923bd-147">RELATED LINKS</span></span>

[<span data-ttu-id="923bd-148">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="923bd-148">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="923bd-149">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="923bd-149">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="923bd-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="923bd-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="923bd-151">Nowe — AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="923bd-151">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="923bd-152">Nowe — AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="923bd-152">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="923bd-153">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="923bd-153">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="923bd-154">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="923bd-154">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


