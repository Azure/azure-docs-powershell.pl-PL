---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: 809e7e82948d155ad73a80cbd430499d5372b644
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708412"
---
# <span data-ttu-id="45125-101">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="45125-101">Get-AzDeploymentOperation</span></span>

## <span data-ttu-id="45125-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45125-102">SYNOPSIS</span></span>
<span data-ttu-id="45125-103">Operacja pobierania wdrożenia</span><span class="sxs-lookup"><span data-stu-id="45125-103">Get deployment operation</span></span>

## <span data-ttu-id="45125-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45125-104">SYNTAX</span></span>

### <span data-ttu-id="45125-105">GetByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="45125-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45125-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="45125-106">GetByDeploymentObject</span></span>
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45125-107">Opis</span><span class="sxs-lookup"><span data-stu-id="45125-107">DESCRIPTION</span></span>
<span data-ttu-id="45125-108">Polecenie cmdlet **Get-AzDeploymentOperation** wyświetla wszystkie operacje, które były częścią wdrożenia, aby ułatwić identyfikowanie i podawanie dodatkowych informacji na temat operacji, które nie powiodły się dla określonego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="45125-108">The **Get-AzDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="45125-109">Może również pokazać odpowiedź i zawartość żądania dla każdej operacji wdrażania.</span><span class="sxs-lookup"><span data-stu-id="45125-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="45125-110">Są to te same informacje, które są dostępne w szczegółach wdrażania w portalu.</span><span class="sxs-lookup"><span data-stu-id="45125-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="45125-111">Aby uzyskać żądanie i zawartość odpowiedzi, Włącz ustawienie podczas przesyłania wdrożenia przez **nowe-AzDeployment**.</span><span class="sxs-lookup"><span data-stu-id="45125-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzDeployment**.</span></span>
<span data-ttu-id="45125-112">Może rejestrować i uwidaczniać klucze tajne, takie jak hasła używane we właściwościach zasobu lub operacjach **listKeys** , które zostaną zwrócone po pobraniu operacji wdrażania.</span><span class="sxs-lookup"><span data-stu-id="45125-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="45125-113">Aby uzyskać więcej informacji na temat tego ustawienia i sposobu jego włączania, zobacz New-AzDeployment i debugowanie wdrożeń szablonów ARM</span><span class="sxs-lookup"><span data-stu-id="45125-113">For more on this setting and how to enable it, see New-AzDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="45125-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45125-114">EXAMPLES</span></span>

### <span data-ttu-id="45125-115">Uzyskaj operacje wdrażania pod nazwą wdrożenia</span><span class="sxs-lookup"><span data-stu-id="45125-115">Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

<span data-ttu-id="45125-116">Pobiera operację wdrażania o nazwie "test" w bieżącym zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="45125-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="45125-117">Uzyskiwanie wdrożenia i wykonywanie operacji wdrażania</span><span class="sxs-lookup"><span data-stu-id="45125-117">Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

<span data-ttu-id="45125-118">To polecenie pobiera wdrożenie "test" w bieżącym zakresie subskrypcji i przeprowadza operacje wdrażania.</span><span class="sxs-lookup"><span data-stu-id="45125-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="45125-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45125-119">PARAMETERS</span></span>

### <span data-ttu-id="45125-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="45125-120">-ApiVersion</span></span>
<span data-ttu-id="45125-121">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="45125-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="45125-122">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="45125-122">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="45125-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45125-123">-DefaultProfile</span></span>
<span data-ttu-id="45125-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="45125-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45125-125">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="45125-125">-DeploymentName</span></span>
<span data-ttu-id="45125-126">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="45125-126">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45125-127">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="45125-127">-DeploymentObject</span></span>
<span data-ttu-id="45125-128">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="45125-128">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45125-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="45125-129">-OperationId</span></span>
<span data-ttu-id="45125-130">Identyfikator operacji wdrażania.</span><span class="sxs-lookup"><span data-stu-id="45125-130">The deployment operation Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45125-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="45125-131">-Pre</span></span>
<span data-ttu-id="45125-132">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="45125-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="45125-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45125-133">CommonParameters</span></span>
<span data-ttu-id="45125-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45125-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45125-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45125-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45125-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45125-136">INPUTS</span></span>

### <span data-ttu-id="45125-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="45125-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="45125-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45125-138">OUTPUTS</span></span>

### <span data-ttu-id="45125-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="45125-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="45125-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45125-140">NOTES</span></span>

## <span data-ttu-id="45125-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45125-141">RELATED LINKS</span></span>
