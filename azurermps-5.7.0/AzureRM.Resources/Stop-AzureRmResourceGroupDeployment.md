---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/stop-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 4cdc70928f2b27ae1e1604c52e5703798a302a66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551607"
---
# <span data-ttu-id="b9409-101">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b9409-101">Stop-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="b9409-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b9409-102">SYNOPSIS</span></span>
<span data-ttu-id="b9409-103">Anuluje wdrożenie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b9409-103">Cancels a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9409-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b9409-104">SYNTAX</span></span>

### <span data-ttu-id="b9409-105">StopByResourceGroupDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b9409-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9409-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="b9409-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9409-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b9409-107">DESCRIPTION</span></span>
<span data-ttu-id="b9409-108">Polecenie cmdlet **stop-AzureRmResourceGroupDeployment** anuluje wdrożenie grup zasobów platformy Azure, które zostało uruchomione, ale nie zostało ukończone.</span><span class="sxs-lookup"><span data-stu-id="b9409-108">The **Stop-AzureRmResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="b9409-109">Aby zatrzymać wdrożenie, wdrożenie musi mieć niekompletny stan inicjowania obsługi, taki jak obsługa administracyjna, a nie stan wykonania, na przykład zainicjowana obsługa administracyjna lub niepowodzenie.</span><span class="sxs-lookup"><span data-stu-id="b9409-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="b9409-110">Zasób platformy Azure to jednostka zarządzana przez użytkownika, taka jak witryna sieci Web, baza danych lub serwer bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b9409-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="b9409-111">Grupa zasobów to zbiór zasobów wdrożonych jako jednostka.</span><span class="sxs-lookup"><span data-stu-id="b9409-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="b9409-112">Aby wdrożyć grupę zasobów, użyj polecenia cmdlet New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="b9409-112">To deploy a resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span>

<span data-ttu-id="b9409-113">Polecenie cmdlet New-AzureRmResource tworzy nowy zasób, ale nie wyzwala operacji wdrażania grupy zasobów, która może zostać zatrzymana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9409-113">The New-AzureRmResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="b9409-114">To polecenie cmdlet powoduje zatrzymanie tylko jednego uruchomionego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="b9409-114">This cmdlet stops only one running deployment.</span></span>

<span data-ttu-id="b9409-115">Użyj parametru *name* , aby zatrzymać określone wdrożenie.</span><span class="sxs-lookup"><span data-stu-id="b9409-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="b9409-116">Jeśli pominięto parametr *name* , polecenie **stop-AzureRmResourceGroupDeployment** wyszukuje uruchomione wdrożenie i zatrzymuje je.</span><span class="sxs-lookup"><span data-stu-id="b9409-116">If you omit the *Name* parameter, **Stop-AzureRmResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="b9409-117">Jeśli polecenie cmdlet umożliwia znalezienie kilku uruchomionych wdrożeń, wykonanie polecenia nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="b9409-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="b9409-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b9409-118">EXAMPLES</span></span>

## <span data-ttu-id="b9409-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b9409-119">PARAMETERS</span></span>

### <span data-ttu-id="b9409-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b9409-120">-ApiVersion</span></span>
<span data-ttu-id="b9409-121">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="b9409-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="b9409-122">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="b9409-122">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="b9409-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9409-123">-DefaultProfile</span></span>
<span data-ttu-id="b9409-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b9409-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9409-125">-ID</span><span class="sxs-lookup"><span data-stu-id="b9409-125">-Id</span></span>
<span data-ttu-id="b9409-126">Określa identyfikator wdrożenia grupy zasobów, który ma zostać zatrzymany.</span><span class="sxs-lookup"><span data-stu-id="b9409-126">Specifies the ID of the resource group deployment to stop.</span></span>

```yaml
Type: String
Parameter Sets: StopByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9409-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b9409-127">-Name</span></span>
<span data-ttu-id="b9409-128">Określa nazwę wdrożenia grupy zasobów do zatrzymania.</span><span class="sxs-lookup"><span data-stu-id="b9409-128">Specifies the name of the resource group deployment to stop.</span></span>

<span data-ttu-id="b9409-129">Jeśli nie podano tego parametru, to polecenie cmdlet wyszukuje uruchomione wdrożenie w grupie zasobów i zatrzymuje je.</span><span class="sxs-lookup"><span data-stu-id="b9409-129">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="b9409-130">Jeśli okaże się, że nie jest uruchomione więcej niż jedno wdrożenie, polecenie nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="b9409-130">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="b9409-131">Aby uzyskać nazwę wdrożenia, użyj polecenia cmdlet Get-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="b9409-131">To get the deployment name, use the Get-AzureRmResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9409-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="b9409-132">-Pre</span></span>
<span data-ttu-id="b9409-133">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="b9409-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b9409-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9409-134">-ResourceGroupName</span></span>
<span data-ttu-id="b9409-135">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b9409-135">Specifies the name of the resource group.</span></span>
<span data-ttu-id="b9409-136">To polecenie cmdlet zatrzymuje wdrożenie grupy zasobów, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="b9409-136">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9409-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b9409-137">-Confirm</span></span>
<span data-ttu-id="b9409-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9409-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9409-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9409-139">-WhatIf</span></span>
<span data-ttu-id="b9409-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9409-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9409-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b9409-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9409-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9409-142">CommonParameters</span></span>
<span data-ttu-id="b9409-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9409-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9409-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9409-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9409-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9409-145">INPUTS</span></span>

### <span data-ttu-id="b9409-146">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b9409-146">None</span></span>

## <span data-ttu-id="b9409-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b9409-147">OUTPUTS</span></span>

### <span data-ttu-id="b9409-148">Wartość</span><span class="sxs-lookup"><span data-stu-id="b9409-148">Boolean</span></span>

## <span data-ttu-id="b9409-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b9409-149">NOTES</span></span>

## <span data-ttu-id="b9409-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9409-150">RELATED LINKS</span></span>

[<span data-ttu-id="b9409-151">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b9409-151">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b9409-152">Nowe — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b9409-152">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="b9409-153">Nowe — AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b9409-153">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="b9409-154">Nowe — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b9409-154">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b9409-155">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b9409-155">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="b9409-156">Test — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b9409-156">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


