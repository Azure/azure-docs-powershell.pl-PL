---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeploymentOperation.md
ms.openlocfilehash: 557aa312200a2e5c49e33f8a176079ee4b27b629
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542356"
---
# <span data-ttu-id="8ba22-101">Get-AzureRmResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8ba22-101">Get-AzureRmResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="8ba22-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ba22-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba22-103">Pobiera operację wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8ba22-103">Gets the resource group deployment operation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ba22-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ba22-104">SYNTAX</span></span>

```
Get-AzureRmResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8ba22-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8ba22-105">DESCRIPTION</span></span>
<span data-ttu-id="8ba22-106">Polecenie cmdlet **Get-AzureRmResourceGroupDeploymentOperation** wyświetla wszystkie operacje, które były częścią wdrożenia, aby ułatwić identyfikowanie i podawanie dodatkowych informacji na temat operacji, które nie powiodły się dla określonego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="8ba22-106">The **Get-AzureRmResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="8ba22-107">Może również pokazać odpowiedź i zawartość żądania dla każdej operacji wdrażania.</span><span class="sxs-lookup"><span data-stu-id="8ba22-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="8ba22-108">Są to te same informacje, które są dostępne w szczegółach wdrażania w portalu.</span><span class="sxs-lookup"><span data-stu-id="8ba22-108">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="8ba22-109">Aby uzyskać żądanie i zawartość odpowiedzi, Włącz ustawienie podczas przesyłania wdrożenia przez **nowe-AzureRmResourceGroupDeployment**.</span><span class="sxs-lookup"><span data-stu-id="8ba22-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzureRmResourceGroupDeployment**.</span></span>
<span data-ttu-id="8ba22-110">Może rejestrować i uwidaczniać klucze tajne, takie jak hasła używane we właściwościach zasobu lub operacjach **listKeys** , które zostaną zwrócone po pobraniu operacji wdrażania.</span><span class="sxs-lookup"><span data-stu-id="8ba22-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="8ba22-111">Aby uzyskać więcej informacji na temat tego ustawienia i sposobu jego włączania, zobacz New-AzureRmResourceGroupDeployment i debugowanie wdrożeń szablonów ARM</span><span class="sxs-lookup"><span data-stu-id="8ba22-111">For more on this setting and how to enable it, see New-AzureRmResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="8ba22-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ba22-112">EXAMPLES</span></span>

### <span data-ttu-id="8ba22-113">Get1</span><span class="sxs-lookup"><span data-stu-id="8ba22-113">Get1</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="8ba22-114">Pobiera operację wdrażania o nazwie "Testuj" w grupie zasób "test"</span><span class="sxs-lookup"><span data-stu-id="8ba22-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="8ba22-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ba22-115">PARAMETERS</span></span>

### <span data-ttu-id="8ba22-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8ba22-116">-ApiVersion</span></span>
<span data-ttu-id="8ba22-117">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="8ba22-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="8ba22-118">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="8ba22-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba22-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ba22-119">-DefaultProfile</span></span>
<span data-ttu-id="8ba22-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8ba22-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ba22-121">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="8ba22-121">-DeploymentName</span></span>
<span data-ttu-id="8ba22-122">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="8ba22-122">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba22-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8ba22-123">-InformationAction</span></span>
<span data-ttu-id="8ba22-124">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="8ba22-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8ba22-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8ba22-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8ba22-126">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="8ba22-126">Continue</span></span>
- <span data-ttu-id="8ba22-127">Ignorować</span><span class="sxs-lookup"><span data-stu-id="8ba22-127">Ignore</span></span>
- <span data-ttu-id="8ba22-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="8ba22-128">Inquire</span></span>
- <span data-ttu-id="8ba22-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8ba22-129">SilentlyContinue</span></span>
- <span data-ttu-id="8ba22-130">Przestaw</span><span class="sxs-lookup"><span data-stu-id="8ba22-130">Stop</span></span>
- <span data-ttu-id="8ba22-131">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="8ba22-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba22-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8ba22-132">-InformationVariable</span></span>
<span data-ttu-id="8ba22-133">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="8ba22-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba22-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="8ba22-134">-Pre</span></span>
<span data-ttu-id="8ba22-135">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="8ba22-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8ba22-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ba22-136">-ResourceGroupName</span></span>
<span data-ttu-id="8ba22-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8ba22-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba22-138">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8ba22-138">-SubscriptionId</span></span>
<span data-ttu-id="8ba22-139">Abonament, którego należy użyć.</span><span class="sxs-lookup"><span data-stu-id="8ba22-139">The subscription to use.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba22-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba22-140">CommonParameters</span></span>
<span data-ttu-id="8ba22-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ba22-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ba22-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ba22-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba22-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ba22-143">INPUTS</span></span>

### <span data-ttu-id="8ba22-144">Wiodąc</span><span class="sxs-lookup"><span data-stu-id="8ba22-144">Guid</span></span>
<span data-ttu-id="8ba22-145">Parametr "subskrypcji" akceptuje wartość typu "GUID" z procesu.</span><span class="sxs-lookup"><span data-stu-id="8ba22-145">Parameter 'SubscriptionId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="8ba22-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ba22-146">OUTPUTS</span></span>

### <span data-ttu-id="8ba22-147">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8ba22-147">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8ba22-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ba22-148">NOTES</span></span>

## <span data-ttu-id="8ba22-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ba22-149">RELATED LINKS</span></span>
