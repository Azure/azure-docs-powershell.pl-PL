---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: 5507e180d5f56b75006f31f9cc6753f50d821a3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973610"
---
# <span data-ttu-id="c6326-101">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="c6326-101">Get-AzDeploymentOperation</span></span>

## <span data-ttu-id="c6326-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6326-102">SYNOPSIS</span></span>
<span data-ttu-id="c6326-103">Uzyskaj operację wdrażania</span><span class="sxs-lookup"><span data-stu-id="c6326-103">Get deployment operation</span></span>

## <span data-ttu-id="c6326-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c6326-104">SYNTAX</span></span>

### <span data-ttu-id="c6326-105">GetByDeploymentName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="c6326-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6326-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="c6326-106">GetByDeploymentObject</span></span>
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6326-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="c6326-107">DESCRIPTION</span></span>
<span data-ttu-id="c6326-108">Polecenie **cmdlet Get-AzDeploymentOperation** zawiera listę wszystkich operacji, które były częścią wdrożenia, co pomaga w zidentyfikowaniu i podawać więcej informacji o dokładnie tych operacjach, które nie powiodły się w danym wdrożeniu.</span><span class="sxs-lookup"><span data-stu-id="c6326-108">The **Get-AzDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="c6326-109">Może też wyświetlać odpowiedź i zawartość żądania dla każdej operacji wdrażania.</span><span class="sxs-lookup"><span data-stu-id="c6326-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="c6326-110">Są to te same informacje, które podano w szczegółach wdrożenia w portalu.</span><span class="sxs-lookup"><span data-stu-id="c6326-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="c6326-111">Aby pobrać żądanie i zawartość odpowiedzi, włącz ustawienie podczas przesyłania wdrożenia za pomocą **programu New-AzDeployment.**</span><span class="sxs-lookup"><span data-stu-id="c6326-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzDeployment**.</span></span>
<span data-ttu-id="c6326-112">Może on potencjalnie rejestrować i ujawniać tajemnice, takie jak hasła używane we właściwości zasobu lub operacje **listKeys,** które są następnie zwracane po pobraniu operacji wdrażania.</span><span class="sxs-lookup"><span data-stu-id="c6326-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="c6326-113">Aby uzyskać więcej informacji na temat tego ustawienia i sposobu włączania go, zobacz New-AzDeployment i Debugowanie ARM wdrożeń szablonów</span><span class="sxs-lookup"><span data-stu-id="c6326-113">For more on this setting and how to enable it, see New-AzDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="c6326-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c6326-114">EXAMPLES</span></span>

### <span data-ttu-id="c6326-115">Przykład 1. Uzyskiwanie operacji wdrażania nadano nazwę wdrożenia</span><span class="sxs-lookup"><span data-stu-id="c6326-115">Example 1: Get deployment operations given a deployment name</span></span>
```powershell
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

<span data-ttu-id="c6326-116">Pobiera operację wdrażania z nazwą "test" w zakresie bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c6326-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="c6326-117">Przykład 2. Uzyskiwanie wdrożenia i uzyskiwanie jego operacji wdrażania</span><span class="sxs-lookup"><span data-stu-id="c6326-117">Example 2: Get a deployment and get its deployment operations</span></span>
```powershell
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

<span data-ttu-id="c6326-118">To polecenie pobiera "test" wdrożenia w bieżącym zakresie subskrypcji i pobiera jego operacje wdrażania.</span><span class="sxs-lookup"><span data-stu-id="c6326-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="c6326-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6326-119">PARAMETERS</span></span>

### <span data-ttu-id="c6326-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6326-120">-DefaultProfile</span></span>
<span data-ttu-id="c6326-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6326-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6326-122">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="c6326-122">-DeploymentName</span></span>
<span data-ttu-id="c6326-123">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="c6326-123">The deployment name.</span></span>

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

### <span data-ttu-id="c6326-124">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="c6326-124">-DeploymentObject</span></span>
<span data-ttu-id="c6326-125">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="c6326-125">The deployment object.</span></span>

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

### <span data-ttu-id="c6326-126">-OperationId</span><span class="sxs-lookup"><span data-stu-id="c6326-126">-OperationId</span></span>
<span data-ttu-id="c6326-127">Identyfikator operacji wdrażania.</span><span class="sxs-lookup"><span data-stu-id="c6326-127">The deployment operation Id.</span></span>

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

### <span data-ttu-id="c6326-128">— Przed</span><span class="sxs-lookup"><span data-stu-id="c6326-128">-Pre</span></span>
<span data-ttu-id="c6326-129">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="c6326-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c6326-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6326-130">CommonParameters</span></span>
<span data-ttu-id="c6326-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6326-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6326-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6326-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6326-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6326-133">INPUTS</span></span>

### <span data-ttu-id="c6326-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="c6326-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="c6326-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6326-135">OUTPUTS</span></span>

### <span data-ttu-id="c6326-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="c6326-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="c6326-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c6326-137">NOTES</span></span>

## <span data-ttu-id="c6326-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6326-138">RELATED LINKS</span></span>
