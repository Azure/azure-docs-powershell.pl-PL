---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
ms.openlocfilehash: 22438110dd66fbbb89e992d79f37b1e8e2e325d9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892558"
---
# <span data-ttu-id="b30e3-101">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="b30e3-101">Get-AzResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="b30e3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b30e3-102">SYNOPSIS</span></span>
<span data-ttu-id="b30e3-103">Pobiera operację wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b30e3-103">Gets the resource group deployment operation</span></span>

## <span data-ttu-id="b30e3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b30e3-104">SYNTAX</span></span>

```
Get-AzResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b30e3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b30e3-105">DESCRIPTION</span></span>
<span data-ttu-id="b30e3-106">Polecenie cmdlet **Get-AzResourceGroupDeploymentOperation** wyświetla wszystkie operacje, które były częścią wdrożenia, aby ułatwić identyfikowanie i podawanie dodatkowych informacji na temat operacji, które nie powiodły się dla określonego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="b30e3-106">The **Get-AzResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="b30e3-107">Może również pokazać odpowiedź i zawartość żądania dla każdej operacji wdrażania.</span><span class="sxs-lookup"><span data-stu-id="b30e3-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="b30e3-108">Są to te same informacje, które są dostępne w szczegółach wdrażania w portalu.</span><span class="sxs-lookup"><span data-stu-id="b30e3-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="b30e3-109">Aby uzyskać żądanie i zawartość odpowiedzi, Włącz ustawienie podczas przesyłania wdrożenia przez **nowe-AzResourceGroupDeployment**.</span><span class="sxs-lookup"><span data-stu-id="b30e3-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzResourceGroupDeployment**.</span></span>
<span data-ttu-id="b30e3-110">Może rejestrować i uwidaczniać klucze tajne, takie jak hasła używane we właściwościach zasobu lub operacjach **listKeys** , które zostaną zwrócone po pobraniu operacji wdrażania.</span><span class="sxs-lookup"><span data-stu-id="b30e3-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="b30e3-111">Aby uzyskać więcej informacji na temat tego ustawienia i sposobu jego włączania, zobacz New-AzResourceGroupDeployment i debugowanie wdrożeń szablonów ARM</span><span class="sxs-lookup"><span data-stu-id="b30e3-111">For more on this setting and how to enable it, see New-AzResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="b30e3-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b30e3-112">EXAMPLES</span></span>

### <span data-ttu-id="b30e3-113">Get1</span><span class="sxs-lookup"><span data-stu-id="b30e3-113">Get1</span></span>
```
PS C:\>Get-AzResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="b30e3-114">Pobiera operację wdrażania o nazwie "Testuj" w grupie zasób "test"</span><span class="sxs-lookup"><span data-stu-id="b30e3-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="b30e3-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b30e3-115">PARAMETERS</span></span>

### <span data-ttu-id="b30e3-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b30e3-116">-ApiVersion</span></span>
<span data-ttu-id="b30e3-117">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="b30e3-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b30e3-118">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="b30e3-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b30e3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b30e3-119">-DefaultProfile</span></span>
<span data-ttu-id="b30e3-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b30e3-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b30e3-121">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="b30e3-121">-DeploymentName</span></span>
<span data-ttu-id="b30e3-122">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="b30e3-122">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b30e3-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b30e3-123">-InformationAction</span></span>
<span data-ttu-id="b30e3-124">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="b30e3-124">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="b30e3-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b30e3-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b30e3-126">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="b30e3-126">Continue</span></span>
- <span data-ttu-id="b30e3-127">Ignorować</span><span class="sxs-lookup"><span data-stu-id="b30e3-127">Ignore</span></span>
- <span data-ttu-id="b30e3-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="b30e3-128">Inquire</span></span>
- <span data-ttu-id="b30e3-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b30e3-129">SilentlyContinue</span></span>
- <span data-ttu-id="b30e3-130">Przestaw</span><span class="sxs-lookup"><span data-stu-id="b30e3-130">Stop</span></span>
- <span data-ttu-id="b30e3-131">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="b30e3-131">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b30e3-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b30e3-132">-InformationVariable</span></span>
<span data-ttu-id="b30e3-133">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="b30e3-133">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b30e3-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="b30e3-134">-Pre</span></span>
<span data-ttu-id="b30e3-135">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="b30e3-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b30e3-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b30e3-136">-ResourceGroupName</span></span>
<span data-ttu-id="b30e3-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b30e3-137">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b30e3-138">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b30e3-138">-SubscriptionId</span></span>
<span data-ttu-id="b30e3-139">Abonament, którego należy użyć.</span><span class="sxs-lookup"><span data-stu-id="b30e3-139">The subscription to use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b30e3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b30e3-140">CommonParameters</span></span>
<span data-ttu-id="b30e3-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b30e3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b30e3-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b30e3-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b30e3-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b30e3-143">INPUTS</span></span>

## <span data-ttu-id="b30e3-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b30e3-144">OUTPUTS</span></span>

## <span data-ttu-id="b30e3-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b30e3-145">NOTES</span></span>

## <span data-ttu-id="b30e3-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b30e3-146">RELATED LINKS</span></span>
