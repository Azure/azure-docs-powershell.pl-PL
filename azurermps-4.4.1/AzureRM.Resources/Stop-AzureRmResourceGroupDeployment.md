---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: f07b2f59f1a38aca780e1e869bb3904725df6dcd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719247"
---
# <span data-ttu-id="1b35c-101">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1b35c-101">Stop-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="1b35c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b35c-102">SYNOPSIS</span></span>
<span data-ttu-id="1b35c-103">Anuluje wdrożenie grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1b35c-103">Cancels a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b35c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b35c-104">SYNTAX</span></span>

### <span data-ttu-id="1b35c-105">Zestaw parametrów nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="1b35c-105">The deployment name parameter set.</span></span> <span data-ttu-id="1b35c-106">Domyślne</span><span class="sxs-lookup"><span data-stu-id="1b35c-106">(Default)</span></span>
```
Stop-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b35c-107">Zestaw parametrów identyfikator wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="1b35c-107">The deployment Id parameter set.</span></span>
```
Stop-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b35c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1b35c-108">DESCRIPTION</span></span>
<span data-ttu-id="1b35c-109">Polecenie cmdlet **stop-AzureRmResourceGroupDeployment** anuluje wdrożenie grup zasobów platformy Azure, które zostało uruchomione, ale nie zostało ukończone.</span><span class="sxs-lookup"><span data-stu-id="1b35c-109">The **Stop-AzureRmResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="1b35c-110">Aby zatrzymać wdrożenie, wdrożenie musi mieć niekompletny stan inicjowania obsługi, taki jak obsługa administracyjna, a nie stan wykonania, na przykład zainicjowana obsługa administracyjna lub niepowodzenie.</span><span class="sxs-lookup"><span data-stu-id="1b35c-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="1b35c-111">Zasób platformy Azure to jednostka zarządzana przez użytkownika, taka jak witryna sieci Web, baza danych lub serwer bazy danych.</span><span class="sxs-lookup"><span data-stu-id="1b35c-111">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="1b35c-112">Grupa zasobów to zbiór zasobów wdrożonych jako jednostka.</span><span class="sxs-lookup"><span data-stu-id="1b35c-112">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="1b35c-113">Aby wdrożyć grupę zasobów, użyj polecenia cmdlet New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="1b35c-113">To deploy a resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span>

<span data-ttu-id="1b35c-114">Polecenie cmdlet New-AzureRmResource tworzy nowy zasób, ale nie wyzwala operacji wdrażania grupy zasobów, która może zostać zatrzymana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b35c-114">The New-AzureRmResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="1b35c-115">To polecenie cmdlet powoduje zatrzymanie tylko jednego uruchomionego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="1b35c-115">This cmdlet stops only one running deployment.</span></span>

<span data-ttu-id="1b35c-116">Użyj parametru *name* , aby zatrzymać określone wdrożenie.</span><span class="sxs-lookup"><span data-stu-id="1b35c-116">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="1b35c-117">Jeśli pominięto parametr *name* , polecenie **stop-AzureRmResourceGroupDeployment** wyszukuje uruchomione wdrożenie i zatrzymuje je.</span><span class="sxs-lookup"><span data-stu-id="1b35c-117">If you omit the *Name* parameter, **Stop-AzureRmResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="1b35c-118">Jeśli polecenie cmdlet umożliwia znalezienie kilku uruchomionych wdrożeń, wykonanie polecenia nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="1b35c-118">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="1b35c-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b35c-119">EXAMPLES</span></span>

## <span data-ttu-id="1b35c-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b35c-120">PARAMETERS</span></span>

### <span data-ttu-id="1b35c-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1b35c-121">-ApiVersion</span></span>
<span data-ttu-id="1b35c-122">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="1b35c-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="1b35c-123">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="1b35c-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="1b35c-124">-ID</span><span class="sxs-lookup"><span data-stu-id="1b35c-124">-Id</span></span>
<span data-ttu-id="1b35c-125">Określa identyfikator wdrożenia grupy zasobów, który ma zostać zatrzymany.</span><span class="sxs-lookup"><span data-stu-id="1b35c-125">Specifies the ID of the resource group deployment to stop.</span></span>

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

### <span data-ttu-id="1b35c-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1b35c-126">-Name</span></span>
<span data-ttu-id="1b35c-127">Określa nazwę wdrożenia grupy zasobów do zatrzymania.</span><span class="sxs-lookup"><span data-stu-id="1b35c-127">Specifies the name of the resource group deployment to stop.</span></span>

<span data-ttu-id="1b35c-128">Jeśli nie podano tego parametru, to polecenie cmdlet wyszukuje uruchomione wdrożenie w grupie zasobów i zatrzymuje je.</span><span class="sxs-lookup"><span data-stu-id="1b35c-128">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="1b35c-129">Jeśli okaże się, że nie jest uruchomione więcej niż jedno wdrożenie, polecenie nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="1b35c-129">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="1b35c-130">Aby uzyskać nazwę wdrożenia, użyj polecenia cmdlet Get-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="1b35c-130">To get the deployment name, use the Get-AzureRmResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b35c-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="1b35c-131">-Pre</span></span>
<span data-ttu-id="1b35c-132">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="1b35c-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1b35c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b35c-133">-ResourceGroupName</span></span>
<span data-ttu-id="1b35c-134">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1b35c-134">Specifies the name of the resource group.</span></span>
<span data-ttu-id="1b35c-135">To polecenie cmdlet zatrzymuje wdrożenie grupy zasobów, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="1b35c-135">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b35c-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1b35c-136">-Confirm</span></span>
<span data-ttu-id="1b35c-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b35c-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b35c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b35c-138">-WhatIf</span></span>
<span data-ttu-id="1b35c-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b35c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b35c-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1b35c-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b35c-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b35c-141">-DefaultProfile</span></span>
<span data-ttu-id="1b35c-142">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b35c-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b35c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b35c-143">CommonParameters</span></span>
<span data-ttu-id="1b35c-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b35c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b35c-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b35c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b35c-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b35c-146">INPUTS</span></span>

### <span data-ttu-id="1b35c-147">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1b35c-147">None</span></span>

## <span data-ttu-id="1b35c-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b35c-148">OUTPUTS</span></span>

### <span data-ttu-id="1b35c-149">Wartość</span><span class="sxs-lookup"><span data-stu-id="1b35c-149">Boolean</span></span>

## <span data-ttu-id="1b35c-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b35c-150">NOTES</span></span>

## <span data-ttu-id="1b35c-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b35c-151">RELATED LINKS</span></span>

[<span data-ttu-id="1b35c-152">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1b35c-152">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="1b35c-153">Nowe — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="1b35c-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="1b35c-154">Nowe — AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1b35c-154">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="1b35c-155">Nowe — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1b35c-155">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="1b35c-156">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1b35c-156">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="1b35c-157">Test — AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1b35c-157">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


