---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 488643c8f977fb59af0f5b73c9388e65b3425c1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549492"
---
# <span data-ttu-id="d3ddf-101">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3ddf-101">Get-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="d3ddf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d3ddf-102">SYNOPSIS</span></span>
<span data-ttu-id="d3ddf-103">Pobiera punkt końcowy profilu usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="d3ddf-103">Gets an endpoint for a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3ddf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d3ddf-104">SYNTAX</span></span>

### <span data-ttu-id="d3ddf-105">Field</span><span class="sxs-lookup"><span data-stu-id="d3ddf-105">Fields</span></span>
```
Get-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3ddf-106">Stream</span><span class="sxs-lookup"><span data-stu-id="d3ddf-106">Object</span></span>
```
Get-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3ddf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d3ddf-107">DESCRIPTION</span></span>
<span data-ttu-id="d3ddf-108">Polecenie cmdlet **Get-AzureRmTrafficManagerEndpoint** Pobiera punkt końcowy dla profilu usługi Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="d3ddf-108">The **Get-AzureRmTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="d3ddf-109">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany w profilu przy użyciu polecenia cmdlet Set-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d3ddf-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="d3ddf-110">Określ punkt końcowy przy użyciu parametrów *Nazwa* i *Typ* .</span><span class="sxs-lookup"><span data-stu-id="d3ddf-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="d3ddf-111">Możesz określić profil usługi Traffic managera przy użyciu parametru *refilename* i *ResourceGroupName* albo określając obiekt **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="d3ddf-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="d3ddf-112">Możesz również przekazać tę wartość, korzystając z potoku.</span><span class="sxs-lookup"><span data-stu-id="d3ddf-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="d3ddf-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d3ddf-113">EXAMPLES</span></span>

### <span data-ttu-id="d3ddf-114">Przykład 1: uzyskiwanie punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="d3ddf-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="d3ddf-115">To polecenie pobiera punkt końcowy Azure o nazwie contoso z profilu o nazwie ContosoProfile w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d3ddf-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="d3ddf-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d3ddf-116">PARAMETERS</span></span>

### <span data-ttu-id="d3ddf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3ddf-117">-DefaultProfile</span></span>
<span data-ttu-id="d3ddf-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d3ddf-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3ddf-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d3ddf-119">-Name</span></span>
<span data-ttu-id="d3ddf-120">Określa nazwę punktu końcowego usługi Traffic Managera, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3ddf-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d3ddf-121">-Refilename</span><span class="sxs-lookup"><span data-stu-id="d3ddf-121">-ProfileName</span></span>
<span data-ttu-id="d3ddf-122">Określa nazwę punktu końcowego usługi Traffic Managera, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3ddf-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d3ddf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3ddf-123">-ResourceGroupName</span></span>
<span data-ttu-id="d3ddf-124">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d3ddf-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="d3ddf-125">To polecenie cmdlet umożliwia pobieranie punktu końcowego usługi Traffic Manager w grupie, w którym ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="d3ddf-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d3ddf-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3ddf-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="d3ddf-127">Określa punkt końcowy usługi Traffic Managera, który jest pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3ddf-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d3ddf-128">-Type</span><span class="sxs-lookup"><span data-stu-id="d3ddf-128">-Type</span></span>
<span data-ttu-id="d3ddf-129">Określa typ punktu końcowego, który jest dodawany przez to polecenie cmdlet do profilu usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="d3ddf-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="d3ddf-130">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="d3ddf-130">Valid values are:</span></span> 

- <span data-ttu-id="d3ddf-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="d3ddf-131">AzureEndpoints</span></span>
- <span data-ttu-id="d3ddf-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="d3ddf-132">ExternalEndpoints</span></span>
- <span data-ttu-id="d3ddf-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="d3ddf-133">NestedEndpoints</span></span>

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

### <span data-ttu-id="d3ddf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3ddf-134">CommonParameters</span></span>
<span data-ttu-id="d3ddf-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3ddf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3ddf-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3ddf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3ddf-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3ddf-137">INPUTS</span></span>

### <span data-ttu-id="d3ddf-138">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3ddf-138">TrafficManagerEndpoint</span></span>
<span data-ttu-id="d3ddf-139">Parametr "TrafficManagerEndpoint" akceptuje wartość typu "TrafficManagerEndpoint" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="d3ddf-139">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="d3ddf-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d3ddf-140">OUTPUTS</span></span>

### <span data-ttu-id="d3ddf-141">Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3ddf-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="d3ddf-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d3ddf-142">NOTES</span></span>

## <span data-ttu-id="d3ddf-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3ddf-143">RELATED LINKS</span></span>

[<span data-ttu-id="d3ddf-144">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3ddf-144">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="d3ddf-145">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3ddf-145">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="d3ddf-146">Nowe — AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3ddf-146">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="d3ddf-147">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3ddf-147">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="d3ddf-148">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d3ddf-148">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)

