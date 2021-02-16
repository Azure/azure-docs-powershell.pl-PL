---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
ms.openlocfilehash: 1ac0ab153177caaf080e5aa9144020ea253b8438
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240083"
---
# <span data-ttu-id="40274-101">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="40274-101">Get-AzResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="40274-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40274-102">SYNOPSIS</span></span>
<span data-ttu-id="40274-103">Pobiera operację wdrażania grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="40274-103">Gets the resource group deployment operation</span></span>

## <span data-ttu-id="40274-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="40274-104">SYNTAX</span></span>

```
Get-AzResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40274-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="40274-105">DESCRIPTION</span></span>
<span data-ttu-id="40274-106">Polecenie **cmdlet Get-AzResourceGroupDeploymentOperation** zawiera listę wszystkich operacji, które były częścią wdrożenia, co pomaga w zidentyfikowaniu i podawać więcej informacji o dokładnie tych operacjach, których wykonanie nie powiodło się w danym wdrożeniu.</span><span class="sxs-lookup"><span data-stu-id="40274-106">The **Get-AzResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="40274-107">Może też wyświetlać odpowiedź i zawartość żądania dla każdej operacji wdrażania.</span><span class="sxs-lookup"><span data-stu-id="40274-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="40274-108">Są to te same informacje, które podano w szczegółach wdrożenia w portalu.</span><span class="sxs-lookup"><span data-stu-id="40274-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="40274-109">Aby uzyskać żądanie i zawartość odpowiedzi, włącz ustawienie podczas przesyłania wdrożenia za pomocą **programu New-AzResourceGroupDeployment.**</span><span class="sxs-lookup"><span data-stu-id="40274-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzResourceGroupDeployment**.</span></span>
<span data-ttu-id="40274-110">Może on potencjalnie rejestrować i ujawniać tajemnice, takie jak hasła używane we właściwości zasobu lub operacje **listKeys,** które są następnie zwracane po pobraniu operacji wdrażania.</span><span class="sxs-lookup"><span data-stu-id="40274-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="40274-111">Aby uzyskać więcej informacji na temat tego ustawienia i sposobu włączania go, zobacz New-AzResourceGroupDeployment i Debugowanie ARM wdrożeń szablonów</span><span class="sxs-lookup"><span data-stu-id="40274-111">For more on this setting and how to enable it, see New-AzResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="40274-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="40274-112">EXAMPLES</span></span>

### <span data-ttu-id="40274-113">Przykład 1. Pobierz</span><span class="sxs-lookup"><span data-stu-id="40274-113">Example 1: Get1</span></span>
```powershell
PS C:\>Get-AzResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="40274-114">Pobiera operację wdrażania z nazwą "test" w obszarze "test" grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="40274-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="40274-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40274-115">PARAMETERS</span></span>

### <span data-ttu-id="40274-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40274-116">-DefaultProfile</span></span>
<span data-ttu-id="40274-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="40274-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40274-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="40274-118">-DeploymentName</span></span>
<span data-ttu-id="40274-119">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="40274-119">The deployment name.</span></span>

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

### <span data-ttu-id="40274-120">— Przed</span><span class="sxs-lookup"><span data-stu-id="40274-120">-Pre</span></span>
<span data-ttu-id="40274-121">Po jej skonfigurowaniu polecenie cmdlet powinno automatycznie określać wersję do użycia przy użyciu wersji przedpremierowej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="40274-121">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="40274-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40274-122">-ResourceGroupName</span></span>
<span data-ttu-id="40274-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="40274-123">The resource group name.</span></span>

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

### <span data-ttu-id="40274-124">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="40274-124">-SubscriptionId</span></span>
<span data-ttu-id="40274-125">Subskrypcja do użycia.</span><span class="sxs-lookup"><span data-stu-id="40274-125">The subscription to use.</span></span>

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

### <span data-ttu-id="40274-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40274-126">CommonParameters</span></span>
<span data-ttu-id="40274-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40274-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40274-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40274-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40274-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40274-129">INPUTS</span></span>

### <span data-ttu-id="40274-130">System.String</span><span class="sxs-lookup"><span data-stu-id="40274-130">System.String</span></span>

### <span data-ttu-id="40274-131">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="40274-131">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="40274-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40274-132">OUTPUTS</span></span>

### <span data-ttu-id="40274-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="40274-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="40274-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="40274-134">NOTES</span></span>

## <span data-ttu-id="40274-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40274-135">RELATED LINKS</span></span>
