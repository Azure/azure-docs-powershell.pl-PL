---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
ms.openlocfilehash: a67bfb43aa4cafe4b9c7f20e6ff757989deee5d6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871840"
---
# <span data-ttu-id="57186-101">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="57186-101">Get-AzResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="57186-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57186-102">SYNOPSIS</span></span>
<span data-ttu-id="57186-103">Pobiera operację wdrożenia grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="57186-103">Gets the resource group deployment operation</span></span>

## <span data-ttu-id="57186-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57186-104">SYNTAX</span></span>

```
Get-AzResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57186-105">Opis</span><span class="sxs-lookup"><span data-stu-id="57186-105">DESCRIPTION</span></span>
<span data-ttu-id="57186-106">Polecenie cmdlet **Get-AzResourceGroupDeploymentOperation** wyświetla wszystkie operacje, które były częścią wdrożenia, aby ułatwić identyfikowanie i podawanie dodatkowych informacji na temat operacji, które nie powiodły się dla określonego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="57186-106">The **Get-AzResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="57186-107">Może również pokazać odpowiedź i zawartość żądania dla każdej operacji wdrażania.</span><span class="sxs-lookup"><span data-stu-id="57186-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="57186-108">Są to te same informacje, które są dostępne w szczegółach wdrażania w portalu.</span><span class="sxs-lookup"><span data-stu-id="57186-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="57186-109">Aby uzyskać żądanie i zawartość odpowiedzi, Włącz ustawienie podczas przesyłania wdrożenia przez **nowe-AzResourceGroupDeployment**.</span><span class="sxs-lookup"><span data-stu-id="57186-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzResourceGroupDeployment**.</span></span>
<span data-ttu-id="57186-110">Może rejestrować i uwidaczniać klucze tajne, takie jak hasła używane we właściwościach zasobu lub operacjach **listKeys** , które zostaną zwrócone po pobraniu operacji wdrażania.</span><span class="sxs-lookup"><span data-stu-id="57186-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="57186-111">Aby uzyskać więcej informacji na temat tego ustawienia i sposobu jego włączania, zobacz New-AzResourceGroupDeployment i debugowanie wdrożeń szablonów ARM</span><span class="sxs-lookup"><span data-stu-id="57186-111">For more on this setting and how to enable it, see New-AzResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="57186-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57186-112">EXAMPLES</span></span>

### <span data-ttu-id="57186-113">Get1</span><span class="sxs-lookup"><span data-stu-id="57186-113">Get1</span></span>
```
PS C:\>Get-AzResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="57186-114">Pobiera operację wdrażania o nazwie "Testuj" w grupie zasób "test"</span><span class="sxs-lookup"><span data-stu-id="57186-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="57186-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57186-115">PARAMETERS</span></span>

### <span data-ttu-id="57186-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="57186-116">-ApiVersion</span></span>
<span data-ttu-id="57186-117">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="57186-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="57186-118">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="57186-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="57186-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57186-119">-DefaultProfile</span></span>
<span data-ttu-id="57186-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="57186-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57186-121">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="57186-121">-DeploymentName</span></span>
<span data-ttu-id="57186-122">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="57186-122">The deployment name.</span></span>

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

### <span data-ttu-id="57186-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="57186-123">-Pre</span></span>
<span data-ttu-id="57186-124">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="57186-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="57186-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57186-125">-ResourceGroupName</span></span>
<span data-ttu-id="57186-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="57186-126">The resource group name.</span></span>

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

### <span data-ttu-id="57186-127">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="57186-127">-SubscriptionId</span></span>
<span data-ttu-id="57186-128">Abonament, którego należy użyć.</span><span class="sxs-lookup"><span data-stu-id="57186-128">The subscription to use.</span></span>

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

### <span data-ttu-id="57186-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57186-129">CommonParameters</span></span>
<span data-ttu-id="57186-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57186-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57186-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57186-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57186-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57186-132">INPUTS</span></span>

### <span data-ttu-id="57186-133">System. String</span><span class="sxs-lookup"><span data-stu-id="57186-133">System.String</span></span>

### <span data-ttu-id="57186-134">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="57186-134">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="57186-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57186-135">OUTPUTS</span></span>

### <span data-ttu-id="57186-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="57186-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="57186-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57186-137">NOTES</span></span>

## <span data-ttu-id="57186-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57186-138">RELATED LINKS</span></span>
