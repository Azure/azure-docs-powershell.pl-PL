---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 3a24063e7b3d74704aa8d409b5bec6d87e35d095
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326177"
---
# <span data-ttu-id="5f59f-101">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5f59f-101">Get-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="5f59f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f59f-102">SYNOPSIS</span></span>
<span data-ttu-id="5f59f-103">Pobiera punkt końcowy profilu usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="5f59f-103">Gets an endpoint for a Traffic Manager profile.</span></span>

## <span data-ttu-id="5f59f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f59f-104">SYNTAX</span></span>

### <span data-ttu-id="5f59f-105">Field</span><span class="sxs-lookup"><span data-stu-id="5f59f-105">Fields</span></span>
```
Get-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f59f-106">Stream</span><span class="sxs-lookup"><span data-stu-id="5f59f-106">Object</span></span>
```
Get-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f59f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5f59f-107">DESCRIPTION</span></span>
<span data-ttu-id="5f59f-108">Polecenie cmdlet **Get-AzTrafficManagerEndpoint** Pobiera punkt końcowy dla profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="5f59f-108">The **Get-AzTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="5f59f-109">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany w profilu przy użyciu polecenia cmdlet Set-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5f59f-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="5f59f-110">Określ punkt końcowy przy użyciu parametrów *Nazwa* i *Typ* .</span><span class="sxs-lookup"><span data-stu-id="5f59f-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="5f59f-111">Możesz określić profil usługi Traffic managera przy użyciu parametru *refilename* i *ResourceGroupName* albo określając obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="5f59f-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="5f59f-112">Możesz również przekazać tę wartość, korzystając z potoku.</span><span class="sxs-lookup"><span data-stu-id="5f59f-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="5f59f-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f59f-113">EXAMPLES</span></span>

### <span data-ttu-id="5f59f-114">Przykład 1: uzyskiwanie punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="5f59f-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="5f59f-115">To polecenie pobiera punkt końcowy Azure o nazwie contoso z profilu o nazwie ContosoProfile w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5f59f-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="5f59f-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f59f-116">PARAMETERS</span></span>

### <span data-ttu-id="5f59f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f59f-117">-DefaultProfile</span></span>
<span data-ttu-id="5f59f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f59f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f59f-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5f59f-119">-Name</span></span>
<span data-ttu-id="5f59f-120">Określa nazwę punktu końcowego usługi Traffic Managera, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f59f-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5f59f-121">-Refilename</span><span class="sxs-lookup"><span data-stu-id="5f59f-121">-ProfileName</span></span>
<span data-ttu-id="5f59f-122">Określa nazwę punktu końcowego usługi Traffic Managera, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f59f-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5f59f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f59f-123">-ResourceGroupName</span></span>
<span data-ttu-id="5f59f-124">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5f59f-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="5f59f-125">To polecenie cmdlet umożliwia pobieranie punktu końcowego usługi Traffic Manager w grupie, w którym ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="5f59f-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5f59f-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5f59f-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="5f59f-127">Określa punkt końcowy usługi Traffic Managera, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f59f-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5f59f-128">-Type</span><span class="sxs-lookup"><span data-stu-id="5f59f-128">-Type</span></span>
<span data-ttu-id="5f59f-129">Określa typ punktu końcowego, który jest dodawany przez to polecenie cmdlet do profilu usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="5f59f-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="5f59f-130">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="5f59f-130">Valid values are:</span></span> 

- <span data-ttu-id="5f59f-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="5f59f-131">AzureEndpoints</span></span>
- <span data-ttu-id="5f59f-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="5f59f-132">ExternalEndpoints</span></span>
- <span data-ttu-id="5f59f-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="5f59f-133">NestedEndpoints</span></span>

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

### <span data-ttu-id="5f59f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f59f-134">CommonParameters</span></span>
<span data-ttu-id="5f59f-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f59f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f59f-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f59f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f59f-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f59f-137">INPUTS</span></span>

### <span data-ttu-id="5f59f-138">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5f59f-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="5f59f-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f59f-139">OUTPUTS</span></span>

### <span data-ttu-id="5f59f-140">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5f59f-140">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="5f59f-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f59f-141">NOTES</span></span>

## <span data-ttu-id="5f59f-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f59f-142">RELATED LINKS</span></span>

[<span data-ttu-id="5f59f-143">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5f59f-143">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="5f59f-144">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5f59f-144">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="5f59f-145">Nowe — AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5f59f-145">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="5f59f-146">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5f59f-146">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="5f59f-147">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5f59f-147">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)


