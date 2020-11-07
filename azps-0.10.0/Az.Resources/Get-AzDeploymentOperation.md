---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: 1eafc934777809d7fd4041496b004ea682e97910
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892621"
---
# <span data-ttu-id="ae7ba-101">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="ae7ba-101">Get-AzDeploymentOperation</span></span>

## <span data-ttu-id="ae7ba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae7ba-102">SYNOPSIS</span></span>
<span data-ttu-id="ae7ba-103">Operacja pobierania wdrożenia</span><span class="sxs-lookup"><span data-stu-id="ae7ba-103">Get deployment operation</span></span>

## <span data-ttu-id="ae7ba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae7ba-104">SYNTAX</span></span>

### <span data-ttu-id="ae7ba-105">GetByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ae7ba-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae7ba-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="ae7ba-106">GetByDeploymentObject</span></span>
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae7ba-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ae7ba-107">DESCRIPTION</span></span>
<span data-ttu-id="ae7ba-108">Polecenie cmdlet **Get-AzDeploymentOperation** wyświetla wszystkie operacje, które były częścią wdrożenia, aby ułatwić identyfikowanie i podawanie dodatkowych informacji na temat operacji, które nie powiodły się dla określonego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ae7ba-108">The **Get-AzDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="ae7ba-109">Może również pokazać odpowiedź i zawartość żądania dla każdej operacji wdrażania.</span><span class="sxs-lookup"><span data-stu-id="ae7ba-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="ae7ba-110">Są to te same informacje, które są dostępne w szczegółach wdrażania w portalu.</span><span class="sxs-lookup"><span data-stu-id="ae7ba-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="ae7ba-111">Aby uzyskać żądanie i zawartość odpowiedzi, Włącz ustawienie podczas przesyłania wdrożenia przez **nowe-AzDeployment**.</span><span class="sxs-lookup"><span data-stu-id="ae7ba-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzDeployment**.</span></span>
<span data-ttu-id="ae7ba-112">Może rejestrować i uwidaczniać klucze tajne, takie jak hasła używane we właściwościach zasobu lub operacjach **listKeys** , które zostaną zwrócone po pobraniu operacji wdrażania.</span><span class="sxs-lookup"><span data-stu-id="ae7ba-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="ae7ba-113">Aby uzyskać więcej informacji na temat tego ustawienia i sposobu jego włączania, zobacz New-AzDeployment i debugowanie wdrożeń szablonów ARM</span><span class="sxs-lookup"><span data-stu-id="ae7ba-113">For more on this setting and how to enable it, see New-AzDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="ae7ba-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae7ba-114">EXAMPLES</span></span>

### <span data-ttu-id="ae7ba-115">Uzyskaj operacje wdrażania pod nazwą wdrożenia</span><span class="sxs-lookup"><span data-stu-id="ae7ba-115">Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

<span data-ttu-id="ae7ba-116">Pobiera operację wdrażania o nazwie "test" w bieżącym zakresie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ae7ba-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="ae7ba-117">Uzyskiwanie wdrożenia i wykonywanie operacji wdrażania</span><span class="sxs-lookup"><span data-stu-id="ae7ba-117">Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

<span data-ttu-id="ae7ba-118">To polecenie pobiera wdrożenie "test" w bieżącym zakresie subskrypcji i przeprowadza operacje wdrażania.</span><span class="sxs-lookup"><span data-stu-id="ae7ba-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="ae7ba-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae7ba-119">PARAMETERS</span></span>

### <span data-ttu-id="ae7ba-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ae7ba-120">-ApiVersion</span></span>
<span data-ttu-id="ae7ba-121">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="ae7ba-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ae7ba-122">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="ae7ba-122">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="ae7ba-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae7ba-123">-DefaultProfile</span></span>
<span data-ttu-id="ae7ba-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae7ba-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae7ba-125">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="ae7ba-125">-DeploymentName</span></span>
<span data-ttu-id="ae7ba-126">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ae7ba-126">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae7ba-127">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="ae7ba-127">-DeploymentObject</span></span>
<span data-ttu-id="ae7ba-128">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="ae7ba-128">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae7ba-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="ae7ba-129">-OperationId</span></span>
<span data-ttu-id="ae7ba-130">Identyfikator operacji wdrażania.</span><span class="sxs-lookup"><span data-stu-id="ae7ba-130">The deployment operation Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae7ba-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="ae7ba-131">-Pre</span></span>
<span data-ttu-id="ae7ba-132">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="ae7ba-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ae7ba-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae7ba-133">CommonParameters</span></span>
<span data-ttu-id="ae7ba-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae7ba-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae7ba-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae7ba-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae7ba-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae7ba-136">INPUTS</span></span>

### <span data-ttu-id="ae7ba-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ae7ba-137">System.String</span></span>
<span data-ttu-id="ae7ba-138">System. Nullable "1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ae7ba-138">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="ae7ba-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae7ba-139">OUTPUTS</span></span>

### <span data-ttu-id="ae7ba-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="ae7ba-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="ae7ba-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae7ba-141">NOTES</span></span>

## <span data-ttu-id="ae7ba-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae7ba-142">RELATED LINKS</span></span>
