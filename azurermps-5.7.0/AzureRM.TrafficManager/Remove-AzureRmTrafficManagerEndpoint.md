---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 3b3eb2fb0539be4750f4cce7dedb7cd2f26931a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544039"
---
# <span data-ttu-id="737af-101">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="737af-101">Remove-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="737af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="737af-102">SYNOPSIS</span></span>
<span data-ttu-id="737af-103">Umożliwia usunięcie punktu końcowego z usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="737af-103">Removes an endpoint from Traffic Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="737af-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="737af-104">SYNTAX</span></span>

### <span data-ttu-id="737af-105">Field</span><span class="sxs-lookup"><span data-stu-id="737af-105">Fields</span></span>
```
Remove-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="737af-106">Stream</span><span class="sxs-lookup"><span data-stu-id="737af-106">Object</span></span>
```
Remove-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="737af-107">Opis</span><span class="sxs-lookup"><span data-stu-id="737af-107">DESCRIPTION</span></span>
<span data-ttu-id="737af-108">Polecenie cmdlet **Remove-AzureRmTrafficManagerEndpoint** umożliwia usunięcie punktu końcowego z usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="737af-108">The **Remove-AzureRmTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="737af-109">To polecenie cmdlet umożliwia przekazanie każdej zmiany do usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="737af-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="737af-110">Aby usunąć wiele punktów końcowych z obiektu profilu lokalnego Menedżera ruchu i przekazać zmiany w ramach jednej operacji, użyj polecenia cmdlet Remove-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="737af-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="737af-111">Za pomocą operatora potoku możesz przekazać obiekt **TrafficManagerEndpoint** do tego polecenia cmdlet lub określić obiekt **TrafficManagerEndpoint** przy użyciu parametru *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="737af-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="737af-112">Możesz też określić nazwę i typ punktu końcowego przy użyciu parametrów *Nazwa* i *Typ* wraz z parametrami *refilename* i *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="737af-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="737af-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="737af-113">EXAMPLES</span></span>

### <span data-ttu-id="737af-114">Przykład 1: Usuwanie punktu końcowego z profilu</span><span class="sxs-lookup"><span data-stu-id="737af-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="737af-115">To polecenie usuwa punkt końcowy Azure o nazwie contoso z profilu o nazwie ContosoProfile w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="737af-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="737af-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="737af-116">PARAMETERS</span></span>

### <span data-ttu-id="737af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="737af-117">-DefaultProfile</span></span>
<span data-ttu-id="737af-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="737af-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="737af-119">-Force</span><span class="sxs-lookup"><span data-stu-id="737af-119">-Force</span></span>
<span data-ttu-id="737af-120">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="737af-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="737af-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="737af-121">-Name</span></span>
<span data-ttu-id="737af-122">Określa nazwę punktu końcowego usługi Traffic Managera, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="737af-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="737af-123">-Refilename</span><span class="sxs-lookup"><span data-stu-id="737af-123">-ProfileName</span></span>
<span data-ttu-id="737af-124">Określa nazwę profilu usługi Traffic Manager, z którego to polecenie cmdlet usuwa punkt końcowy.</span><span class="sxs-lookup"><span data-stu-id="737af-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="737af-125">Aby uzyskać profil, użyj polecenia cmdlet Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="737af-125">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="737af-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="737af-126">-ResourceGroupName</span></span>
<span data-ttu-id="737af-127">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="737af-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="737af-128">To polecenie cmdlet umożliwia usunięcie punktu końcowego usługi Traffic managera z profilu usługi Traffic Manager w grupie, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="737af-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="737af-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="737af-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="737af-130">Określa punkt końcowy usługi Traffic Managera, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="737af-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="737af-131">Aby uzyskać obiekt **TrafficManagerEndpoint** , użyj polecenia cmdlet Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="737af-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="737af-132">-Type</span><span class="sxs-lookup"><span data-stu-id="737af-132">-Type</span></span>
<span data-ttu-id="737af-133">Określa typ punktu końcowego, który jest dodawany przez to polecenie cmdlet do profilu usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="737af-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="737af-134">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="737af-134">Valid values are:</span></span> 

- <span data-ttu-id="737af-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="737af-135">AzureEndpoints</span></span>
- <span data-ttu-id="737af-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="737af-136">ExternalEndpoints</span></span>
- <span data-ttu-id="737af-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="737af-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="737af-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="737af-138">-Confirm</span></span>
<span data-ttu-id="737af-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="737af-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="737af-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="737af-140">-WhatIf</span></span>
<span data-ttu-id="737af-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="737af-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="737af-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="737af-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="737af-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="737af-143">CommonParameters</span></span>
<span data-ttu-id="737af-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="737af-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="737af-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="737af-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="737af-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="737af-146">INPUTS</span></span>

### <span data-ttu-id="737af-147">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="737af-147">TrafficManagerEndpoint</span></span>
<span data-ttu-id="737af-148">Parametr "TrafficManagerEndpoint" akceptuje wartość typu "TrafficManagerEndpoint" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="737af-148">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="737af-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="737af-149">OUTPUTS</span></span>

### <span data-ttu-id="737af-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="737af-150">System.Boolean</span></span>

## <span data-ttu-id="737af-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="737af-151">NOTES</span></span>

## <span data-ttu-id="737af-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="737af-152">RELATED LINKS</span></span>

[<span data-ttu-id="737af-153">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="737af-153">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="737af-154">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="737af-154">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="737af-155">Nowe — AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="737af-155">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="737af-156">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="737af-156">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="737af-157">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="737af-157">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


