---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: e64fdd0300f2ccad4c3904d472563bbc30374b67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549911"
---
# <span data-ttu-id="68f00-101">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="68f00-101">Get-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="68f00-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68f00-102">SYNOPSIS</span></span>
<span data-ttu-id="68f00-103">Pobiera wdrożenia w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="68f00-103">Gets the deployments in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68f00-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68f00-104">SYNTAX</span></span>

### <span data-ttu-id="68f00-105">Zestaw parametrów nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="68f00-105">The deployment name parameter set.</span></span> <span data-ttu-id="68f00-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="68f00-106">(Default)</span></span>
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68f00-107">Zestaw parametrów identyfikator wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="68f00-107">The deployment Id parameter set.</span></span>
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68f00-108">Opis</span><span class="sxs-lookup"><span data-stu-id="68f00-108">DESCRIPTION</span></span>
<span data-ttu-id="68f00-109">Polecenie cmdlet **Get-AzureRmResourceGroupDeployment** pobiera wdrożenia w grupie zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="68f00-109">The **Get-AzureRmResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="68f00-110">Określ *nazwę* lub parametr *ID* , aby przefiltrować wyniki.</span><span class="sxs-lookup"><span data-stu-id="68f00-110">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="68f00-111">Domyślnie polecenie **Get-AzureRmResourceGroupDeployment** pobiera wszystkie wdrożenia określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="68f00-111">By default, **Get-AzureRmResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>

<span data-ttu-id="68f00-112">Zasób platformy Azure jest zarządzaną przez użytkownika jednostką Azure, taką jak serwer bazy danych, baza danych lub witryna sieci Web.</span><span class="sxs-lookup"><span data-stu-id="68f00-112">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="68f00-113">Grupa zasobów platformy Azure to zbiór zasobów platformy Azure wdrożonych jako jednostka.</span><span class="sxs-lookup"><span data-stu-id="68f00-113">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

<span data-ttu-id="68f00-114">Wdrożenie to operacja, która powoduje, że zasoby w grupie zasobów są dostępne do użytku.</span><span class="sxs-lookup"><span data-stu-id="68f00-114">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="68f00-115">Aby uzyskać więcej informacji na temat zasobów platformy Azure i grup zasobów platformy Azure, zobacz polecenie cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="68f00-115">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="68f00-116">Za pomocą tego polecenia cmdlet można śledzić śledzenie.</span><span class="sxs-lookup"><span data-stu-id="68f00-116">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="68f00-117">W przypadku debugowania Użyj tego polecenia cmdlet, korzystając z polecenia cmdlet Get-AzureRmLog.</span><span class="sxs-lookup"><span data-stu-id="68f00-117">For debugging, use this cmdlet with the Get-AzureRmLog cmdlet.</span></span>

## <span data-ttu-id="68f00-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68f00-118">EXAMPLES</span></span>

### <span data-ttu-id="68f00-119">Przykład 1. pobieranie wszystkich wdrożeń dla grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="68f00-119">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="68f00-120">To polecenie pobiera wszystkie wdrożenia grupy zasobów ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="68f00-120">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="68f00-121">Wynik przedstawia wdrożenie dla blogu WordPress, który używa szablonu galerii.</span><span class="sxs-lookup"><span data-stu-id="68f00-121">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="68f00-122">Przykład 2: uzyskiwanie wdrożenia według nazwy</span><span class="sxs-lookup"><span data-stu-id="68f00-122">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="68f00-123">To polecenie pobiera DeployWebsite01 wdrożenia grupy zasobów ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="68f00-123">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="68f00-124">Możesz przypisać nazwę do wdrożenia podczas tworzenia go za pomocą poleceń cmdlet **New-AzureRmResourceGroup** lub **New-AzureRmResourceGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="68f00-124">You can assign a name to a deployment when you create it by using the **New-AzureRmResourceGroup** or **New-AzureRmResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="68f00-125">Jeśli nie przypiszesz nazwy, aplety poleceń będą dostarczały nazwę domyślną na podstawie szablonu, który jest wykorzystywany do tworzenia wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="68f00-125">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="68f00-126">Przykład 3: pobieranie wdrożeń wszystkich grup zasobów</span><span class="sxs-lookup"><span data-stu-id="68f00-126">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="68f00-127">To polecenie pobiera wszystkie grupy zasobów w ramach subskrypcji przy użyciu polecenia cmdlet Get-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="68f00-127">This command gets all resource groups in your subscription by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="68f00-128">Polecenie przekazuje grupy zasobów do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="68f00-128">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="68f00-129">Bieżące polecenie cmdlet pobiera wszystkie wdrożenia wszystkich grup zasobów w ramach subskrypcji i przekazuje wyniki do polecenia cmdlet Format-Table, aby wyświetlić ich wartości właściwości **ResourceGroupName** , **deploymentname** i **ProvisioningState** .</span><span class="sxs-lookup"><span data-stu-id="68f00-129">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="68f00-130">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68f00-130">PARAMETERS</span></span>

### <span data-ttu-id="68f00-131">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="68f00-131">-ApiVersion</span></span>
<span data-ttu-id="68f00-132">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="68f00-132">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="68f00-133">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="68f00-133">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="68f00-134">-ID</span><span class="sxs-lookup"><span data-stu-id="68f00-134">-Id</span></span>
<span data-ttu-id="68f00-135">Określa identyfikator wdrożenia grupy zasobów do pobrania.</span><span class="sxs-lookup"><span data-stu-id="68f00-135">Specifies the ID of the resource group deployment to get.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment Id parameter set.
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f00-136">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="68f00-136">-Name</span></span>
<span data-ttu-id="68f00-137">Określa nazwę wdrożenia, które ma zostać pozyskane.</span><span class="sxs-lookup"><span data-stu-id="68f00-137">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="68f00-138">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="68f00-138">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68f00-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="68f00-139">-Pre</span></span>
<span data-ttu-id="68f00-140">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="68f00-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="68f00-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68f00-141">-ResourceGroupName</span></span>
<span data-ttu-id="68f00-142">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="68f00-142">Specifies the name of a resource group.</span></span>
<span data-ttu-id="68f00-143">Polecenie cmdlet umożliwia pobieranie wdrożeń dla grupy zasobów określanych przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="68f00-143">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="68f00-144">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="68f00-144">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="68f00-145">Ten parametr jest wymagany, a w każdym poleceniu można określić tylko dla jednej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="68f00-145">This parameter is required and you can specify only one resource group in each command.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68f00-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68f00-146">-DefaultProfile</span></span>
<span data-ttu-id="68f00-147">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="68f00-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f00-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68f00-148">CommonParameters</span></span>
<span data-ttu-id="68f00-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68f00-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68f00-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68f00-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68f00-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68f00-151">INPUTS</span></span>

### <span data-ttu-id="68f00-152">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="68f00-152">None</span></span>

## <span data-ttu-id="68f00-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68f00-153">OUTPUTS</span></span>

### <span data-ttu-id="68f00-154">Microsoft. Azure. Commands. ResourceManagement. models. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="68f00-154">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroupDeployment</span></span>
<span data-ttu-id="68f00-155">Polecenie cmdlet zwraca wdrożenia grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="68f00-155">The cmdlet returns resource group deployments.</span></span>

## <span data-ttu-id="68f00-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68f00-156">NOTES</span></span>

## <span data-ttu-id="68f00-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68f00-157">RELATED LINKS</span></span>

[<span data-ttu-id="68f00-158">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="68f00-158">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="68f00-159">Nowe — AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="68f00-159">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="68f00-160">Nowe — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="68f00-160">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="68f00-161">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="68f00-161">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="68f00-162">Zatrzymaj — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="68f00-162">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="68f00-163">Test — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="68f00-163">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


