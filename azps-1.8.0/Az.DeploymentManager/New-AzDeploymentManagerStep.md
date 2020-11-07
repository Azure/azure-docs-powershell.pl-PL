---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 2013f1722ee246db023f4d26d456eafffa8f40eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709957"
---
# <span data-ttu-id="ca205-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="ca205-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="ca205-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ca205-102">SYNOPSIS</span></span>
<span data-ttu-id="ca205-103">Tworzy krok.</span><span class="sxs-lookup"><span data-stu-id="ca205-103">Creates a step.</span></span>

## <span data-ttu-id="ca205-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ca205-104">SYNTAX</span></span>

```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca205-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ca205-105">DESCRIPTION</span></span>
<span data-ttu-id="ca205-106">Polecenie cmdlet **New-AzDeploymentManagerStep** umożliwia utworzenie kroku wdrożenia, do którego można odwoływać się w trakcie wdrażania.</span><span class="sxs-lookup"><span data-stu-id="ca205-106">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="ca205-107">Określ *imię i nazwisko* , *ResourceGroupName* oraz wymagane właściwości.</span><span class="sxs-lookup"><span data-stu-id="ca205-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="ca205-108">Zwrócony obiekt można zmodyfikować lokalnie, a następnie zastosować zmiany do kroku przy użyciu polecenia cmdlet Set-AzDeploymentManagerStep.</span><span class="sxs-lookup"><span data-stu-id="ca205-108">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="ca205-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ca205-109">EXAMPLES</span></span>

### <span data-ttu-id="ca205-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ca205-110">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="ca205-111">Tworzy krok w ContosoResourceGroup o nazwie ContosoService1WaitStep z centralą centralną jako lokalizację zasobu.</span><span class="sxs-lookup"><span data-stu-id="ca205-111">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="ca205-112">Właściwość Duration zawiera czas trwania, przez jaki rozmieszczenie będzie oczekiwać przed uruchomieniem następnego kroku.</span><span class="sxs-lookup"><span data-stu-id="ca205-112">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="ca205-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ca205-113">PARAMETERS</span></span>

### <span data-ttu-id="ca205-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca205-114">-DefaultProfile</span></span>
<span data-ttu-id="ca205-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca205-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca205-116">— Czas trwania</span><span class="sxs-lookup"><span data-stu-id="ca205-116">-Duration</span></span>
<span data-ttu-id="ca205-117">Czas oczekiwania na oczekiwanie w formacie ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="ca205-117">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="ca205-118">Na przykład: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="ca205-118">E.g.: PT30M, PT1H</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca205-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ca205-119">-Location</span></span>
<span data-ttu-id="ca205-120">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="ca205-120">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca205-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ca205-121">-Name</span></span>
<span data-ttu-id="ca205-122">Nazwa kroku.</span><span class="sxs-lookup"><span data-stu-id="ca205-122">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca205-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca205-123">-ResourceGroupName</span></span>
<span data-ttu-id="ca205-124">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="ca205-124">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca205-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="ca205-125">-Tag</span></span>
<span data-ttu-id="ca205-126">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="ca205-126">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca205-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ca205-127">-Confirm</span></span>
<span data-ttu-id="ca205-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca205-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca205-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca205-129">-WhatIf</span></span>
<span data-ttu-id="ca205-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca205-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca205-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ca205-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca205-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca205-132">CommonParameters</span></span>
<span data-ttu-id="ca205-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca205-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca205-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca205-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca205-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca205-135">INPUTS</span></span>

### <span data-ttu-id="ca205-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ca205-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ca205-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ca205-137">OUTPUTS</span></span>

### <span data-ttu-id="ca205-138">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="ca205-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="ca205-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ca205-139">NOTES</span></span>

## <span data-ttu-id="ca205-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca205-140">RELATED LINKS</span></span>
