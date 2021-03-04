---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/get-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 04764a27a6940c0bc2b5d0e6df0baad350606972
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950778"
---
# <span data-ttu-id="a0efc-101">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a0efc-101">Get-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="a0efc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0efc-102">SYNOPSIS</span></span>
<span data-ttu-id="a0efc-103">Pobiera punkt końcowy dla profilu menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="a0efc-103">Gets an endpoint for a Traffic Manager profile.</span></span>

## <span data-ttu-id="a0efc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a0efc-104">SYNTAX</span></span>

### <span data-ttu-id="a0efc-105">Pola</span><span class="sxs-lookup"><span data-stu-id="a0efc-105">Fields</span></span>
```
Get-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0efc-106">Obiekt</span><span class="sxs-lookup"><span data-stu-id="a0efc-106">Object</span></span>
```
Get-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0efc-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a0efc-107">DESCRIPTION</span></span>
<span data-ttu-id="a0efc-108">Polecenie **cmdlet Get-AzTrafficManagerEndpoint** uzyskuje punkt końcowy profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="a0efc-108">The **Get-AzTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="a0efc-109">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany do profilu za pomocą Set-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0efc-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="a0efc-110">Określ punkt końcowy za pomocą *parametrów Nazwa* *i Typ.*</span><span class="sxs-lookup"><span data-stu-id="a0efc-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="a0efc-111">Profil menedżera ruchu można określić za pomocą parametrów *ProfileName* i *ResourceGroupName* lub obiektu **TrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="a0efc-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="a0efc-112">Ewentualnie można przekazać te wartości przy użyciu potoku.</span><span class="sxs-lookup"><span data-stu-id="a0efc-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="a0efc-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a0efc-113">EXAMPLES</span></span>

### <span data-ttu-id="a0efc-114">Przykład 1. Uzyskiwanie punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="a0efc-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="a0efc-115">To polecenie pobiera punkt końcowy platformy Azure o nazwie contoso z profilu o nazwie ContosoProfile w grupie zasobów o nazwie Grupa Zasobów11, a następnie przechowuje ten obiekt w zmiennej $TrafficManagerEndpoint zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0efc-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="a0efc-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0efc-116">PARAMETERS</span></span>

### <span data-ttu-id="a0efc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0efc-117">-DefaultProfile</span></span>
<span data-ttu-id="a0efc-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0efc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0efc-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a0efc-119">-Name</span></span>
<span data-ttu-id="a0efc-120">Określa nazwę punktu końcowego menedżera ruchu, który otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0efc-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a0efc-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a0efc-121">-ProfileName</span></span>
<span data-ttu-id="a0efc-122">Określa nazwę punktu końcowego menedżera ruchu, który otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0efc-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a0efc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0efc-123">-ResourceGroupName</span></span>
<span data-ttu-id="a0efc-124">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0efc-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a0efc-125">To polecenie cmdlet pobiera punkt końcowy Menedżera ruchu w grupie, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="a0efc-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a0efc-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a0efc-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="a0efc-127">Określa punkt końcowy Menedżera ruchu, który otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0efc-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a0efc-128">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="a0efc-128">-Type</span></span>
<span data-ttu-id="a0efc-129">Określa typ punktu końcowego, który to polecenie cmdlet dodaje do profilu Menedżera ruchu.</span><span class="sxs-lookup"><span data-stu-id="a0efc-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="a0efc-130">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="a0efc-130">Valid values are:</span></span> 

- <span data-ttu-id="a0efc-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="a0efc-131">AzureEndpoints</span></span>
- <span data-ttu-id="a0efc-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="a0efc-132">ExternalEndpoints</span></span>
- <span data-ttu-id="a0efc-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="a0efc-133">NestedEndpoints</span></span>

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

### <span data-ttu-id="a0efc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0efc-134">CommonParameters</span></span>
<span data-ttu-id="a0efc-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0efc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0efc-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0efc-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0efc-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0efc-137">INPUTS</span></span>

### <span data-ttu-id="a0efc-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a0efc-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="a0efc-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0efc-139">OUTPUTS</span></span>

### <span data-ttu-id="a0efc-140">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a0efc-140">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="a0efc-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a0efc-141">NOTES</span></span>

## <span data-ttu-id="a0efc-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0efc-142">RELATED LINKS</span></span>

[<span data-ttu-id="a0efc-143">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a0efc-143">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a0efc-144">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a0efc-144">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a0efc-145">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a0efc-145">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a0efc-146">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a0efc-146">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a0efc-147">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a0efc-147">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)


