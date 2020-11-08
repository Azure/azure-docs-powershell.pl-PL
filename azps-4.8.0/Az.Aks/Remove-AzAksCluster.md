---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
ms.openlocfilehash: d6364030eedb75b59c5f9a86bb57499864270fa2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219650"
---
# <span data-ttu-id="c83df-101">Remove-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="c83df-101">Remove-AzAksCluster</span></span>

## <span data-ttu-id="c83df-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c83df-102">SYNOPSIS</span></span>
<span data-ttu-id="c83df-103">Usuń zarządzany klaster Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="c83df-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="c83df-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c83df-104">SYNTAX</span></span>

### <span data-ttu-id="c83df-105">GroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c83df-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c83df-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c83df-106">InputObjectParameterSet</span></span>
```
Remove-AzAksCluster -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c83df-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c83df-107">IdParameterSet</span></span>
```
Remove-AzAksCluster [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c83df-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c83df-108">DESCRIPTION</span></span>
<span data-ttu-id="c83df-109">Usuń zarządzany klaster Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="c83df-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="c83df-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c83df-110">EXAMPLES</span></span>

### <span data-ttu-id="c83df-111">Usuwanie istniejącego klastra zarządzanego Kubernetes</span><span class="sxs-lookup"><span data-stu-id="c83df-111">Delete an existing managed Kubernetes cluster</span></span>
```powershell
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="c83df-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c83df-112">PARAMETERS</span></span>

### <span data-ttu-id="c83df-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c83df-113">-AsJob</span></span>
<span data-ttu-id="c83df-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c83df-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c83df-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c83df-115">-DefaultProfile</span></span>
<span data-ttu-id="c83df-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c83df-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c83df-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c83df-117">-Force</span></span>
<span data-ttu-id="c83df-118">Usuwanie zarządzanego klastra Kubernetes bez monitowania</span><span class="sxs-lookup"><span data-stu-id="c83df-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="c83df-119">-ID</span><span class="sxs-lookup"><span data-stu-id="c83df-119">-Id</span></span>
<span data-ttu-id="c83df-120">Identyfikator zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="c83df-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c83df-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c83df-121">-InputObject</span></span>
<span data-ttu-id="c83df-122">Obiekt PSKubernetesCluster, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="c83df-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c83df-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c83df-123">-Name</span></span>
<span data-ttu-id="c83df-124">Nazwa zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="c83df-124">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c83df-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c83df-125">-PassThru</span></span>
<span data-ttu-id="c83df-126">Zwraca wartość PRAWDA, Jeśli usunięcie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="c83df-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="c83df-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c83df-127">-ResourceGroupName</span></span>
<span data-ttu-id="c83df-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c83df-128">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c83df-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c83df-129">-Confirm</span></span>
<span data-ttu-id="c83df-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c83df-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c83df-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c83df-131">-WhatIf</span></span>
<span data-ttu-id="c83df-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c83df-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c83df-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c83df-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c83df-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c83df-134">CommonParameters</span></span>
<span data-ttu-id="c83df-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c83df-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c83df-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c83df-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c83df-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c83df-137">INPUTS</span></span>

### <span data-ttu-id="c83df-138">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="c83df-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="c83df-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c83df-139">System.String</span></span>

## <span data-ttu-id="c83df-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c83df-140">OUTPUTS</span></span>

### <span data-ttu-id="c83df-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c83df-141">System.Boolean</span></span>

## <span data-ttu-id="c83df-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c83df-142">NOTES</span></span>

## <span data-ttu-id="c83df-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c83df-143">RELATED LINKS</span></span>
